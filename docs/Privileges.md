# Privileges

**Privilege ID Structure:** Action Type + [[Model State]] + Model Name

**Default PrivilegeID for each model:**
1. New: privilegeID = "InsertModelName"
2. View: privilegeID = "ViewModelName"
3. Update: privilegeID = "UpdateModelName"
4. Delete: privilegeID = "DeleteModelName"

<br>
<hr>

**Icons**

Back End should send each and every icon to the front end so they can show it or not,
icons related to an action are depend in the action privilege while general icons like
User, Groups ... etc are dependes on one of the actions if user has the right of one action
then he can see the icon otherwise the icon will be hidden.

Icons privileges are sent as part of the response to any request from the user as shown:
```json json_schema
{
  "type": "object",
  "properties": {
    "status": {
      "type": "Integer"
    },
    "message": {
      "type": "String"
    },
    "iconsRole": {
      "type": "Array"
    },
    "data": {
      "type": "object"
    }
  }
}
```
Icons Privileges are:
1. Model Icon: iconsRole index = "ModelName".
2. New Icon: iconsRole index = "InsertModelName".
3. View Icon: iconsRole index = "ViewModelName".
4. Update Icon: iconsRole index = "UpdateModelName".
5. Delete Icon: iconsRole index = "DeleteModelName".

and there are some specific icons roles related to each model will be mentioned later.

for example when user request all users in the system the respons IconsRole part will be:

  **"iconsRole":**

        "InsertUser": true,
        "UpdateUser": false,
        "DeleteUser": false,
        "ResetUserPassword": true,
        "ChangeUserState": false

<br>
<hr>

**Specific Privileges:**

a. Users:
1. Reset Password: privilegeID = "ResetUserPassword".
2. Change State:  privilegeID = "ChangeUserState".
3. Change Type: privilegeID = "ChangeUserType".
4. Change Role Group: privilegeID = "ChangeRoleGroup".

b. Role Groups:
1. Change Role Group Privileges: privilegeID = "ChangeRoleGroupPrivilege".
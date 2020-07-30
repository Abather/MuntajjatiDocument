# Privileges

Privilege ID Structure: Action Type + [[Model State]] + Model Name

**Default Privilege for each model:**
1. New: privilegeID = "InsertModelName"
2. View: privilegeID = "ViewModelName"
3. Update: privilegeID = "UpdateModelName"
4. Delete: privilegeID = "DeleteModelName"

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


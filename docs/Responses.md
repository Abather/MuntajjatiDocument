# Responses

The default response sturecure of the system is as:

    [
    status: represent the action result.
    message: the maessage that will be shown to the user.
    iconsRole: array of privileges of the icons to show them or not.
    data: the data that the user requested or the result of his action
    ],
    code: the numeric represent

Status Codes:

    200: Action Completed
    201: Recored Created
    304: Action Not Completed
    401: Action Not Allowed
    404: Recored Not Found
    422:
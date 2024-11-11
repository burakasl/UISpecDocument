# User Interface Specification Document for User Management Screen

## Purpose and Target Audience

- **Purpose:** Define the visuals and behaviour of **User Management Screen**
- **Target Audience:** Administrators with priviliges to make changes on user data

## User Flows

- **Edit User Flow:**
  - User clicks the row with needed user data.
  - **Edit User** panel is displayed.
  - User updates the necessary fields.
  - User clicks **Save User** button.
  - On success, a pop-up with the success message is displayed. Then the screen is reloaded, displaying the updated data.
  - On failure, a pop-up with the error message regarding the problem is displayed.
- **Add User Flow**
  - User clicks the **New User** button.
  - **New User** panel is displayed.
  - User enters all data on respective fields.
  - User clicks the **Save User** button.
  - On success, a pop-up with the success message is displayed. Then the screen is reloaded, displaying users including the newly added.
  - On failure, a pup-up with the error message regarding the problem is displayed.
- **Order User List Flow**
  - User clicks a cell on the header row.
  - If list was not ordered by the data on the selected row, it gets sorted by that data in descending order.
  - If list was sorted in descending order by the data on the selected row, it gets sorted by that data in ascending order.
  - If list was sorted in ascending order by the data on the selected row, it gets sorted by that data in descending order.
- **Toggle Disabled Users Flow**
  - User clicks the **Hide Disabled User** text or its **checkbox**
  - The checkbox is toggled on/off.
  - Disabled users on the list are set visible or invisible according to the state of the checkbox.

## UI Elements

| Element                  | Type       | Label Text           | Behaviour                                                                                                                        | Position                                                     |
| ------------------------ | ---------- | -------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| New User Button          | Button     | "New User"           | Displays the "New User" panel                                                                                                    | On top left corner                                           |
| Disabled User Checkbox   | Checkbox   | "Hide Disabled User" | Default checked, toggled when clicked                                                                                            | To right of the New User Button                              |
| Save User Button         | Button     | "Save User"          | Applies the user changes on input fields; Triggers the notification pop-up                                                       | On top right corner                                          |
| User Table               | Table      | N/A                  | Displays user data in rows and columns; Sortable by column headers                                                               | Below New User Button, left                                  |
| New User Panel           | Panel      | N/A                  | Container for input fields                                                                                                       | To right of the User Table                                   |
| Username Input Field     | Text Field | "Username:"          | Focused by default; Triggers warning if left blank                                                                               | Inside the New User Panel, on the top, centered horizontally |
| Display Name Input Field | Text Field | "Display Name:"      | Triggers warning if left blank                                                                                                   | Below the Username Input Field, centered horizontally        |
| Phone Input Field        | Phone      | "Phone:"             | Triggers warning if left blank                                                                                                   | Below the Display Name Input Field, centered horizontally    |
| Email Input Field        | Text Field | "Email:"             | Validates email format                                                                                                           | Below the Phone Input Field, centered horizontally           |
| User Roles Dropdown      | Select     | "User Roles:"        | Displays a list of roles; User can select multiple roles; A hint is shown ("Select user roles..."); Selected roles are displayed | Below the Email Input Field, centered horizontally           |
| Enabled Checkbox         | Checkbox   | "Enabled:"           | Default unchecked, toggled when clicked                                                                                          |

## Error Handling

- **Invalid Username**
  - Message: "Please enter a valid username."
  - Style: Red text, 12px, below Username Input Field
- **Invalid Display Name**
  - Message: "Please enter a valid name."
  - Style: Red text, 12px, below Display Name Input Field
- **Invalid Phone**
  - Message: "Please enter a valid phone number."
  - Style: Red text, 12px, below Phone Input Field
- **Invalid Email**
  - Message: "Please enter a valid e-mail address."
  - Style: Red text, 12px, below Email Input Field
- **Invalid User Role**
  - Message: "Please enter at least one user role."
  - Style: Red text, 12px, below User Roles Dropdown

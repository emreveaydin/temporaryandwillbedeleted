# User Management Screen — UI Specification (UI Only)

This document specifies the **visible UI components** and the **user interactions/behaviors** for the “User Management” screen shown in the provided mockup.

## 1. Screen Overview
The screen is a two-panel user management page:
- **Left panel**: a toolbar and a users list table
- **Right panel**: a user details form and a “Save User” action

## 2. What the user sees on initial load
On initial load, the UI shows:
- The **users table** populated with existing users (as in the mockup).
- The **details form** in **“New User”** state (title “New User”) with empty inputs (as in the mockup).

## 3. Left Panel — Toolbar
### 3.1 `+ New User` button
- **Label**: `+ New User`
- **Behavior**: switches the right panel to the “New User” form state and clears the form inputs.

### 3.2 `Hide Disabled User` checkbox
- **Label**: `Hide Disabled User`
- **Behavior**:
  - When checked, the users table hides users that are disabled (i.e., `Enabled = false`).
  - When unchecked, the users table shows both enabled and disabled users.

## 4. Left Panel — Users Table
### 4.1 Columns
The table contains these columns (left to right):
1. **ID**
2. **User Name**
3. **Email**
4. **Enabled** (shows `true/false` in the mockup)

### 4.2 Header actions (sorting/filtering)
The column headers display icons indicating:
- **Sorting** on columns
- **Filtering** on columns

Exact filter UI (popup vs inline, operators, etc.) is not specified in the mockup; implement filtering and sorting consistent with the icons and the product’s table component.

### 4.3 Row selection
- Clicking a row selects that user in the table.
- Selecting a user loads that user into the right-side form for editing (fields populated with the selected user’s data).

## 5. Right Panel — User Form
### 5.1 Form title
- **New user state**: title is **“New User”** (as shown).

When a user is selected in the table, the form displays that user’s details (edit state). (The exact title text for edit state is not shown in the mockup.)

### 5.2 Fields (top to bottom)
The form contains the following labeled fields:
1. **Username**: text input
2. **Display Name**: text input
3. **Phone**: text input
4. **Email**: text input
5. **User Roles**: dropdown / selector input (shows placeholder “Select user roles...”)
6. **Enabled**: checkbox

### 5.3 User Roles selector
- Opens a list of roles.
- Roles visible in the mockup:
  - `Guest`
  - `Admin`
  - `SuperAdmin`

(Single vs multi-select behavior is not explicitly indicated in the mockup; implement according to the product requirement.)

### 5.4 Enabled checkbox
- Represents whether the user is enabled/disabled.
- The table’s “Enabled” column should reflect this value for each user.

## 6. Save User
### 6.1 `Save User` button
- **Label**: `Save User`
- **Behavior**:
  - In **New User** state: saves (creates) a new user with the form values.
  - In **Edit** state (after selecting a user): saves (updates) the selected user with the edited form values.

The mockup does not define validation rules, error messages, or success notifications; those should be implemented according to the product’s requirements and design system.


Title:
As an admin, I want to log into the portal with my username and password, so that I can manage the platform securely.

Acceptance Criteria:

A login form is presented on the portal's home page or a dedicated /login route.

The system authenticates the provided credentials against the database.

Upon successful login, the user is redirected to a protected admin dashboard.

Upon failed login, a clear error message is displayed without specifying whether the username or password was incorrect.

Priority: High
Story Points: 3
Notes:

Credentials must be transmitted and stored securely (e.g., hashed passwords).

The session should expire after a period of inactivity.

Title:
As an admin, I want to log out of the portal, so that I can protect system access when I am finished.

Acceptance Criteria:

A clearly visible "Log Out" button or link is available on all pages within the admin portal.

Clicking the button terminates the user's session and invalidates the authentication token.

Upon logout, the user is redirected to the public login page or home page and can no longer access protected admin routes.

Priority: High
Story Points: 1
Notes:

This is a critical security feature.

Title:
As an admin, I want to add a new doctor to the portal, so that they can be scheduled for appointments by patients.

Acceptance Criteria:

A form is available (e.g., on an "Add Doctor" page) to input doctor details: name, specialty, contact information, bio, etc.

Upon form submission, the data is validated (e.g., required fields, email format).

The new doctor's profile is saved to the database.

A success confirmation message is displayed, and the admin can view the new doctor in the system's list.

Priority: High
Story Points: 5
Notes:

Consider if a doctor should receive an automated email with login instructions upon being added.

The form should prevent the creation of duplicate entries.

Title:
As an admin, I want to delete a doctor's profile from the portal, so that I can remove doctors who are no longer with the organization.

Acceptance Criteria:

From a list of doctors, an admin can select a doctor and choose a "Delete" action.

A confirmation dialog appears to prevent accidental deletion.

Upon confirmation, the doctor's record is removed from the database (or marked as inactive).

A success message confirms the deletion, and the doctor is removed from the list.

Priority: Medium
Story Points: 3
Notes:

Critical: Deletion must handle relational data integrity (e.g., what happens to the doctor's future and past appointments?). A "soft delete" (setting an is_active flag to false) is highly recommended over a hard delete from the database.

Title:
As an admin, I want to run a predefined stored procedure from the MySQL CLI to get the number of appointments per month, so that I can track platform usage statistics.

Acceptance Criteria:

A stored procedure named GetAppointmentsPerMonth (or similar) exists in the database.

The procedure, when called with a year parameter (e.g., CALL GetAppointmentsPerMonth(2023);), returns a result set.

The result set shows each month of the given year and the total count of appointments for that month.

The procedure handles years with no appointments, returning 0 for those months.

Priority: Low
Story Points: 5
Notes:

This is a backend/database task with no direct user interface. The acceptance criteria are based on database functionality.

The story points cover the creation and testing of the complex SQL query for the procedure.

This functionality could later be extended to a visual report within the admin portal.
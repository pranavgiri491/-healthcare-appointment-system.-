Of course. Here are the doctor user stories formatted as requested.

---

### **Title:**
_As a doctor, I want to log into the portal with my credentials, so that I can manage my appointments and availability._

**Acceptance Criteria:**
1. A login form is accessible to doctors.
2. The system authenticates the doctor's credentials against the database.
3. Upon successful login, the doctor is redirected to their personal dashboard.
4. The dashboard view and functionality are tailored specifically for a doctor's role (e.g., shows appointments, not patient sign-ups).

**Priority:** High
**Story Points:** 3
**Notes:**
- The login endpoint/flow might be shared with patients and admins, but the redirect and session must be role-specific.

---

### **Title:**
_As a doctor, I want to log out of the portal, so that I can protect my patient data and schedule when I am finished._

**Acceptance Criteria:**
1. A clear "Log Out" button is present on the doctor's dashboard.
2. Clicking the button successfully terminates the session and invalidates the authentication token.
3. The user is redirected to the public homepage or login screen and can no longer access the doctor dashboard.

**Priority:** High
**Story Points:** 1
**Notes:**
- This is a critical security and privacy feature to comply with regulations like HIPAA.

---

### **Title:**
_As a doctor, I want to view my appointment calendar, so that I can stay organized and see my daily, weekly, and monthly schedule at a glance._

**Acceptance Criteria:**
1. The doctor's dashboard features a calendar view of their appointments.
2. The view can be toggled between day, week, and month formats.
3. Each appointment block displays the patient's name and the appointment time.
4. Clicking on an appointment block reveals more details (e.g., reason for visit, patient contact info).

**Priority:** High
**Story Points:** 8
**Notes:**
- This is a complex feature requiring a calendar UI component and robust backend scheduling logic.

---

### **Title:**
_As a doctor, I want to mark specific time slots as unavailable, so that patients can only book appointments during my available hours._

**Acceptance Criteria:**
1. Within the calendar or a dedicated "Availability" section, I can select dates and times to block off.
2. I can provide a reason for unavailability (e.g., "Vacation", "Conference", "Lunch Break").
3. Once saved, the blocked time slots are removed from the pool of available slots that patients can see and book.
4. Existing appointments in blocked periods remain unaffected and are still visible.

**Priority:** Medium
**Story Points:** 5
**Notes:**
- Should support setting recurring unavailability (e.g., every Wednesday afternoon).
- Consider a interface for setting default working hours.

---

### **Title:**
_As a doctor, I want to update my professional profile information, including my specialization, bio, and contact details, so that patients have accurate and up-to-date information about my practice._

**Acceptance Criteria:**
1. A "My Profile" or "Edit Profile" page is accessible from the dashboard.
2. I can edit fields such as: biography, list of specializations, qualifications, and contact information.
3. Changes are saved to the database upon submission.
4. The updated information is immediately reflected on the public doctor listing page.

**Priority:** Medium
**Story Points:** 3
**Notes:**
- Some fields (like name or internal ID) might be restricted and only editable by an admin.

---

### **Title:**
_As a doctor, I want to view the details of a patient who has booked an appointment with me, so that I can be prepared for our consultation._

**Acceptance Criteria:**
1. When I click on an upcoming appointment in my calendar, a details panel opens.
2. The panel displays the patient's full name, profile photo, phone number, and the reason for the appointment.
3. I can also see a history of past appointments I have had with this specific patient (e.g., date and reason).

**Priority:** Medium
**Story Points:** 5
**Notes:**
- This data must be presented in a secure manner, ensuring privacy compliance.
- Access to patient details must be strictly limited to appointments for that specific doctor.
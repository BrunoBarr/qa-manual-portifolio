## FORM VALIDATION – TEST CASES

---

### TC-FORM-01 — Required field left empty

**Objective:**  
Ensure that required fields display an error message when left empty.

**Steps:**
1. Access the form page
2. Leave all required fields empty
3. Attempt to submit the form

**Expected result:**  
An error message is displayed indicating that the field is required.

---

### TC-FORM-02 — Invalid email validation

**Objective:**  
Verify email format validation.

**Test data:**
- Email: `testemail` (missing `@` and domain)

**Steps:**
1. Enter an invalid email format in the email field
2. Fill in the remaining fields with valid data
3. Submit the form

**Expected result:**  
An error message is displayed stating **“Invalid email format”**.

---

### TC-FORM-03 — Character limit exceeded

**Objective:**  
Ensure that a maximum character limit is enforced for text fields.

**Test data:**
- Text field with more than 255 characters (e.g., repeated `AAAAA...`)

**Steps:**
1. Enter a value exceeding the allowed character limit
2. Submit the form

**Expected result:**  
The system prevents submission or displays an error indicating that the character limit has been exceeded.

---

### TC-FORM-04 — Numeric field with invalid characters

**Objective:**  
Verify validation of numeric input fields.

**Test data:**
- Number: `abc123`

**Steps:**
1. Enter alphabetic characters into a numeric field
2. Submit the form

**Expected result:**  
An error message is displayed indicating an invalid format.

---

### TC-FORM-05 — Password validation according to defined rules

**Objective:**  
Verify that the password follows the defined security requirements.

**Test data:**
- Password: `123` (too short or missing required criteria)

**Steps:**
1. Enter a password that does not meet the security rules
2. Submit the form

**Expected result:**  
An error message is displayed indicating the minimum password requirements (e.g., “minimum 8 characters”).

---

### TC-FORM-06 — Submission with valid data

**Objective:**  
Verify that the form accepts valid input data.

**Test data:**
- Email: `user@example.com`
- Number: `12345`
- Text: `QA Test`

**Steps:**
1. Fill in all fields with valid values
2. Click **Submit**

**Expected result:**  
The form is successfully submitted and a confirmation message is displayed.

---

### TC-FORM-07 — Read-only field

**Objective:**  
Validate that fields marked as **read-only** cannot be edited.

**Steps:**
1. Attempt to modify the read-only field

**Expected result:**  
The field cannot be edited.

---

### TC-FORM-08 — Disabled field

**Objective:**  
Confirm that disabled fields do not accept user input.

**Steps:**
1. Attempt to enter any value into the disabled field

**Expected result:**  
The field does not accept any input.

---

### TC-FORM-09 — Valid file upload

**Objective:**  
Test the upload functionality with allowed file types.

**Test data:**
- Valid file (`.jpg`, `.pdf`)

**Steps:**
1. Select an allowed file
2. Upload the file

**Expected result:**  
The file is uploaded successfully.

---

### TC-FORM-10 — Invalid file upload

**Objective:**  
Verify file type restrictions during upload.

**Test data:**
- Invalid file (`.exe` or unsupported format)

**Steps:**
1. Select an invalid file
2. Attempt to upload the file

**Expected result:**  
An error message is displayed indicating that the file format is not allowed.

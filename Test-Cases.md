# Heroku QA Demo – Test Cases

This document contains manually executed test cases for key features of “The Internet” Heroku application, focusing on functionality, UI behavior, and error handling.

## Feature: Form Authentication

### FA-01 – Valid Login
**Steps:**
1. Navigate to the Login page
2. Enter username: `tomsmith`
3. Enter password: `SuperSecretPassword!`
4. Click the Login button

**Expected Result:**  
User is redirected successfully and success message is displayed.

**Actual Result:**  
User is redirected successfully and success message is displayed.

**Status:**  Pass

---

### FA-02 – Invalid Username
**Steps:**
1. Navigate to the Login page
2. Enter username: `tom`
3. Enter password: `SuperSecretPassword!`
4. Click the Login button

**Expected Result:**  
User receives error message: *"Your username is invalid!"*

**Actual Result:**  
Error message *"Your username is invalid!"* displayed as expected.

**Status:**  Pass

---

### FA-03 – Invalid Password
**Steps:**
1. Navigate to the Login page
2. Enter username: `tomsmith`
3. Enter password: `WrongPassword!`
4. Click the Login button

**Expected Result:**  
User receives error message: *"Your password is invalid!"*

**Actual Result:**  
Error message *"Your password is invalid!"* displayed as expected.

**Status:**  Pass

---

### FA-04 – Blank Username and Password
**Steps:**
1. Navigate to the Login page
2. Enter username: ``
3. Enter password: ``
4. Click the Login button

**Expected Result:**  
User receives error message: *"Your username is invalid!"*

**Actual Result:**  
Error message *"Your username is invalid!"* displayed as expected.

**Status:**  Pass

---

### FA-05 – Blank Username
**Steps:**
1. Navigate to the Login page
2. Enter username: ``
3. Enter password: `SuperSecretPassword!`
4. Click the Login button

**Expected Result:**  
User receives error message: *"Your username is invalid!"*

**Actual Result:**  
Error message *"Your username is invalid!"* displayed as expected.

**Status:**  Pass

---

| Test Case ID | Title                         | Description                                  | Status |
|--------------|-------------------------------|----------------------------------------------|--------|
| FA-01        | Valid Login                   | Correct credentials login succeeds           |  Pass  |
| FA-02        | Invalid Username              | Wrong username triggers error message        |  Pass  |
| FA-03        | Invalid Password              | Wrong password triggers error message        |  Pass  |
| FA-04        | Blank Username and Password   | Empty fields return validation message       |  Pass  |
| FA-05        | Blank Username                | Username empty triggers username error       |  Pass  |

---

## Feature: Broken Images

### BI-01 – Identify Broken Images Visually
**Steps:**
1. Navigate to the Broken Images page
2. Inspect all image elements


**Expected Result:**  
Two images show broken file icons indicating load failure

**Actual Result:**  
 Two images show broken file icons indicating load failure. 
 One image appears with blank avatar

**Status:**  Pass

---

### BI-02 – Inspect with DevTools
**Steps:**
1. Navigate to the Broken Images page
2. Right-click each image and select "Inspect"
3. View the `src` attribute in DevTools  
4. Copy the `src` URL and open it in a new tab

**Expected Result:**  
At least one image does not load properly and displays a broken image icon or placeholder

**Actual Result:**  
- Two image `src` URLs returned a 404 Not Found when opened in a new tab  
- One image loaded successfully in the browser

**Status:**  Pass

---

## Test Case Summary – Broken Images

| Test Case ID | Title                           | Description                             | Status |
|--------------|---------------------------------|-----------------------------------------|--------|
| BI-01        | Identify Broken Images Visually | Confirm broken images are visible       | Pass   |
| BI-02        | Inspect with DevTools           | Validate image `src` responses          | Pass   |


---

## Feature: Dropdown

### DD-01 – Default Dropdown Option
**Steps:**
1. Navigate to the Dropdown page
2. Inspect the dropdown menu  
3. Observe the default selected option

**Expected Result:**  
Default selection is "Please select an option"

**Actual Result:**  
Default selection is "Please select an option"

**Status:**  Pass

---

### DD-02 – Select Option 1
**Steps:**
1. Navigate to the Dropdown page
2. Click the dropdown menu  
3. Select Option 1

**Expected Result:**  
Option 1 is displayed as the selected value in the dropdown

**Actual Result:**  
Option 1 was correctly displayed as selected after selection

**Status:**  Pass

---

### DD-03 – Select Option 2
**Steps:**
1. Navigate to the Dropdown page
2. Click the dropdown menu  
3. Select Option 2

**Expected Result:**  
Option 2 is displayed as the selected value in the dropdown

**Actual Result:**  
Option 2 was correctly displayed as selected after selection

**Status:**  Pass

---

## Test Case Summary – Dropdown

| Test Case ID | Title                   | Description                                | Status |
|--------------|-------------------------|--------------------------------------------|--------|
| DD-01        | Default Dropdown Option | Verify the default selected option         |  Pass  |
| DD-02        | Select Option 1         | Confirm Option 1 can be selected from menu |  Pass  |
| DD-03        | Select Option 2         | Confirm Option 2 can be selected from menu |  Pass  |

---

## Feature: Notification Message

### NM-01 – Trigger Notification Message
**Steps:**
1. Navigate to the Notification Message page
2. Click the **Click here** link

**Expected Result:**  
A notification message appears at the top of the screen. The message text may vary (e.g., "Action successful", "Action unsuccessful", etc.)

**Actual Result:**  
A notification message appears. The content changes with each click.

**Status:**  Pass

---

### NM-02 – Dismiss Notification Message

**Steps:**
1. Navigate to the Notification Message page  
2. Click the **Click here** link to trigger a message  
3. Click the **"×" (close)** icon on the notification banner

**Expected Result:**  
The notification message disappears from the screen after clicking the close icon.

**Actual Result:**  
The message was successfully dismissed and no longer visible.

**Status:**  Pass

---

## Test Case Summary – Notification Messages

| Test Case ID | Title                        | Description                                        | Status |
|--------------|------------------------------|----------------------------------------------------|--------|
| NM-01        | Trigger Notification Message | Verify that a notification appears after clicking  |  Pass  |
| NM-02        | Dismiss Notification Message | Confirm that the notification can be dismissed     |  Pass  |

---








# Method 1: Windows User Management Using GUI

## Help Desk Ticket #4561292 – Add User to Windows Computer

### 1. Overview

This method demonstrates how to create and configure a local Windows user account using the graphical interface (GUI) in Windows 11 Enterprise.

**Operating System:** Windows 11 Enterprise  
**Tool:** Computer Management  
**Feature:** Local Users and Groups  
**Account Name:** Richard  
**Ticket Category:** User Management

### 2. Ticket Requirements

The requester needs:

- A new local Windows user named `Richard`.
- Membership in the local Administrators group.
- A requirement to change the password at the next login.

### 3. Procedure

#### Step 1: Open Computer Management

1. Press `Win + R`.
2. Type `compmgmt.msc`.
3. Press Enter.
4. Computer Management will open.

#### Step 2: Navigate to Local Users and Groups

1. Expand System Tools.
2. Click Local Users and Groups.
3. Select Users.

#### Step 3: Create a New User

1. Right-click Users.
2. Select New User.
3. Enter the following information:

| Field | Value |
|---|---|
| User name | Richard |
| Full name | Richard |
| Description | Help Desk test account |
| Password | Temporary password |

4. Select **User must change password at next logon**.
5. Click Create.
6. Click Close.

#### Step 4: Add User to Administrators Group

1. Find Richard in the Users list.
2. Double-click Richard.
3. Open the Member Of tab.
4. Click Add.
5. Enter `Administrators`.
6. Click Check Names.
7. Click OK.
8. Click Apply and OK.

#### Step 5: Verify User Account

Verify the following:

- Richard exists in the Users list.
- Administrators appears in the Member Of tab.
- The password change requirement is configured.

### 4. Expected Outcome

The local user account should be created successfully with the requested administrator group membership and first-login password change requirement.

### 5. Screenshots and Evidence


## 5.1.  Computer Management opened 

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_22_28_58" src="https://github.com/user-attachments/assets/63108d8d-0f86-42ba-8699-db6144d644e9" />


## 5.2  Local Users and Groups 

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_22_29_38" src="https://github.com/user-attachments/assets/eeca4b40-1823-4169-942c-b07cd4cd82a3" />


## 5.3 User Configuration

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_22_31_44" src="https://github.com/user-attachments/assets/8c7d5c43-2e20-439b-9ebc-eb6ca2866552" />


## 5.4 Richard User Created 

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_22_32_15" src="https://github.com/user-attachments/assets/eb40c897-3ea4-40c0-ae00-2397710b9a7e" />


## 5.5 Password change requirement

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_23_19_21" src="https://github.com/user-attachments/assets/6c549bb6-1ff2-4fa1-a813-87cbdbc3441a" />



## 5.6 Administrators group membership 

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_22_33_11" src="https://github.com/user-attachments/assets/c9b64007-a72e-4cbf-a5f5-0f8dffe7b6fc" />


### 6. Skills Practiced

- Windows 11 Administration
- Local User Account Management
- Computer Management
- User Provisioning
- Administrator Group Management
- Password Configuration
- Help Desk Ticket Resolution

### 7. Learning Outcome

Learned how to create local Windows accounts, configure password requirements, assign administrator group membership, and verify account settings using the Windows graphical interface.

### 8. Disclaimer

This is an educational hands-on lab performed in a test environment for IT Support and Help Desk portfolio development. It does not represent professional employment experience.

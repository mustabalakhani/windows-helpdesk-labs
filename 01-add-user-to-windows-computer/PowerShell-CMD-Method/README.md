# Method 2: Windows User Management Using PowerShell and CMD

## Help Desk Ticket #4561292 – Add User to Windows Computer

### 1. Overview

This method demonstrates how to create and configure a local Windows user account using PowerShell and Command Prompt in Windows 11 Enterprise.

**Operating System:** Windows 11 Enterprise  
**Tools:** PowerShell and Command Prompt  
**Account Name:** Richard  
**Ticket Category:** User Management

### 2. Ticket Requirements

- Create a local user named `Richard`.
- Add Richard to the local Administrators group.
- Require a password change at the next login.

### 3. Procedure

**Important:** Run these commands in an elevated PowerShell or Command Prompt window on your test computer. If Richard already exists from Method 1, do not create the account again. Use a separate test VM or reset your lab account before demonstrating account creation.

#### Step 1: Open PowerShell as Administrator

1. Open the Start menu.
2. Search for PowerShell.
3. Right-click Windows PowerShell.
4. Select Run as administrator.

#### Step 2: Create the Local User

Run:

```powershell
$password = Read-Host "Enter a temporary password" -AsSecureString

New-LocalUser -Name "Richard" -FullName "Richard" -Description "Help Desk test account" -Password $password
```

This creates the local user account.

#### Step 3: Add Richard to Administrators

Run:

```powershell
Add-LocalGroupMember -Group "Administrators" -Member "Richard"
```

This adds Richard to the local Administrators group.

#### Step 4: Require Password Change at Next Login

Run:

```powershell
net user Richard /logonpasswordchg:yes
```

This configures the password-change requirement.

#### Step 5: Verify the User Account

Run:

```powershell
Get-LocalUser -Name "Richard"
```

Verify group membership:

```powershell
Get-LocalGroupMember -Group "Administrators"
```

Verify the password-change setting:

```powershell
net user Richard
```

#### Step 6: Command Prompt Alternative

The following CMD commands can also be used to create and configure the account on a clean test system:

```cmd
net user Richard * /add
net localgroup Administrators Richard /add
net user Richard /logonpasswordchg:yes
```

The first command prompts for a password instead of displaying it in the command.

### 4. Expected Outcome

- The local user Richard is created successfully.
- Richard is added to the Administrators group.
- The password-change requirement is configured.
- The account and group membership can be verified using commands.

### 5. Screenshots and Evidence

## 5.1 PowerShell opened as Administrator.

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_23_46_42" src="https://github.com/user-attachments/assets/1a3e3b23-e3f7-477c-a1f3-784e9ecd3f2b" />

## 5.2 Richard user account created.

<img width="1024" height="214" alt="VirtualBox_Windows 11_02_11_2026_23_56_40" src="https://github.com/user-attachments/assets/ef04046b-db20-4df3-9935-a63f577e2e6b" />

## 5.3 Richard added to Administrators.

<img width="1024" height="148" alt="VirtualBox_Windows 11_03_11_2026_00_11_18" src="https://github.com/user-attachments/assets/8710fc6d-57e0-4e39-aeac-c461e0eeb042" />

## 5.4 User account verification.

<img width="1024" height="195" alt="VirtualBox_Windows 11_02_11_2026_23_59_16" src="https://github.com/user-attachments/assets/60a440e9-fd0b-4890-a1d3-06bd9ea8e4cc" />


## 5.5 Administrators group verification.

<img width="1030" height="200" alt="VirtualBox_Windows 11_03_11_2026_00_15_16" src="https://github.com/user-attachments/assets/7252b3b1-7d15-403f-9072-c206367aa146" />

## 5.6 Password-change setting verification.

<img width="1024" height="768" alt="VirtualBox_Windows 11_02_11_2026_23_19_21" src="https://github.com/user-attachments/assets/2be5f74c-6d37-4a3e-a4bb-50038a899da3" />

### 6. Skills Practiced

- PowerShell Basics
- Windows Command Prompt
- Local User Management
- User Provisioning
- Administrator Group Management
- Account Verification
- Help Desk Ticket Resolution

### 7. Learning Outcome

Learned how to create local Windows accounts, configure group membership, set password requirements, and verify account settings using PowerShell and CMD.

### 8. Disclaimer

This is an educational hands-on lab performed in a test environment for IT Support and Help Desk portfolio development. It does not represent professional employment experience.

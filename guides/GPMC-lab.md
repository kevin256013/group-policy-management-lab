# GPMC (Group Policy Management) Lab

## Step 1: Navigating Group Policy Object's (GPO's)

1. In VM, open Group Policy Management, and elect your AD domain
![GPO Creation](../docs/screenshots/gpo-creation.png)

2. Go into "Group Policy Object" folder and right-click Default Domain Controllers Policy -> Edit
![GPO Creation](../docs/screenshots/gpo-creation-2.png)

3. Select where to create a GPO:
    - Computer Configuration - settings that apply to the whole computer.
    - User Configuration - settings that apply only to a specific user account.

## Step 2: Create/Setup a GPO (Password Policy) - To enforce strong passwords and enhance security

1. Open Group Policy Management, right-click domain name -> select "Create a GPO in this domain, and Link it here..."
2. Create GPO name (Use Descriptive Naming)
![Password GPO](../docs/screenshots/password-gpo.png)

3. Right-click on newly created policy -> select "Edit"
![Password GPO](../docs/screenshots/password-gpo-2.png)

4. Navigate to Computer Configuration -> Policies -> Windows Settings -> Security Settings -> Account Policies -> Password Policy 
![Password GPO](../docs/screenshots/password-gpo-3.png)

5. Select "Minimum password length", click "Define this policy setting", initiate minimum password length, click "Apply" and  "OK"
![Password GPO](../docs/screenshots/password-gpo-4.png)

6. Select "Password must meet complexity requirements", click "Define this policy setting", Select "Enable" , click "Apply" and  "OK"
![Password GPO](../docs/screenshots/password-gpo-5.png)

7. Select "Maximum password age", click "Define this policy setting", initiate password expiration, click "Apply" and  "OK"
![Password GPO](../docs/screenshots/password-gpo-6.png)

8. On the Policy Setting (Right Column) all changes to poicy are visible
![Password GPO](../docs/screenshots/password-gpo-7.png)

## Step 3: Create/Setup a GPO (Drive Mapping Policy) - Map network drives for users when they log in

1. In VM, open Group Policy Management, right-click domain name -> select "Create a GPO in this domain, and Link it here..."
2. Create GPO name (Use Descriptive Naming)
![Drive Mapping GPO](../docs/screenshots/drive-mapping-gpo.png)

3. Right-click on newly created policy -> select "Edit"

4. Navigate to User Configuration -> Preferences -> Windows Settings -> Drive Maps
![Drive Mapping GPO](../docs/screenshots/drive-mapping-gpo-2.png)

5. Right-click on Drive Maps -> New -> select Mapped Drive

6. fill "Location" with path of network share, in "Drive Letter" select "Use" and a Drive(A-Z), click "Apply" and "OK"
![Drive Mapping GPO](../docs/screenshots/drive-mapping-gpo-3.png)
![Drive Mapping GPO](../docs/screenshots/drive-mapping-gpo-4.png)

## Step 4: Create/Setup a GPO (Desktop Wallpaper Policy) - Set a default desktop wallpaper for all users

1. In VM, open Group Policy Management, right-click domain name -> select "Create a GPO in this domain, and Link it here..."
2. Create GPO name (Use Descriptive Naming)
![Desktop Wallpaper GPO](../docs/screenshots/desktop-wallpaper-gpo.png)

3. Right-click on newly created policy -> select "Edit"

4. Navigate to User Configuration -> Policies -> Administrative Templates -> Desktop -> Desktop
![Desktop Wallpaper GPO](../docs/screenshots/desktop-wallpaper-gpo-2.png)

5. Select "Desktop Wallpaper", select "Enabled", fill in Wallpaper Name with path of wallpaper, click "Apply" and "OK"
![Desktop Wallpaper GPO](../docs/screenshots/desktop-wallpaper-gpo-3.png)

## Step 5: Create/Setup a GPO (Restrict Control Panel) - Prevent users from accessing the Control Panel 

1. In VM, open Group Policy Management, right-click domain name -> select "Create a GPO in this domain, and Link it here..."
2. Create GPO name (Use Descriptive Naming)
![Control Panel Restriction](../docs/screenshots/restrict-control-panel-gpo.png)

3. Right-click on newly created policy -> select "Edit"

4. Navigate to User Configuration -> Policies -> Administrative Templates -> Control Panel
![Control Panel Restriction](../docs/screenshots/restrict-control-panel-gpo-2.png)

5. Select "Prohibit access to Control Panel & settings", select "Enabled", click "Apply" and "OK"
![Control Panel Restriction](../docs/screenshots/restrict-control-panel-gpo-3.png)
![Control Panel Restriction](../docs/screenshots/restrict-control-panel-gpo-4.png)

## Step 6: Create/Setup a GPO (Disable USB Storage) - Prevent users from using USB storage devices

1. In VM, open Group Policy Management, right-click domain name -> select "Create a GPO in this domain, and Link it here..."
2. Create GPO name (Use Descriptive Naming)
![USB Devices Disabled](../docs/screenshots/disable-usb-devices-gpo.png)

3. Right-click on newly created policy -> select "Edit"

4. Navigate to Computer Configuration -> Policies -> Administrative Templates -> System -> Removable Storage Access
![USB Devices Disabled](../docs/screenshots/disable-usb-devices-gpo-2.png)

5. Select "All Removable Storage classes: Deny all access", select "Enabled", click "Apply" and "OK"
![USB Devices Disabled](../docs/screenshots/disable-usb-devices-gpo-3.png)
![USB Devices Disabled](../docs/screenshots/disable-usb-devices-gpo-4.png)

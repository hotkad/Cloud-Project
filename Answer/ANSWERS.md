# Answers to Conditional Access Project Tasks

## Task 1: Create Two Test Users

* **Usernames**: test.user1@skt42.onmicrosoft.com, test.user2@skt42.onmicrosoft.com
* **Licenses**: E5 license assigned to both
* **Reason**: E5 includes Azure AD Premium P2, required for Conditional Access and Identity Protection
<img width="1862" height="925" alt="Screenshot 2025-08-14 085658" src="https://github.com/user-attachments/assets/5775ba29-2114-472a-b937-7da37b87ab79" />
<img width="1860" height="928" alt="Screenshot 2025-08-14 085715" src="https://github.com/user-attachments/assets/6dc08e45-9d3b-4a16-a5cd-ae3f6bb20cd9" />

## Task 2: Risk-Based Conditional Access Policy (User1)

* **Policy Name**: User1\_Risk\_PasswordReset
* **User Assignment**: User1
* **Risk Levels**: Medium and High
* **Grant Control**: Require password change
* **Policy State**: Enabled
* **Explanation**: Targets risky sign-ins (Sign-in risk and User Risk) to enforce password hygiene
<img width="1860" height="926" alt="Screenshot 2025-08-14 085857" src="https://github.com/user-attachments/assets/a1d4e6c3-513e-4d8a-8b68-3d171bc149fc" />
<img width="1861" height="928" alt="Screenshot 2025-08-14 085920" src="https://github.com/user-attachments/assets/0fe256cb-e128-4bb6-86ad-ec26bc65792f" />
<img width="1855" height="924" alt="Screenshot 2025-08-14 090019" src="https://github.com/user-attachments/assets/bc695921-ef6a-4507-b35e-b1efc95a7c9a" />
USER RISK
<img width="716" height="911" alt="Screenshot 2025-08-15 143221" src="https://github.com/user-attachments/assets/9a73608a-d377-4179-bf2b-0195465cf537" />
<img width="409" height="874" alt="Screenshot 2025-08-15 143239" src="https://github.com/user-attachments/assets/47e5bf17-6454-4597-a68a-ecff50849e56" />
<img width="452" height="871" alt="Screenshot 2025-08-15 143305" src="https://github.com/user-attachments/assets/02260576-57f9-47de-bef0-3fa8808e338e" />

## Task 3: Simulate Risk for User1

* **Method**: Used TOR browser and VPN from a high-risk IP
* **Reason**: Microsoft flags anonymous or suspicious IPs as risky
  <img width="1855" height="918" alt="Screenshot 2025-08-14 092823" src="https://github.com/user-attachments/assets/6809ce38-fb4a-451f-acc8-b6a02ae9e5f2" />
<img width="1858" height="931" alt="Screenshot 2025-08-15 114904" src="https://github.com/user-attachments/assets/38c9dee0-4d27-4885-99d9-5a5dc7f37fd2" />
<img width="1159" height="644" alt="Screenshot 2025-08-15 143908" src="https://github.com/user-attachments/assets/d352c67a-c0fd-4377-a4a1-eb1c4adb114a" />

## Task 4: Enforcement Outcome (User1)

* **Experience**: Prompted to change password/Blocked login 
* **Logs**: Identity Protection shows Medium/High sign-in risk/ user risk
* **Screenshots**: Included in screenshots folder
  <img width="1902" height="838" alt="Screenshot 2025-08-15 102847" src="https://github.com/user-attachments/assets/56a91712-1fc8-41df-b6fb-bbee329a5b5f" />
<img width="1920" height="860" alt="Screenshot 2025-08-14 154251" src="https://github.com/user-attachments/assets/2270d1bd-c4d1-4940-b52b-8680505ee407" />
<img width="1159" height="644" alt="Screenshot 2025-08-15 143908" src="https://github.com/user-attachments/assets/86c0b8e4-5fe7-44dd-a64c-faae3516624a" />
## Task 5: Location-Based Conditional Access Policy (User2)

* **Policy Name**: User2\_Block\_Nigeria
* **User Assignment**: User2
* **Named Location**: Nigeria
* **Included Locations**: Nigeria
* **Grant Control**: Block access
* **Policy State**: Enabled
* **Explanation**: Prevent access from high-risk geography
  <img width="1862" height="928" alt="Screenshot 2025-08-14 090121" src="https://github.com/user-attachments/assets/9bb81df0-9068-40cf-a0c6-5d91e96129f5" />
<img width="1855" height="921" alt="Screenshot 2025-08-14 090158" src="https://github.com/user-attachments/assets/286f54ff-e4df-4cff-8d74-48ee12fa3cc7" />
<img width="1861" height="925" alt="Screenshot 2025-08-14 090220" src="https://github.com/user-attachments/assets/7b4e1cc0-2139-47c2-96fe-4037aeacb454" />
<img width="1853" height="922" alt="Screenshot 2025-08-14 090332" src="https://github.com/user-attachments/assets/28a5c57b-d158-4200-b754-9bcb60b4fa3b" />
<img width="1856" height="924" alt="Screenshot 2025-08-14 090344" src="https://github.com/user-attachments/assets/1444b46c-c8f3-46ab-b930-941bb23bad5f" />


## Task 6: Test Location Policy (User2)

* **Method**: VPN with Nigerian IP
* **Evidence**: Blocked sign-in logs and screenshots
<img width="1920" height="848" alt="Screenshot 2025-08-14 154622" src="https://github.com/user-attachments/assets/2753667f-6c6a-47a8-addd-c97c3f13906f" />

## Task 7: Recommendations

* Enable alerts for risky sign-ins
* Document exceptions and trusted locations
* Automate policy deployment with scripts

Answers to Conditional Access Project Tasks

Task 1: Create Two Test Users

* Usernames: test.user1@skt42.onmicrosoft.com, test.user2@skt42.onmicrosoft.com
* Licenses**: E5 license assigned to both
* Reason: E5 includes Azure AD Premium P2, required for Conditional Access and Identity Protection

 Task 2: Risk-Based Conditional Access Policy (User1)

* Policy Name: User1\_Risk\_PasswordReset
* User Assignment: User1
* Risk Levels: Medium and High
* Grant Control: Require password change
* Policy State: Enabled
* Explanation: Targets risky sign-ins (Sign-in risk and User Risk) to enforce password hygiene

Task 3: Simulate Risk for User1

* Method: Used TOR browser and VPN from a high-risk IP
        * Microsoft graph was implored to create a semblance of compromise user for user1 
* Reason: Microsoft flags anonymous or suspicious IPs as risky

Task 4: Enforcement Outcome (User1)

* Experience: Prompted to change password/Blocked login 
* Logs: Identity Protection shows Medium/High sign-in risk/ user risk
* Screenshots: Included in screenshots folder

 Task 5: Location-Based Conditional Access Policy (User2)

* Policy Name: User2\_Block\_Nigeria
* User Assignment: User2
* Named Location: Nigeria
* Included Locations: Nigeria
* Grant Control: Block access
* Policy State: Enabled
* Explanation: Prevent access from high-risk geography

 Task 6: Test Location Policy (User2)

* Method: VPN with Nigerian IP
* Evidence: Blocked sign-in logs and screenshots

 Task 7: Recommendations

* Enable alerts for risky sign-ins
* Document exceptions and trusted locations
* Automate policy deployment with scripts

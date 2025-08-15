Risk-Based Conditional Access Policy — User1

Policy Name
User1_Risk_PasswordReset

User Assignment
- Included: test.user1@skt42.onmicrosoft.com
  
Target Resource
- All Cloud Apps
 
 Conditions
- User Risk Levels: Medium and High

Grant Controls
- Require password change

 Policy State
- On


Policy Name
User1 Sign-in_Risk

User Assignment
- Included: test.user1@skt42.onmicrosoft.com
 
Target Resource
- All Cloud Apps
  
 Conditions
- Sign-in Risk Levels: Medium and High

Grant Controls
- Block

 Policy State
- On


 Notes
- Policy targets risky sign-ins to enforce password reset, and also blocks the login attempt
- Tested using T VPN

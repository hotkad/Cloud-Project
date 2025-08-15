Entra ID Conditional Access — Risk & Location Challenge

Objective
This project demonstrates the design, implementation, and testing of two Conditional Access policies in an Entra ID test tenant:
1. Sign-in Risk Policy — Enforces a password change for risky sign-ins.
2. Location-Based Policy — Blocks sign-ins from Nigeria.

The goal is to help trainees understand how to configure, test, and safely roll out Conditional Access controls.



Environment Assumptions
- Azure AD (Entra ID) test tenant with E5 licenses assigned to test users.
- Identity Protection and Conditional Access features are enabled.
- Admin access to Microsoft Graph API or Graph Explorer for risk simulation.
- VPN or TOR browser available for location and sign-in risk simulation.

Test Users
- User1: Used for user risk and sign-in risk policy testing.
- User2: Used for location-based policy testing.



 Policies Implemented

1. user risk and Sign-in Risk Policy (User1)
- Trigger: Medium or High sign-in risk
- Action: Require password change
- Simulation: TOR browser or VPN to simulate risky sign-in
- Verification: Identity Protection logs and sign-in logs

 2. Location-Based Policy (User2)
- Trigger: Sign-ins from Nigeria
- Action: Block access
- Simulation: VPN with Nigerian IP
- Verification: Sign-in logs and Conditional Access insights



 Testing Steps

Sign-in Risk Simulation
1. Sign in as User1 using TOR or VPN.
2. Confirm sign-in risk is detected in Identity Protection.
3. Verify Conditional Access policy enforcement (password change prompt).

User Risk Simulation
1. Use Microsoft Graph API to mark User1 as compromised.
2. Confirm user risk is detected in Identity Protection.
3. Verify Conditional Access policy enforcement (block or password reset).

Location-Based Simulation
1. Sign in as User2 using VPN from Nigeria.
2. Confirm sign-in is blocked.
3. Capture logs and screenshots.



Evidence Requirements
- Screenshots of:
  - Policy configuration pages
  - Identity Protection logs
  - Sign-in logs showing risk detection
  - Blocked access or password change prompts
- All screenshots must include timestamps and unaltered metadata.
- If automation was used, include:
  - The command executed
  - Resulting policy in the console



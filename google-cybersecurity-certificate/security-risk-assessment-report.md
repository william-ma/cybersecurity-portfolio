# Security risk assessment report

## Part 1: Select up to three hardening tools and methods to implement

The three network hardening tools I would implement would be password policies, port filtering and multi-factor authentication. 

Password policies specify the requirements for passwords, such as a minimum length, checking password strength, requiring certain letters and disallowing defaults or password reuse. 

Port filtering allows or blocked network traffic based on the port number. This can be used to filter application-level traffic. 

Multi-factor authentication (MFA) requires the user to produce an extra factor during the authentication process such as a fingerprint or code sent to the user's device. 

## Part 2: Explain your recommendations

I recommended password policies because the organization's employees' share passwords and the admin password for the database is set to the default.
The admin password for the database shouldn't be the default password. It should be strong and only known to authorized employees. 
Employees in the organization shouldn't share passwords, this is a vulnerability. Because, there's more surface for an account to be compromised. 
If they need to, they should do it in a secure manner such as via a password manager. This would prevent brute-force attacks in the future. 

Policies such as a login-limit would be very effective in defending as brute-force attacks. 

I recommended port filtering, because the organization has a firewall, however no rules are set up to filter traffic. 
Port filtering can be set up to only allow traffic the organization uses, thereby greatly reducing the attack surface. 
This protects the internal network from potential malicious traffic coming from outside. 

Multi-factor authentication (MFA) adds an additional layer of security on top of the user's password. This adheres to the defense-in-depth principle. 
MFA will make brute-force attacks more difficult as an extra factor is required in the authentication process. 
MFA could also dissuade employees from sharing passwords, due to the additional effort required to login. 

All the hardening techniques recommended should be implemented and audited every few months, 
due to how rapidly the cybersecurity landscape changes and in order to accomodate the organization's needs. 

# Security risk assessment report

## Part 1: Select up to three hardening tools and methods to implement

The three network hardening tools I would implement would be password policies, port filtering and multi-factor authentication. 

## Part 2: Explain your recommendations

I recommended password policies because the organization's employees' share passwords and the admin password for the database is set to the default.
The admin password for the database shouldn't be the default password. It should be strong and only known to authorized employees. 
Employees in the organization shouldn't share passwords, this is a vulnerability. Because, there's more surface for an account to be compromised. 
If they need to, they should do it in a secure manner such as via a password manager. This would prevent brute-force attacks in the future. 

I recommended port filtering, because the organization has a firewall, however no rules are set up to filter traffic. 
Port filtering can be used to only allow traffic containing the ports the organization uses, thereby greatly reducing the attack surface. 

I recommended multi-factor authentication (MFA). This further helps protect against brute-force attacks that could compromise employee's and administrator accounts. 
Because MFA, requires an extra factor in addition to the user's password, such as a fingerprint or code sent to the user's device, it follows the defense-in-depth model. 

All the hardening techniques recommended should be auditied every few months, because the cybersecurity landscape changes so rapidly. 

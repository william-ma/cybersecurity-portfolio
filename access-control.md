# Access controls

## Scenario

You’re the first cybersecurity professional hired by a growing business.

Recently, a deposit was made from the business to an unknown bank account. 
The finance manager says they didn’t make a mistake. 
Fortunately, they were able to stop the payment. 
The owner has asked you to investigate what happened to prevent any future incidents.

To do this, you’ll need to do some accounting on the incident to better understand what happened. 
First, you will review the access log of the incident. 
Next, you will take notes that can help you identify a possible threat actor. 
Then, you will spot issues with the access controls that were exploited by the user. 
Finally, you will recommend mitigations that can improve the business' access controls and reduce the likelihood that this incident reoccurs.

## Notes

From the Event log, I can see the following information about the unauthorized deposit:
1. It was made on `10/03/2023` at `08:29.57 AM`
2. The IP address is `152.207.255.255`
3. The user account is `Legal\Administrator`
4. The host name of the computer is `Up2-NoGud`
5. Payroll event added to `FAUX_BANK`

## Issues

After reviewing the Employee directory, we can see `Robert Taylor Jr.` a contractor has an IP address of `152.207.255.255`, the same IP address used to make the unauthorized deposit. 
Their role is `Legal attorney`, which explains the user account and their last login time was at `08:29.57 AM`. 

Some obvious issues found in the employee directory are:
1. All employees are given `Admin` level authorization, including contractors.
2. It says `Robert Taylor Jr.`'s end date is `12/27/2019`, so that account should have been deactivated. There's a lot of `N/A` in the `End date` column. 

## Recommendations

1. Have proper access controls. Give employees the minimum level of access they need to complete their task.
2. Regularly audit user accounts. This ensures employees that are no longer working at the company, won't have active accounts. 

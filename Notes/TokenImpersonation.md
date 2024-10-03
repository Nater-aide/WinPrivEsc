# Token Impersonation attacks
Tokens are cookies for your computer. 
- Delegate token -- seen most often. Someone logging into a machine or RDP
- Impersonate -- non interactive such as attaching a netowrk drive or login script

Look for **SEAssignPrimaryToken** or **SEImpersonatePrivilege** access -- this indicates a possible potato attack

## Rotten Potato  
https://foxglovesecurity.com/2016/09/26/rotten-potato-privilege-escalation-from-service-accounts-to-system/

## Juicy potato
https://github.com/ohpe/juicy-potato


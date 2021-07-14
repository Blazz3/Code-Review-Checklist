# Code-Review-Checklist
## Some of the following questions might be excluded depending on the type of software you might be dealing with, but they are meant to be as general as possible to be a good guidance during the review process.

- [ ] Is any sensitive/private/confidential information logged?
- [ ] Is any sensitive/private/confidential information disclosed?
- [ ] Are audit trails present?
- [ ] Are authentication and authorization mechanisms consistently enforced? Are they adequate to the intended security degree wanted?
- [ ] Is every access to an object authorized (i.e., complete mediation)?
- [ ] Is the least privilege principle enforced?
- [ ] Is defense in depth applied?
- [ ] Is segregation of duties principle ensured?
- [ ] In case of failures, does the system fail safely?
- [ ] Is encryption performed? Is it adequate to the security needs?
- [ ] Are weak ciphers used?
- [ ] Are security keys too small to provide adequate security?
- [ ] Are certificates valid?
- [ ] Are security keys protected from unauthorized access?
- [ ] Are hashing mechanisms used to check for integrity when needed?
- [ ] Are security tests in place?
- [ ] Which is the weakest link in the security chain? Is it secure enough?
- [ ] Are systems secure enough to expose the least attack surface as possible?
- [ ] Are all entry points to the system secured?
- [ ] Is input validated against well-known attacks (e.g., SQL injection, XSS injection)?
- [ ] Does the system plan for failure?
- [ ] Is security by obscurity in place instead of proper mechanisms?
- [ ] Does the code contain any security bug (also language dependent)?
- [ ] Are privacy-enhanced protocols in place when required?
- [ ] Are the used protocols tamper resistant?
- [ ] Is the code resistant to buffer overflow?
- [ ] Is there any hard-coded password?
- [ ] Is there any backdoor in the code?
- [ ] Is the code compliant with security policies and standards?
- [ ] Are security requirements clear?
- [ ] Is the team well trained on security?
- [ ] Are security response plan and processes in place?

## Notes on approach a target

- [ ] Subdomain enumeration
- [ ] Discovery files/folders/endpoints/functions using a generic wordlist and a target/technology specific wordlist
- [ ] Javascript files
- [ ] Read documentation
- [ ] Trying, experimenting, and reading

Workflow
1. Basic recon over the app through browsing and firing payloads.
2. Proxying with Burp and normal recon over the functions in the app.
3. Pick up a particular function and testing business logic.

Quotes
"Curiosity is the mother of Invention"

Before submitting any bug, ask yourself: "How can an attacker leverage this behavior into crafting a real-world or practical exploitation scenario?" and if you can’t figure out a possible scenario, then don’t submit. 

ZSEANO Notes
Hunting and finding interesting functionality
- [ ] What is this doing? 
- [ ] What is going on here? 
- [ ] Can I do anything here?
- [ ] What happens if I do this? 
- [ ] How did they prevent against?
- [ ]  What did the developers do?
- [ ] I wonder if the devs thought about XYZ when creating this feature
- [ ] I notice a website is using a new framework to protect from XSS, I will stop looking for XSS and focus on what MAY be vulnerable
- [ ] I'd also do research into how they've protected from something like XSS
- [ ] And do opposite things which application saying.

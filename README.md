Task 1: OWASP Top 10 Risk Analysis & Case Study
Instructions:
1. Visit the OWASP official website: https://owasp.org/.

2. Provide a brief introduction to OWASP by answering:
   
What is OWASP, and why is it important?
The Open Web Application Security Project (OWASP) is a global non-profit that aims to make software more secure. Established in 2001, OWASP is a community-driven initiative that seeks to assist developers, security experts and organizations with the resources, tools and education needed to fix the vulnerabilities present in their web and mobile applications. Because its projects are not tied to any particular vendor, OWASP can be considered a neutral vendor which adds credibility in the cybersecurity industry. OWASP is vital in today’s world because of the increased reliance on web applications for a wide range of business activities, communication and commercial purposes. With the advancement of technology comes the associated risks and vulnerabilities that come with them. The proactive and reactive measures that companies and users need to take because of insecure APIs, ransomware attacks, data breaches and other severe threats are exceedingly common. OWASP’s mission is to aid organizations and developers in adopting practices that reduce these risks.

What is the OWASP Top 10, and how does it help organizations?
OWASP Top 10 is a well-known document in the world, which describes the 10 most serious things that threaten the safety of web applications. Originally published in 2003, it has been amended periodically to address the changing threat landscape. The most recent edition (from 2021) continues its work as an all-in-one resource for developers, security pros, and organizations, summarizing the most prevalent and powerful weaknesses that can be exploited to compromise web apps. For organizations involved in the development or deployment of web applications, the OWASP Top 10 is commonly used as a security benchmark. The OWASP Top 10 provides a roadmap for developers to follow in order to address security risks during the software development lifecycle, giving them the knowledge to incorporate security best practices and inhibit vulnerabilities from forming as early as possible.

How often is the OWASP Top 10 updated, and why does it change?
The OWASP Top 10 is updated in a three to four year cycle that depends on factors like the development and emergent nature of new threats, changes in the security ecosystem and the need to provide more accurate guidance. The most recent update was in 2021 with its predecessors in 2017, 2013 and 2010. The OWASP community keeps a close eye on emerging trends and vulnerabilities to make sure their list stays up-to-date and genuinely helpful for developers and security experts.

3. Select one security risk from the OWASP Top 10.
A03:2021-Injection

4. Provide a detailed analysis of the selected risk, including:
   
Risk description: What does this vulnerability mean?
Injection vulnerabilities occur when an application mistakenly treats untrusted user input, such as text in a form or search bar, as executable code. An attacker can exploit this vulnerability by injecting malicious commands to trick the application into performing unintended actions. For example, in a SQL injection attack, an attacker might enter a SQL statement into a login field. If the application fails to validate or filter this input, malicious SQL code could be executed, potentially exposing sensitive data, deleting records, or even granting the attacker control over the database. To prevent this from happening, all user input must be properly validated and filtered before it is processed.

How it happens: How do attackers exploit this weakness?
Attackers exploit this vulnerability by entering input that the application mistakenly treats as executable code or commands. For example, in a web application with a login form that verifies user credentials using an SQL query, if the input from users is directly inserted into the query such as SELECT * FROM users WHERE username = '$username' AND password = '$password', it becomes vulnerable to manipulation. An attacker could input something like ' OR '1'='1 into both the username and password fields. This changes the logic of the query to always return true, effectively bypassing authentication and granting the attacker unauthorized access.

Prevention: How can developers protect web applications from this risk?
To defend against injection vulnerabilities, developers should always use parameterized queries or prepared statements, which separate SQL logic from input data. This guarantees that user inputs are not regarded as executable code but only as data. An ORM framework to formulate the raw SQL queries would also decrease the injection chances. Another key area in which to focus is input validation, which allows applications to strictly enforce acceptable input types and formats. Proper escaping can be used to neutralize harmful characters when user input must be used in a command or query. In addition to all of this, the least privilege principle should also be applied where database accounts used by applications should have only the necessary permissions they require. Web Application Firewalls (WAFs) can be used by developers to monitor and filter out harmful input and security testing tools such as OWASP ZAP or SQLMap can be used on a regular basis to run tests for vulnerabilities in code. Working to adopt these best practices can go a long way to help developers reduce the threat of injection attacks and keep their web applications safe from serious security breaches. 

5. Research a real-world web security breach that reflects your selected risk.
Equifax Data Breach (2017)

6. Answer the following in relation to the chosen risk:
   
What happened in the breach?
A vulnerability (CVE-2017-5638) in the web application framework Apache Struts was made public in March 2017. Through injection attacks, this vulnerability enabled attackers to remotely carry out arbitrary commands. Equifax's systems were left vulnerable because they neglected to repair the flaw. In May 2017, attackers used malicious commands injected into web requests to take advantage of the unpatched system. Attackers stole 147 million people's names, Social Security numbers, birth dates, and addresses during the 76 days that the breach remained undiscovered. Equifax only became aware of the hack in July 2017 and made it public in September of the same year.

How does the breach relate to the selected OWASP risk?
The attackers took use of an unpatched injection vulnerability in Apache Struts to introduce malicious commands into Equifax's web application. Due to this vulnerability, they were able to remotely run arbitrary code and get unauthorised access to private information kept in Equifax's systems. Attackers can modify queries and system instructions due to injection issues, such as SQL Injection and Command Injection, which arise when an application handles user input incorrectly. In this instance, the Apache Struts vulnerability was well known, but Equifax neglected to patch the system, leaving it vulnerable to assault.

What could have prevented the attack?
Patching and updating on time - The assault may have been avoided if Equifax had installed the Apache Struts security patch as soon as it was made available.
Validation and Sanitisation of Input - Command injection hazards might have been reduced with proper input validation and escape.
Firewall for Web Applications (WAF) - Malicious injection attempts may have been identified and stopped by a WAF before they reached the web server.
Frequent penetration tests and security audits - Vulnerabilities may have been found and repaired by security testing before attackers took use of them.
The Principle of Least Privilege - Limiting access to databases and applications might have lessened the breach's effects.

REFERENCES
Portnox. (2025). What is OWASP & why is it important? Retrieved from https://www.portnox.com/cybersecurity-101/what-is-owasp-why-is-it-important/#:~:text=OWASP%20is%20important%20because%20web,the%20risks%20associated%20with%20vulnerabilities

Barracuda. (2025). OWASP Top 10. Retrieved from https://www.barracuda.com/support/glossary/owasp-top-10#:~:text=The%20Top%2010%20lists%20are,focuses%20on%20improving%20software%20security

Kiuwan. (2024, June 27). What Is New in the OWASP Top 10 in 2024? Retrieved from https://www.kiuwan.com/blog/owasp-top-10/#:~:text=The%20OWASP%20Top%2010%20is,2017%2C%202013%2C%20and%202010

OWASP. (2021). A03:2021 – Injection. Retrieved from https://owasp.org/Top10/A03_2021-Injection/   

Breachsense. (2024, December 8). Equifax Data Breach Explained: A Case Study. Retrieved from https://www.breachsense.com/blog/equifax-data-breach/ 

Fruhlinger, J. (2020, February 12). Equifax data breach FAQ: What happened, who was affected, what was the impact? Retrieved from https://www.csoonline.com/article/567833/equifax-data-breach-faq-what-happened-who-was-affected-what-was-the-impact.html 

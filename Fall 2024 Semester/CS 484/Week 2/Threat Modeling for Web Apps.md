

What is Threat Modeling?
	A systematic approach to identifying and addressing potential security threats in software systems.

Web apps can get increasingly important for businesses and personal use, they should be protected.



Threat Modeling is the process of identifying threats and vulnerabilities in systems.
You can use threat modeling to determine the potential impact of these threats and figure out how to mitigate/eliminate these threats


Key concepts in Threat Modeling:
	[[assets]]
	[[threats]]
	[[vulnerabilities]]
	[[attackers]]
	[[mitigations]]


The Threat Modeling Process:
	1. Identify [Assets](assets.md)
		- Identify what needs protection in a web application
			- **User Data** (personal information, passwords, payment details)
			- **Application Logic** ( the code that drives your app)
			- **Infrastructure** ( Servers, databases, and networking components)
	2. Create an Architecture Diagram
		- A diagram that shows how different parts of your web app interact
			- Client-side components (browser, mobile apps)
			- Server-side components (web servers, app servers, databases)
			- External Systems (third party services, APIs)
	3. Identify [Threats](threats.md)
		- Consider possible threats to each component in the architecture diagram
		- You can use the [[STRIDE model]] to identify
			- Spoofing
			- Tampering
			- Repudiation
			- Information Disclosure
			- Denial of Service
			- Elevation of Privilege
	1. Identify [Vulnerabilities](vulnerabilities.md)
		- For each [threat](threats.md) identify what vulnerability could be exploited
			- SQL Injection
			- Insecure Direct Object References (IDOR)
			- Weak Authentication
	2. Mitigate [Threats](threats.md)
			- Decide how to mitigate each identified threat.
			- Input validation and sanitization for SQL Injection prevention
			- Access controls to ensure users can only access data they are authorized for
			- Authentication measures to prevent spoofing and unauthorized access
			- And other [[security principles]]
	
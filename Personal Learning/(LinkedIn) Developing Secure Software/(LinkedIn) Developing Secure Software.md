

Vulnerabilities
	- Any weakness exploitable by threats
	Defects
	- Any errors introducing vulnerabilities
	Flaws
	- Design errors resulting in vulnerabilities
	Bugs
	- Coding errors resulting in vulnerabilities


Probability:
	How likely a software vulnerability is likely to be exploited by a threat
Consequences:
	The extent to which a software security incident can be damaging




Software Security Threats
	***- Threats to software security***
		- Threat vector
			- a mechanism by which cyber security criminals get unauthorized access to protected resources
		- Disgruntled employees that drop logic bombs in code
			- Good to perform code reviews by peers to avoid future attacks at the code level
		-  Trusted Platform Modules (TPM)
			- Counter measure designed to prevent breaches from hardware vulnerabilities
		- Security Requirements
			- access control: 
				- without this anyone can access the software
	***- Hardware level threats***
		- Hardware keyloggers or disruption to hardware
		- Natural disasters can destroy hardware where software is running
		- Software Security relies on hardware/physical security
		- Countermeasures
			- Redundancy to avoid a single point of failure
			- UPS (uninterruptible power supply)
			- Physical security
	***- Code level threats***
		- Unintentional
			- Coding errors (need for more secure coding knowledge)
			- buffer overflow attacks in C
		- Intentional
			- Malicious insider
				- Who plant a logic bound in source code
					- Eventually will make software misbehave or vulnerable
		- Prevention
			- Education and training
			- Automatic (static and dynamic code analysis)
		- Preventing Intentional Threats
			- Peer code reviews
			- Job Rotations
			- Mandatory Vacation (keep employees happy i guess)
	***- Detailed design level threats***
		- Recurring security problems
			- Improper input validation
			- SQL injection attacks
		- Design patterns for security
			- Well-known solutions to recurring security problems
		- Three choices
			- No action (worst option)
			- Your solution (suboptimal option)
			- Adopting design patterns
		- Design pattern limitations
			- Local solution
			- partial coverage
			- remaining vulnerabilities
		- Design patterns for Security
			- No use (no protection)
			- local use (partial protection)
	***- Architectural level threats***
		- Overarching design decisions
		- software security problems
		- Architectural patterns
			- Widely accepted solutions to recurring architectural design problems
			- Quality attribute: security, performance, modifiability
			- Example:
				- Single access point
				- Architectural pattern
				- One entry point
	*- **Requirements level threats****
		- Problems:
			- Customers and users don't know what they want
			- Requirements engineers don't know what to ask.
		- Solutions to mitigate
			- Extra resource
			- Software security expert
			- Security Requirements Checklist
				- Stakeholders can add to the checklist
				- Requirements engineers ask questions
	*- **Threat Modeling & Tools***
		- Identify
		- Analysis
		- Categorization (provides basis for prioritizing threats)
		- Mitigation
		- Threat Modeling tool
			- STRIDE
				- Spoofing
				- Tampering
				- Repudiation
				- Information Disclosure
				- Denial of Service
				- Elevation of Privilege
			- Should be ongoing throughout the lifetime of a software system.
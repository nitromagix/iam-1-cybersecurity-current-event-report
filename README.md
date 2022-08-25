# iam-1-cybersecurity-current-event-report

### Buffer overflow

In March 2020 a security flaw, tracked as CVE-2020-0796, was described as "a Buffer Overflow Vulnerability in Microsoft SMB Servers" and received a maximum severity rating. (zdnet.com) The SMB vulnerability was accidentally disclosed when Cisco Talos published a report on Microsoft's Patch Tuesday, which included information about the flaw and "wormable" attacks that could exploit it. (techtarget.com)

"The vulnerability is due to an error when the vulnerable software handles a maliciously crafted compressed data packet," Fortinet said. "A remote, unauthenticated attacker can exploit this to execute arbitrary code within the context of the application." (zdnet.com)

Buffers are areas of memory set aside to hold data. Buffer overflow attacks are triggered when malformed inputs larger than the buffer's alloted size are written to the buffer and consequently overwrite data or executable code adjacent to the buffer. Using some specially crafted input an attacker can overwrite a local variable that is located near the vulnerable buffer on the stack, and insert code to change the behavior of the program, often gaining control of the machine executing the code. Buffer overflow attacks can occur when input (particularly the length/size of the input) is not checked properly.

Buffer overflows were understood and partially publicly documented as early as 1972, when the Computer Security Technology Planning Study laid out the technique: "The code performing this function does not check the source and destination addresses properly, permitting portions of the monitor (kernel) to be overlaid by the user. This can be used to inject code into the monitor (kernel) that will permit the user to seize control of the machine." (wikipedia.com)

As a workaround for CVE-2020-0796, SMB Servers could be protected by disabling SMBv3 compression. Microsoft released a patch a few days after the vulnerability was discovered.


### Data leak

In 2020, Broadvoice, a well-known VoIP provider that serves small- and medium-sized businesses, leaked more than 350 million customer records related to the company’s “b-hive” cloud-based communications suite. Broadvoice left an Elasticsearch database cluster containing such information open to the internet, accessible to anyone, with no authentication required. Names, phone numbers, and millions of voicemail transcripts, many involving sensitive information such as details about medical prescriptions and financial records, were left open. (techradar.com)

The major problem here is that Broadvoice left a database open without any authentication required for access. Because lots of personal information flows through Broadvoice’s systems on behalf of doctor’s offices, law firms, retail stores, and other businesses, having a database cluster with client information that doesn’t even require a password to access is absolutely egregious. (paubox.com)

Two-factor authentication is specifically designed to stop leaks like this from occurring and can satisfy the electronic PHI (ePHI) access requirements as per the HIPAA Security Rule. (paubox.com)

Additionally, since Broadvoice stores PHI on behalf of its healthcare customers, it should have executed a business associate agreement (BAA). The purpose of a BAA is that a business associate agrees to protect PHI. Medical providers that partner with services that do not sign a BAA open themselves up to severe liabilities. (paubox.com)

The flaw was reported by researcher Bob Diachenko on Oct. 1, and the databases were secured the same day, according to Broadvoice. The cluster had been uploaded on Sept. 28, meaning it was exposed for about four days. Although Broadvoice acted quickly to patch the security flaw, it is too early to say with any certainty if the leaked data has been accessed. 

“The leaked database represents a wealth of information that could help facilitate targeted phishing attacks,” according to Comparitech. “In the hands of fraudsters, it would offer a ripe opportunity to dupe Broadvoice clients and their customers out of additional information and possibly into handing over money. For example, criminals could pose as Broadvoice or one of its clients to convince customers to provide things like account login credentials or financial information.” (threatpost.com)

Malicious actors could have used the information that had been exposed to facilitate targeted email phishing attacks. During the attack, hackers could have posed as Broadvoice or a client and convinced customers to provide login credentials or financial information. Subsequently, hackers could have either held the data as ransom and threatened to expose it on the black market or they could have used the credit card information to drain the customer’s bank account. The latter is a form of identity theft that can result in thousands of dollars in expenses that the customer must pay in order to correct the issue. (paubox.com)

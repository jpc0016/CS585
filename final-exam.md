# Final Exam Notes

Each section contains notes on questions Dr. Zhu asked in lectures.

Basic Notes
* located in OKT room N324 @ 11:30 am - 2:00 pm
* 6 pages long
* covers decks 9 - 13.2 (6 decks)
* OS (deck 12) starts from slide 22 due to recording issue

### Deck 10 - Identity (OCT 31 & NOV 5)

* If a user account is deleted by an administrator and reinstated (with same name), the user cannot access their old files due to having a new UID.  One UID is granted per user.
* Is using your Charger ID (for buildings, meals, library) considered low or high assurance? - low assurance
* DNS does not have built-in security
* Naming conventions have 3 levels:
  1.  mneumonic/common name
  2.  IP address
  3.  machine name
* web browser can send **ANY** cookie to a web server
* Does anon.penet.fi achieve anonymity?  No.  Use proxy server or anonymizer to strip headers from data. anonymizer is not truly anonymous.  If communication mappings are retrieved, an attacker can figure out who sent what. Transaction records are still kept.
* What kind of encryption and keys used for a message to be  revealed in a anonymizer chain?  Which part should be encrypted: content or headers?  Encrypt message body with recipient's public key.  How to decrypt?

### Deck 11 - Intrusion Detection (NOV 7 & NOV 12)

* What are other examples of bypassing IDS?
* Three methods of Intrusion detection:
    * threshold metrics
    * statistical moments
    * markov model
* Feature Selection.  3 types of algorithms:
  * Backwards Sequential Search: assume full set, delete features until error rate minimized. (fastest)
  * Beam Search: Order possible clusters from best to worst. Search from best.
  * Random Sequential Search: begin with random feature set, add and delete features. (slowest)

* Why would certain algorithms take longer?  How many cases are necessary to figure out best feature set (13:30)?  Best case: 1; worst case: all 7 features.  If all cases need to be tried, it will be (2^7)-1 features.  More features = more time consumed.
* Models of Intrusion Detection: **(These three are on exam)**
  * Anomaly detection (signature based) - What is known is usual, what is unusual is bad.
  * Misuse detection - IDS matches data against rule sets made by developers; can't detect attacks unknown to developers.  What is bad is known, what is not bad is "good"
  * Specification-based detection - What is good is known, what is not good is bad.

* Which method is best for detecting a new attack (29:50)? Anomaly Detection you can detect new attack, spec-based is possible to detect.
* Where is Network-Based Agent (IDS) placed (39:40)? Firewall is good choice. Downside: can only detect external attacks; however, most attacks come from external sources.  Another downside: can slow down firewall if a lot of traffic passes through firewall.  Can use dedicated machines for net-based agents to view all nodes.
* Cannot conduct content monitoring if end-to-end encryption is used.
* Run director on separate system to avoid negatively impacting performance.
* 6 phases of intrusion handling:
  1.  Preparation for attack
  2.  Identification of attack
  3.  Containment of attack
  4.  Eradication of attack
  5.  Recovery from attack
  6.  Follow-up to attack

### Deck 12 - OS Security (NOV 19 0:00 - 30:00)

* Slides start at 22 due to recording error
* Patch management handled with automatic updates
* Can both Windows FAT and NTFS file systems implement Users administration and access controls (4:20)? [FAT does not.](https://www.sciencedirect.com/topics/computer-science/new-technology-file-system)
* Encrypting File System (EFS) - 2 partitions: 1 to encrypt personal data
* Virtualization: What security concerns exist for cloud computing (24:30)?  How to isolate data from someone else (26:10). Depends how secure remote administration is; should be considered in design of IDS and network firewalls. Administration traffic should use separate tightly-controlled network.

### Deck 13.1 - Malicious Software (NOV 19 30:00 - 60:00 & NOV 21 0:00 - 30:00)

* Which virus would be most difficult to detect (48:40 @ Virus Classifications slide)?  Stealth, TSR, and Encrypted viruses.
* Difference between worms and viruses (51:10)?  Which parts are similar?  Both infect.  Virus can infect another file.  Worms are more focused on propagation between media such as operating systems.
* Social engineering victims are more likely to be victims again

### Deck 13.2 - Malicious Logic (NOV 21 30:00 - 63:00 & NOV 26 25:00)

* Trojan horse: program with an overt purpose and covert purpose
* Viruses operate in 2 phases: insertion phase, execution phase.  Only insertion phase is required.
* TSR Viruses = "Terminate and Stay Resident."  Stays in active memory after application finishes
* Encrypted viruses are more difficult to detect using signatures.
* Which part of encrypted virus pseudo-code actually encrypts the malicious code (7:25)?  The XOR line encrypts the code.
* Which level of polymorphic viruses are harder to detect (12:30)?  Instruction or algorithm level?  Algorithm is harder.  Arbitrary instructions are easier to insert than changing the logic (e.g. ADD EAX, 0;)
* Strong typing leads to separating data and instructions.

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
  * Backwards Sequential Search: assume full set, delete features until error rate minimized.
  * Beam Search: Order possible clusters from best to worst. Search from best.
  * Random Sequential Search: begin with random feature set, add and delete features.
Why would certain algorithms take longer?

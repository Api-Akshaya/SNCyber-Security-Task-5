DIGITAL FORENSICS REPORT – SUSPICIOUS FILE INVESTIGATION
1. Introduction

This investigation analyzes a file named suspicious_file.txt, which was flagged as potentially suspicious.
The objective is to perform static forensic analysis to determine whether the file exhibits characteristics commonly associated with malware or data exfiltration.

2. File Creation (Simulation)

A simulated suspicious file was created to safely demonstrate digital forensic procedures.

Content of the file:

Confidential data. Contacting http://malicious-test-server.com/upload.php for exfiltration.


The text mimics typical malicious behavior such as unauthorized data transmission to an external server.

3. Integrity Verification (Hash Calculation)

The SHA-256 hash of the file was computed using:

sha256sum suspicious_file.txt


Output:

27d39d3def70ccf2195a1d63e8753badfe50851ab7de0bce395a444426e81a9  suspicious_file.txt


Purpose:

Ensures the file has not been altered during analysis.

Establishes a baseline for chain-of-custody procedures.

4. Static Analysis
4.1 Viewing the File Content
cat suspicious_file.txt


The file contains references to confidential data and a URL—behavior often associated with exfiltration attempts.

4.2 Extracting Strings
strings suspicious_file.txt


Key finding:

http://malicious-test-server.com/upload.php


This indicates potential communication with an external server, which is a common indicator in malicious scripts or trojans.

5. Analysis Summary

The file contains:

A reference to confidential data

A suspicious URL resembling a data upload endpoint

Language implying transmission or exfiltration

These characteristics match typical indicators used in malware investigations, even though the file in this simulation is harmless.

6. Conclusion

Based on static analysis, the file demonstrates characteristics commonly associated with malicious activity, particularly unauthorized data exfiltration.
Although the file itself is not harmful in this controlled simulation, the analysis procedure mirrors real-world forensic workflows used to assess suspicious artifacts.

This exercise successfully demonstrates:

File integrity verification using SHA-256

Static digital forensic techniques

Identification of suspicious indicators

Formulation of an investigative conclusion

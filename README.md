A Python automation tool to generate RSA keys and Certificate Signing Requests (CSRs) in bulk for Secure Network Analytics (SNA) appliances, legacy network gear, and any technology requiring robust certificate management.

Why this tool?
Manual certificate management is a bottleneck. This solution is engineered for:

Air-gapped Environments: Securely generate credentials without external connectivity.

Legacy & Modern Appliances: Seamlessly handle devices lacking modern APIs, including SNA versions below 7.6, and any platform using standard security certificates.

Scalability: Transition from manual, error-prone OpenSSL commands to a standardized, batch-processed workflow.

Business Value
Significant Time Savings: Reduce deployment windows from hours to seconds by automating hundreds of CSRs in a single execution.

Operational Consistency: Eliminate human error in certificate metadata, ensuring compliance across diverse infrastructure.

Enhanced Security: Standardize key length (4096-bit) and security parameters across the enterprise.

Project Structure
Function_test.py: The main automation script.

CommonName.cnf: OpenSSL configuration template.

CSR_infofile.csv: Input file containing device details.

Getting Started
Ensure OpenSSL is installed and accessible in your system PATH.

Ensure Function_test.py, CommonName.cnf, and CSR_infofile.csv are in the same directory.

Edit CSR_infofile.csv with your device details.

Run the script:

Bash
python3 Function_test.py
Security
Private keys (.key) and CSRs (.csr) are automatically isolated and excluded from version control via .gitignore to prevent sensitive data exposure.

Contributing
Contributions are welcome. Please open an issue or submit a pull request for any improvements or bug fixes.

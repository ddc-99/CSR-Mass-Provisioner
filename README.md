# CSR-Mass-Provisioner

A Python automation tool to generate RSA keys and Certificate Signing Requests (CSRs) in bulk for Secure Network Analytics (SNA) appliances, legacy network gear, and any technology utilizing standard security certificates.

## Why this tool?
Manual certificate management is a massive bottleneck. This tool runs on your local workstation to automate the preparation of CSRs, eliminating hundreds of repetitive clicks and manual data entry tasks. It is engineered for:
* **Air-gapped Environments:** Securely generate credentials locally without requiring external connectivity.
* **Compatibility:** Streamlines certificate preparation for any device lacking modern APIs or automated enrollment protocols—including legacy SNA versions below 7.6—by generating the necessary artifacts for manual import.
* **Scalability:** Transition from error-prone, manual OpenSSL command-line entry to a standardized, batch-processed workflow.

## Business Value
* **Significant Time Savings:** Reduce deployment windows from hours to seconds by automating the generation of hundreds of CSRs in a single execution.
* **Operational Consistency:** Eliminate human error in certificate metadata, ensuring configuration compliance across diverse infrastructure.
* **Enhanced Security:** Standardize key length (4096-bit) and security parameters across the entire enterprise.

## Project Structure
* `Function_test.py`: The main automation script.
* `CommonName.cnf`: OpenSSL configuration template.
* `CSR_infofile.csv`: Input file containing device details.

## Getting Started
1. Ensure OpenSSL is installed and accessible in your system PATH.
2. Ensure `Function_test.py`, `CommonName.cnf`, and `CSR_infofile.csv` are in the same directory.
3. Edit `CSR_infofile.csv` with your device details.
4. Run the script: 
   `python3 Function_test.py`

## Security
Private keys (`.key`) and CSRs (`.csr`) are automatically isolated and excluded from version control via `.gitignore` to prevent sensitive data exposure.

## Contributing
Contributions are welcome. Please open an issue or submit a pull request for any improvements or bug fixes.

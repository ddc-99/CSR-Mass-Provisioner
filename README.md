# CSR Automation Script

This script automates the generation of RSA keys and Certificate Signing Requests (CSRs) for Cisco devices using OpenSSL.

## Project Structure
- `Function_test.py`: The main automation script.
- `CommonName.cnf`: OpenSSL configuration template.
- `CSR_infofile.csv`: Input file containing device details.

## Getting Started
1. Ensure you have OpenSSL installed.
2. Edit `CSR_infofile.csv` with your required metadata.
3. Run the script: `python3 Function_test.py`

## Security
- Private keys (`.key`) and CSRs (`.csr`) are generated in local directories and are excluded from version control via `.gitignore`# CSR Automation Script

This script automates the generation of RSA keys and Certificate Signing Requests (CSRs) for secure network appliances (like Cisco DNA Center/SNA) and legacy infrastructure.

## Why this tool?
In environments with dozens or hundreds of appliances, manual certificate management is a bottleneck. This solution is specifically engineered for:
- **Air-gapped Environments:** Securely generate credentials without external connectivity.
- **Legacy Appliances:** Seamlessly handle devices lacking modern APIs or automated enrollment protocols (like SCEP/EST).
- **Scalability:** Transition from manual, error-prone OpenSSL commands to a standardized, batch-processed workflow.

## Business Value
- **Significant Time Savings:** Reduce deployment windows from hours to seconds by automating the generation of hundreds of CSRs in a single execution.
- **Operational Consistency:** Eliminate "human error" in certificate metadata, ensuring compliance across your entire infrastructure.
- **Enhanced Security:** Standardize key length (4096-bit) and security parameters across the enterprise.

## Project Structure
- `Function_test.py`: The main automation script.
- `CommonName.cnf`: OpenSSL configuration template.
- `CSR_infofile.csv`: Input file containing device details.

## Getting Started
1. Ensure OpenSSL is installed.
2. Edit `CSR_infofile.csv` with your device details.
3. Run the script: `python3 Function_test.py`

## Security
Private keys (`.key`) and CSRs (`.csr`) are automatically isolated and excluded from version control via `.gitignore`.

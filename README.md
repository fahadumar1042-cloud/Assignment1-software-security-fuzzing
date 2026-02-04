# Assignment 1 – Software Security and Fuzzing

## Overview
This repository contains the submission for Assignment 1 of the Software Security and Fuzzing module.
The goal of this project is to demonstrate how automatically generated code can introduce security
vulnerabilities, and how fuzzing can be used to discover and fix them.

The project uses AFL++ to fuzz a JavaScript parsing target and identifies a crash caused by a memory
safety vulnerability. A patch is provided along with a vulnerability analysis and CVE-style report.

---

## Repository Structure

- `fuzz/`
  - Docker environment for building and running AFL++
  - Compiles the vulnerable target and starts fuzzing automatically
  - Contains the fuzzing seed and required build files

- `fixed/`
  - Contains the patched version of the vulnerable code
  - Applies the fix using a standard **`patch(1)`** file
  - Demonstrates that the crash no longer occurs

- `CVE-2025-11132.txt`
  - CVE-style vulnerability description including CVSS metrics and CPE identifier

- `report_team04.pdf`
  - Detailed vulnerability analysis, root cause explanation, and patch justification

---

## How to Run

### Fuzzing
```bash
cd fuzz
./run.sh
```

### Patching
```bash
cd fixed
./run.sh
```






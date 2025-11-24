# Semgrep Custom Rules for OWASP Mutillidae II

This repository contains my custom Semgrep rules and test files created for the SAST Lab (Lab 4).  
The purpose of this work is to detect vulnerable patterns inside the Mutillidae II PHP codebase using static analysis.

 Contents
*semgrep/semgrep-rules.yml*  
  Custom rules that detect:
  - SQL Injection (raw user input in SQL queries)
  - Cross-Site Scripting (unsanitized echo)

 *semgrep/tests*  
  Test files used to verify that the rules work correctly:
  - `sqli-bad.php`
  - `sqli-good.php`
  - `xss-bad.php`
  - `xss-good.php`

 How to Run Semgrep
Run the following command inside the Mutillidae directory:

*bash
semgrep --config semgrep/semgrep-rules.yml .

What the Rules Detect?
Direct usage of $_GET or $_POST inside SQL queries

Echoing user-controlled input without sanitization

 *Report*

A full technical report (PDF) was submitted separately as required.

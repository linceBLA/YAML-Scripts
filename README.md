# YAML-Scripts
# Enhancing Pentesting with Nuclei and Custom YAML Templates

In my work as a pentester, I often have to assess large applications with thousands of URLs. One of the tools I find particularly useful is Nuclei, as it allows me to write custom templates in YAML. This flexibility is key because it enables me to target specific vulnerabilities that I suspect may exist within an application. Below are three example YAML templates I’ve written, though each application typically requires its own set of tailored templates.

## YAML Templates

### 1. `auth-data-leak.yaml`

This template focuses on detecting potential data leaks on authenticated pages. Data leaks are a common issue, especially in low-code or no-code platforms, where users might gain access to data they shouldn't. For example, a regular user might be able to access admin-level information. This template helps by scanning page bodies for any sensitive information that may be exposed.

### 2. `auth-data-leak-with-url.yaml`

This template builds on the first but extends the search to URLs. It's not uncommon for sensitive data to be unintentionally exposed in URLs, which can lead to serious security risks. This template checks the URLs for any potential data leaks, ensuring that sensitive information isn’t present in the URL paths.

### 3. `auth-PII-pages.yaml`

This template is designed to identify pages that handle Personally Identifiable Information (PII). For applications that require sensitive data, such as Social Security Numbers (SSNs), this template scans for any pages that include such information. It provides a list of these sensitive pages so that I can focus on testing them thoroughly.

---

These templates are just examples, and every application requires its own customized approach for effective pentesting. Nuclei’s ability to create tailored templates ensures that I can quickly and efficiently identify potential vulnerabilities, covering as much of the attack surface as possible.


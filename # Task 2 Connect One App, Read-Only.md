# Task 2: Connect One App, Read-Only

## Connected App
* **App Connected:** Gmail
* **Data Retrieved:** Calibration request email regarding the 200kV X-ray generator from EEPCON.

## Permission Assessment (One-Sentence Note)
"I granted the AI read-only access to my Gmail to query, retrieve, and summarize specific incoming calibration service requests. I do not currently need write permissions, as I prefer to manually review and send the drafted response myself to ensure final administrative oversight."

## How Access Was Granted & Filtered
1. **Scope:** Secure OAuth 2.0 read-only permissions allow the AI to view email messages and metadata without granting permission to send, delete, or modify emails.
2. **Targeting:** Instead of reading the entire inbox line-by-line, natural language keywords ("calibration request") were passed to filter the search, retrieving only the relevant message thread.
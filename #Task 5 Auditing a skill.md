# Canva Skill — Safety Assessment

## 1. Installation
Canva is connected as an MCP connector in the account (the modern equivalent of a "Skill" for external services). This exposes Canva's tools so the assistant can create and edit designs directly inside the user's Canva workspace when asked.

## 2. What It Does (Plain English)
The Canva connector allows the assistant to:
- Create new designs (presentations, social posts, docs) inside the connected Canva account
- Search existing Canva designs and folders
- Edit or export designs that already exist
- Pull in templates and assets from Canva's template library

In short, it acts as an extra pair of hands inside the actual Canva workspace, rather than just describing what a design should look like in chat.

## 3. Sensitivity Check

| Question | Answer |
|---|---|
| Contacts an external server? | Yes — calls go to Canva's own API (mcp.canva.com), not an unrelated third party. |
| Handles credentials? | Yes, indirectly. Access is granted via OAuth at connection time. The assistant never sees the account password — only a scoped access token limited to the permissions granted. |
| Sends data anywhere unexpected? | Only data relevant to the specific task (e.g., a design prompt or a file being placed into Canva) is sent to Canva. No silent uploading of unrelated files, browsing history, or other personal data. |
| Scope of access | Depends on what was approved during OAuth — typically read/write access to designs, not unrelated accounts (e.g., email or full Drive) unless those are separately connected. |

## 4. Safety Verdict
**Safe to enable for normal use, with one caveat.**

Reasoning:
- Canva is a mainstream, well-established service.
- The connector only communicates with Canva's official API — no unknown or unverified endpoints.
- Access is scoped through OAuth rather than a raw password, limiting exposure.

Caveats to keep in mind:
- Only connect a Canva account that the user is comfortable having an AI assistant edit directly — avoid connecting a shared or admin/brand account if AI-made edits to it aren't desired.
- Since the connector can create/edit real designs, AI-generated changes should be reviewed before publishing anything external-facing, the same as with any human collaborator's edits.

**Overall risk level:** Standard "granted an app OAuth access" risk — no indicators of credential leakage, hidden data exfiltration, or contact with unknown/untrusted servers.

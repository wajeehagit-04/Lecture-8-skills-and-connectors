# Task 3: Wire Skill + Connector Together

## The Combined Workflow
* **The Plain-English Trigger Sentence:** "i want yoy to connect to my gmail and write a formal reply to calibration request"
* **How It Worked:** A single sentence caused the environment to execute two steps seamlessly without manual copy-pasting:
  1. The **Gmail Connector** activated to query and retrieve live text from the EEPCON calibration email.
  2. The **Precise Formal Letter Writer Skill** immediately caught that raw data and structured it into a strict, professional, 3-paragraph response layout.

## Verification & Spot-Checking
Before trusting the output, I spot-checked the generated letter against the original email source:
* **Verified Metric:** The AI correctly extracted the target hardware asset (**200kV X-ray generator**) and matching client name (**EEPCON**). 
* **Format Check:** The output completely bypassed the usual conversational AI intro fluff and kept the letter to a concise three paragraphs, verifying the skill rules were fully enforced on live data.
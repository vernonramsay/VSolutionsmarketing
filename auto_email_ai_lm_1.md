# V Solutions NYC homeowner education email drafts

**Status:** Editorial drafts only; no campaign is authorized or launched.
**Reviewed:** October 26, 2026.
**Scope:** Three alternative messages and three subject lines for the current homeowner education offering. The follow-up is optional, not an automated schedule.

## Review findings and campaign decision

The May 2 draft reads as business-to-business AI automation outreach: it addresses teams and companies, discusses operations/support/lead handling, and uses `{{CompanyName}}`. That establishes the draft's audience, not the existence of a separate business AI product.

The current public website supports a different audience: New York homeowners exploring mortgage assistance and real estate decisions. Its public app bundle contains a homeowner academy page, loan modification education, a link to https://vsolutionsai.app, and Zoom consulting copy. No business automation offering or AI-LM-1 product definition was found in the inspected repository text or current public app bundle.

**Recommendation:** Use homeowner education positioning for this PR. Keep any future business AI campaign separate, with its own confirmed product specification, audience, evidence, and landing page. Do not equate AI-LM-1 with MyLoanMod AI or the academy without owner confirmation. The original B2B wording remains available in Git history.

### Specific corrections

| Original element | Finding | Correction |
| --- | --- | --- |
| "AI in your business," "your team," and `{{CompanyName}}` | Business audience conflicts with current homeowner goals. | Use individual greetings and education about loan modification. |
| "We recently launched AI-LM-1" | No current launch evidence or verified product definition. | Remove launch wording and external AI-LM-1 branding. |
| "save your team hours each week" and "fastest ROI" | Unsupported performance and financial benefit claims. | Remove; make no quantified savings or ROI promises. |
| Automate tasks, improve response speed, scale communication, "without adding complexity" | These product capabilities are not established by the inspected sources. | Remove; do not substitute unverified AI drafting, document upload, eligibility, or lender-integration claims. |
| https://vsolutionsnyc.com/ai-lm-1 | Returns HTTP 200 with the same Base44 app shell as the homepage. The inspected deployed route table has no /ai-lm-1 route and uses a wildcard fallback. | Replace with https://vsolutionsnyc.com/academy, an explicitly defined homeowner education route. |
| Presumed prior knowledge, "high-volume," and automatic 3–5 day follow-up | Does not establish a suitable homeowner contact list or permission to send. | Use alternative drafts; no schedule or recipient list is configured. |
| Inconsistent signatures and missing commercial-email footer | Sender details and opt-out handling must be complete before use. | Add a consistent sender, postal-address field, ad identification, and opt-out link to every draft. |

### Evidence and limits

- PR reviewed: https://github.com/vernonramsay/VSolutionsmarketing/pull/1
- Original file commit: `2059548a8ca44c07f28038367b160be566a7c188`.
- Current homepage: https://vsolutionsnyc.com/
- Current education route: https://vsolutionsnyc.com/academy
- Public deployed bundle inspected: https://vsolutionsnyc.com/assets/index-CGgkn7Vq.js
- The homepage describes New York homeowner support, links to the academy, and publishes (516) 854-8306 and info@vsolutionsnyc.com.
- The bundle defines / and /academy plus authentication routes and a wildcard fallback; it contains no AI-LM-1 identifier. This is source inspection, not a completed browser, booking, or external academy test.
- Search results still expose older GoDaddy consultation copy. Those indexed pages are not evidence of current Base44 features, pricing, or product availability.
- The repository's main branch contains a contacts workbook; the PR adds this Markdown file. Neither the PR's open state nor this repository inspection establishes whether these emails have been used elsewhere. No email-platform logs, deployments outside this repository, or contact-list suitability were verified.

## Subject line options

1. Explore loan modification education with V Solutions NYC
2. A starting point for understanding mortgage assistance options
3. Learn about the loan modification process

Use one subject line per message. Do not put a recipient's hardship, foreclosure status, loan balance, address, or other sensitive information in the subject.

## Variant 1 — General homeowner education outreach

Hi {{FirstName}},

Understanding mortgage assistance options can feel overwhelming. V Solutions NYC offers loan modification education for homeowners who want to learn more about the process.

You can explore our homeowner education page here:
https://vsolutionsnyc.com/academy

If you would like to discuss whether our educational resources fit your questions, reply to this email. Please do not send financial documents or account details by email.

Our educational information is not legal advice. Your mortgage servicer determines available options and whether a modification is approved; no approval, payment reduction, or foreclosure outcome is guaranteed.

Best,
{{YourName}}
V Solutions Consulting Corporation
{{Phone}}
{{ReplyEmail}}

Advertisement from V Solutions Consulting Corporation.
{{PostalAddress}}
Unsubscribe from marketing emails: {{UnsubscribeURL}}

## Variant 2 — Optional follow-up

Hi {{FirstName}},

Following up on my earlier email about V Solutions NYC's homeowner education resources.

If you are interested in learning about the loan modification process, you can start here:
https://vsolutionsnyc.com/academy

Would you like to discuss the educational resources? You can reply with a general question; please leave out account numbers and financial documents.

This is educational information, not legal advice. Your mortgage servicer determines available options and approval. No approval, payment reduction, or foreclosure outcome is guaranteed.

Best,
{{YourName}}
V Solutions Consulting Corporation
{{Phone}}
{{ReplyEmail}}

Advertisement from V Solutions Consulting Corporation.
{{PostalAddress}}
Unsubscribe from marketing emails: {{UnsubscribeURL}}

## Variant 3 — Short homeowner education outreach

Hi {{FirstName}},

Want to learn about the loan modification process? Explore V Solutions NYC's homeowner education resources:
https://vsolutionsnyc.com/academy

Reply if you would like to discuss the resources. Please do not email financial documents or account details.

Educational information only, not legal advice. Your mortgage servicer determines available options and approval. No approval, payment reduction, or foreclosure outcome is guaranteed.

Best,
{{YourName}}
V Solutions Consulting Corporation
{{Phone}}
{{ReplyEmail}}

Advertisement from V Solutions Consulting Corporation.
{{PostalAddress}}
Unsubscribe from marketing emails: {{UnsubscribeURL}}

## Personalization and use notes

| Field | Rule |
| --- | --- |
| `{{FirstName}}` | Use an accurate first name. If absent, replace the entire greeting with "Hello,"; never leave a blank or unresolved field. |
| `{{YourName}}` | Actual authorized sender, such as Vernon Ramsay when he is the sender. |
| `{{Phone}}` | Verified business number; the current homepage publishes (516) 854-8306. |
| `{{ReplyEmail}}` | Verified, monitored business reply address; the homepage publishes info@vsolutionsnyc.com, but delivery and monitoring were not tested. |
| `{{PostalAddress}}` | Actual valid business postal address; a city name alone is insufficient. No address is invented here. |
| `{{UnsubscribeURL}}` | Working recipient-specific opt-out URL from the eventual sending platform. Do not include sensitive loan or hardship information in its URL. |

Remove `{{CompanyName}}` and `{{Title}}` from homeowner mappings. Do not infer that an individual is delinquent or in foreclosure, invent a prior interaction, or treat the existing workbook as an approved homeowner mailing list.

Before any separately authorized use:
- Render every field, check sender identity and reply handling, and test the academy link in a browser, including its external destination. The /academy route currently links out to https://vsolutionsai.app; access, functionality, pricing, and AI features there were not verified.
- Keep the destination consistent with these educational claims. Do not add promises about AI capabilities, free service, fees, savings, eligibility, lender negotiation, government affiliation, or foreclosure prevention without evidence and appropriate review.
- Use variant 2 only if a first message was actually sent and the recipient has not replied or opted out. Do not enable a recurring sequence from this file.
- Confirm audience suitability, suppression handling, valid postal address, accurate headers/subjects, and functional unsubscribe handling. FTC CAN-SPAM guidance: https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business
- Obtain review of the actual offering and applicable New York and federal mortgage-assistance advertising requirements before use. Calling an offer "education" or "software" does not by itself settle regulatory coverage; these drafts are not a legal compliance certification. FTC MARS guidance: https://www.ftc.gov/business-guidance/resources/mortgage-assistance-relief-services-rule-compliance-guide-business

This edit changes proposed copy only. It does not merge the PR, alter the website or contacts workbook, connect a sending service, schedule follow-ups, or send email.

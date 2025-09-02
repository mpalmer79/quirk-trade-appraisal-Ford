Quirk Ford Trade Tool - Deployment Notes
========================================

This is a direct clone of the Chevrolet/Braintree trade tool with the following updates:
- Title and smallprint updated to "Quirk Ford"
- Success page title/message/button updated and links point to https://www.quirkford.com
- Any in-app references to "Quirk Chevrolet" swapped to "Quirk Ford"
- No changes to Netlify functions behavior. Make sure to set these environment variables in the Netlify site settings:

  SENDGRID_API_KEY = (your key)
  FROM_EMAIL       = (verified sender, e.g. web@quirkcars.com)
  TO_EMAIL         = comma-separated recipients for Quirk Ford (sales desk)
  SHEETS_WEBHOOK_URL (optional backup)

Netlify Build & Functions:
- netlify.toml routes /api/trade-appraisal to the function at netlify/functions/trade-appraisal.js
- Success redirect stays at /success/index.html

Spanish:
- Success page loads Spanish automatically when the user submitted the form in Spanish (app.js handles language persistence).

Suggested recipients for Ford (edit in Netlify env TO_EMAIL):
- mpalmer@quirkcars.com
- steve@quirkcars.com
- gmcintosh@quirkcars.com
- (add the Quirk Ford desk / BDC emails)
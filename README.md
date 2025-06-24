# Analyze-a-Phishing-Email-Sample
## Analyzing Phishing Emails: Step-by-Step Guide

This section outlines how to identify and analyze phishing emails, using the provided "Urgent Account Recovery!!!" email as an example. Follow these steps to detect malicious traits and secure your network.

### Practice Steps to Analyze Phishing Emails

1. **Find Phishing Email Templates**:
   - Use online templates to simulate phishing emails:
     - [PhishingTemplates](https://github.com/criggs626/PhishingTemplates) (GoPhish-compatible templates).
     - [LinkSec Phishing Templates](https://github.com/LinkSec/phishing-templates) (50+ ethical training templates).
     - [CanIPhish Templates](https://caniphish.com) (90+ themed templates).
   - **Note**: Search GitHub for "phishing templates" if links are broken, and verify repository activity before use.
   - These provide sample structures for testing.

2. **Create and Send a Test Email**:
   - Craft an email with a malicious link (e.g., `http://fake-site.com/reset?code=123`).
   - Send it to a controlled target (e.g., a test account) with permission.

3. **Open and Analyze Email Headers**:
   - Access the email’s full header in your email client (e.g., Gmail: Click the three dots > "Show original").
   - Copy the header text or upload the `.eml` file.
   - Use [Trustifi Email Analyzer](https://trustifi.com/email-analyzer/) to analyze:
     - Paste the header into the text box or upload the `.eml` file.
     - Click "Analyze" to get a breakdown of sender details, routing, and security settings.

### Steps to Understand Phishing Traits

4. **Check for Urgency**:
   - Look for phrases like "Urgent Account Recovery!!!" or "Click Here Immediately."
   - **Finding**: The email uses excessive exclamation marks and urgent language, a common phishing tactic to prompt quick action.

5. **Inspect the Sender Address**:
   - Verify if the domain matches the claimed sender (e.g., LinkedIn should use `@linkedin.com`).
   - **Finding**: "noreply@anonymousemail.eu" is suspicious as it’s not a LinkedIn domain, indicating potential spoofing.

6. **Identify Malicious Links**:
   - Hover over links (don’t click) to check the URL (e.g., right-click > "Copy link address").
   - **Finding**: The link "Click Here Immediately" likely leads to a fake site; analyze via Trustifi to confirm it’s not `linkedin.com`.

7. **Look for Grammar and Spelling Mistakes**:
   - Check for errors like "recived" instead of "received" or awkward phrasing.
   - **Finding**: The email has no obvious typos, but the phrase "we have recived a request" (if intended) would be a red flag.

8. **Detect Mismatched URLs or Domains**:
   - Ensure the link domain matches the sender’s claimed identity.
   - **Finding**: The email claims to be from LinkedIn but uses an unrelated domain, a clear mismatch.

9. **Analyze Header Details with Trustifi**:
   - Check authentication results (SPF, DKIM, DMARC) for failures.
   - Look for unusual routing or IP addresses.
   - **Finding**: Trustifi may show failed authentication or an IP not associated with LinkedIn, confirming phishing.

10. **Identify Additional Phishing Traits**:
    - Watch for fake greetings (e.g., "Hi jalp001" without personalization) or outdated dates (e.g., "24 June 2020 04:15pm GMT").
    - **Finding**: The generic "Hi jalp001" and old date suggest a template email, not a legitimate recovery notice.

### Mitigation and Best Practices

- **Avoid Clicking Links**: Report suspicious emails to your email provider (e.g., Gmail’s "Report Phishing" option) and avoid interacting with unknown links.
- **Educate Users**: Train others to recognize urgency, mismatched domains, and generic greetings as phishing red flags.
- **Secure Headers**: Regularly use tools like [Trustifi Email Analyzer](https://trustifi.com/email-analyzer/) to monitor email authentication (SPF, DKIM, DMARC) and routing.
- **Verify Sender**: Cross-check sender domains against official sources (e.g., `linkedin.com` for LinkedIn emails) before responding.
- **Update Systems**: Keep email clients and security software updated to block known phishing patterns.
- **Backup Data**: Maintain offline backups to recover from potential phishing-related data loss.

> **Warning**: Always analyze with permission to avoid legal issues. This guide is for educational purposes only.


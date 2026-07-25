[Linkedin Email Finder](https://apify.com/vulnv/linkedin-email-finder?fpr=data)

# 📧 LinkedIn Email Finder ⚡ Find Emails for LinkedIn Profiles

## Overview

The **LinkedIn Email Finder** is an Apify Actor that finds email addresses for LinkedIn profiles. Simply provide LinkedIn profile URLs and get email addresses if they are available. Perfect for lead generation, sales outreach, and contact enrichment.

✅ Fast email lookup | ✅ Bulk processing | ✅ Clean JSON output | ✅ High success rate

---

### **Features**

- **Email Discovery** — Find email addresses for LinkedIn profiles
- **Bulk Processing** — Process multiple LinkedIn URLs in parallel
- **Contact Information** — Get additional contact details when available (name, company, domain)
- **Clean Results** — Structured JSON output with clear success/failure indicators
- **Rate Limited** — Concurrent processing with proper rate limiting
- **Error Handling** — Robust error handling with detailed error messages

---

## 🧾 Input Configuration

Submit an array of LinkedIn profile URLs:

```
{
  "urls": [
    "https://www.linkedin.com/in/williamhgates/",
    "https://www.linkedin.com/in/mark-cuban-06a0755b/"
  ]
}
```

---

## 📤 Output Format

Each LinkedIn URL will return a result with either an email address or an error:

### Successful Email Found:

```
{
  "linkedin_url": "https://www.linkedin.com/in/williamhgates/",
  "found": true,
  "email": "bill@microsoft.com",
  "name": "Bill Gates",
  "domain": "microsoft.com",
  "company": "Bill & Melinda Gates Foundation"
}
```

### No Email Found:

```
{
  "linkedin_url": "https://www.linkedin.com/in/example-profile/",
  "found": false,
  "error": "No email found in response"
}
```

---

## 📊 Output & Export

### **Dataset Storage**

- All results are stored in your Apify dataset
- Each LinkedIn URL becomes one dataset item
- Success and failure cases are clearly marked with the `found` field

### **Export Formats**

- **JSON** — Raw structured data for API integration
- **CSV** — Spreadsheet-compatible format
- **Excel** — Formatted spreadsheet

---

## 💼 Common Use Cases

### **Lead Generation & Sales**

- Find email addresses for LinkedIn prospects
- Enrich existing lead databases with contact information
- Build comprehensive contact lists for outreach campaigns

### **Recruitment & Talent Sourcing**

- Get contact information for potential candidates
- Build talent pipelines with direct contact details
- Reach out to passive candidates directly

### **Marketing & Outreach**

- Contact industry professionals and influencers
- Build email lists for targeted marketing campaigns
- Connect with potential partners and collaborators

### **CRM Data Enrichment**

- Automatically find email addresses for LinkedIn contacts
- Update contact records with verified email addresses
- Maintain current contact information in your CRM

---

## ✅ Example Usage

### Input:

```
{
  "urls": [
    "https://www.linkedin.com/in/sample-profile/"
  ]
}
```

### Output:

The dataset will contain the email address (if found) along with additional contact information, or a clear error message if no email was found.

---

## ⚠️ Important Notes

- Email availability depends on data sources and coverage
- Some profiles may not have discoverable email addresses
- The actor respects rate limits to ensure reliable operation
- Only valid LinkedIn profile URLs are processed

---

## 🚀 Getting Started

1. **Add LinkedIn URLs** to the input array
2. **Run the Actor**
3. **Download Results** from the dataset in your preferred format
4. **Use the Email Addresses** for your outreach campaigns

The actor will process all URLs concurrently and provide clear results for each profile, making it easy to identify which profiles have discoverable email addresses.
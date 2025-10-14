# EmailJS Setup Instructions for CC Hendrix Contact Form

This guide will help you set up EmailJS to send emails from your contact form to **chendrix@cchendrix.com**.

## What is EmailJS?

EmailJS is a free service that allows you to send emails directly from JavaScript without needing a backend server. It's perfect for static websites like yours.

---

## Step 1: Create an EmailJS Account

1. Go to [EmailJS.com](https://www.emailjs.com/)
2. Click **"Sign Up"** (top right corner)
3. Create a free account using your email
4. Verify your email address

---

## Step 2: Add an Email Service

1. After logging in, go to the **"Email Services"** page
2. Click **"Add New Service"**
3. Choose your email provider:
   - **Gmail** (recommended for most users)
   - **Outlook/Office 365**
   - **Yahoo**
   - Or any other SMTP service
4. Follow the instructions to connect your email account
5. **Important**: Use the email account that will SEND the emails (this can be a business Gmail account)
6. Click **"Create Service"**
7. **Copy the Service ID** - you'll need this later (looks like: `service_abc123`)

---

## Step 3: Create an Email Template

1. Go to the **"Email Templates"** page
2. Click **"Create New Template"**
3. Set up your template:

### Template Name
```
CC Hendrix Contact Form
```

### Subject
```
New Contact Form Submission from {{from_name}}
```

### Content (HTML)
```html
<p><strong>New contact form submission from CC Hendrix website:</strong></p>

<p><strong>Name:</strong> {{from_name}}</p>
<p><strong>Email:</strong> {{from_email}}</p>
<p><strong>Phone:</strong> {{phone}}</p>
<p><strong>Service Type:</strong> {{service}}</p>

<p><strong>Message:</strong></p>
<p>{{message}}</p>

<hr>
<p><em>This email was sent from the CC Hendrix website contact form.</em></p>
```

### To Email
```
chendrix@cchendrix.com
```

4. Click **"Save"**
5. **Copy the Template ID** - you'll need this (looks like: `template_xyz789`)

---

## Step 4: Get Your Public Key

1. Go to **"Account"** in the navigation menu
2. Find the **"Public Key"** section
3. **Copy your Public Key** (looks like: `A1b2C3d4E5f6G7h8I`)

---

## Step 5: Update Your Website Code

Now you need to add the IDs you copied to your website:

### Open `script.js` and replace the placeholder values:

**Line 5** - Replace `YOUR_PUBLIC_KEY`:
```javascript
emailjs.init('A1b2C3d4E5f6G7h8I'); // Your actual public key here
```

**Lines 114-115** - Replace `YOUR_SERVICE_ID` and `YOUR_TEMPLATE_ID`:
```javascript
emailjs.sendForm(
    'service_abc123',     // Your actual service ID here
    'template_xyz789',    // Your actual template ID here
    contactForm
)
```

### Example of completed code:
```javascript
// At the top of script.js
(function() {
    emailjs.init('A1b2C3d4E5f6G7h8I'); // Your public key
})();

// In the form submission section
emailjs.sendForm(
    'service_abc123',     // Your service ID
    'template_xyz789',    // Your template ID
    contactForm
)
```

---

## Step 6: Test Your Form

1. Open your website in a browser
2. Scroll to the contact form
3. Fill out all required fields
4. Click "Send Message"
5. You should see a success message
6. Check the inbox of **chendrix@cchendrix.com** for the email

---

## Troubleshooting

### Email not received?

1. **Check spam folder** - EmailJS emails sometimes go to spam initially
2. **Verify the "To Email"** in your template is correct: `chendrix@cchendrix.com`
3. **Check the browser console** for errors (press F12, go to Console tab)
4. **Verify all IDs are correct** - make sure you copied the Service ID, Template ID, and Public Key correctly

### Getting "Failed" message?

1. **Check your Public Key** is correctly initialized
2. **Verify Service ID and Template ID** match your EmailJS dashboard
3. **Check your internet connection**
4. **Ensure your EmailJS service is connected** to an email account

### Form fields not appearing in email?

Make sure the `name` attributes in your HTML form match the template variables:
- `from_name` → {{from_name}}
- `from_email` → {{from_email}}
- `phone` → {{phone}}
- `service` → {{service}}
- `message` → {{message}}

---

## EmailJS Free Plan Limits

- **200 emails per month** (free tier)
- If you need more, upgrade to a paid plan
- Monitor usage in your EmailJS dashboard

---

## Auto-Reply to Customers (Optional)

To send an automatic confirmation email to customers:

1. Create a **second template** in EmailJS
2. Subject: `Thank you for contacting CC Hendrix`
3. To Email: `{{from_email}}` (this sends to the customer)
4. Content:
```html
<p>Hello {{from_name}},</p>

<p>Thank you for contacting CC Hendrix! We have received your message and will get back to you within 24 hours.</p>

<p>In the meantime, if you have any urgent questions, please call us at (866) 287-8475.</p>

<p>Best regards,<br>
CC Hendrix Team</p>
```

5. Add a second `emailjs.send()` call in your JavaScript after the first one succeeds

---

## Security Notes

✅ **Safe to expose**: Public Key, Service ID, Template ID (these are meant to be public)  
❌ **Never expose**: Your EmailJS account password  
✅ **Protected**: EmailJS automatically prevents spam and limits abuse

---

## Support

- **EmailJS Documentation**: https://www.emailjs.com/docs/
- **EmailJS Support**: support@emailjs.com
- **Rate Limits**: Check your dashboard for current usage

---

## Quick Checklist

- [ ] Created EmailJS account
- [ ] Added email service and got Service ID
- [ ] Created email template and got Template ID
- [ ] Got Public Key from account settings
- [ ] Updated script.js with all three IDs
- [ ] Set "To Email" in template to: chendrix@cchendrix.com
- [ ] Tested the form
- [ ] Received test email successfully
- [ ] Added sender email to contacts (prevents spam filtering)

---

**Once you complete these steps, your contact form will automatically send emails to chendrix@cchendrix.com!**

For questions or issues, refer to the EmailJS documentation or contact their support team.

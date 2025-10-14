# Quick Start Guide - EmailJS Setup

## 🎯 Your Mission

Make the contact form send emails to **chendrix@cchendrix.com**

**Time Required**: 5-10 minutes  
**Cost**: FREE (up to 200 emails/month)

---

## 📋 The 3 IDs You Need

You need to get 3 pieces of information from EmailJS and add them to your code:

1. **Public Key** - Your account identifier
2. **Service ID** - Which email service to use
3. **Template ID** - The email format/template

---

## 🚀 Step-by-Step (Simple Version)

### STEP 1: Sign Up (2 minutes)
1. Go to: https://www.emailjs.com/
2. Click "Sign Up" (top right)
3. Use your email to create free account
4. Verify your email

### STEP 2: Connect Email (2 minutes)
1. In EmailJS dashboard, click "Email Services"
2. Click "Add New Service"
3. Choose "Gmail" (or your email provider)
4. Follow prompts to connect your email
5. **COPY the Service ID** (looks like: service_abc123)
   - Save it in a notepad!

### STEP 3: Create Template (3 minutes)
1. Click "Email Templates"
2. Click "Create New Template"
3. Fill in these fields:

**Template Name**: `Contact Form`

**To Email**: `chendrix@cchendrix.com`

**Subject**: `New Contact from {{from_name}}`

**Message Content** (copy/paste this):
```
Name: {{from_name}}
Email: {{from_email}}
Phone: {{phone}}
Service: {{service}}

Message:
{{message}}
```

4. Click "Save"
5. **COPY the Template ID** (looks like: template_xyz789)
   - Save it in a notepad!

### STEP 4: Get Public Key (1 minute)
1. Click "Account" in menu
2. Find "Public Key" section
3. **COPY your Public Key** (looks like: A1b2C3d4E5f6G7h8I)
   - Save it in a notepad!

### STEP 5: Update Your Code (2 minutes)

Open `script.js` in your code editor and find these lines:

**Line 5** - Replace this:
```javascript
emailjs.init('YOUR_PUBLIC_KEY');
```
**With** (using YOUR public key):
```javascript
emailjs.init('A1b2C3d4E5f6G7h8I');
```

**Lines 114-115** - Replace this:
```javascript
emailjs.sendForm(
    'YOUR_SERVICE_ID',
    'YOUR_TEMPLATE_ID',
    contactForm
)
```
**With** (using YOUR IDs):
```javascript
emailjs.sendForm(
    'service_abc123',
    'template_xyz789',
    contactForm
)
```

Save the file!

### STEP 6: Test It! (1 minute)
1. Open your website
2. Scroll to contact form
3. Fill it out
4. Click "Send Message"
5. Should see green success message
6. Check email: chendrix@cchendrix.com

---

## ✅ Done!

Your contact form now sends emails automatically!

---

## 🆘 Having Issues?

### "Failed to send" error?
- Double-check you copied all 3 IDs correctly
- Make sure you saved script.js after editing
- Refresh your browser (Ctrl + F5)

### No email received?
- Check spam folder
- Verify "To Email" in template is: chendrix@cchendrix.com
- Make sure email service is connected in EmailJS

### Still stuck?
- Read the detailed guide: `EMAILJS_SETUP.md`
- Check EmailJS docs: https://www.emailjs.com/docs/

---

## 📊 What You Get (Free Plan)

✅ 200 emails per month  
✅ No credit card required  
✅ Works on any hosting  
✅ Spam protection included  
✅ No backend server needed  

---

## 🎓 Pro Tips

1. **Add sender to contacts** - Prevents emails going to spam
2. **Monitor usage** - Check EmailJS dashboard monthly
3. **Test regularly** - Make sure form still works
4. **Keep IDs safe** - Save them in a secure note

---

**That's it! Follow these steps and your form will be sending emails in 10 minutes!**

For the detailed version with troubleshooting, see `EMAILJS_SETUP.md`

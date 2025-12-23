# Waitlist Setup Guide - Email Automation & Spreadsheet

## 🎯 Overview

Your waitlist form is configured and ready to go! This guide will show you how to:
1. Send automatic confirmation emails to customers
2. Collect all submissions in a Google Sheets spreadsheet
3. Get notified when someone joins the waitlist

**Total setup time:** 15-20 minutes

---

## ✅ What's Already Done

- ✅ Waitlist form created with all required fields
- ✅ Netlify Forms configured (will work automatically when deployed)
- ✅ Thank-you page created
- ✅ Form fields include: name, email, phone, address, yard size, HOA, interested product
- ✅ Timestamp automatically captured by Netlify

---

## 📧 Part 1: Set Up Automatic Confirmation Emails (Zapier)

### Why Zapier?
- **Free tier** includes 100 tasks/month (perfect for starting)
- Easy to set up (no coding)
- Sends professional emails from contact@myrobotmowers.com
- Automatically creates Google Sheets spreadsheet

### Step-by-Step Setup:

#### 1. Create Zapier Account
1. Go to https://zapier.com
2. Sign up for free account
3. Click "Create Zap"

#### 2. Set Up Trigger (Netlify Form Submission)
1. Search for "Netlify"
2. Choose **"New Form Submission"** as trigger
3. Click "Continue"
4. Connect your Netlify account:
   - Go to https://app.netlify.com/user/applications
   - Create new personal access token
   - Copy token and paste into Zapier
5. Choose your site: **myrobotmowers.com**
6. Choose form: **spring-waitlist**
7. Test trigger (you may need to submit a test form first)
8. Click "Continue"

#### 3. Add Action: Send Email to Customer
1. Click "+ Add Step"
2. Search for "Email by Zapier" (built-in, no account needed)
3. Choose **"Send Outbound Email"**
4. Fill in the fields:

**To:** (Click "+" and select "Email" from Netlify form data)

**From:** contact@myrobotmowers.com

**From Name:** My Robot Mowers

**Reply To:** contact@myrobotmowers.com

**Subject:** You're on the Spring Install Waitlist 🌱

**Body:** (Copy and paste this - Zapier will auto-fill the {{name}} field)
```
Hi {{Name}},

Thanks for reserving your spot with My Robot Mowers!

You're officially on our Spring 2025 Installation Waitlist. We'll review your property details and contact you within 2-3 business days to confirm qualification and scheduling.

YOUR SUBMISSION DETAILS:
• Name: {{Name}}
• Address: {{Address}}
• Yard Size: {{Yard Size}}
• HOA: {{HOA}}
• Interested In: {{Interested In}}

EARLY WAITLIST MEMBER BENEFITS:
✓ Priority scheduling - First to get installed when spring arrives
✓ Locked-in launch pricing - Special early adopter rates guaranteed
✓ VIP support package - Extended warranty & priority service calls

WHAT'S NEXT:
1. We'll review your property within 2-3 business days
2. Our team will reach out to discuss your specific needs
3. You'll be among the first scheduled for spring installation

Have questions? Just reply to this email or call us at (208) 589-7797.

Looking forward to transforming your yard care!

–The My Robot Mowers Team
Orem & Provo's Autonomous Lawn Care Experts
(208) 589-7797 | myrobotmowers.com
```

5. Test the email
6. Click "Continue"

#### 4. Add Action: Google Sheets (Your Waitlist Spreadsheet)
1. Click "+ Add Step"
2. Search for "Google Sheets"
3. Choose **"Create Spreadsheet Row"**
4. Connect your Google account
5. **Drive:** My Drive
6. **Spreadsheet:** Click "Create a new spreadsheet in Google Sheets"
   - Name it: **Spring 2025 Waitlist - My Robot Mowers**
7. **Worksheet:** Sheet1
8. Map the fields (Zapier will auto-create columns):
   - **Name** → {{Name}}
   - **Email** → {{Email}}
   - **Phone** → {{Phone}}
   - **Address** → {{Address}}
   - **Yard Size** → {{Yard Size}}
   - **HOA** → {{HOA}}
   - **Interested In** → {{Interested In}}
   - **Submission Date** → {{Created At}} (Netlify timestamp)
   - **Form Name** → {{Form Name}}
9. Test the Google Sheet step
10. Click "Continue"

#### 5. Add Action: Email Notification to YOU
1. Click "+ Add Step"
2. Search for "Email by Zapier"
3. Choose **"Send Outbound Email"**
4. Fill in:
   - **To:** contact@myrobotmowers.com (or your personal email)
   - **From:** notifications@zapier.com
   - **Subject:** 🚨 New Waitlist Signup - {{Name}}
   - **Body:**
```
NEW SPRING WAITLIST SIGNUP!

Customer Details:
• Name: {{Name}}
• Email: {{Email}}
• Phone: {{Phone}}
• Address: {{Address}}
• Yard Size: {{Yard Size}}
• HOA: {{HOA}}
• Interested In: {{Interested In}}

Submitted: {{Created At}}

View full details in Google Sheets:
https://docs.google.com/spreadsheets/d/YOUR_SHEET_ID

Action Required:
- Review property details
- Reach out within 2-3 business days
- Confirm qualification and scheduling
```

5. Test the notification
6. Click "Continue"

#### 6. Activate Your Zap
1. Name your Zap: "Waitlist - Email + Spreadsheet"
2. Turn it ON
3. Done! 🎉

---

## 📊 Part 2: Your Google Sheets Waitlist Tracker

### What Gets Captured Automatically:
- ✅ Full Name
- ✅ Email Address
- ✅ Phone Number
- ✅ Home Address
- ✅ Yard Size
- ✅ HOA Status
- ✅ Product Interest
- ✅ Submission Date & Time
- ✅ Form Name

### Customize Your Spreadsheet:
You can add additional columns to track:
- **Status** (New / Contacted / Qualified / Scheduled / Installed)
- **Notes**
- **Follow-up Date**
- **Installation Date**
- **Property Size (calculated from address lookup)**

### Pro Tips:
1. **Conditional Formatting:** Color-code rows by status
2. **Filters:** Create views for different statuses
3. **Charts:** Track signups over time
4. **Share Access:** Give team members view/edit access

---

## 🔔 Part 3: SMS Notifications (Optional Upgrade)

Want instant text alerts when someone signs up?

### Option 1: Zapier SMS (Paid)
Add another action in your Zap:
- Use "SMS by Zapier" ($20/month for 100 messages)

### Option 2: Twilio (Cheaper for High Volume)
- Sign up at https://www.twilio.com
- Add Twilio action to your Zap
- Pay per message (~$0.0075 per SMS)

---

## 🚀 Deployment Steps

### 1. Add Waitlist to Your Pages

**Where to add the waitlist section:**
- ✅ **Homepage** (index.html) - Before the final CTA
- ✅ **Lawn Mowers page** (lawn-mowers.html) - After product details
- ✅ **Snow Blower page** (snow-blower.html) - After product details

**How to add it:**
1. Open the HTML file where you want the waitlist
2. Copy the entire contents of `waitlist-section.html`
3. Paste it where you want it to appear (usually before the final CTA section)

**Example placement in index.html:**
```html
<!-- ... existing homepage content ... -->

<!-- PRODUCTS SECTION -->
<section class="products">
    <!-- ... products ... -->
</section>

<!-- ADD WAITLIST HERE -->
<!-- Copy and paste waitlist-section.html content here -->

<!-- FINAL CTA -->
<section class="final-cta">
    <!-- ... existing CTA ... -->
</section>
```

### 2. Upload Files to Netlify
1. Add `waitlist-thank-you.html` to your root directory
2. Upload the updated HTML files with the waitlist section
3. Deploy to Netlify

### 3. Test Everything
1. Go to your live site
2. Fill out the waitlist form with test data
3. Submit
4. **Verify:**
   - ✅ Redirected to waitlist-thank-you.html
   - ✅ Received confirmation email
   - ✅ New row appeared in Google Sheets
   - ✅ You received notification email
   - ✅ Form visible in Netlify dashboard

---

## 🎨 Customization Options

### Change the Urgency Message
In `waitlist-section.html`, find:
```html
<div class="urgency-badge">
    Limited Spring Slots Available
</div>
```
Change to:
- "Only 25 Spots Left"
- "Early Bird Special Ends Soon"
- "Spring 2025 - Limited Availability"

### Change the Social Proof
Find:
```html
<p><strong>15 families</strong> have already reserved their spot this week</p>
```
Update the number as real signups come in!

### Add More Benefits
Add to the `waitlist-benefits` section:
```html
<div class="benefit-item">
    <svg><!-- checkmark icon --></svg>
    <div>
        <strong>Your Benefit Title</strong>
        <span>Your benefit description</span>
    </div>
</div>
```

---

## ❓ Troubleshooting

### Email not sending?
1. Check Zapier dashboard for errors
2. Verify email addresses are correct
3. Check spam folder
4. Make sure Zap is turned ON

### Not appearing in Google Sheets?
1. Check if Google Sheets action succeeded in Zapier
2. Verify correct spreadsheet is selected
3. Make sure all fields are mapped correctly

### Form not submitting?
1. Verify deployed to Netlify (forms don't work locally)
2. Check Netlify Forms dashboard for submissions
3. Look for JavaScript errors in browser console

---

## 📈 Next Steps & Best Practices

### Week 1:
- Test the complete flow
- Share waitlist link on social media
- Add waitlist CTA to email signature

### Ongoing:
- Review new signups daily
- Respond to qualified leads within 24-48 hours
- Update social proof numbers weekly
- Export spreadsheet monthly for backup

### Marketing Ideas:
- Share "X families joined this week" on social media
- Offer referral bonuses for waitlist members
- Create urgency: "Only 25 spring install slots"
- Send monthly updates to waitlist members

---

## 💰 Cost Breakdown

**Free Tier (100 signups/month):**
- ✅ Netlify Forms: FREE
- ✅ Zapier: FREE
- ✅ Google Sheets: FREE
- ✅ Email by Zapier: FREE

**If you exceed 100/month:**
- Zapier Starter: $19.99/month (750 tasks)
- Netlify Forms Level 1: $19/month (1,000 submissions)

**You're all set with the free tier to start!**

---

## ✅ Final Checklist

Before going live:
- [ ] Zapier Zap created and turned ON
- [ ] Test email sent and received
- [ ] Google Sheet created and receiving data
- [ ] Notification emails working
- [ ] `waitlist-thank-you.html` uploaded to Netlify
- [ ] Waitlist section added to homepage
- [ ] Tested form submission on live site
- [ ] Updated social proof numbers
- [ ] Added waitlist link to other marketing materials

---

## 🎉 You're Ready!

Your waitlist system is professional, automated, and ready to capture early adopters. The confirmation emails will build trust, and your Google Sheet will keep everything organized.

**Questions?** The Zapier and Netlify documentation are excellent resources, or feel free to ask!

Good luck with your spring launch! 🚀

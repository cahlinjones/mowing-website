# Waitlist Setup Guide - SIMPLE VERSION (Gmail Only)

## 🎯 Quick Overview

This simplified guide uses **Gmail** to send confirmation emails. It's 100% free and takes about 15 minutes to set up.

**What you'll get:**
✅ Automatic confirmation emails sent from your Gmail
✅ All submissions saved to Google Sheets spreadsheet
✅ Email notifications when someone signs up
✅ Everything 100% FREE

---

## 📧 Setup Instructions (15 Minutes)

### Step 1: Create Zapier Account (2 minutes)
1. Go to https://zapier.com
2. Sign up for **FREE account** (no credit card needed)
3. Click **"Create Zap"** button

---

### Step 2: Set Up Trigger - Netlify Form (5 minutes)

1. **Search for:** "Netlify"
2. **Choose:** "New Form Submission"
3. **Click:** "Continue"

4. **Connect Netlify Account:**
   - Go to https://app.netlify.com/user/applications
   - Click **"New access token"**
   - Name it: "Zapier"
   - Copy the token
   - Paste into Zapier
   - Click "Yes, Continue to Netlify"

5. **Choose Site:** Select **myrobotmowers.com** from dropdown

6. **Choose Form:** Select **spring-waitlist**

7. **Test Trigger:**
   - Click "Test trigger"
   - If no submissions yet, go submit a test on your live site first
   - Click "Continue"

---

### Step 3: Send Confirmation Email (Gmail) (5 minutes)

1. **Click:** "+ Add Step" or "Action"
2. **Search for:** "Gmail"
3. **Choose:** "Send Email"
4. **Click:** "Sign in to Gmail"
   - Allow Zapier to access your Gmail
   - Use whichever Gmail you want (personal or business Gmail)

5. **Fill in Email Fields:**

**To:** 
- Click the **"+"** button
- Select **"Email"** from the Netlify data dropdown

**From:**
- This auto-fills with your Gmail address (that's perfect!)

**Subject:**
```
You're on the Spring Install Waitlist 🌱
```

**Body Type:** Plain Text

**Body:** (Copy and paste this exactly - Zapier will auto-fill the {{fields}})
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

6. **Click:** "Test action" to send a test email
7. **Click:** "Continue"

---

### Step 4: Save to Google Sheets (3 minutes)

1. **Click:** "+ Add Step"
2. **Search for:** "Google Sheets"
3. **Choose:** "Create Spreadsheet Row"
4. **Click:** "Sign in to Google Sheets"
   - Allow Zapier to access your Google account

5. **Choose Drive:** My Drive

6. **Create New Spreadsheet:**
   - Click "Create a new spreadsheet in Google Sheets"
   - Name it: **Spring 2025 Waitlist - My Robot Mowers**
   - Click "Save"

7. **Worksheet:** Sheet1

8. **Map the Fields:**
   - Click in each field and select the matching data from Netlify:

| Column | Select from Netlify Data |
|--------|--------------------------|
| **Name** | Name |
| **Email** | Email |
| **Phone** | Phone |
| **Address** | Address |
| **Yard Size** | Yard Size |
| **HOA** | HOA |
| **Interested In** | Interested In |
| **Submitted** | Created At |

9. **Click:** "Test action" (this creates a row in your spreadsheet)
10. **Click:** "Continue"

---

### Step 5: Get Notified When Someone Signs Up (2 minutes)

1. **Click:** "+ Add Step"
2. **Search for:** "Gmail"
3. **Choose:** "Send Email"
4. **Already connected** (uses same Gmail from Step 3)

5. **Fill in Fields:**

**To:** 
```
your-email@gmail.com
```
(Type your own email where you want notifications)

**Subject:**
```
🚨 New Spring Waitlist Signup - {{Name}}
```

**Body:**
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

Action Required:
✓ Review property details
✓ Reach out within 2-3 business days
✓ Confirm qualification and scheduling

View in Google Sheets:
https://docs.google.com/spreadsheets/
```

6. **Click:** "Test action"
7. **Click:** "Continue"

---

### Step 6: Turn On Your Zap! (1 minute)

1. **Name your Zap:** "Waitlist Automation"
2. **Click the toggle** to turn it ON
3. **Done!** 🎉

---

## ✅ Test Everything (5 minutes)

1. Go to your live website: **myrobotmowers.com**
2. Fill out the waitlist form
3. Submit

**You should see:**
✅ Redirected to thank-you page
✅ Confirmation email arrives in customer's inbox (from your Gmail)
✅ New row in Google Sheets
✅ Notification email sent to you
✅ Submission visible in Netlify dashboard

---

## 📊 Your Google Sheets Waitlist

**Open your spreadsheet:**
https://sheets.google.com

**You'll see all submissions with:**
- Name
- Email
- Phone
- Address
- Yard Size
- HOA Status
- Product Interest
- Timestamp

**Pro Tips:**
1. Add a **"Status"** column to track: New / Contacted / Qualified / Scheduled
2. Add a **"Notes"** column for property details
3. Use filters to sort by submission date
4. Color-code rows by status
5. Export as Excel anytime (File → Download → Excel)

---

## 💡 Important Notes

### About Sending from Gmail:
- ✅ **FREE** - No cost at all
- ✅ **Easy** - Simple setup
- ✅ **Reliable** - Gmail has great deliverability
- ⚠️ **Note:** Emails will show as from your Gmail address, not contact@myrobotmowers.com

**Options to improve:**
1. **Set up Gmail forwarding:**
   - Make contact@myrobotmowers.com forward to your Gmail
   - Set Gmail to "Send mail as" contact@myrobotmowers.com
   - Then replies go to the right place

2. **Use a professional email service later:**
   - If you want emails from contact@myrobotmowers.com, you can upgrade to SendGrid (also free for 100/day)
   - See the full guide for SendGrid setup

### Free Tier Limits:
- **Zapier Free:** 100 tasks/month
- **Gmail:** Unlimited (within Gmail's normal sending limits)
- **Google Sheets:** Unlimited rows
- **Netlify Forms:** 100 submissions/month

**100 signups/month is plenty to start!**

---

## ❓ Troubleshooting

**Problem:** Email not sending
- Check Gmail connection in Zapier
- Make sure Zap is turned ON
- Check spam folder

**Problem:** Not appearing in Google Sheets
- Verify Google Sheets action succeeded in Zapier task history
- Check you selected the right spreadsheet
- Refresh your Google Sheet

**Problem:** Form not submitting
- Must be deployed to Netlify (doesn't work locally)
- Check browser console for errors
- Verify Netlify Forms is enabled

**Problem:** {{Name}} showing instead of actual name
- You must click the "+" button and select fields from dropdown
- Don't type {{Name}} manually
- Use the field selector in Zapier

---

## 🎯 Next Steps

### After Your First Real Signup:
1. Update social proof on website ("16 families joined!")
2. Respond within 24 hours
3. Add to your Google Sheet status column
4. Call to discuss their property

### Marketing Ideas:
- Share "X families joined this week" on social
- Add waitlist link to email signature
- Create Facebook post about limited spring slots
- Offer referral bonuses for waitlist members

---

## 💰 Cost Breakdown

**Everything is FREE:**
- Zapier: FREE (100 tasks/month)
- Gmail: FREE (unlimited)
- Google Sheets: FREE (unlimited)
- Netlify Forms: FREE (100/month)

**Total Cost: $0/month** 🎉

---

## ✅ Final Checklist

- [ ] Zapier Zap created
- [ ] Netlify trigger connected
- [ ] Gmail action for customer email set up
- [ ] Google Sheets action configured
- [ ] Gmail notification to yourself set up
- [ ] Zap turned ON
- [ ] Tested with live submission
- [ ] Received confirmation email
- [ ] Saw data in Google Sheets
- [ ] Got notification email

---

**You're all set!** Your waitlist is now automated and professional. Customers get instant confirmation, you get organized in a spreadsheet, and you're notified immediately. 🚀

**Questions?** Check Zapier's excellent documentation or contact their support - they're very helpful for free tier users!

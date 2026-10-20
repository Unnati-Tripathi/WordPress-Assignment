# Contact Page — ClearPath

**Slug:** `/contact`

---

## Section 1: Page Header

> **Gutenberg blocks:** Heading + Paragraph

### Content:

**Heading (H1):**  
Get in Touch

**Intro Paragraph:**  
Have a question about our services, need career advice, or just want to say hello? We'd love to hear from you. Fill out the form below and we'll get back to you as soon as possible.

---

## Section 2: Contact Form

> **Gutenberg blocks:** WPForms block (use the WPForms widget/shortcode block)

### WPForms Setup:

1. Go to **WPForms → Add New** in the WordPress dashboard
2. Name the form: **"ClearPath Contact Form"**
3. Select the **"Simple Contact Form"** template
4. The template includes: Name, Email, Message
5. **Add one more field:** Drag a "Single Line Text" field and label it **"Subject"**. Place it between Email and Message.
6. Reorder fields: Name → Email → Subject → Message
7. Configure **Notifications:**
   - Send To Email: `admin@clearpath.local` (or your actual email)
   - Subject: `New Contact Form Submission — ClearPath`
   - From Name: `{field_id="0"}` (visitor's name)
8. Configure **Confirmation:**
   - Type: Message
   - Text: "Thank you for reaching out! This is a sample project, so responses are not actively monitored. In a real deployment, you would receive a reply within 1–2 business days."
9. Click **Save**
10. Go back to the Contact page in Gutenberg
11. Add a **WPForms** block
12. Select the "ClearPath Contact Form" from the dropdown

### Form Fields:

| Field | Type | Required | Placeholder |
|-------|------|----------|-------------|
| Name | Text | Yes | Your full name |
| Email | Email | Yes | your.email@example.com |
| Subject | Text | No | What can we help with? |
| Message | Textarea | Yes | Tell us a bit about your situation... |

---

## Section 3: Alternative Contact

> **Gutenberg blocks:** Kadence Row Layout (light gray background) → Heading + Paragraph

### Content:

**Background:** Light warm gray (`#F0EDE8`)

**Heading (H3):**  
Other Ways to Reach Us

**Paragraph:**  
**Email:** contact@clearpath-careers.com *(sample address — not actively monitored)*

Please note: This is a portfolio project. The contact form above is fully functional, but email delivery depends on the hosting environment. On some hosting platforms, form submissions may not be delivered to an inbox. In a production environment, we would configure an SMTP email service to ensure reliable delivery.

---

## Section 4: Important Note on Email Delivery

> **Gutenberg blocks:** Paragraph (italic, smaller text)

### Content:

*This contact form is built using WPForms Lite and demonstrates a standard WordPress contact form implementation. On free hosting providers, PHP mail delivery may be restricted. If you are evaluating this project, the form's functionality can be verified by testing the submission process and checking the confirmation message. In a real deployment, an SMTP plugin (such as WP Mail SMTP) would be configured with a reliable email provider to guarantee delivery.*

---

## Notes for Building This Page:

### WPForms Lite Limitations:
- WPForms Lite does **not** store form entries in the WordPress database (that's a paid feature)
- It relies on PHP `mail()` to send notifications
- On free hosting (InfinityFree), PHP `mail()` is often blocked or unreliable
- The form will still **appear and function** (visitors can fill it out and see the confirmation), but the email notification may not arrive

### How to Explain This in an Interview:
> "I implemented the contact form using WPForms Lite because it's a well-maintained, beginner-friendly plugin that doesn't require any code. I'm aware that on free hosting, email delivery isn't reliable because PHP's built-in mail function is often restricted. In a production environment, I would add the WP Mail SMTP plugin and configure it with a service like Gmail SMTP or SendGrid to ensure messages actually reach the inbox. For this project, I focused on demonstrating the form setup, validation, and user experience."

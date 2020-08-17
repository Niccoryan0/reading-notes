# 401-30 Readings

## How to use SendGrid email
[Link](https://docs.microsoft.com/en-us/azure/sendgrid-dotnet-how-to-send-email)

- SendGrid is a cloud-based email service that can be used for:
  - Automatically sending receipts or purchase confirmations to customers.
  - Administering distribution lists for sending customers monthly fliers and promotions.
  - Collecting real-time metrics for things like blocked email and customer engagement.
  - Forwarding customer inquiries.
  - Processing incoming emails.
- SendGrid can be brought in as an API via a personal key supplied by azure
- Lists for who it's from and to are constructed, and then the MailHelper is used to compose and send the email itself. AddAttachment can be used to add an attachment.
- SendGrid provides additional email functionality through the use of mail settings and tracking settings. These settings can be added to an email message to enable specific functionality such as click tracking, Google analytics, subscription tracking, and so on. For a full list of apps, see the [Settings Documentation.](https://sendgrid.com/docs/API_Reference/SMTP_API/apps.html)

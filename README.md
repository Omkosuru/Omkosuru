from email.message import EmailMessage
import ssl
import smtplib

email_sender = 'omkosuru2004@gmail.com'
email_password = 'cpxw hueo wztm awwj'

email_receiver =''

subject = "i am going to learn python"
body ="""
i am learing python by watching videos from youtube
"""
em = EmailMessage()
em['From'] = email_sender
em['To'] = email_receiver
em['subject'] = subject
em.set_content(body)


context = ssl.create_default_context()
with smtplib.SMTP_SSL('smtp.gmail.com', 465, context = context) as smtp:
    smtp.login(email_sender, email_password)
    smtp.sendmail(email_sender, email_receiver, em.as_string())


<!---
Omkosuru/Omkosuru is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

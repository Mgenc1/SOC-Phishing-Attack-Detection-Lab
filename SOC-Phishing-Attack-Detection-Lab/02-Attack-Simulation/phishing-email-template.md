# Phishing Email Template

This document describes the phishing email template used in the SOC Phishing Attack Simulation.

The email is designed to imitate a corporate IT password reset notification in order to simulate a realistic credential harvesting attack.

---

## 1. Attack Type

- **Category:** Phishing (Credential Harvesting)
- **Theme:** Password Reset Notification
- **Impersonation:** Corporate IT Security Department
- **User Interaction Required:** Yes

---

## 2. Email Template (HTML)

The following HTML template was used in the Gophish campaign:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; margin: 0; padding: 20px; }
        .container { max-width: 600px; margin: auto; background: white; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
        .header { background-color: #0078D4; color: white; padding: 20px; text-align: center; border-radius: 8px 8px 0 0; }
        .header h2 { margin: 0; font-weight: normal; }
        .content { padding: 30px; }
        .button { display: inline-block; background-color: #0078D4; color: white; text-decoration: none; padding: 12px 30px; border-radius: 5px; font-weight: bold; margin: 20px 0; }
        .footer { background-color: #f4f4f4; padding: 15px; text-align: center; font-size: 12px; color: #666; border-radius: 0 0 8px 8px; }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h2>Consoto IT Security</h2>
        </div>
        <div class="content">
            <p>Dear {{.FirstName}},</p>
            <p>We received a <strong>password reset request</strong> for your account. If this was you, please click the link below to create a new password. This link will remain valid for <strong>30 minutes</strong>.</p>
            <p style="text-align: center;">
                <a href="{{.URL}}" class="button">Reset My Password</a>
            </p>
            <p><small>If you did not request this, please ignore this email or contact the IT department immediately.</small></p>
            <hr>
            <p><strong>Note:</strong> This is an automated message. Please do not reply.</p>
        </div>
        <div class="footer">
            &copy; 2025 Consoto IT. All rights reserved.
        </div>
    </div>
</body>
</html>

---

## 3. Dynamic Variables Used

The template includes Gophish dynamic placeholders:

- `{{.FirstName}}` → Personalizes the email for the target user  
- `{{.URL}}` → Automatically replaced with the unique phishing tracking link  

These dynamic variables increase realism and improve click-through likelihood.

---

## 4. Social Engineering Techniques Used

This email leverages common phishing tactics:

- **Authority Impersonation:** Posing as corporate IT Security  
- **Urgency:** Limited-time (30 minutes) reset link  
- **Legitimacy Signals:** Professional design and corporate-style branding  
- **Personalization:** Addressing the user by first name  

---

## 5. Expected Technical Artifacts

When the victim clicks the phishing button:

1. The browser initiates an HTTP connection to the attacker-controlled host  
2. Sysmon logs a **Network Connection event (Event ID 3)**  
3. Logs are forwarded to Splunk via Universal Forwarder  
4. SOC detection and correlation analysis begin  

---

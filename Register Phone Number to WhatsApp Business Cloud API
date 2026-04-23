STEP 1: PREPARE THE NUMBER
Delete the App: If the number is currently being used on a regular WhatsApp or WhatsApp Business app on a phone, you must delete the account first.
Go to Dashboard: Log in to facebook.com and open your App.

STEP 2: ADD THE NUMBER TO META USING POSTMAN

Go to WhatsApp > API Setup (on the left menu).
Scroll to the bottom and click Add Phone Number.
Type in your Business Name and your real Phone Number.
Verify the number by typing in the 6-digit code Meta sends to your phone via SMS or Voice.

STEP 3: TURN OFF OLD SECURITY (IF NEEDED)

If you get a "PIN Mismatch" error later, do this:
Go to WhatsApp Manager > Phone Numbers.
Click the Settings (Gear icon) next to your number.
Click Two-Step Verification and click Turn Off.

STEP 4: REGISTER THE NUMBER (POSTMAN)

This tells Facebook "I am ready to use this number for the API."
Open Postman and start a new request.
Method: Set it to POST.
URL: [https://facebook.com](https://graph.facebook.com/v18.0/{phone-number-id}/register)
Auth Tab: Select Bearer Token and paste your Access Token from Meta.
Body Tab: Select raw and JSON. Paste this:
json
{
  "messaging_product": "whatsapp",
  "pin": "6_DIGIT_PIN_OF_YOUR_CHOICE"
}
Use code with caution.
Hit Send. Look for {"success": true}.

STEP 5: SEND A TEST MESSAGE (POSTMAN)

This proves everything is working.
Method: Set to POST.
URL: Change the end of the URL from /register to /messages.
[https://facebook.com](https://graph.facebook.com/v18.0/{{phone_number_id}}/messages)
Body Tab: Select raw and JSON. Paste this:
json
{
  "messaging_product": "whatsapp",
  "to": "YOUR_PERSONAL_PHONE_NUMBER",
  "type": "template",
  "template": {
    "name": "hello_world",
    "language": {
      "code": "en_US"
    }
  }
}
Use code with caution.
Hit Send. Your personal phone should receive a WhatsApp message!

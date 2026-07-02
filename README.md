# telegram-to-twilio-forwarder
A real-time Make.com automation blueprint that watches a Telegram bot for updates and instantly forwards incoming alerts or messages as SMS/WhatsApp notifications via Twilio.
# Telegram Bot to Twilio Message Forwarder

This repository contains a Make.com (formerly Integromat) scenario blueprint that builds an instant notification and forwarding pipeline between a Telegram Bot and Twilio.

## 🚀 How It Works
1. **Trigger (Telegram Bot - Watch Updates):** Listens instantly via webhooks for any incoming messages, commands, or alerts sent by users or external channels to your custom bot.
2. **Action (Twilio - Create a Message):** Extracts the text content or metadata from the Telegram payload and dynamically formats it into a native SMS or WhatsApp message dispatched straight to a designated phone number.

## 📦 What's Included
* `/blueprints/telegram-to-twilio-forwarder.json`: The complete exported Make.com scenario blueprint configuration file.

## 🔧 Setup Instructions
1. Open your **Make.com** dashboard.
2. Create a new scenario, click the three dots (`...`) located on the bottom navigation control bar, and choose **Import Blueprint**.
3. Upload the `.json` blueprint file from this repository.
4. Establish your account credentials and parameters:
   * **Telegram Bot Module:** Generate an API Token by messaging Telegram's official `@BotFather` and create a connection in Make to activate the live webhook listener.
   * **Twilio Module:** Connect using your Twilio Account SID and Auth Token. Specify your Twilio "From" phone number (or WhatsApp sender number) and your personal "To" phone number.
5. Map fields like `Message Text` or `Sender Username` from the Telegram trigger dynamically into the Twilio message body field.
6. Save the configuration and flip the main scheduling toggle switch to **ON**.

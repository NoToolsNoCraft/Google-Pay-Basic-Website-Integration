# Google Pay Web Setup

This repository demonstrates the integration of Google Pay for a virtual gift card purchase application. It allows users to buy using Google Pay as a payment method.

This collection will help you set up a Google Pay button in your web app. That's the basic integration. This button is fully functional and triggers the Google Pay checkout.

## How to Use

### Prerequisites

Before you can use this integration, make sure you have the following:

- A Google Pay Merchant account. You'll need your `gatewayMerchantId` to replace the placeholder `gatewayMerchantId` in the code.
- A local or hosted environment to run the application.

### Files

This project contains two main files:

1. **`index.html`** - The HTML file that renders the page and displays the Google Pay button.
2. **`client.js`** - The JavaScript file that contains the logic for setting up Google Pay and handling the payment process.

### Step-by-Step Guide

#### 1. Clone the Repository

git clone https://github.com/NoToolsNoCraft/Google-Pay-Basic-Website-Integration/

cd pepco-virtual-gift-cards



#### 2. Set Up the Google Pay Button

Open `index.html` and take note of the following:

- The Google Pay button will be inserted into the `<div id="buy-now"></div>` element.
- The `onload` attribute of the Google Pay script calls the `onGooglePayLoaded()` function from `client.js`.

#### 3. Set Up Google Pay Logic in `client.js`

The logic for configuring Google Pay, handling the Google Pay button click event, and processing the payment is contained in `client.js`.

- **Tokenization Specification**: This defines how the payment information is handled. Replace the `gatewayMerchantId` placeholder with your actual Google Pay merchant ID.
- **Google Pay Configuration**: This includes details on the supported payment methods, such as card networks (VISA, MasterCard), and payment authorization methods.

**Payment Flow:**

- The script loads the Google Pay API and checks if the device is ready to support Google Pay.
- A button is created if Google Pay is supported.
- When the user clicks the button, the payment data request is made, and the payment is processed.

#### 4. Run the Application

- **Without a Server**: Open `index.html` directly in your browser. The Google Pay button will appear, and you can test the Google Pay integration.
- **With a Local Server**: If you're running this in a Node.js environment, make sure to set up an Express server or another server of your choice. Once the server is up and running, open the `index.html` file in your browser.

### Troubleshooting

If you run into issues such as Google Pay not showing or errors in the browser console:

- Ensure you have configured the `gatewayMerchantId` with your actual Google Pay Merchant ID.
- Make sure your environment is set to **TEST** for testing or **PRODUCTION** for live transactions when you go live.
- Check the console for error messages and verify if the Google Pay API script is being loaded correctly.


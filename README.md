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


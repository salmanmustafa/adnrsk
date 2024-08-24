# Adyen RiskData

The `adyen-riskdata` npm module is a Node.js implementation designed to generate `dfValue` (riskData) and `components` key required for payment posts on some Adyen-integrated websites. This module simplifies the process of generating essential risk-related data, adhering to Adyen's standards for enhanced security in payment transactions.

## Features

- Generates `dfValue` (riskData) and `components` for Adyen payment processing.
- Customizable for different device and browser environments.
- Easy to integrate with existing Node.js applications.

## Usage

To use the module, simply require it in your Node.js application and create an instance of the `RiskData` class with appropriate parameters. Here's an example:

```javascript
const RiskData = require("adyen-riskData");

let riskDataInstance = new RiskData(
    "Mozilla/5.0 (Linux; Android 10; SM-A205U) AppleWebKit/537...", // userAgent
    "en-US", // language
    24, // colorDepth
    4, // deviceMemory 
    8, // hardwareConcurrency
    360, // screenWidth
    640, // screenHeight
    360, // availScreenWidth
    640, // availScreenHeight
    -300, // timezoneOffset
    "America/Chicago", // timezone
    "MacIntel" // platform
);

console.log(riskDataInstance.generate());

// Output:
eyJ2ZXJzaW9uIjoiMS4wLjAiLCJkZXZpY2VGaW5nZXJwcmludCI6IkRwcXdVNHpFZE4wMDUwMDAwMDAwMDAwMDAwQlRXRGZZWlZSMzAwMDU2OTg3NzY1V3BZV2lLekJHZmV5cE5BU0FSUVZHZm0zSlFEemcwMDJjRzNCZG5YVm1mMDAwMDBZVnhFcjAw...
```


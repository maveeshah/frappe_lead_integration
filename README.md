## Facebook Lead Integration with Frappe/ERPNext
Facebook Lead Integration is a Frappe app that captures and manages leads generated from Facebook ad campaigns. This app connects with Facebook's API to verify webhooks, receives real-time lead data, and automatically creates lead records in the Frappe Lead doctype. It includes features for token management, custom field creation, and dynamic lead data mapping, enabling seamless integration with Facebook for lead handling.

## Features
Webhook Verification: Verifies Facebook webhook events for secure data exchange.
Real-Time Lead Capture: Receives lead data from Facebook ads in real-time.
Lead Creation: Automatically creates new leads in Frappe's Lead doctype.
Token Management: Exchanges short-lived tokens with long-lived tokens for persistent access.
Dynamic Field Mapping: Maps custom lead fields dynamically based on Facebook lead form data.
Custom Field Creation: Automatically creates custom fields in the Lead doctype if needed.

## Installation
Install the app:
bench get-app facebook_lead_integration /path/to/facebook_lead_integration
bench install-app facebook_lead_integration

## Configuration
In Frappe, navigate to Facebook Lead Integration settings.
Configure the following values:
App ID and App Secret from your Facebook App.
Page Access Token (short-lived), which will be exchanged for a long-lived token.
Verify Token for webhook verification.
Doctype Name (e.g., "Lead") where Facebook leads will be stored.

## Usage
Webhook Setup: In your Facebook App settings, set up the webhook with the URL provided by this app, using the configured Verify Token for validation.
Lead Data Handling: When a lead is submitted on Facebook, the app:
Verifies the webhook request.
Retrieves lead details via Facebook’s API.
Maps data to Frappe fields, including dynamic custom fields.
Creates a new lead record in the specified doctype with the received data.

## Custom Field Creation
If the Facebook lead form includes fields not present in your Frappe Lead doctype, this app dynamically creates those fields as custom fields in the specified doctype.

## License
MIT

# Axiad SAML

## Overview
This document provides step-by-step instructions on how to configure and establish a SAML-based Single Sign-On (SSO) connection between **Axiad** and **Ping Advanced Identity Cloud**.

## Prerequisites
Before you begin, ensure you have the following:
- Administrator access to **Ping Advanced Identity Cloud**.
- Administrator access to **Axiad**.

## Step 1: Configure Ping Identity as the Identity Provider (IdP)

### 1.1 Create a SAML Application in Ping
1. Log in to the **Ping Advanced Identity Cloud** admin portal.
2. Navigate to **Applications**.
3. Click **Add Custom Application** and select **SAML**.
4. Enter a name (e.g., `Axiad`) and owner.

### 1.2 Configure SAML Settings
1. **ACS (Assertion Consumer Service) URL**: Obtain from Axiad.
2. **Attribute Mapping**: Map required user attributes (e.g., `First Name`, `Last Name`, `Email`).
3. Click **Save** to finalize the configuration.

### 1.3 Download the IdP Metadata
1. Once the application is created, go to **SAML Settings**.
2. Download the **IdP metadata XML file**.

## Step 2: Configure Axiad as the Service Provider (SP)

### 2.1 Upload Ping Identity IdP Metadata
1. Click **Upload Metadata** and select the XML file from Axiad.
2. Verify that the **ACS URL** and **Entity ID** match the Ping configuration.
3. Save the configuration.

## Step 3: Test and Verify the SAML Integration
1. Initiate an SSO login from Axiad and verify redirection to Ping Identity.
2. Authenticate using Ping Identity credentials.
3. Confirm successful login to Axiad.
4. If issues occur, check logs in both **Ping Identity** and **Axiad** for troubleshooting.

## Conclusion
You have successfully configured SAML-based SSO between **Ping Advanced Identity Cloud** and **Axiad**. Users can now log in seamlessly using their Ping Identity credentials.

## Troubleshooting
- **Invalid SAML response**: Ensure that entity IDs and ACS URLs are correctly configured.
- **User not found**: Verify attribute mappings between Ping Identity and Axiad.
- **Certificate issues**: Confirm that the correct IdP signing certificate is uploaded in Axiad.

For further assistance, refer to the documentation for **Ping Advanced Identity Cloud** and **Axiad**, or contact support.

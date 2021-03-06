---
title: Configuration
slug: configuration-get-started
tags: configuration, getting started
publish: true
position: 30
---

# Configuration

In this article we'll discuss about how to configure Fiddler Everywhere in your system. 

By default, the Fiddler Everywhere client intercepts insecure traffic (**HTTP**) only and needs an account with administrative rights to capture secure traffic (**HTTPS**). The Fiddler Everywhere client acts as a man-in-the-middle (against the HTTPS traffic). To enable capturing and decrypting HTTPS traffic, you will need to explicitly install a root trust certificate via the __HTTPS__ sub-menu in __Settings__.

## Configure on macOS

1. Start Fiddler Everywhere on the device that will capture the traffic.

2. Go to __Settings > HTTPS__

3. Click the __Trust Root Certificate__ button. 

    ![default https settings](../images/settings/settings-trust-root-certificate.png)

4. A keychain user & password box appears. Enter your __machine administrative credentials__.

    ![Enter Keychain credentials to trust the root certificate](../images/settings/settings-https-mac-keychain.png)

5. The __Capture HTTPS traffic__ checkbox is now active. Check the box to enable capturing HTTPS traffic.

    ![Enable capturing HTTPS traffic](../images/settings/settings-https-capture-https.png)
    
6. Click the __Save__ button to save the changes.

## Configure on Windows

1. Start Fiddler Everywhere on the device that will capture the traffic.

2. Go to __Settings > HTTPS__

3. Click the __Trust Root Certificate__ button. 

    ![default https settings](../images/settings/settings-trust-root-certificate.png)

4.  Trust certificate popup appears to confirm and add the certificate. 

    ![Enter Keychain credentials to trust the root certificate](../images/settings/settings-https-cert-win.png)

5. The __Capture HTTPS traffic__ checkbox is now active. Check the box to enable capturing HTTPS traffic.

    ![Enter Keychain credentials to trust the root certificate](../images/settings/settings-https-capture-https.png)
    
6. Click the __Save__ button to save the changes.

## Configure on Linux

Some Linux distributions are using different security features and different ways of adding a root certificate. For such cases, the Fiddler Everywhere provides means to export the root trust certificate so that it could be manually imported in your Linux OS. Use the __Export Root Certificate to Desktop and Trust Certificate__ option as follows:

1. Start Fiddler Everywhere on the device that will capture the traffic.

2. Go to __Settings > HTTPS__

3. Expand the __Advanced Settings__ sub-menu

4. Click the __Export Root Certificate to Desktop__ button.

    ![Export root certificate](../images/settings/settings-export-cert.png)

5. Import and trust the exported certificate. To be able to install the FE certificate, you need to follow some additional steps on Linux:

    - Create a directory and copy the certificate (exported in the previous steps). The last command will start the tool to upgrade the certificates. 

        ![Make dir and copy certificate](../images/configuration/cert_ubunto_001.png)

    - From the prompt select **Yes** to install new certificates

        ![Add new certificate](../images/configuration/cert_ubunto_002.png)

    - Choose the FiddlerRootCertificate.crt and press **OK**

        ![Add Fiddler certificate](../images/configuration/cert_ubunto_003.png)

    - The certificates are being updated

        ![Add Fiddler certificate](../images/configuration/cert_ubunto_004.png)


6. The __Capture HTTPS traffic__ checkbox is now active. Check the box to enable capturing HTTPS traffic.

    ![Enable capturing HTTPS traffic](../images/configuration/cert_ubunto_005.png)

7. Click the __Save__ button to save the changes.

    >important Some Linux distributions like Ubuntu will use localized paths (for example, the __Desktop__ folder is renamed with the related word used in the locale language). That might cause for __step 3__ to fail due to a missing folder named __Desktop__ with an error message of type _Could not find a part of the path ..._. Until an out-of-the-box solution is implemented, you could easily workaround this issue by creating a folder called __Desktop__ at your root directory (`mkdir ~/Desktop`) and then export the certificate to the newly-created directory. Once the certificate is installed, you could safely remove the directory.


For more information about Fiddler Everywhere settings, visit [**_Settings_**]({%slug decrypt-https-traffic%}) page.

## Additional Resources

Once the client is configured, you can start using its features. Get to know how to:

- [Inspect captured traffic]({%slug inspecting-traffic-get-started%}).
- [Create an API request via the Composer]({%slug composer-get-started%})
- [Modify traffic]({%slug modify-traffic-get-started%})
- [Mock server response]({%slug autoresponder-get-started%})
- [Share captured traffic with collaborators]({%slug collaboration-get-started%}).
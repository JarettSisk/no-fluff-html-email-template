


# Basic html email template

A list of resources and code snippets to help get you up and running with your html email template.
Note that this is not a bullet-proof solution. As with anything in tech, there is high chance for change. These are merely the solutions Ive came to after a reasonable amount of research and testing.

Last updated Feb 8th 2024.

## Resources

**Need to format your css styles to be inline?**  

-   [https://htmlemail.io/inline/](https://htmlemail.io/inline/) (free)
    
-   [https://app.postdrop.io/](https://app.postdrop.io/) (free)  

- https://templates.mailchimp.com/resources/inline-css/ (free)

**Need to send test emails?**  

-   [https://app.postdrop.io/](https://app.postdrop.io/) (free)  

**Need to validate that your HTML works with different email providers?**  

-   [https://www.htmlemailcheck.com/check/](https://www.htmlemailcheck.com/check/) (free on first check. Refresh page for more free checks)  
    
-   [https://www.emailonacid.com/](https://www.emailonacid.com/ "https://www.emailonacid.com/") (free 7 day trial. $99/mo after. Only 5 free tests during free trial)  

**A note on image embedding:**

Your best bet is to host your image, as many email providers dont supprt base64 encoded image embedding.
 
Some additional information on image hosting
- https://mailchimp.com/resources/image-hosting/

**Additional resources:**  
- https://templates.mailchimp.com/resources/email-client-css-support/ (Email provider css support)


## The Template

To make this plug-and-play. I made made the elements more or less modular, so you can copy and paste where needed.

Note that these will not be heavily styled. If you need to style further, the easiest route is to grab the emailNoStyles.html, and the existing styles in styles.css then paste the code into [https://app.postdrop.io/](https://app.postdrop.io/) add additional styling as needed and hit download/export to grab the inlined version. Just don't forget to do your research and test that your email looks and functions as expected. 
  
**Base**
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <meta name="viewport" content="width=device-width">
    <title>Your Title</title>
    <!--[if gte mso 9]><xml>
    <o:OfficeDocumentSettings>
        <o:AllowPNG/>
        <o:PixelsPerInch>96</o:PixelsPerInch>
    </o:OfficeDocumentSettings>
</xml><![endif]-->
</head>
<body style="padding: 0; margin: 10px;">
<!-- place pre-header here -->
<table class="container" role="presentation" style="border-spacing: 0; padding: 0; font-family: Arial, sans-serif; font-size: 16px; border: 0; width: 100%;" width="100%">
    <tr>
        <td class="widthWrapper" style="font-family: Arial, sans-serif; width: 640px;" width="640">
				<!-- place elements here -->
			</td>
			<!-- Empty td to fill in dead space (dont remove) -->
            		<td></td>
		</tr>
	</table>
</body>
</html>
```

**Pre header**
```
<span class="preheader" style="visibility: hidden; mso-hide: all; font-size: 1px; color: #ffffff; line-height: 1px; max-height: 0; max-width: 0; opacity: 0; overflow: hidden; display: none;">This is preheader text. Some clients will show this text as a preview.</span>
```

**Header**
```
<table class="header" role="presentation" style="border: 0; border-spacing: 0; padding: 0; width: 100%;" width="100%">
    <tr>
        <td style="font-family: Arial, sans-serif;">
            <h1 style="font-family: Arial, sans-serif;">Test Header</h1>
        </td>
    </tr>
</table>
```

**Main content**
```
<table class="main-content" role="presentation" style="border: 0; border-spacing: 0; padding: 0; width: 100%;" width="100%">
    <tr>
        <td style="font-family: Arial, sans-serif;">
            <p style="margin: 0 0 16px 0; font-family: Arial, sans-serif; font-size: 16px;">
                Hello!
            </p>
            <p style="margin: 0 0 16px 0; font-family: Arial, sans-serif; font-size: 16px;">
                This is some basic test content! I hope that this email
                template proves to be handy!
            </p>
            <p style="margin: 0 0 16px 0; font-family: Arial, sans-serif; font-size: 16px;">
                Thank you!
            </p>
        </td>
    </tr>
</table>
```
**Footer**
```
<table class="footer" role="presentation" style="border: 0; border-spacing: 0; padding: 0; width: 100%;" width="100%">
    <tr>
        <td style="font-family: Arial, sans-serif;">
            <p style="margin: 0 0 16px 0; font-family: Arial, sans-serif; font-size: 16px;">
                Test footer
            </p>
        </td>
    </tr>
</table>
```

**Clickable email address**
```
<a class="mailto-link" rel="noopener" href="mailto:YOUREMAIL@test.com" target="_blank" title="extra information about link" style="margin: 0; color: blue;">youremail@test.com</a>
```

**Unordered List**
```
<table class="unordered-list" role="presentation" style="border: 0; border-spacing: 0; padding: 0; margin: 0 0 16px 12px;">
    <tr>
        <td style="font-family: Arial, sans-serif; vertical-align: top;" valign="top">•</td>
        <td style="font-family: Arial, sans-serif; vertical-align: top;" valign="top">List item 1</td>
    </tr>
    <tr>
        <td style="font-family: Arial, sans-serif; vertical-align: top;" valign="top">•</td>
        <td style="font-family: Arial, sans-serif; vertical-align: top;" valign="top">List item 2</td>
    </tr>
    <tr>
        <td style="font-family: Arial, sans-serif; vertical-align: top;" valign="top">•</td>
        <td style="font-family: Arial, sans-serif; vertical-align: top;" valign="top">List item 3</td>
    </tr>
</table>
```
**Button (CTA)**
```
<table class="button" role="presentation" style="border: 0; border-spacing: 0; padding: 12px 18px 12px 18px; border-radius: 5px; background-color: #1F7F4C; margin: 0 0 16px 0;" bgcolor="#1F7F4C">
    <tr>
        <td style="font-family: Arial, sans-serif; text-align: center;" align="center">
            <a rel="noopener" href="https://www.google.com/" target="_blank" title="extra information about link" style="font-size: 18px; color: #ffffff; text-decoration: none; text-align: center;">I am a button</a>
        </td>
    </tr>
</table>
```

**Unsubscribe Link**
```
<a class="unsubscribe-link" rel="noopener" href="https://www.google.com/" target="_blank" title="extra information about link" style="margin: 0; color: blue; font-size: 12px;">unsubscribe</a>
```
**Image**
```
<img alt="Your Image Description" src="https://www.w3schools.com/images/w3schools_green.jpg">
```

**Block wrapper (for making any element display as a block)**
```
<div class="blockWrapper" style="margin: 0 0 16px 0;">
    Any element you want to be a block-level element (that isnt natively)
    IE: a tags, img tags, etc.
</div>
<div class="blockWrapperNoMargin" style="margin: 0;">
    Any element you want to be a block-level element (that isnt natively)
    IE: a tags, img tags, etc.
</div>
```

**Paragraph (block level text with bottom margin)**
```
<p style="margin: 0 0 16px 0; font-family: Arial, sans-serif; font-size: 16px;">
    Hello! I will be writting on a new line.
</p>
```

**Bold Text**
```
<b>I am bold!</b> OR <strong>I am bold!</strong>
```


# Html email template

A list of resources and code snippets to help get up and running with your html email template.
Note that this is not a bullet-proof solution. As with anything in tech, there is high chance for change. These are merely the solutions Ive came to after a reasonable amount of research and testing.

Last updated Feb 8th 2024.

## Resources

**Need to format your css styles to be inline?**  

-   [https://htmlemail.io/inline/](https://htmlemail.io/inline/) (free)  
    
-   [https://app.postdrop.io/](https://app.postdrop.io/) (free)  

**Need to send test emails?**  

-   [https://app.postdrop.io/](https://app.postdrop.io/) (free)  

**Need to validate that your HTML works with different email providers?**  

-   [https://www.htmlemailcheck.com/check/](https://www.htmlemailcheck.com/check/) (free on first check. Refresh page for more free checks)  
    
-   [https://www.emailonacid.com/](https://www.emailonacid.com/ "https://www.emailonacid.com/") (free 7 day trial. $99/mo after. A very extensive service)  

**A note on image embedding:**
You have a few options when it comes to using images in  your HTML email template.
The most straightforward option (imo) is to base 64 encode the image, and use that.

 - https://www.base64-image.de/ (Free base 64 image encoder)
 
 Here is a site listing other options to embed your images
 
 - https://www.pipedrive.com/en/blog/embedding-images-in-emails

## The Template

To make this plug-and-play. I split out the chunks so you can copy paste where needed.

Note that these will not be heavily styled. If you need to style further, the easiest route is to grab the emailNoStyles.html, and the existing styles in styles.css then paste the code into [https://app.postdrop.io/](https://app.postdrop.io/) and add additional styling as needed and hit download/export to grab the inlined version. Just don't forget to do your research and test that your email looks and functions as expected. 
  
**Base**
```
<!DOCTYPE html>  
<html lang="en">  
<head>  
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />  
	<meta name="viewport" content="width=device-width">  
	<title>Your Title</title>  
</head>  
<body style="padding: 0; margin: 10px;">
    <!-- if desired, insert pre-header here. --> 
	<table class="container" style="font-family: Calibri, sans-serif; font-size: 16px; font-weight: normal; max-width: 640px;">  
		<tr>  
			<td>  
				<!-- paste additional elements here! -->  
			</td>  
		</tr>  
	</table>  
</body>  
</html>
```

**Pre header**
```
<span  class="preheader"  style="color: transparent; display: none; height: 0; max-height: 0; max-width: 0; opacity: 0; overflow: hidden; mso-hide: all; visibility: hidden; width: 0;">This is preheader text. Some clients will show this text as a preview.</span>
```

**Header**
```
<table  class="header"  role="presentation"  style="border: 0; border-spacing: 0; padding: 0; width: 100%;"  width="100%">
	<tr>
		<td>
			<h1>Test Header</h1>
		</td>
	</tr>
</table>
```

**Main content**
```
<table  class="main-content"  role="presentation"  style="border: 0; border-spacing: 0; padding: 0; width: 100%;"  width="100%">
	<tr>
		<td>
			<p  style="margin: 0 0 16px 0;">
				Hello!
			</p>
			<p  style="margin: 0 0 16px 0;">
				This is some basic test content. I hope that this email
				template proves to be handy!
			</p>
			<p  style="margin: 0 0 16px 0;">
				Thank you!
			</p>
		</td>
	</tr>
</table>
```
**Footer**
```
<table  class="footer"  role="presentation"  style="border: 0; border-spacing: 0; padding: 0; width: 100%;"  width="100%">
	<tr>
		<td>
			<p  style="margin: 0 0 16px 0;">
				Test footer
			</p>
			<a  rel="noopener"  href="mailto:YOUREMAIL@test.com">youremail@test.com</a>
			<a  id="unsubscribe-link"  rel="noopener"  href="https://www.google.com/"  target="_blank">unsubscribe</a>
		</td>
	</tr>
</table>
```

**Clickable email address**
```
<a  rel="noopener"  href="mailto:YOUREMAIL@test.com">youremail@test.com</a>
```

**Unordered List**
```
<table  class="unordered-list"  role="presentation"  style="border: 0; border-spacing: 0; padding: 0; margin: 0 0 16px 12px;">
	<tr>
		<td  style="vertical-align: top;"  valign="top">•</td>
		<td  style="vertical-align: top;"  valign="top">List item 1</td>
	</tr>
	<tr>
		<td  style="vertical-align: top;"  valign="top">•</td>
		<td  style="vertical-align: top;"  valign="top">List item 2</td>
	</tr>
	<tr>
		<td  style="vertical-align: top;"  valign="top">•</td>
		<td  style="vertical-align: top;"  valign="top">List item 3</td>
	</tr>
</table>
```
**Button (CTA)**
```
<table  class="button"  style="border: 0; border-spacing: 0; padding: 12px 18px 12px 18px; border-radius: 5px; background-color: #1F7F4C; margin: 0 0 16px 0;"  bgcolor="#1F7F4C">
	<tr>
		<td  style="text-align: center;"  align="center">
			<a  rel="noopener"  href="https://www.google.com/"  target="_blank"  style="font-size: 18px; color: #ffffff; text-decoration: none; display: block; text-align: center;">I am a button</a>
		</td>
	</tr>
</table>
```

**Unsubscribe Link**
```
<a  id="unsubscribe-link"  rel="noopener"  href="https://www.google.com/"  target="_blank">unsubscribe</a>
```

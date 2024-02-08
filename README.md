
# Html email template

A list of resources and code snippets to plug into your html email template as needed.
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

To make this plug-and-play. I split out the chunks and you can copy paste where needed.

Note that these will not be heavily styled. If you need to style further, the easiest route is to piece together you're template, then put your styles in a ```<script></script>``` tag in the html head and make use of the classes,
then use [https://app.postdrop.io/](https://app.postdrop.io/) to **inline** all your new styles. Then the script tag can be removed. 
  
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
	<table class="container" style="font-family: Calibri, sans-serif; font-size: 16px; font-weight: normal; width: 640px;"  width="640">  
		<tr>  
			<td>  
				<!-- paste additional elements here! -->  
			</td>  
		</tr>  
	</table>  
</body>  
</html>
```

**Header**
```
<table  class="header"  role="presentation"  style="border: 0; padding: 0; width: 100%;"  width="100%">
	<tr>
		<td>
			<h1>Test Header</h1>
		</td>
	</tr>
</table>
```

**Main content**
```
<table  class="main-content"  role="presentation"  style="border: 0; padding: 0; width: 100%;"  width="100%">
	<tr>
		<td>
			<p  style="margin: 16px 0;">
				Hello!,
			</p>
			<p  style="margin: 16px 0;">
				This is some basic test content! I hope that this email <br>
				template proves to be handy!
			</p>
			<p  style="margin: 16px 0;">
				Thank you!,<br>
				tester@test.com
			</p>
		</td>
	</tr>
</table>
```
**Footer**
```
<table  class="footer"  role="presentation"  style="border: 0; padding: 0; width: 100%;"  width="100%">
	<tr>
		<td>
			<p style="margin: 16px 0;">
				Test footer
			</p>
			<a  id="unsubscribe-link"  href="REPLACEME"  target="_blank">unsubscribe</a>
		</td>
	</tr>
</table>
```

**Unordered List**
```
<table  class="unordered-list"  role="presentation"  style="border: 0; padding: 0; width: 100%; margin-left: 16px;"  width="100%">
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

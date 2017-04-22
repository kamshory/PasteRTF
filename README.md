# PasteRTF
This script will paste data from clipboard containing image, HTML or plain text.

When you copying object to the clipboard and paste it to web application, clipboard data type can be on or more of:

1. text/plain
2. text/html
3. Files

If you copying image from web application, the clipboard data type is text/html and Files. If you copying image from other application, the clipboard data type is Files.

If clipboard data type is Files, program will get blob data as a file using FileReader. Then the FileReader will produce result as base64 data of the image. The image data can be used as you want.

If clipboard data type is Files and text/html, program will parse the text/html data and find the absolute image URL from it. Then image URL can be used as you want.

Some Windows applications like Microsoft Visio and Adobe Fireworks, automaticaly convert object as image when you copy it and can be pasted as an image to other application, including web application. So you can copy Microsoft Visio or Adobe Fireworks object as an image to your application without save it as file first.

Equation Editor in Microsoft Word does not convert the object into image when you copy it. So, if you copy some equation from Microsoft Word, you will only get text data when you paste it into web application. Fortunately, you can use Snipping Tool to put equation from Microsoft Word into web application without save it firts.

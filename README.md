# PasteRTF
This script will paste data from clipboard containing image, HTML or plain text.

When you copying object to the clipboard and paste it to web application, clipboard data type can be on or more of:

1. text/plain
2. text/html
3. Files

If you copying image from web application, the clipboard data type is text/html and Files. If you copying image from other application, the clipboard data type is Files.

If clipboard data type is Files, program will get blob data as a file using FileReader. Then the FileReader will produce result as base64 data of the image. The image data can be used as you want.

If clipboard data type is Files and text/html, program will parse the text/html data and find the absolute image URL from it. Then image URL can be used as you want.

# Create a QR Code with Python

It is first necessary to install the pyqrcode module. You can execute this command by writing it in your command prompt or terminal.

`pip install pyqrcode`

It will take a few seconds to install the module.
We need to create a Python file from which we will generate a QR code. 

**1) Import essential modules.**

`import pyqrcode
from pyqrcode import QRCode`

**2) Create the string that will represent the QR Code.**

`s = "https://khushnoodasif.com"`

**3) The following commands will generate the QR code.**

`qr = pyqrcode.create(s)`

**4) The QR code is generated and stored in a 'qr' variable. The svg file can now be created and saved as "website.svg".**

`qr.svg("website.svg",scale = 7)`

Now that we have the code finished, we can run the program. The program creates a .svg file named "website.svg" in the directory where the python file is located. When you open the file, you'll see a QR code (see the QR code image below). Scan it and you will see the string 's' that points to my website.

**QR Code**

![QR Code](https://github.com/khushnoodasif/create-qr-code-with-python/blob/main/qrcode.png?raw=true)

I have posted this python file's source code on my [GitHub repository](https://github.com/khushnoodasif/create-qr-code-with-python). Also, check the walk-through on [YouTube](https://youtu.be/N9AT6u3Ey-4).

Thanks for reading!



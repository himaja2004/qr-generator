# qr-generator
import qrcode
from PIL import Image
qr= qrcode.QRCode(version=1,error_correction=qrcode.constants.ERROR_CORRECT_H,
                 box_size=10,border=4)
str=input()
qr.add_data(str)
qr.make(fit=True)
img=qr.make_image(fill_color="green")
img.save("youtube.png")

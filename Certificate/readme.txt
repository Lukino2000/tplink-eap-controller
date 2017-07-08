you need already done private and public certificate

openssl pkcs12 -export -in MYSITE.crt -inkey MYSITE.key -name eap -out MYSITE.p12

it is important that the name used is "eap"

copy MYSITE.p12 in C:\Program Files (x86)\TP-LINK\EAP Controller\keystore
from C:\Program Files (x86)\TP-LINK\EAP Controller\keystore

..\jre\keytool -importkeystore -deststorepass tplink -destkeystore eap.keystore -srckeystore MYSITE.p12 -srcstoretype PKCS12
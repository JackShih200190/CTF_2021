## 使用套件
```
! pip install pycrypto
```
 - [pycrypto](https://pypi.org/project/pycrypto/)
## 對稱式加密
```python
from Crypto.Cipher import AES

obj = AES.new('This is a key123', AES.MODE_CBC, 'This is an IV456')

message = "flag(HappyCrypt)"

ciphertext = obj.encrypt(message)
ciphertext
```
![image](https://user-images.githubusercontent.com/55253641/134445359-a0b8b008-8083-440f-ad59-97a7959bef4d.png)


## 解密
```python
obj2 = AES.new('This is a key123', AES.MODE_CBC, 'This is an IV456')

obj2.decrypt(ciphertext)
```
![image](https://user-images.githubusercontent.com/55253641/134445392-63ac2b18-89ca-42e7-aa50-58816395c848.png)

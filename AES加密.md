## 使用套件
```
! pip install pycrypto
```
 - [pycrypto](https://pypi.org/project/pycrypto/)


```
def new(key, *args, **kwargs)
Create a new AES cipher

:Parameters:
  key : byte string
    The secret key to use in the symmetric cipher.
It must be 16 (*AES-128*), 24 (*AES-192*), or 32 (*AES-256*) bytes long.
:Keywords:
  mode : a *MODE_** constant
    The chaining mode to use for encryption or decryption.
Default is MODE_ECB.
  IV : byte string
    The initialization vector to use for encryption or decryption.

    It is ignored for MODE_ECB and MODE_CTR.

    For MODE_OPENPGP, IV must be block_size bytes long for encryption
and block_size +2 bytes for decryption (in the latter case, it is
actually the *encrypted* IV which was prefixed to the ciphertext).
It is mandatory.

    For all other modes, it must be block_size bytes longs. It is optional and
when not present it will be given a default value of all zeroes.
  counter : callable
    (*Only* MODE_CTR). A stateful function that returns the next
*counter block*, which is a byte string of block_size bytes.
For better performance, use Crypto.Util.Counter.
  segment_size : integer
    (*Only* MODE_CFB).The number of bits the plaintext and ciphertext
are segmented in.
It must be a multiple of 8. If 0 or not specified, it will be assumed to be 8.

:Return: an AESCipher object
```

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

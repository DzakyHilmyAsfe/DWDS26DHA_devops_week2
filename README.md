# Proses Instalasi dan Konfigurasi Aplikasi Node.js, Python dan Go

**1. Node.js**

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash```

![1](https://user-images.githubusercontent.com/90166624/134762830-e8f85b98-209b-40b6-96ac-d790d0d59cc4.png)


* Jika terminal mengatakan  bahwa *command curl is not found* , maka terlebih dahulu kita menginstall curl dengan perintah :

```sudo apt install curl```

* Lalu kita akan menginstal nvm agar kita dapat memilih versi node.js yang akan kita pakai, dengan memasukkan perintah :

`nvm install 14`

![2](https://user-images.githubusercontent.com/90166624/134762893-13cfc0b6-754a-46ea-b526-0140f443c16d.png)


* Gunakan perintah ini untuk menggunakan nvm versi 14 :

```nvm use 14```

![3](https://user-images.githubusercontent.com/90166624/134762906-19dca4f7-0dc1-4f24-984d-4a23d36b3b28.png)

* Gunakan perintah ini untuk mengecek instalasi yang telah dilakukan :

```node -v``` ```nvm -v```

![Screenshot from 2021-09-25 14-14-51](https://user-images.githubusercontent.com/90166624/134762948-8025c84b-9722-4e86-bdb9-afdece73d4de.png)

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

```exec bash``` atau  ```exec zsh```

* Lalu kita akan membuat folder baru, dan masuk kedalam folder tersebut

```mkdir myapp-nodejs``` ```cd myapp-nodejs```

![Screenshot from 2021-09-25 14-16-28](https://user-images.githubusercontent.com/90166624/134763039-6629fb67-8b59-41a1-baf9-9ab44a0855c3.png)

* Kita akan membuat file package.json :

```npm init-y```

![Screenshot from 2021-09-25 14-17-39](https://user-images.githubusercontent.com/90166624/134763151-5869a85e-c686-444f-ac66-641438f8c411.png)

* Install express, express ini seperti library agar sebuah code bisa berjalan :

```npm install express --save```

![Screenshot from 2021-09-25 14-18-35](https://user-images.githubusercontent.com/90166624/134763160-80361b27-d4d3-4c50-8fa7-7e9addd80743.png)

* Setelah itu kita akan membuat coding program sederhana pada node js, dengan menggunakan perintah :

```nano index.js```

![Screenshot from 2021-09-25 14-19-34](https://user-images.githubusercontent.com/90166624/134763169-d7b790ee-d7f5-4191-92d0-32ffd7ade3f5.png)

* Masukkan kode berikut :

```node
const express = require('express')
const app = express()
const port = 3000
app.get('/',(req, res) => {
res.send('Hello World!')
})
app.listen(port, ()=>{
console.log(`Example app listening at http://localhost:$(port)`)
})
```

* Jalankan kode, menggunakan perintah :

```node index.js```

![Screenshot from 2021-09-25 14-21-26](https://user-images.githubusercontent.com/90166624/134763191-5fa49217-f7ba-4254-afea-20cb4fba1c0e.png)

* Jika berhasil tanpa error, lalu buka alamat web https://localhost:3000 pada browser :

![Screenshot from 2021-09-25 14-22-14](https://user-images.githubusercontent.com/90166624/134763202-80f60e90-31ae-4e53-ad8f-c5f310448127.png)


**2. Python**

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```sudo apt update```

![Screenshot from 2021-09-26 01-38-02](https://user-images.githubusercontent.com/90166624/134783266-9249590f-e7d4-45f6-b1ee-0b524d4bf632.png)


* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```sudo apt upgrade -y```

![Screenshot from 2021-09-26 01-39-34](https://user-images.githubusercontent.com/90166624/134783271-bbe1e2b9-1a30-4b18-9e3c-61ebcce91bca.png)


* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```python3 -V```

![Screenshot from 2021-09-26 01-43-20](https://user-images.githubusercontent.com/90166624/134783275-db692e4c-0d16-4332-9fa6-057ca8e0def0.png)


* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```sudo apt install python3-pip```

![Screenshot from 2021-09-26 01-43-55](https://user-images.githubusercontent.com/90166624/134783293-a825384c-a8bc-4529-badc-e5c047f56582.png)


* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```pip install flask```

![Screenshot from 2021-09-26 01-45-08](https://user-images.githubusercontent.com/90166624/134783297-26ada642-58e2-4e09-8f97-0106a764e6c3.png)


* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```mkdir python```

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```nano index.py```

![Screenshot from 2021-09-26 01-54-27](https://user-images.githubusercontent.com/90166624/134783311-aafe4602-bcc6-4f87-8083-bc707d2b61d3.png)


* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```python
from flask import Flask
app = Flask(__name__)
@app.route("/")
	def main():
return "Welcome to port 5000!"
if __name__=="__main__":
	app.run()
```

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```python3 index.py```

![Screenshot from 2021-09-26 01-55-56](https://user-images.githubusercontent.com/90166624/134783320-4fccb92a-d4f0-4028-af91-66d7d3aa949a.png)

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

![Screenshot from 2021-09-26 01-56-48](https://user-images.githubusercontent.com/90166624/134783335-09d04e59-a270-434b-956e-56d14dded742.png)


**3. Go**

```wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su```

```rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit```

```export PATH=$PATH:usr/local/go/bin```

```go version```

```mkdir myapp-golang```

```cd myapp-golang```

```nano index.go```

```go
package main
import "fmt"
func main(){
	fmt.Println("Hello world di terminal!")
}
```

```go run index.go```

```go build index.go```

```./index.go```


# Service Management Pada Sistem Operasi

```sudo apt install nginx```

```sudo systemctl status nginx```

```sudo systemctl start nginx```

```sudo systemctl enable nginx```

```sudo systemctl restart nginx```

```sudo systemctl disable nginx```

# Memory

```sudo apt install htop```

```htop```

# Storage

```df -h```

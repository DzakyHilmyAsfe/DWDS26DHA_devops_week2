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

* Jika berhasil tanpa error, lalu buka alamat web https://localhost:3000 pada browser

![Screenshot from 2021-09-25 14-22-14](https://user-images.githubusercontent.com/90166624/134763202-80f60e90-31ae-4e53-ad8f-c5f310448127.png)


**2. Python**

* Sebelum menginstall aplikasi python kita akan meng update serta meng upgrade sistem menggunakan perintah :

```sudo apt update``` dan ```sudo apt upgrade -y```

![Screenshot from 2021-09-26 01-38-02](https://user-images.githubusercontent.com/90166624/134783266-9249590f-e7d4-45f6-b1ee-0b524d4bf632.png)


![Screenshot from 2021-09-26 01-39-34](https://user-images.githubusercontent.com/90166624/134783271-bbe1e2b9-1a30-4b18-9e3c-61ebcce91bca.png)


* Aplikasi python akan ada setelah itu, dan kita cek versinya :

```python3 -V```

![Screenshot from 2021-09-26 01-43-20](https://user-images.githubusercontent.com/90166624/134783275-db692e4c-0d16-4332-9fa6-057ca8e0def0.png)


* Selanjutnya kita akan menginstall package manager dan flask untuk python.

```sudo apt install python3-pip```

![Screenshot from 2021-09-26 01-43-55](https://user-images.githubusercontent.com/90166624/134783293-a825384c-a8bc-4529-badc-e5c047f56582.png)

```pip install flask```

![Screenshot from 2021-09-26 01-45-08](https://user-images.githubusercontent.com/90166624/134783297-26ada642-58e2-4e09-8f97-0106a764e6c3.png)


* Buat folder baru menggunakan perintah :

```mkdir python```

* Lalu buat file phyton baru menggunakan perintah :

```nano index.py```

![Screenshot from 2021-09-26 01-54-27](https://user-images.githubusercontent.com/90166624/134783311-aafe4602-bcc6-4f87-8083-bc707d2b61d3.png)


* Masukkan kode berikut :

```python
from flask import Flask
app = Flask(__name__)
@app.route("/")
	def main():
return "Welcome to port 5000!"
if __name__=="__main__":
	app.run()
```

* UJalankan kode menggunakan perintah :

```python3 index.py```

![Screenshot from 2021-09-26 01-55-56](https://user-images.githubusercontent.com/90166624/134783320-4fccb92a-d4f0-4028-af91-66d7d3aa949a.png)

* Jika berhasil tanpa error, lalu buka alamat web https://localhost:5000 pada browser

![Screenshot from 2021-09-26 01-56-48](https://user-images.githubusercontent.com/90166624/134783335-09d04e59-a270-434b-956e-56d14dded742.png)


**3. Go**

* Sebelum menginstall aplikasi go kita akan menjalankan perintah perintah berikut ini pada terminal linux, perintah ini akan mendownload file golang, dan memberikan akses root :

```wget https://golang.org/dl/go1.16.5.linux-amd64.tar.gz && sudo su```

![Screenshot from 2021-09-26 02-08-37](https://user-images.githubusercontent.com/90166624/134784806-98852ffc-b761-4628-abfc-217f14d7eba3.png)

* Lalu extract dan copy file yang sudah kita download tadi menggunakan perintah :

```rm -rf /usr/local/go && tar -C /usr/local -xzf go1.16.5.linux-amd64.tar.gz && exit```

* Selanjutnya pindahkan path go pada bashrc, menggunakan perintah :

```export PATH=$PATH:/usr/local/go/bin```

* Cek versi instalasi go :

```go version```

* Buat folder baru :

```mkdir myapp-golang```

* Masuk ke folder tersebut :

```cd myapp-golang```

![1](https://user-images.githubusercontent.com/90166624/134784753-8749de3e-94ac-4110-8810-1682b6d009c3.png)

* Buat file golang baru, dan masukkan kode :

```nano index.go```

![2](https://user-images.githubusercontent.com/90166624/134784774-65f4792b-7f99-4434-81ff-8e5d7d54d649.png)

```go
package main
import "fmt"
func main(){
	fmt.Println("Hello world di terminal!")
}
```

* Jalankan kode menggunakan perintah :

```go run index.go```

![3](https://user-images.githubusercontent.com/90166624/134784783-9661167c-c4a0-4980-bfb7-0aebd3fe4c84.png)

* Lalu build aplikasi golang dengan perintah :

```go build index.go```

* Lalu jalankan aplikasi yang telah di build dengan perintah :

```./index```

![Screenshot from 2021-09-28 01-55-44](https://user-images.githubusercontent.com/90166624/134968332-c195a1e9-6616-461c-ad62-bdf0d27a6477.png)


# Service Management Pada Sistem Operasi

* Perintah untuk menginstall nginx :

```sudo apt install nginx```

![Screenshot from 2021-09-26 03-11-19](https://user-images.githubusercontent.com/90166624/134784970-92df48d4-7ab3-4b02-b02e-70c44c72572b.png)

* Perintah untuk melihat keadaan nginx :

```sudo systemctl status nginx```

![Screenshot from 2021-09-26 03-12-08](https://user-images.githubusercontent.com/90166624/134784978-854e3ded-38b6-481d-8062-166697489fb6.png)

* Perintah untuk memulai nginx:

```sudo systemctl start nginx```

* Perintah untuk mengaktifkan nginx :

```sudo systemctl enable nginx```

* Perintah untuk memulai ulang nginx :

```sudo systemctl restart nginx```

* Perintah untuk menonaktifkan nginx :

```sudo systemctl disable nginx```

![Screenshot from 2021-09-26 03-14-32](https://user-images.githubusercontent.com/90166624/134784981-453125b0-afa9-4cd7-9eeb-96d3bce7029a.png)

# Memory

* Perintah untuk menginstall htop :

```sudo apt install htop```

![Screenshot from 2021-09-26 03-15-02](https://user-images.githubusercontent.com/90166624/134784990-492b83df-f3a8-44a3-b358-59c93e721841.png)

* Perintah untuk menjalankan htop :

```htop```

![Screenshot from 2021-09-26 03-15-22](https://user-images.githubusercontent.com/90166624/134784992-af1a8a1f-439d-436a-8863-1fc9d0a850ab.png)

# Storage

* Perintah untuk melihat keadaan penyimpanan device :

```df -h```

![Screenshot from 2021-09-26 03-15-46](https://user-images.githubusercontent.com/90166624/134784995-b5c9c4ca-6f77-42e4-8c21-031345ebfa92.png)

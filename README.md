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

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

```mkdir myapp-nodejs``` ```cd myapp-nodejs```

![Screenshot from 2021-09-25 14-16-28](https://user-images.githubusercontent.com/90166624/134763039-6629fb67-8b59-41a1-baf9-9ab44a0855c3.png)

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

```npm init-y```

![Screenshot from 2021-09-25 14-17-39](https://user-images.githubusercontent.com/90166624/134763151-5869a85e-c686-444f-ac66-641438f8c411.png)

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

```npm install express --save```

![Screenshot from 2021-09-25 14-18-35](https://user-images.githubusercontent.com/90166624/134763160-80361b27-d4d3-4c50-8fa7-7e9addd80743.png)

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

```nano index.js```

![Screenshot from 2021-09-25 14-19-34](https://user-images.githubusercontent.com/90166624/134763169-d7b790ee-d7f5-4191-92d0-32ffd7ade3f5.png)

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

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

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

```node index.js```

![Screenshot from 2021-09-25 14-21-26](https://user-images.githubusercontent.com/90166624/134763191-5fa49217-f7ba-4254-afea-20cb4fba1c0e.png)

* Jika instalasi nya belum terdeteksi, maka gunakan perintah berikut :

![Screenshot from 2021-09-25 14-22-14](https://user-images.githubusercontent.com/90166624/134763202-80f60e90-31ae-4e53-ad8f-c5f310448127.png)


**2. Python**

```sudo apt update```

```sudo apt update -y```

```python3 -V```

```sudo apt install python3-pip```

```pip install flask```

```mkdir-python```

```nano index.py```

```python3 index.py```

```python
from flask import Flask
app = Flask(__name__)
@app.route("/")
	def main():
return "Welcome!"
if __name__=="__main__":
	app.run()
```

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
	fmt.Println("Hello world!")
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

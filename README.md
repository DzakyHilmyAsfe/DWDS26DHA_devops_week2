# Proses Instalasi dan Konfigurasi Aplikasi Node.js, Python dan Go

**1. Node.js**

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash```

* Jika terminal mengatakan  bahwa *command curl is not found* , maka terlebih dahulu kita menginstall curl dengan perintah :

```sudo apt install curl```

* Lalu kita akan menginstal nvm agar kita dapat memilih versi node.js yang akan kita pakai, dengan memasukkan perintah :

`nvm install 14`

* Gunakan perintah ini untuk menggunakan nvm versi 14 :

```nvm use 14```

```node -v```

```nvm -v```

```exec bash```

```nmkdir myapp-nodejs```

```cd myapp-nodejs```

```npm init-y```

```npm install express --save```

```nano index.js```


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

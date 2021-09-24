# DWDS26DHA_devops_week2

## Proses Instalasi dan Konfigurasi Aplikasi Node.js, Python dan Go

**1. Node.js**

* Untuk menginstall aplikasi node.js kita akan menjalankan perintah perintah berikut ini pada terminal linux :

```curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash```

* Jika terminal mengatakan  bahwa *command curl is not found* , maka terlebih dahulu kita menginstall curl dengan perintah :

```sudo apt install curl```

* Lalu kita akan menginstal nvm agar kita dapat memilih versi node.js yang akan kita pakai, dengan memasukkan perintah :

```nvm install 14```

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



const express = require('express')

const app = express()

const port = 3000

app.get('/',(req, res) => {

res.send('Hello World! i am doing my 2nd task')

})

app.listen(port, ()=>{

console.log(`Example app listening at http://localhost:$(port)`)

})


**2. Python**

```sudo apt update```

```sudo apt update -y```

```python3 -V```

```sudo apt install python3-pip```

```pip install flask```

```mkdir-python```

```nano index.py```

```python3 index.py```

```from flask import Flask
app = Flask(__name__)
@app.route("/")
	def main():
return "Welcome!"
if __name__=="__main__":
	app.run()```

**3. Go**

```sudo apt update```

```sudo apt update -y```

```python3 -V```

```sudo apt install python3-pip```

```pip install flask```

```mkdir-python```

```nano index.py```

```python3 index.py```

```from flask import Flask
app = Flask(__name__)
@app.route("/")
	def main():
return "Welcome!"
if __name__=="__main__":
	app.run()```



## Service Management Pada Sistem Operasi

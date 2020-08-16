# 01-1 使用Flask


### 1. 檔案放置方式
```
 <web>
   |
   |__ <static>
   |      |__ <css>
   |      |     |__ main.css
   |      |     |__ menu.css
   |      |     |__ color.css
   |      |
   |      |__ <imgs>
   |            |__ header.jpg  (1000px * 150px)
   |
   |__ <templates>
   |      |__ index.html 
   |      
   |__ app.py  
```


### 2. 測試版本
```
Python 3.8.1 32-bit
```

### 3. 範例下載
```
<下載>中的 web.zip
```


### 4. 追加外掛
```
pip install flask
```

### 5. app.py
``` py
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('index.html')
    
if __name__ == '__main__':
    app.run(debug=True, port=3000, threaded=True)    
```


### 6. 測試
```
http://localhost:3000

(如要修改了程式要重載新內容, 請按著[shift]鍵, 同時按瀏覽器的重整畫面)
```

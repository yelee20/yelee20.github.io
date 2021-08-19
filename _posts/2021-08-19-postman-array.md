---
title: "[Postman] Send an array as form-data"
categories:
- Tools
last_modified_at: 2021-08-19T14:00:00+09:00
toc: true
---

## [Postman] Send an array as form-data
💭 What is Postman?
- 🧐 Postman is an application used for **API testing**. You can test various types of HTTP requests (POST, GET, PUT, PATCH, DELETE) . Please refer to [Postman official website](https://www.postman.com/) for more details.
<br>

### 1.  Send an array as form-data in Postman
- Suffix your variable's name with squared brackets **[ ]**
- ex) array[index]

| Key | Value |
|--|--|
| score[0] | 10 |
|score[1]|7|
|score[2]|8|

<br>
<center><img src="https://user-images.githubusercontent.com/54275926/130093729-060991dd-b83e-4aaa-89d8-475e5b1ab76e.png" width="100%" height="100%"></center>
<br>

Check the data packet by 
📋 < Node.js code >
~~~javascript
console.log(req.body.score);
~~~


📋 < Result >
~~~ubuntu
[10, 7, 8]
~~~

### 2. Send an array of dictionaries as form-data
- ex) array[index][key]

| Key | Value |
|--|--|
| score[0][math] | 98 |
|score[0][physics]|78|
|score[0][chemistry]|89|
|score[1][math]|72|
|score[1][physics]|30|
|score[1][chemistry]|90|

📋 < Result >
~~~ubuntu
"score": [
    {
        "math": 98,
        "physics": 78,
        "chemistry": 89,
    },
    {
        "math": 72,
        "physics": 30,
        "chemistry": 90,
    }
]
~~~



Reference:

[https://stackoverflow.com/questions/12756688/is-it-possible-to-send-an-array-with-the-postman-chrome-extension](https://stackoverflow.com/questions/12756688/is-it-possible-to-send-an-array-with-the-postman-chrome-extension)
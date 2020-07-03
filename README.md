#### Node的fs模块快速封装使用

将原生的fsfs模块进行promise封装，可以快速的使用async—await模式

- read(读取文件)
-  write（写入文件）
- mkdir（创建目录）
- reName（目录重命名）
- readdir（读取目录路径）

1.安装

```javascript
npm i vt-fs
```

2.使用

```javascript
// 1.直接使用
const {read} = require('vt-fs');

let path = '../../static' // 要读取的文件

// 返回的回调函数
read(path).then((res) => {
	console.log(res)
})

// 2.结合async
(async function () {
	let data = await read(path)
	console.log(data)
} )()
```


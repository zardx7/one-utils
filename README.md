<h1 align="center">Welcome to one-utils 👋</h1>
<p>
  <a href="https://www.npmjs.com/package/one-utils" target="_blank">
    <img alt="Version" src="https://img.shields.io/npm/v/one-utils.svg">
  </a>
  <a href="LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
</p>

> Module created for facilitated your life ;) Bringing some native PHP modules to the NODE

## Install

```sh
$ npm i one-utils -s
```

## Usage

### IMPORT ALL FUNCTIONS

```js
const { GetStr, sleep, curl, gerarCpf, include, rand, randomizador, proxy, proxy1 } = require("one-utils")
```

### FUNCTIONS

* [curl](#curl): Function async/await for famous Curl (for request in web or applications)
* [gerarCpf](#GerarCpf): function for generate CPF valid
* [GetStr](#GetStr): function for exploding strings
* [include](#include): function to include code from another file
* [proxy](#proxy): function for testing your proxy in server lumtest
* [proxy1](#proxy1): function for testing your proxy in server Google
* [rand](#rand): function native of PHP to randomize numbers
* [randomizador](#randomizador): function for randomize strings or keys in array
* [sleep](#sleep): function async/await for sleeping your application for some time

***

### CURL

```js
const { curl } = require("one-utils")

const _ = async function(){

    let first_req = await curl({
        url: '', // url of site
        method: '', // method of request: GET, PUT, POST, OPTION
        headers: {
            '':''
        },
        proxy: '', // if use proxy, `http://${username}:${password}@${url}:${port}` or `http://${url}:${port}`
        body: '' // if use method POST
    })

    console.log(first_req) // print the result of the request on the console

}()
```

### GerarCpf

```js
const { gerarCpf } = require("one-utils")
// generate cpf without punctuation
let cpf = gerarCpf()
// generate cpf with punctuation
let cpf_with_punctuation = gerarCpf(true)
// print on the console
console.log(cpf, cpf_with_punctuation)
```

### GetStr

```js
const { GetStr } = require("one-utils")

let string = 'hello world, one-utils'

let capture = GetStr(string, ', ', '-') // print 'JohnGrimm'

console.log(string, capture)
```

### INCLUDE

code js: test.js
```js
const { gerarCpf } = require("one-utils")
// generate cpf without punctuation
let cpf = gerarCpf()
// generate cpf with punctuation
let cpf_with_punctuation = gerarCpf(true)

```

code js: index.js
```js
const { include } = require("one-utils")

include('test.js') // here's including all the code from the test.js file

console.log(cpf, cpf_with_punctuation)
```

### PROXY

```js
const { proxy } = require("one-utils")

const _ = async funtion(){

    let ip_proxy = 'http://127.0.0.1:80'

    let condition = await proxy(ip_proxy)

    if( condition == undefined ){
        console.log(`The Proxy: ${ip_proxy} is OFF`)
    } else if( condition.includes('ip') ){
        console.log(`The Proxy: ${ip_proxy} is ON`)
    } else {
        console.log(`The Proxy: ${ip_proxy} is OFF`)
    }

}()
```

### PROXY1

```js
const { proxy1 } = require("one-utils")

const _ = async funtion(){

    let ip_proxy = 'http://127.0.0.1:80'

    let condition = await proxy1(ip_proxy)

    if( condition == undefined ){
        console.log(`The Proxy: ${ip_proxy} is OFF`)
    } else if( condition.includes('google') ){
        console.log(`The Proxy: ${ip_proxy} is ON`)
    } else {
        console.log(`The Proxy: ${ip_proxy} is OFF`)
    }

}()
```

### RAND

```js
const { rand } = require("one-utils")

let number = rand(0, 999) // print number between 0 - 999

console.log(number)
```

### RANDOMIZADOR

```js
const { randomizador } = require("one-utils")

let keys = ['John', 'Grimm', 'Utils', 'Module']

let randomize = randomizador(keys) // print a random key from the array

console.log(randomize)
```

### SLEEP

```js
const { sleep } = require("one-utils")

const _ = async function() {
    console.log(1)
    await sleep(1000) // declared time in ms
    console.log(2)
}()
```
## Author

👤 **JohnGrimm**

* Github: [@One7](https://github.com/zardx7)
* Telegram: [@One7](https://t.me/y0rkzin)
* Discord: one7 !#8667

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2020 [One7](https://github.com/zardx7).<br />
This project is [MIT](LICENSE) licensed.
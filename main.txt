//alert()
console.log("hello".length);
console.log("hello".charAt(0));
console.log("hello, world".replace("hello","goodbye"));
console.log("hello, world".toUpperCase());

const Pi = 3.14; //局部声明常量

//if else 语句
var name1 = "DasAuto"; //声明变量
if (name1 = "Simon") {
    console.log("Simon");
} else if (name1 = "Jefferson") {
    console.log("Not Simon");
} else {
    console.log("Stranger");
}

// for 循环语句
var age = 20;
for (let i = 0; i < 5; i++) { //迭代量的初始化 -> 走到最后的时候走i++ -> 直到不满足i < 5 才退出循环
    age++;
    console.log(age);
}

// do while 循环语句
var a = 19;
do {
    a++;
    console.log(a);
} while (age == a);

//三元操作符
var age = 17
var allowed = (age >= 18) ? "Yes" : "No"; //age >= 18条件满足Yes 不满足No
console.log(allowed);

//switch语句中switch检查name是否等于case引入具体实例
var name1 = "Simon";
switch(name1) {
    case 'Simon':
        console.log("Simon");
        break; //跳出switch循环的作用
    case 'John':
        console.log("John");
        break;
    default:
        console.log("Stranger");
}

//代码块
if (true) {
    let age = 20 ////let局部声明变量，作用域(变量访问的范围)限定在if语句里面
}

//对象obj
var obj = new Array();
var obj2 = {};

obj = {
    name1: "Jefferson",
    age: "27",
    email: "1224817019@qq.com",
    contact: {
        phone: "18012877790",
        Telegram: "@Jefferson",
    }
};

obj.age = "21"; //修改值
obj.contact.WeChat = "tisenyichen"; //加新的变量

console.log(obj.contact.Telegram); //第1种打印方式：点操作符|链式表达
console.log(obj["contact"]["phone"]); //第2种打印方式
 
//数组array
var a = new Array();
var b = [];

a[0] = "dog";
a[1] = "cat";
a[5] = "tiger";

console.log(a);

for (let i in a) {
    console.log(a[i]);
}

b = ["dog","cat","tiger"]

b.shift() //删除
b.pop();

b.unshift() //追加
b.push("sheep");

console.log(b);

for (let i = 0; i < b.length; i++) {
    console.log(b[i]);
}

//函数
let a = 1;

function add(x){
    a += x;
}

add(4);
console.log(a);


function add1() { //声明add方法
    let sum = 0;

    for (let i = 0, j = arguments.length; i < j; i++) {
        sum += arguments[i];
    } //i目的是遍历j

    return sum;
}

let sum = add1(1, 2, 3);

console.log(sum);

//回调函数
//闭包
function makeAdder(c) {
    return function(b){ // B只能在另外一个地方传入参数
        return c + b;
    }
}

var x = makeAdder(5);
var sum = x(6);

console.log(sum);
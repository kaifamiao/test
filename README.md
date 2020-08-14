# test
# test
# test
# nodejs异步变同步的几种方式
async库，es6的promise-then，es7的await-async

##1. nodejs的async库，有好多种方法支持异步变同步的，常用的有:
async.each(): for循环中牵涉到异步变同步，经常使用。
async.waterfull(): 同步执行，function之间有数据交互，上一个function的输出，可作为下一个function的输入。
async.series(): 同步执行，function之间无交互。

##2. promise-then和await-async
两个等同的方法，await-async使用起来更加简单优雅，async方法同步return相当于新建了一个Promise 返回出去了，await相当于.then()

async = return new Promise, await = then 

// return promise, 必须用.then或者await接收
function promiseDemo () {
	return new Promise((resolve) => {
	resolve(2);
})
}
 
// then方式
function testPromiseDemo1 () {
	promiseDemo().then((data) => {
		console.log(data);
	})
}
testPromiseDemo1();
 ----
// await方式
async function testPromiseDemo2 () {
	var val = await promiseDemo();
	console.log(val);
	return val;
}
testPromiseDemo2();  // 内部打印2
testPromiseDemo2().then((data) => {
	console.log(data);  // 打印返回值2
})
 
 
 ---
// 相当于return new Promise((resolve) => {resolve(1)})
async  function asyncDemo() {
	return 1;
}
 
// then方式接收，或者也可以用await接收
asyncDemo().then((data) => {
	console.log(data);  
})



# command


> echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/kaifamiao/test.git
git push -u origin master
                # test
# test
# test
# test
# test
# test
# test
# test

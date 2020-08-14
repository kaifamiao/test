#继续深入理解Node.js的回调机制（三个函数相互调用关系）
我们在js里普通函数的执行顺序如下：
![](media/15865420998083/15865421738932.jpg)
定义了三个函数，myFirstFun()的返回值，赋值给mySecondFun()，myLastFun()函数，调用了mySecondFun()构成了一个相互传递的过程
即:
A-->B-->C,C输出。这是一种顺序，逻辑关系。
那么在Node.js里就完全不一样了，因为是异步的关系，所以写起来就非常麻烦。
不过Node.js提供了一个async框架，可以完全解决这个问题。
![](media/15865420998083/15865424706227.jpg)



# command


> echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/kaifamiao/test.git
git push -u origin master
                
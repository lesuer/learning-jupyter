### Node.js异步线程
****
Node.js内置了创建线程和让它们异步触发的机制。 使用http://book.mixu.net/node/ch7.html中的示例，我们有以下内容：


```
//thread function - invoked for every number in items array function async(arg, callback) {

console.log('cube ''+arg+'', and return 2 seconds later'); setTimeout(function() { callback(arg * 3); }, 2000);

}

//function called once - after all threads complete function final() { console.log('Done', results); }
 

[ 116 ]

 
Jupyter JavaScript Coding

//list of numbers to operate upon

var items = [ 0, 1, 1, 2, 3, 5, 7, 11 ]; //results of each step

var results = [];

//loop the drives the whole process items.forEach(function(item) {

async(item, function(result){ results.push(result); if(results.length == items.length) {
final();

}

})

});

```
该脚本创建一个在数字上运行的异步函数。 对于每个数字（item），我们调用内联函数将数字传递给将数字应用于结果列表的函数。 在这种情况下，它只是三倍的数量，等待两秒钟。 主循环（在脚本的底部）为列表中的每个数字创建一个线程，然后在调用final（）例程之前等待它们全部完成。

笔记本页面如下所示：

![](/assets/去.jpg)

当我们运行这个脚本时，我们得到了这样的输出：

![](/assets/我.jpg)


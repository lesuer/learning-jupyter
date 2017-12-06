### 火花素数

我们可以通过一个过滤器来运行一系列数字，以确定每个数字是否为素数。 我们可以使用这个脚本：


```
import pyspark

if not 'sc' in globals():

sc = pyspark.SparkContext() def is_it_prime(number):

#	make sure n is a positive integer number = abs(int(number))

#	simple tests

if number < 2: return False

#	2 is prime if number == 2:
return True

#	other even numbers aren't if not number & 1:

return False

#	check whether number is divisible into it's square root for x in range(3, int(number**0.5)+1, 2):

if number % x == 0: return False

#if we get this far we are good return True

#	create a set of numbers to 100,000

numbers = sc.parallelize(xrange(100000))

# count out the number of primes we found print numbers.filter(is_it_prime).count()


```
该脚本生成的数字高达100,000。

然后，我们遍历每个数字，并将其传递给我们的过滤器。 如果过滤器返回true，我们会得到一个记录。 然后，我们只计算我们找到了多少结果。
 














[207]

 
Jupyter和大数据

在Jupyter中运行它，我们看到以下内容：

![](/assets/你=了.jpg)

这非常快 我在等，没有注意到它发生得这么快。
 















[208]
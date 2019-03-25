---
layout: post
title:  "Extra Long Factorial"
date:   2019-03-25
category: problems
---

Hackerrank Question Link : 

Complete the extraLongFactorials function in the editor below. It should print the result and return.

extraLongFactorials has the following parameter(s):

n: an integer

Note: Factorials of n > 20 can't be stored even in a 64 bit long long variable. Big integers must be used for such calculations. Languages like Java, Python, Ruby etc. can handle big integers, but we need to write additional code in C/C++ to handle huge values.

We recommend solving this challenge using BigIntegers. 


### Credits : Hackerank 

Here we will be solving using Python , Java , C , GO . 

BigIntegers are available in Python , Java , Go . But Not C . So I searched a lot of blogs regarding this questions of handling large integers in C . 

### Python :
```python
def fact(num):
	if(num == 1):
		return 1
	return (num * fact(num-1))

number = int(input())
print (fact(number))
```

### JAVA :
```java
import java.util.*;
import java.math.BigInteger;

public class ExtraLongFactorials{
	
	
	public static void main(String [] args){
		int num;
		Scanner sc = new Scanner(System.in);
		num = sc.nextInt();
		BigInteger ans = BigInteger.ONE;
		while(num>0){
			ans = ans.multiply(BigInteger.valueOf(num));
			num--;
		}
		System.out.println(ans);
	}
}
```

### Go 
```go
package main 

import ("fmt"
		"math/big")

func main(){
	var num int
	var limit int 
	ans:= big.NewInt(1)
	fmt.Scanf("%d",&num)
	limit = num 
	for i:=0;i<limit;i++{
		ans = ans.Mul(big.NewInt(int64(num)) , ans )
		num--;
	}
	fmt.Println(ans)
}
```

for C refer here : https://discuss.codechef.com/questions/7349/computing-factorials-of-a-huge-number-in-cc-a-tutorial



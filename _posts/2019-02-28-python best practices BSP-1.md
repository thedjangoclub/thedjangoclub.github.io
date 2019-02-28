---
layout: post
title:  "Python Best Practices"
date:   2019-02-28
category: opentech
---

## Best Practices 

### Why best practice ?
Any programmer can write a code to solve a problem . But it's okay to follow their own style when their projects are not 
involving any collaboration . Sometime it feels difficult to add a new update to the code . which may lay a path to not turning to the 
project again . We need to follow some rules (only some) to create a good working project . Best Practices will make a uniform standard
to write the code . Which will attract the other developers to collaborate into your project . 

### What is python's Best Practice ?
PEP - Python Enhancement Proposal is set of rules for python best practices . [PEP official Link][pep-link]
Here i include some things that i follow during developing an project . These will all be to the point and not in detail . 
<b>These are simple but deep .</b>

<h4> Here's is a question for you ? </h4>

In your life time of coding , have you read most ? or written most ? . Answer will be discussed at the end .   

1. First Thing First , Ensure that your variables are readble . Avoid using single letter variables like x , y , i , j .

{% highlight python %}
# not recommended
a = input('Enter your age')
# recommended
age = input('Enter your age')
{% endhighlight %}

all variables must be readable . Else you will be confused with it later not sooner . 

2. Class Names should be in Pascal Case . Function and Variables should be small letter words connected by " _ " .
{% highlight python %}
# not recommended
# Class Name
class foo:

# Function Name 
def GetAbsoluteUrl():
  return 

# Variable Name 
isActive = true 

# recommended
# Class Name 
class Foo:

# Function Name
def get_absolute_url():
  return 

# Variable Name 
is_active = true 
age = input('Enter your age')
{% endhighlight %}

3. Dont Hard Code (Substituting values in place of variables). Consider you are creating an application to send mail . Inorder to send the mail we should not write the password on the code .
Instead we should use some env variables (environment variables) to get the required password . 
In python , we have [python-dotenv][pdotenv] . Follow this link , its really good .

4. While you are writing the code , have in mind that you're gonna update it very soon . So write based on that . 

5. DRY - Dont Repeat Yourself . Reusability is the key to be lazy and clever . Write functions for those things that you will be needed to repeat it again and again . It makes code lesser and easy modification . But be sure that over breaking down will lead to more work . 

6. Comment your code . Just do it . It should include why the snippet is needed and what it does . But dont do comment when the code itself explaining good . 

{% highlight python %}

# Not Recommended
import random 
num_list = range(10)
# Shuffle the list 
random.shuffle(numlist)

# Recommended 
import random 
num_list = range(10)
random.shuffle(numlist)

{% endhighlight %}

7. Do one thing and Do best . Your function or module should be very specific to the point . 
Login module should be specific to login functionality and should not deal with creating a user model . 

8. Use some version control system like git , mercurial . So that you can track back the 
foot prints . For sure , some error will occur during development . the newly updated code will take attack you like Thanos . During those times we can just time travel like Doctor Strange the code to make it work .

9. Share the code with other devs , dedicated telegram groups and ask them to use it . They actually kill it , mock it , no respect will be given (Sometimes) . Don't bother , just try to improve your code . 

10. Like sharing ; read other's too . They might have an different approach , learn from it . 

11. Use Virtual Environments . I will put another blog on this . 

Blogs you might refer :

| Name          | Link          | 
| ------------- |:-------------:| 
| Real Python   | [How to Write Beautiful Python Code With PEP 8][pep-8] | 
| Python.org    | [PEP-8 Doc][pep-link]      | 
| Topal | [Python Best Practices and Tips by Toptal Developers][topal-link]      | 


[total-link] : https://www.toptal.com/python/tips-and-practices
[pep-8]: https://realpython.com/python-pep8/
[pep-link] : https://www.python.org/dev/peps/pep-0008/
[pdotenv] : https://github.com/theskumar/python-dotenv

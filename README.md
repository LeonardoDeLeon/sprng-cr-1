# sprng-cr-1

## Spring Core w/o Spring

1. What is tightly coupled?
2. What is loosely coupled?
3. What is code to interface?
4. What is Spring Core?
5. What is Spring Framework?

### What is tightly coupled?

Given two classes Alpha and Beta below:

```
class Alpha {
	void show(){}
}
```
&

```
class Beta {
	void disp(){}
}
```

How can method in Beta be used in Alpha?  What are the ways?

By 

Composition
: create an object of Beta in Alpha, then call the method

```
class Alpha 
{
	void show()
	{
		System.out.println(new Beta().disp());
	}
	
}
``` 
 
Or by

Inheritance
: Alpha extends Beta

```
class Alpha extends Beta 
{
	void show()
	{
		System.out.println(disp());
	}
}

``` 

In either way, if Beta class has a problem, then Alpha class is also affected.  In the above example, Alpha is tightly coupled with Beta.

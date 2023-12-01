
# Introduction of ASP.net & C#

### Asp.net Page Life cycle 

![ASP.Net Page Life cycle](https://drive.google.com/uc?export=view&id=1cMGoj0hqphDdMwvjTVQV8FmJpjQE0Rfu)

### ASP.Net Application Life Cycle 

![MVC 2 Life Cycle ](https://drive.google.com/uc?export=view&id=1ePzaIRej4lVJVixqrGGulGSlSKnNxgbu)

- Applicaiton Start => When user request to server start.cs
- Object Creatation  => HttpContext, HttpRequest (user cookies, sesion, browser info), HttpReponse (send to client) this type of object are created 
- HttpApplication Creation => two application News and Card order each application work respectively 
- Dispose => clear the unused resocers 
- Application End =>  applicaiton finaly uloaded from the memory 


### MVC Life Cycle 

![MVC Life Cycle ](https://drive.google.com/uc?export=view&id=1140etNMDvQusPt6mSUohbBlywsWa1yEp)

![MVC 2 Life Cycle ](https://drive.google.com/uc?export=view&id=1bZCpZDTSS9YLP1zZQih1PTyBYJEytuMg)

- First request come from web browser 
- Router Router Receive the request
- Initialize the cotroler 
- TempData
- Action 
- Respnse view or Return Result 

## IS VS AS

- **Key Point**
- IS str1 variable type of String (two of the variable same type or not)
```C#
    object str1 = "Mehedi";

    if(str1 is string)
    {
        Console.WriteLine("This is string type variable");
    }

```

- Can We convert str1 string AS a Object (Type cast one type to another type or not )

```C#

    object str1 = "Mehedi";

    string x = str1 as string ;
```


## ref vs out 

- ref and out are way to pass reference of variable to a Function 
- In case **ref** argument pass inside function accept arg value as conideration 
```C#
    void passAsRef(ref int a)
    {
        a = a + 10;  
    }

    public static void Main(string[] args)
    {
        int a = 10;
        passAsRef(ref a);
        
        Console.log(a); // output: 20
    }
```
- In case **out** argument value not coder That's why we have to local initialization is import to variable 
```C#
    void passAsRef(out int a)
    {   a = 5;   // local value take  not argument value 
        a = a + 10;  
    }

    public static void Main(string[] args)
    {
        int a = 10;
        passAsRef(out a);
        
        Console.log(a); // output: 15
    }
```
## Boxing - Unboxing 

- Boxing value type to Reference type (Stact to Heep memory )
- Unboxing Reference type to Value type (Heep to Stact memory)

```C#
int i = 0;

object obj = (object) i; // i is boxed here
obj = ((int) i) + 3; // changing i on the heap
i += 1; // changing i on the stack

```


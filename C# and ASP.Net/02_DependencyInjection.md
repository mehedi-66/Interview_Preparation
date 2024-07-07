

https://www.youtube.com/watch?v=yVKTvtevM0w

1. What is need of DI?

        DI is a desing methodology where in rather than caller creating the instance its injected by some framework or some other mechanism. 

        HomeController( DBContext db)
        {
            // NOT
            DBContext obj = new DBContext();
        }

        In startup.cs

        service.AddSingleton< DBContext, SQLSserver >();
        
        infutre OracalServer use this DBContext object
        
        this will inject int whereever call to service


2. Explain IOC (Inversion of control)?

        Inversion of Controll is a principle whre we say focus on your work and other tasks delegate to someone else

        HomeController() has show UI and login somthing his taks not to create Instances like DBContext


3. What the benefit of DI?

        DI helps to implement decoupled architecture where you change at one place and changes are reflected at many places

4. Scoped VS Transient VS Singleton ?

        Scoped, Transient, or Singleton define the life time of the Depenecency injected object.

        --------------------
        1. Singleton

        Throught the server one object is create.

        For All User and all requeste

        Singleton: Only one instance of object is created for the whole web application.

        2. Scoped:
            two point rem
        # For every request new instance will be injected

        # With In same request if we DI multiple time same instance will be injected.

        HomeController(DBContext obj1, DBContext obj2, DBContext obj3)

        ob1, ob2, ob3 same instance will be injected to all of them


        3. Transient: 

            two point rem

        # For every request new instance will be injected.

        # With in same request if we DI multiple times different instance will be injected.

        HomeController(DBContext obj1, DBContext obj2, DBContext obj3)

        ob1, ob2, ob3 DIFFERNT instance will be injected to all of them



5. When should we use What?

    Singleton: 
    - One Instance will be created and it will share whole application 
    - like HitCount, ShareServices, Cache.

    Scoped: 
    - Most of the time it used;
    - In same request One instance will be created and All DI point it as References
    - Repository for same tranaction, Businsee objects, Used most of the time
    - Like DBContext object Same connection do commit, Rollback


    Transient:

    - In constructor we use two variable that means we want new new copy of obj1, obj2
    - Suppose different transcation we commit diffrent way to commit

    obj1.Add("Some value");
    obj1.commit();

    obj2.Add("Some Other value");
    obj2.commit();

    - Instance should not affect each other like different transcation, Thread saftry as objects are diffeernt instances, same object asked multipule time in constructior 



# Proxy Pattern

## What is a Proxy
Proxy is a structural design pattern that lets you provide a substitute or placeholder for another object. A proxy controls access to the original object, allowing you to perform something either before or after the request gets through to the original object.

### It works as an intermediate between the user and the internet, Prociding the following:

- Firewall
- Filtering
- Caching
- Protection
- Privacy
- Security

# The Problem
## Why would you want to control access to an object?
Here is an example: you have a massive object that consumes a vast amount of system resources. You need it from time to time, but not always.

You could implement lazy initialization: create this object only when it’s actually needed. All of the object’s clients would need to execute some deferred initialization code. Unfortunately, this would probably cause a lot of code duplication.

![image](https://github.com/Husam-AbuZina/Learning-OOP-and-Design-Patterns/assets/109718076/9328a7db-37a4-4e11-ade2-4ce295eb9373)

# The Solution
The Proxy pattern suggests that you create a new proxy class with the same interface as an original service object. Then you update your app so that it passes the proxy object to all of the original object’s clients. Upon receiving a request from a client, the proxy creates a real service object and delegates all the work to it.

![image](https://github.com/Husam-AbuZina/Learning-OOP-and-Design-Patterns/assets/109718076/804be929-c546-4c10-b115-cc28e1196238)

But what’s the benefit? If you need to execute something either before or after the primary logic of the class, the proxy lets you do this without changing that class. Since the proxy implements the same interface as the original class, it can be passed to any client that expects a real service object.

# Real-World Analogy

![image](https://github.com/Husam-AbuZina/Learning-OOP-and-Design-Patterns/assets/109718076/a857b90b-1569-4403-8bba-b27a002c571d)

A credit card is a proxy for a bank account, which is a proxy for a bundle of cash. Both implement the same interface: they can be used for making a payment. A consumer feels great because there’s no need to carry loads of cash around. A shop owner is also happy since the income from a transaction gets added electronically to the shop’s bank account without the risk of losing the deposit or getting robbed on the way to the bank.


## Applicability

1. Lazy initialization (virtual proxy). This is when you have a heavyweight service object that wastes system resources by being always up, even though you only need it from time to time.

Instead of creating the object when the app launches, you can delay the object’s initialization to a time when it’s really needed.

2.  Access control (protection proxy). This is when you want only specific clients to be able to use the service object; for instance, when your objects are crucial parts of an operating system and clients are various launched applications (including malicious ones).

 The proxy can pass the request to the service object only if the client’s credentials match some criteria.

 3. Local execution of a remote service (remote proxy). This is when the service object is located on a remote server.

 In this case, the proxy passes the client request over the network, handling all of the nasty details of working with the network.

 4.  Logging requests (logging proxy). This is when you want to keep a history of requests to the service object.

 The proxy can log each request before passing it to the service.

 5.  Caching request results (caching proxy). This is when you need to cache results of client requests and manage the life cycle of this cache, especially if results are quite large.

 The proxy can implement caching for recurring requests that always yield the same results. The proxy may use the parameters of requests as the cache keys.

 5.  Smart reference. This is when you need to be able to dismiss a heavyweight object once there are no clients that use it.

 The proxy can keep track of clients that obtained a reference to the service object or its results. From time to time, the proxy may go over the clients and check whether they are still active. If the client list gets empty, the proxy might dismiss the service object and free the underlying system resources.

The proxy can also track whether the client had modified the service object. Then the unchanged objects may be reused by other clients.

### Notes: 📝
- This Article is Quoted from refactoring.guru, But i try to summarize it as much as posssible for fellow GitHub Friends.
- You Can Find the Original Article On: [refactoring.guru.proxy](https://refactoring.guru/design-patterns/proxy)

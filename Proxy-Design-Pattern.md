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

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

## Why would you want to control access to an object?
Here is an example: you have a massive object that consumes a vast amount of system resources. You need it from time to time, but not always.

You could implement lazy initialization: create this object only when it’s actually needed. All of the object’s clients would need to execute some deferred initialization code. Unfortunately, this would probably cause a lot of code duplication.

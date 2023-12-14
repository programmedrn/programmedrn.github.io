---
title: Exception Handling Rules
categories: 
    - exception
    - rule
    - tip
excerpt: |
    When and how to handle exceptions
feature_text: |
    ## Exception Handling Rules
     When and how to handle exceptions
feature_image: "/FirstBlog/assets/insertedImg/2023-12-12-java-interface-vs-abstractClass/basic_codes.png"
# aside: true
# heads: true
---

## Goal

To get an advice for exception handling.

## Rules

1. Clean Up resources using Finally Block or Try-With-Resources
    
    Don’t forget to clean used resources up.
    
2. Prefer Specific Exceptions
    
    Don’t handle exceptions in ambiguous way.
    
3. Document the Exception You Specify
    
    Add `@throws` in you javadoc.
    
4. Throw Exceptions With Descriptive Messages
    
    Specify the reason the exception happened.
    
5. Catch the Most Specific Exception First
    
    Don’t catch its super class exception before.
    
6. Don’t Catch Throwable
    
    Of course you can catch some throwables too, but don’t.
    
7. Don’t Ignore Exceptions
    
    That exception might not that important or not like to happen for now, but you never know.
    
8. Don’t Log and Throw
    
    If you were gonna re-throw it forward it to handle it later, why would you log it?
    
9. Wrap the Exception Without Consuming It
    
    Stack your exceptions, even when making new one.

## References
- [9 Best Practices to Handle Java Exceptions](https://stackify.com/best-practices-exceptions-java/ "https://stackify.com/best-practices-exceptions-java/")
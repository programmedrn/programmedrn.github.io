---
title: "[Java] interface vs abstractClass"
categories:
- java
- think
- interface
- abstractClass
excerpt: |
  During developing on Java, I have needed to choose which to use interface or abstractClass. So I researched a little.
feature_text: |
  ## [Java] interface vs abstractClass
  During developing on Java, I have needed to choose which to use interface or abstractClass. So I searched a little.
feature_image: "/FirstBlog/assets/insertedImg/2023-12-12-java-interface-vs-abstractClass/basic_codes.png"
# image: "/FirstBlog/assets/insertedImg/2023-12-07-GitHub-issue-closing/githubImage.png"
# aside: true
# heads: true
---
## Goal

To get an advice for choosing between interface with default methods and abstractClass

### The thing is

As I'm using default methods in interfaces, they seems not to have any differences. So I became wonder, which one to use? If I change from interfaces to abstract classes, won't it be matter?

### Differences

Still, there were differences.

- interface

  - Java allows only one "extends" from class.
  - You can develop using interface, though there is not a clear hierarchy.

- abstractClass

  - You can use the states of the object, Field variables.

### Dicision

As I didn't want to occupy the only chance for extending, and there were not clear hierarchies, I decided to use interfaces. Now, the problem is accessing to the state. In interface, there were no way to force a object to holds certain states. I can try forcing some getter methods but its purpose may look vague for the other developers. I think this happened because I referenced many python codes, where multi inheritance is available. And I also found saying there is a way to serve both interface and abstractClass for user's convenience, but for now, I think that's too much.

## References

- [Basic Facts about both](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue/ "https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue/")
- [Case by case for interface and abstractClass](https://www.myanglog.com/Java%20interface%20vs%20abstract%20class%20-%20%EC%96%B8%EC%A0%9C%20%EB%AC%B4%EC%97%87%EC%9D%84%20%EC%93%B8%EA%B9%8C "https://www.myanglog.com/Java%20interface%20vs%20abstract%20class%20-%20%EC%96%B8%EC%A0%9C%20%EB%AC%B4%EC%97%87%EC%9D%84%20%EC%93%B8%EA%B9%8C/")
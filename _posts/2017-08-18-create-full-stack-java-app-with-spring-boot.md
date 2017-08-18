---
layout: post
category : Spring Boot
tagline: ""
tags : [java, spring-boot, java-full-stack, design-question]
---
{% include JB/setup %}

## What is Spring Boot
Spring Boot is just an another library to consume. It makes easier to setup, configure, build and ship to developers. Since Spring Framework has become a de-facto framework for all Java Technology projects, Spring Boot has made it lot easier to start off with a project.

### Creating a Spring Boot Project

You may use your IDE to create new project or just use [Spring Initilizer](http://start.spring.io/) for creating the archetype of the project. And add dependecies (I have added Web, Thymleaf and H2 that would be enough to start off.)

![Spring Initilizer]({{ site.baseurl }}/images/si.PNG "Spring Initilizer")

This will download you a zip file of the project archetype which you can simply `import as a Maven Project` in your IDE.

You can run the application by `run as Spring Boot App`, and It will run the application on your `localhost:8080`. You can change the port by adding `server.port=xxxx` in `application.properties` if port 8080 is already in use.

### Adding views
#### Add `index.html` under `src/resources/templates`.
```html
<!DOCTYPE html>
<html>
<head>
<title>Ordinary Title</title>
</head>
<body>
<h3>Hey this is your view.</h3>
</body>
</html>
```
Add controller with `RequestMapping` to the view. eg. Add TestController.java with following content.

```java
@Controller
public class TestController {
	
	@GetMapping("/myurl")
	public String myurl() {
		return "index";
	}
}
```

Now go to the newly created url to see your view. `localhost:8080/myurl`.
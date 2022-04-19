---
layout: post
title: Log all endpoints
categories: [Java,Spring,Spring Boot]
excerpt: Log all endpoints in Spring Boot
snippet: true
date: 2022.02.11
---

The following class logs all endpoints including the path and the corresponding controller class. This is mainly for debugging purpose.

```java
class EndpointListener{
    @EventListener
    public void handleContextRefresh(ContextRefreshedEvent event) {
        ApplicationContext applicationContext = event.getApplicationContext();
        RequestMappingHandlerMapping requestMappingHandlerMapping = applicationContext
        .getBean("requestMappingHandlerMapping", RequestMappingHandlerMapping.class);
        Map<RequestMappingInfo, HandlerMethod> map = requestMappingHandlerMapping
        .getHandlerMethods();
        map.forEach((key, value) -> LOGGER.info("{} {}", key, value));
    }
}
```

Source and more info [here](https://www.baeldung.com/spring-boot-get-all-endpoints)
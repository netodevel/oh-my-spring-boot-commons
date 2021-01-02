# oh-my-spring-boot-commons
several common things I use on a daily basis with spring boot :)

### Goal

keep all things in common in a single project to avoid duplication of code.
Of course, only things like: Utility Class, Tests Setups

### Current Itens

* StringKit
* SocketKit
* Embedded Redis

### Documentation

#### Utility classes

* String kit

```java
    StringKit.isBlank(value);
    StringKit.isNotBlank(value);
    StringKit.isBlankThen(value, (e) -> {
                throw new IllegalArgumentException("can not be blank");
            });
    StringKit.isNumber(value);
    StringKit.toCapitalize(value);
```

* SocketKit

```java
    SocketKit.isPortAlreadyUsed(6379);
```

* FileKit

```java
    FileKit.inputStreamToString(inputStream);
    FileKit.inputStreamToString(inputStream, "\n");
```

#### Embedded Servers For Integration Tests

Goal: Run services with Auto Configuration of Spring Boot to run integrated tests.

* Embedded Redis
    
  `just add dependecy`
  
  * props
  
  `embedded.redis.port=6379`
  
  `embedded.redis.active=true`
  

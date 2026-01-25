When a prototype bean is injected into a singleton bean, it loses its prototype behavior and acts as a singleton.
```java
@Scope(value=ConfigurableBeanFactory.SCOPE_PROTOTYPE, proxyMode=ScopedProxyMode.TARGET_CLASS)
```
Another is @lookup

# It's SPRING!

## Constructor or bean-init or @PostConstruct?

Order of calling:
1. Constructor
2. Inject the dependencies or bean-init also?
3. @PostConstruct

So essentially if you are using some mumbo jumbo logic inside the constructor which requires dependencies to be
initialized, you will get an NPE because they haven't been initialized yet

### Also Interestingly!
If the bean scope is 'request', that is for an HTTP request, if the application is web aware, the @PostConstruct 
method will get called with every new request

[https://www.baeldung.com/running-setup-logic-on-startup-in-spring](Nice blog about bean initializations)

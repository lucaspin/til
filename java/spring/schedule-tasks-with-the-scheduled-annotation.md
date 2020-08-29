Spring provides a `@Scheduled` annotation which can be placed in a method (void with no arguments) to run it as a scheduled task. To enable it on the app, you need to annotate any of your beans with `@EnableScheduling`.

You can use __delays__, __rates__ and __cron expressions__ to schedule your tasks - [Check the docs here](https://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/scheduling/annotation/Scheduled.html).

A few things to be aware when using it:
- By default, Spring uses only 1 thread for the scheduler responsible to run all the `@Scheduled` tasks. You can tweak that value with the `spring.task.scheduling.pool.size` property
- `@Scheduled` methods are synchronous by default, i.e., the next execution will wait for the previous one to finish
- If you want independent executions, use `@EnableAsync` (on the bean), and `@Async` (on the method). Make sure you're using the proper number of threads for that as well, with `spring.task.execution.pool.core-size` (default is 8)
- Be always aware of the scheduled methods you have, how they are triggered and how many threads you use for them. Losing track of these things may cause your methods not be run when you need them to.
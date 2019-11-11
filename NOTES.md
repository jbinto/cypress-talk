# From 12pmish today

Why cypress?
DEMO

CONFIDENCE
Unit tests weren't giving us confidence- sure it works if you call it exactly like that...- and if the behavior of that API you mocked never changes...
We test for lots of reasons. Show the 5 from Sarah Mei
Often find yourself with all unit tests passing, even 100% test coverage. Show "2 unit test 0 i tegration tests" memes
Cypress lets us upgrade big dependencies: webpack, react, material-ui and ensure things still work. 
(show dependabot PRs, green check)
It lets us entirely redesign how we structure the internals of our app (refactoring) and ensure things still work.
"Test public API" - Kent C Dodds
For a website, your user interface is public API
React team entirely rewrote internals between 15 and 16. 

EMPHASIS ON RELIABILITY, SAFETY
Modern web apps are async. This adds challenges:
- You can never know the page is "ready"- Timing conditions can mean having to retry assertions, or write manual `wait(2000) // ms`
BOLD ASSERTION: You never, ever have to write a manual `wait(ms)` call in cypress. (* fine print applies, not valid in texas)
- Cypress gives you a set tools that abstract away this complexity for you - But it means you have to play by the rules
- No messing with async yourself.  - No promises, no async/await. Color within the lines Cy gives you and you get rewarded.
- Retryability: your commands are invisibly and automatically retried 

WELL DOCUMENTED
Cypress has some of the best technical documentation I've ever read.
If you've used something like Jest, Mocha, or RSpec it will look familiar. But there is a lot to unlearn.
- Common pitfalls- Retryability- Conditional testing

IMPRESSIVE FEATURE SET
- You can stub HTTP calls- You can write arbitrary Node.js code to prepare data out of band- You can fast forward time (think: test Gmail undo feature)- You can stub out any Javascript function in your app to change its behavior

IMPRESSIVE TEST RUNNER
- Each step is logged, and a snapshot of before/after state is stored- You can interact with the live system at the point of test failures- It takes screenshots and records videos of your test run- It can be parallelized for larger test suites- It can collect code coverage metrics
LET'S LOOK AT THAT DEMO AGAIN


y
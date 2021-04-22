# Choose _being_ agile over _doing_ agile

We expect our teams to be similar but different, shaped by the context they are in but expressing the same principles

What Andy Longshaw calls "2021 style software development" 

## Principles

* Working on everything _over_ working only in my specialism
* Working together _over_ working alone
* Releasing to users often _over_ accumulating changes
* Working at a pace we can maintain _over_ working with urgency
* Checking it was valuable _over_ meeting requirements

These are in git because they should change as we learn

----

# Themes

## Closed Loop Control

Prefer _closed-loop control_. This is the difference between having a thermostat on your central heating (a closed loop exists between the boiler and the temperature in your house) and only having a time clock that turns your boiler on and off (open loop [sic]). It's the difference between actively steering your car and just pointing it in the direction of your destination and hoping for the best. It's the difference between adding a little salt to a dish and tasting it to see if it needs more, and lobbing in a handful all at once. Most industrial control systems implement closed-loop control in terms of minimizing an error, or difference, between the present situation and the set point which represent the goal.

At the finest-grained level, for us that shows up as TDD. Rather than set the Software Engineer the task of creating a perfect implementation by predicting what the code needs to end up looking like, instead we create an environment where the Software Engineer can continuously, incrementally improve the code, guided by feedback from tests and other tools. The next test that we add represents a refinement of the set point, and "test failed" is the error, and we reduce it (to "test passed") by changing our code. This is why TDD tools tend to be silent when all tests pass: that represents a zero error. Now, test passed vs test failed is only one bit of Shannon information, which is part of why we should write _small_ tests, and not overburden that one bit. 

At the largest scale, for us this shows up as "Digital" thinking: rather than set Product Managers the task of creating a perfect product or service by predicting what the market and the users will find valuable, instead we create an environment in which they can continuously, incrementally improve the value to the user, guided by feedback from the users themselves.

This way of working is much _easier_ than requiring everyone to be really, really good at prediction, and much more _effective_, and much _lower risk_. It does, however, require everyone to be comfortable with the idea that the current state of the code, service, product, whatever it is we work on, is now and always will be imperfect and unfinished. And also changing and improving all the time, but imperfect and unfinished. And everyone needs to be comfortable with the idea of planned re-work, we plan to work again on what was worked on before, and everyone needs to be comfortable with the possibility of needing to back-track, to revert or roll back a change and try something different. In that sense, this closed-loop way of working is less "efficient", it is intrinsically more wasteful than doing the right thing once. Trouble is, in almost all economically interesting cases, doing the right thing once is infeasibly difficult.

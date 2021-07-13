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

## Leadership Principles
The above principles are the seeds of our culture, but that garden must be actively cultivated by our leaders, and they should use these principles to guide their actions.

- Allow their team to self-organise.
	- Don't treat your team as your execution arm. If the team are happy with something you're not, either convince them otherwise or bite your tongue.
	- Don't direct people to work how you want them to work. Instead, convince them of the value of your idea, and let them decide what to do about it.
	- A leader must never say something like "everyone must mob". That's not leadership, that's management, and it acts to suppress the creativity of your team.
- Ensure their team understand **why** they are working in a certain way.
	- We don't want cargo culting from disengaged teams. If asked "why do you work this way", we don't want to hear "because X told us to".
- Cultivate a safe environment where people can talk about problems with the team
	- All problems are leadership problems, and a team **always** has problems. If you think your team doesn't have problems, it's because they're not telling you about them.

----

# Themes

## Systems Thinking

### Closed-loop Control

Prefer _closed-loop control_. This is the difference between having a thermostat on your central heating (a closed loop exists between the boiler and the temperature in your house) and only having a time clock that turns your boiler on and off (open loop [sic]). It's the difference between actively steering your car and just pointing it in the direction of your destination and hoping for the best. It's the difference between adding a little salt to a dish and tasting it to see if it needs more, and lobbing in a handful all at once. Most industrial control systems implement closed-loop control in terms of minimizing an error, or difference, between the present situation and the set point which represent the goal. That could be: difference between the current and target temperature, lack of tastiness, or remaining journey time to destination.

At the finest-grained level, for us that shows up as TDD. Rather than set the Software Engineer the task of creating a perfect implementation by predicting what the code needs to end up looking like, instead we create an environment where the Software Engineer can continuously, incrementally improve the code, guided by feedback from tests and other tools. The next test that we add represents a refinement of the set point, and "test failed" is the error, and we reduce it (to "test passed") by changing our code. This is why TDD tools tend to be silent when all tests pass: that represents a zero error. Now, test passed vs test failed is only one bit of Shannon information, which is part of why we should write _small_ tests, and not overburden that one bit. 

At the largest scale, for us this shows up as "Digital" thinking: rather than set Product Managers the task of creating a perfect product or service by predicting what the market and the users will find valuable, instead we create an environment in which they can continuously, incrementally improve the value to the user, guided by feedback from the users themselves.

This way of working is much _easier_ than requiring everyone to be really, really good at prediction, and much more _effective_, and much _lower risk_. It does, however, require everyone to be comfortable with the idea that the current state of the code, service, product, whatever it is we work on, is now and always will be imperfect and unfinished. And also changing and improving all the time, but imperfect and unfinished. And everyone needs to be comfortable with the idea of planned re-work, we plan to work again on what was worked on before, and everyone needs to be comfortable with the possibility of needing to back-track, to revert or roll back a change and try something different. In that sense, this closed-loop way of working is less "efficient", it is intrinsically more wasteful than doing the right thing once. Trouble is, in almost all economically interesting cases, doing the right thing once is infeasibly difficult.

### More General Systems

Closed-loop control is a specific case of Systems Thinking. The action of the closed loop is to converge on a stable equilibrium through _negative feedback_. If A and B influence each other in a loop, but in opposed directions (more A means more B, but more B means less A), then there is negative feedback. Introducing closed-loop control is a big step forward over open loops.

Another step is to consider the effect of _positive feedback_, which leads away from otherwise stable equilibria. If A and B influence each other, but in the same directions (more A means more B, more B means more A) then the system will very quickly reach a state of maximum A and B and stay there. The presence of both kinds of feedback in a system opens the possibility of regular cyclical behaviour, maybe with several intermediate states which can recur in complex patterns, through to semi-period behaviour, and then fully chaotic behaviour. A fully general system can appear to have very tightly constrained, regular behaviour, and then for no very obvious reason, suddenly change to completely different behaviour. The weather does this. Markets do this. Teams do this.

Systems are characterised by a boundary, across which matter, energy, and information flow. The system boundary is _chosen_.  Systems are extended in time and space. The parts of a system interact, and the behaviour of the whole system has more to do with those interactions than it does with the properties of the parts themselves. 

The revolutionary insight of systems thinking was that simple parts, interacting with each other in simple ways can, taken as a whole, have arbitrarily rich and complex behaviour. Because a system is distributed in space, the cause of an effect can be far away. Because a system is distributed in time, the cause of an effect can be far in the past. This makes it very hard to understand why a system does what it does, and thus very hard to make it do what we want. This is as true of the information systems we build as it is of systems which "just grow". Such as teams. Such as businesses.

Alastair Cockburn described software development as being something like an iterated game (in the "Prisoners' Dilemma" sense of a "game"), where the goal is to get to play the game again. And he described the system that builds software, the team working in a business setting, as being built out of non-linear components: people.

2021 Agile grapples with this sort of complexity head on. It does this by recognising that an approach or technique which worked at one scale, might not work at another; that worked at one time might not work later; by recognising that the teams we build and the contexts in which they work are systems, systems of the type which tend to have particularly rich behaviour. And that we therefore are unlikely to be able to manage them to a successful outcome by pretending that they are well understood and well behaved and likely to operate as designed.

Instead, 2021 Agile treats the (IT) systems we build and the (human) systems of of production which build them, as potentially chaotic, in the technical and metaphorical sense of the word.

Code's not even the right verb anymore, right? But I have to express my will to my agents for 16 hours a day. Manifest.

How can I have not just a single session of Claude Code or Codex or some of these agent harnesses? How can I have more of them? How can I do that appropriately?

The agent part is now taken for granted. Now the claw-like entities are taken for granted. And now you can have multiple of them, and now you can have instructions to them, and now you can have optimization over the instructions. But there, I mean, this is why it gets to the psychosis, is that this is infinite and everything is skill issue.

Hi listeners, welcome back to No Priors. Today I’m here with Andrej Karpathy, and we have a wide-ranging conversation for you about code agents, the future of engineering and AI research, how more people can contribute to research, what’s happening in robotics, his prediction for how agents can reach out into the real world, and education in this next age.

Welcome, Andrej.

Andrej: Thanks for doing this.

Yeah, thank you for having me.

So, it’s been a very exciting couple of months in AI.

Yeah, you could say that.

I remember walking into the office at some point and you were really locked in, and I was asking what you were up to, and you were like, “I have to code for 16 hours a day,” or code’s not even the right verb anymore, right? But I have to express my will to my agents for 16 hours a day. Manifest. Because there’s been a jump in capability. What’s happening? Tell me about your experience.

Yeah, I kind of feel like I was just in this perpetual — I still am often in this state of AI psychosis all the time. Because there was a huge unlock in what you can achieve as a person, as an individual, right? Because you were bottlenecked by your typing speed and so on.

But now with these agents, really, I would say in December is when something flipped, where I kind of went from 80/20 of writing code by myself versus delegating to agents, to like 20/80. And I don’t even think it’s 20/80 by now. I think it’s a lot more than that. I don’t think I’ve typed a line of code probably since December, basically, which is an extremely large change.

I was talking about it to, for example, my parents and so on, and I don’t think a normal person actually realizes that this happened or how dramatic it was. Literally, if you just find a random software engineer at their desk and what they’re doing, their default workflow of building software is completely different as of basically December.

So I’m just in this state of psychosis of trying to figure out what’s possible, trying to push it to the limit. How can I have not just a single session of Claude Code or Codex or some of these agent harnesses? How can I have more of them? How can I do that appropriately? And then how can I use these claws? What are these claws?

There’s a lot of new things. I want to be at the forefront of it, and I’m very antsy that I’m not at the forefront of it. And I see lots of people on Twitter doing all kinds of things, and they all sound like really good ideas, and I need to be at the forefront or I feel extremely nervous. So I guess I’m just in this psychosis of what’s possible, because it’s unexplored fundamentally.

Well, if you’re nervous, the rest of us are nervous. We have a team that we work with at Conviction, and their setup is everybody is like — none of the engineers write code by hand, and they’re all microphoned, and they just whisper to their agents all the time. It’s the strangest work setting ever. And I thought they were crazy, and now I fully accept it. I was like, “Oh, this was the way.” Like, you’re just ahead of it.

How do you think about your own capacity now to explore or to do projects? What is it limited by?

Yeah. What is it limited by? I think everything. So many things, even if they don’t work, to a large extent you feel like it’s skill issue. It’s not that the capability is not there. It’s that you just haven’t found a way to string together what’s available. Like, I didn’t give good enough instructions in the AGENTS.md file or whatever it may be. I don’t have a nice enough memory tool that I put in there or something like that.

So it all kind of feels like skill issue when it doesn’t work, to some extent. You want to see how you can parallelize them, etc. And you want to be Peter Steinberger, basically. So Peter is famous — he has a funny photo where he’s in front of a monitor with lots of Codex agents tiled on the monitor, and they all take about 20 minutes if you prompt them correctly and use high effort. So they all take about 20 minutes. They have multiple repos checked out, and so he’s just going between them and giving them work.

It’s just like you can move in much larger macro actions. It’s not just like, “Here’s a line of code, here’s a new function.” It’s like, “Here’s a new functionality,” and delegate it to agent one. “Here’s a new functionality that’s not going to interfere with the other one,” give it to agent two. Then try to review their work as best as you can, depending on how much you care about that code.

Like, what are these macro actions that I can manipulate my software repository by? Another agent is doing some research, another one is writing code, another one is coming up with a plan for some new implementation. So everything just happens in these macro actions over your repository, and you’re just trying to become really good at it and develop a muscle memory for it.

It’s extremely rewarding, number one, because it actually works. But it’s also kind of the new thing to learn. So that’s why, hence the psychosis.

Yeah, I do feel like my instinct is, whenever I am waiting for an agent to complete something, the obvious thing to do is like, well, I can do more work, right? Like, if I have access to more tokens, then I should just parallelize and add more tasks. And so that’s very stressful because if you don’t feel very bounded by your ability to spend on tokens, then you are the bottleneck in the system that is max capability.

Yeah. You’re not maximizing your subscription at least, and ideally for multiple agents. If you run out of Codex on Codex, you should switch to Claude or whatnot, I don’t know. That’s what I’ve been trying to do a little bit. And I feel nervous when I have subscription left over. That just means I haven’t maximized my token throughput.

So I actually kind of experienced this when I was a PhD student. You would feel nervous when your GPUs are not running, like you have GPU capability and you’re not maxing out the available FLOPs to you. But now it’s not about FLOPs, it’s about tokens. So what is your token throughput? And what token throughput do you command?

I would actually argue that it’s very interesting that we had at least 10 years where, in many engineering tasks, people just didn’t feel compute-bound. And the entire industry feels that now. They felt resource-bound. And now that you have this big capability jump, you’re like, “Oh, actually it’s not my ability to access the compute anymore. I’m the binding constraint.”

Yeah, it’s a skill issue, which is very empowering, because you could be getting better. So that’s why I think it’s very addictive, because there’s unlocks when you get better.

Where do you think it goes? If you think about okay, Andrej is iterating, and everybody else is too, for 16 hours a day, getting better at using coding agents — what does it look like in a year if you’ve reached mastery?

Yeah. What does mastery look like at the end of the year, or two, three years, five years, ten years, etc.?

Well, I think everyone is basically interested in going up the stack. So I would say, yeah, it’s not about a single session with your agent. Multiple agents — how do they collaborate in teams and so on? So everyone’s trying to figure out what that looks like.

And then I would say claw is also kind of an interesting direction because it really, when I say a claw, I mean this layer that kind of takes persistence to a whole new level. Like, it’s something that keeps looping. It’s not something that you are interactively in the middle of. It kind of has its own little sandbox, its own little setup. It kind of does stuff on your behalf even if you’re not looking. And then it also has maybe more sophisticated memory systems, etc., that are not yet implemented in agents.

So OpenClaw has a lot more sophisticated memory, I would say, than what you would get by default, which is just a memory compaction when your context runs out.

Do you think that’s the piece that resonated for more users versus perhaps broader tool access for OpenClaw?

Yeah. I think there are at least — there are a lot of really good ideas in there. Good job, Peter.

I mean, Peter has done a really amazing job. I saw him recently and I talked to him about it, and he’s very humble about it, but I think he innovated simultaneously in like five different ways and put it all together.

So for example, the soul and demeanor document — he actually really crafted a personality that is kind of compelling and interesting, and I feel like a lot of the current agents don’t get this correctly. I actually think Claude has a pretty good personality. It feels like a teammate and it’s excited with you, etc.

I would say, for example, Codex is a lot more dry, which is kind of interesting because in ChatGPT, ChatGPT is a lot more upbeat and highly sycophantic. But I would say Codex, the coding agent, is very dry. It doesn’t seem to care about what you’re creating. It’s kind of like, “Oh, I implemented it.” It’s like, okay, but do you understand what we’re building? It doesn’t.

It’s true.

The other thing I would say is, for example, with Claude, I think they dialed the psychopathy fairly well, where when Claude gives me praise, I do feel like I slightly deserve it, because sometimes I kind of give it not very well-formed thoughts. I give it an idea that I don’t think is fully baked, and it doesn’t actually react very strongly. It’s like, “Oh yeah, we can implement that.”

But when it’s a really good idea by my own account, it does seem to reward it a bit more. So I kind of feel like I’m trying to earn its praise, which is really weird. And so I do think the personality matters a lot, and I think a lot of the other tools maybe don’t appreciate this as much. In this aspect also, Peter really cares about this, and so that was correct.

And then the memory system, and then he’s just having fun with this, and then the single WhatsApp portal to all of the automation.

Yeah. Is there something that you have done personally with your claws beyond software engineering that you think is fun or interesting?

Yeah. So in January I had a claw — I went through a period of claw psychosis. So I built — I have a claw basically that takes care of my home, and I call him Dobby, the elf claw.

Basically, I used the agents to find all of the smart home subsystems of my home on the local area network, which I was kind of surprised worked out of the box. Like I just told it that I think I have Sonos at home. “Can you try to find it?” And it goes and it did an IP scan of all the computers on the local area network, and it found the Sonos system. It turned out that there’s no password protection or anything like that. It just logged in and it’s like, “Oh yeah, you have these Sonos systems installed. Let me try to reverse engineer how it’s working.”

It does some web searches and it finds, okay, these are the API endpoints, and then it’s like, “Do you want to try it?” And I’m like, whoa, you just did that. And I’m like, “Yeah, can you try to play something in the study?” And it does, and music comes out, and I’m like, “I can’t believe I just typed in, ‘Can you find my Sonos?’ and suddenly it’s playing music.”

That’s crazy. That’s like three prompts.

Yeah. I can’t believe I just typed that and it suddenly worked. And it did the same for lights. So basically it kind of hacked in, figured out the whole thing, created APIs, created a dashboard so I could see the command center of all of my lights in the home. Then it was switching lights on and off. So I can ask it, like, “Dobby, it’s sleepy time.” And when it’s sleepy time, that just means all the lights go off, etc.

So it controls all my lights, my HVAC, my shades, the pool and spa, and also my security system. So I have a camera pointed outside of the house, and anytime someone rolls in, I have a Qwen model that looks at the videos. So first of all there’s change detection, right? And then based on change detection, it goes to Qwen and it actually tells me — it sends me a text to my WhatsApp. It shows an image from outside and says, “Hey, a FedEx truck just pulled up. You might want to check it, and maybe you got mail or something like that.”

And Dobby just texts me this. It’s really incredible. So Dobby is in charge of the house. I text with it through WhatsApp. It’s been really fun to have these macro actions that maintain my house.

I haven’t really pushed it way more beyond that, and I think people are doing a lot more crazy things with it. But for me, even just a home automation setup — I used to use like six completely different apps, and I don’t have to use these apps anymore. Dobby controls everything in natural language. It’s amazing.

So I think I haven’t even pushed the paradigm fully, but already that is so helpful and so inspiring.

Do you think that’s indicative of what people want from a user experience perspective with software? Because I don’t think it’s appreciated enough that it takes humans effort to learn new software, new UI.

Yeah, I think to some extent that’s right. It’s like working backwards from how people think an AI should be, because what people have in their mind of what an AI is is not actually what an LLM is in a raw sense. An LLM is a token generator — more tokens come out. But what they think of is this persona identity that they can tell stuff to, and it remembers it, and it’s just kind of an entity behind a WhatsApp. It’s a lot more understandable.

So I think to some extent it’s matching the expectations that humans already have for what an AI should behave like, but under the hood a lot of technical details go into that, and LLMs are too raw of a primitive to actually typecheck as AI, I think, for most people.

Yeah. I think that’s how we understand what the AI is, and the description of it as Dobby or some personality obviously resonates with people. I also think the unification that you did across your six different software systems for your home automation speaks to a different question of: do people really want all the software that we have today? Because I would argue, well, you have the hardware, but you’ve now thrown away the software, or the UX layer of it. Do you think that’s what people want?

Yeah. I think there’s this sense that these apps that are in the App Store for using these smart home devices shouldn’t even exist, kind of, in a certain sense. Shouldn’t it just be APIs, and shouldn’t agents be just using it directly? And I can do all kinds of home automation stuff that any individual app will not be able to do, right? An LLM can actually drive the tools and call all the right tools and do pretty complicated things.

So in a certain sense it does point to this idea that maybe there’s an overproduction of lots of custom bespoke apps that shouldn’t exist because agents kind of crumble them up, and everything should be a lot more just exposed API endpoints, and agents are the glue of the intelligence that actually tool-calls all the parts.

Another example is my treadmill. There’s an app for my treadmill, and I wanted to keep track of how often I do my cardio. But I don’t want to log into a web UI and go through a flow, etc. All this should just be: make APIs available. This is kind of going towards the agentic web or agent-first tools and all this kind of stuff.

So I think the industry just has to reconfigure in so many ways that the customer is not the human anymore. It’s agents who are acting on behalf of humans, and this refactoring will probably be substantial in a certain sense.

One way that people sometimes push back on this is: do we expect people to vibe-code some of these tools? Do we expect normal people to do this kind of stuff that I described? But I think to some extent this is just technology as it exists today, and right now there is some vibe-coding, and I’m actually watching it and working with the system.

But I kind of feel like this kind of stuff that I just talked about should be free in a year or two or three. There’s no vibe-coding involved. This is trivial. This is table stakes. Any AI, even open-source models, should be able to do this. You should be able to translate from a less technical human’s intent very easily.

Today it’s vibe-coding, it’s involved, and not many people are going to do it. But the barrier will just come down, and it’s just ephemeral software on your behalf, and some kind of claw is handling all the details for you, but you’re not involved. Claw has a machine and it will figure it out, and it’s just presenting you UIs and you’re saying stuff.

Why haven’t you pushed the boundaries of what you can do personally with claws? Is it that you’re focusing on more important projects, auto research, etc., or you’re climbing the hill to mastery, or something else?

Yeah. I just feel like I’m so distracted by everything. So I spent like a week on the claw stuff, and I have more to do almost. But I will say that Jensen Huang was right: tools were all just busier, unfortunately.

Yeah.

I didn’t really take advantage of a lot of email and calendar and all this other stuff, and I didn’t give it access because I’m still a little suspicious and it’s still very new and rough around the edges. So I didn’t want to give it full access to my digital life yet. And part of it is just the security, privacy, and being very cautious in that realm. So some of it is held back by that, I would say. Maybe that’s the dominant feature. But some of it is also just that I feel so distracted, because I had a week of claw and then other stuff is happening.

What was the motivation behind auto research? You’ve talked about being able to train or at least optimize a model as a task you want to see agents do for a long time.

Auto research, yeah. So I had a tweet earlier where I said something along the lines of: to get the most out of the tools that have become available now, you have to remove yourself as the bottleneck. You can’t be there to prompt the next thing. You need to take yourself outside. You have to arrange things such that they’re completely autonomous.

How can you maximize your token throughput and not be in the loop? This is the goal. So I mentioned that the name of the game now is to increase your leverage. I put in very few tokens just once in a while, and a huge amount of stuff happens on my behalf.

And so auto research is an implication of that. I don’t want to be the researcher in the loop looking at results, etc. I’m holding the system back. So the question is: how do I refactor all the abstractions so that I’m not? I have to arrange it once and hit go.

The name of the game is: how can you get more agents running for longer periods of time without your involvement, doing stuff on your behalf? And auto research is just: here’s an objective, here’s a metric, here are your boundaries of what you can and cannot do — go.

You were surprised at its effectiveness.

Yeah. I didn’t expect it to work, because I have the project DataChat, and fundamentally, I think a lot of people are very confused by my obsession with training GPT-2 models and so on. But for me, training GPT models is just a little harness, a little playground for training LLMs.

Fundamentally, what I’m more interested in is this idea of recursive self-improvement, and to what extent you can actually have LLMs improving LLMs. Because I think all the frontier labs — this is the thing, for obvious reasons — and they’re all trying to recursively self-improve, roughly speaking. So for me, this is kind of like a little playpen of that.

I had tuned NanoGPT already quite a bit by hand in a good old-fashioned way that I’m used to. I’m a researcher. I’ve done this for like two decades. I have some amount of earned confidence. I’ve trained these models thousands of times. So I’ve done a bunch of experiments, hyperparameter tuning, all the things I’m very used to, and I’d gotten to a certain point, and I thought it was fairly well tuned.

And then I let auto research go overnight, and it came back with tunings that I didn’t see. It found that the weight decay on the value embeddings was wrong, and my Adam betas were not sufficiently tuned, and these things jointly interact. Once you tune one thing, the other things potentially have to change too.

I shouldn’t be the bottleneck. I shouldn’t be running these hyperparameter search optimizations. I shouldn’t be looking at the results. There are objective criteria in this case, so you just have to arrange it so that it can go forever.

That’s a single version of auto research, like a single loop trying to improve. And I was surprised that it found these things in a repo that was already fairly well tuned.

And that’s just a single loop. Frontier labs have GPU clusters of tens of thousands of them. So it’s very easy to imagine how you would basically get a lot of this automation on smaller models, and fundamentally everything around frontier-level intelligence is about extrapolation and scaling laws. You basically do a ton of the exploration on the smaller models, and then you try to extrapolate out.

So you’re saying our research efforts are going to get more efficient. We’re going to have better direction for when we scale as well if we can do this experimentation better.

Yeah. I would say that the most interesting project, and probably what the frontier labs are working on, is: you experiment on the smaller models, you try to make it as autonomous as possible, remove researchers from the loop — they have way too much confidence, and they shouldn’t be touching any of this really — and so you have to rewrite the whole thing.

Right now, certainly they can contribute ideas, but they shouldn’t actually be enacting those ideas. There’s a queue of ideas, and there’s maybe an automated scientist that comes up with ideas based on all the archived papers and GitHub repos, and it funnels ideas in. Or researchers can contribute ideas, but it’s a single queue, and there are workers that pull items and try them out, and whatever works gets put on the feature branch, and maybe some people monitor the feature branch and merge to the main branch sometimes.

So yeah, just removing humans from the processes and automating as much as possible and getting high tokens-per-second throughput. It does require rethinking all of the abstractions, and everything has to be reshuffled. So yeah, I think it’s very exciting.

If we take one more recursive step here, when is the model going to write a better program.md than you?

Yeah. So program.md is my crappy attempt at describing how the auto researcher should work. Like, do this, then do that, then that, and maybe try these kinds of ideas. Here are maybe some ideas like architecture, optimizer, etc. I just came up with this in markdown, right?

And so, yeah, exactly. You want some kind of auto research loop maybe that looks for — you can imagine that different program.mds would give you different progress. So you basically — every research organization is described by program.md.

A research organization is a set of markdown files that describe all the roles and how the whole thing connects. And you can imagine having a better research organization. Maybe they do fewer standups in the morning because they’re useless. This is all just code, right? So one organization can have fewer standups, one can have more, one can be very risk-taking, one organization can be less.

And so you can definitely imagine that you have multiple research orgs, and then they all have code. And once you have code, then you can imagine tuning the code. So 100%, there’s a meta layer of it.

Did you see my text about my contest idea? My contest idea was: let people write different program.mds, right? And for the same hardware, where do you get the most improvement? Then you can take all that data and then give it to the model and say: write a better program.md.

Yes, yes. Exactly.

We’re going to get something better. Like, there’s no way we don’t.

You can 100% look at where the improvements came from and ask: can I change the program.md such that more of these kinds of things would be done? Or things that didn’t work.

Meta optimization.

Yeah, you can 100% imagine doing that. So I think this is a great idea, but I think you sort of go one step at a time. You have one process, then second process, then the next process, and these are all layers of an onion.

The LLM part is now taken for granted. The agent part is now taken for granted. Now the claw-like entities are taken for granted, and now you can have multiple of them, and now you can have instructions to them, and now you can have optimization over the instructions. And it’s just a little too much. But this is why it gets to the psychosis: this is infinite, and everything is skill issue. That’s why I feel like, yeah, that’s just coming back to why it’s so insane.

Okay. Well, if we’re just trying to diagnose the current moment and what is a relevant skill right now, what do you think is the implication that this is the loop we should be trying to achieve in different areas, and that it works? Remove yourself, create the metric or create the ability for agents to continue working on it without you.

Yeah.

Do we still have performance engineering?

Yeah. I mean, there are a few caveats that I would put on top of the LLM ecosystem. Number one, this is extremely well-suited to anything that has objective metrics that are easy to evaluate.

So for example, writing kernels for more efficient CUDA code for various parts of a model, etc., are the perfect fit. Because you have inefficient code, and then you want efficient code that has the exact same behavior but is much faster. Perfect fit.

A lot of things are a perfect fit for auto research, but many things will not be. If you can’t evaluate, then you can’t auto research it, right? So that’s caveat number one.

And then maybe caveat number two: we’re talking about next steps and we can kind of see what the next steps are, but fundamentally the whole thing is still kind of bursting at the seams a little bit, and there are cracks, and it doesn’t fully work. If you try to go too far ahead, the whole thing is not actually useful, if that makes sense.

These models have improved a lot, but they’re still rough around the edges. I simultaneously feel like I’m talking to an extremely brilliant PhD student who’s been a systems programmer for their entire life, and a 10-year-old. And it’s so weird.

Humans are a lot more coupled. You wouldn’t encounter that combination. This jaggedness is really strange. Humans have some jaggedness, but agents have a lot more, where sometimes I ask for functionality and it comes back with something that’s just totally wrong, and then we get into loops that are totally wrong, and I get so frustrated with the agents all the time still, because you feel the power of it, but also it still does nonsensical things once in a while for me as well.

I get very annoyed when I feel like the agent wasted a lot of compute on something it should have recognized was an obvious problem.

Yeah. I think what’s maybe underneath that is fundamentally these models are trained via reinforcement learning. So they’re actually struggling with the exact same thing we just talked about, which is that the labs can improve the models in anything that is verifiable, anything that has rewards. Did you write the program correctly, and do the unit tests check out? Yes or no.

But some of the things where they’re struggling is, for example, nuance of maybe what I had in mind or what I intended, and when to ask clarifying questions. Anything that feels softer is worse. So you’re either on rails and you’re part of the superintelligence circuits, or you’re not on rails and you’re outside the verifiable domains, and suddenly everything kind of meanders.

Maybe another way to put it is: if today you go to state-of-the-art model ChatGPT and ask it, “Tell me a joke,” do you know what joke you’re going to get? There’s the joke.

I do feel like ChatGPT has like three jokes.

Yeah. The joke that apparently all LLMs laugh the most at is, “Why do scientists not trust atoms? Because they make everything up.”

Okay.

Because they make everything up. So this is the joke you would get like three or four years ago, and this is the joke you still get today.

Okay.

So even though the models have improved tremendously, and if you give them an agentic task they will just go for hours and move mountains for you, and then you ask for a joke and it has a stupid joke, a crappy joke from five years ago. And it’s because it’s outside the RL. It’s outside the reinforcement learning. It’s outside what’s being improved.

It’s part of the jaggedness. Shouldn’t you expect models as they get better to also have better jokes or more diversity of them? It’s just not being optimized, and it’s stuck.

Do you think that implies that we are not seeing generalization in the sense of broader intelligence, of joke-smartness being attached to code-smartness?

Yeah. I think there’s some decoupling where some things are verifiable and some things are not, and some things are optimized for arbitrarily by the labs depending on what data went in, and some things are not.

But the premise from some research groups is that if you are smarter at code generation or in these verifiable fields, you should be better at everything. And the joke situation suggests that that’s not happening in all cases.

I don’t think that’s happening. I think maybe we’re seeing a little bit of that, but not a satisfying amount.

That jaggedness exists in humans. You can be very, very good at math and still tell a really bad joke.

Yeah, that’s true. But it still means that the story isn’t exactly that we’re getting all the intelligence and capabilities in all the domains of society for free as we get better and better models. That’s not exactly fundamentally what’s going on. There are some blind spots, and some things are not being optimized for. And this is all clustered up in these opaque neural net models.

So you’re either on the rails of what it was trained for, and everything is going at speed of light, or you’re not. So it’s jaggedness. That’s why I think even though the progression is obvious, what should happen, you can’t let it fully go there yet because it doesn’t fully work. Or it’s a skill issue and we just haven’t figured out how to use it. So it’s hard to tell.

Can I ask kind of a blasphemous question? If this jaggedness is persisting, and it’s all rolled up in at least a monolithic interface, a single model, does that make sense? Or should it be unbundled into things that can be optimized and improved against different domains of intelligence?

Like unbundling the models into multiple experts in different areas, etc.?

More directly, yeah. Instead of just one thing that we have no exposure to that can be confusing as to why it’s so good at this but not this other thing.

Yeah. I think currently my impression is the labs are trying to have a single monoculture of a model that is arbitrarily intelligent in all these different domains, and they just stuff it into the parameters. I do think we should expect more speciation in the intelligences.

The animal kingdom is extremely diverse in the brains that exist. There are lots of different niches in nature, and some animals have an overdeveloped visual cortex or other parts. I think we should be able to see more speciation. You don’t need this oracle that knows everything. You speciate it, and then you put it on a specific task.

We should be seeing some of that because you should be able to have much smaller models that still have the cognitive core — they’re still competent — but then they specialize, and they can become more efficient in terms of latency or throughput on specific tasks that you really care about. Like if you’re a mathematician working in Lean, I saw for example there’s a few releases that really target that as a domain. So there are probably going to be examples like that where the unbundling kind of makes sense.

One question I have is whether the capacity constraint on available compute infrastructure drives more of this, because efficiency actually matters more. If you have access to full compute for anything you do, like even one single model, right? But if you actually feel pressure where you’re like, “I can’t serve a massive model for every use case,” do you think that leads to speciation?

The question makes sense. What I’m struggling with is I don’t think we’ve seen too much speciation just yet, right?

No.

We’re seeing a monoculture of models. And there’s clearly pressure for, like, make a good code model, put it back in the main merge again, even though there already is pressure on the models.

I guess perhaps I feel like there’s a lot of very short-term supply crunch, and maybe that causes more speciation now.

Yeah. Fundamentally, the labs are serving a model and they don’t really know what the end user is going to be asking about. So maybe that’s part of it because they kind of have to multitask over all the possible things that could be asked.

But I think if you’re coming to a business and maybe partnering on some specific problems you care about, then maybe you would see that there. Or there would be some very high-value applications that are more niche.

I think right now they’re kind of going after the totality of what’s available. I don’t think that the science of manipulating the brains is fully developed yet, partly.

What do you mean by manipulating?

Fine-tuning without losing capabilities, as an example. We don’t have these primitives for actually working with the intelligences in ways other than just context windows. Context windows kind of just work, and they’re very cheap to manipulate. This is how we’re getting some of the customization, etc.

But I think it’s a developing science of how you more deeply adjust the models, how you have continual learning maybe, or how you fine-tune in a certain area, how you get better in a certain area, or how you actually touch the weights, not just the context windows.

It’s a lot more tricky to touch the weights than just the context windows, because you’re fundamentally changing the full model and potentially its intelligence. So maybe it’s just not a fully developed science of speciation. And it also has to be cheap enough for that speciation to be worthwhile in these given contexts.

Can I ask about an extension to auto research that you described in terms of OpenGrunt? You said, okay, well, we have this thing, and we need more collaboration surface around it, essentially for people to contribute to research overall. Can you talk about that?

Yeah. So we talked about auto research as a single thread of “I’m going to try stuff in a loop,” but fundamentally the parallelization of this is the interesting component. I was trying to play around with a few ideas, but I don’t have anything that clicks as simply as — I don’t have something that I’m super happy with just yet, but it’s something I’m working on on the side when I’m not working on my claw.

I think one issue is, if you have a bunch of nodes of parallelization available to you, then it’s very easy to just have multiple auto researchers talking through a common system or something like that.

What I was more interested in is how you can have an untrusted pool of workers out there on the internet. So for example in auto research, you’re just trying to find the piece of code that trains a model to a very low validation loss. If anyone gives you a candidate commit, it’s very easy to verify that that commit is correct, is good. Someone could claim from the internet that this piece of code will optimize much better and give you much better performance. You could just check. Very easy, but probably a lot of work goes into that checking.

Fundamentally, they could lie, etc. So you’re basically dealing with a similar kind of — it almost actually looks a little bit more like a blockchain, a little bit, because instead of blocks, you have commits. These commits can build on each other, and they contain changes to the code as you’re improving it.

The proof of work is basically doing tons of experimentation to find the commits that work. That’s hard. Then the reward is just being on the leaderboard right now. There’s no monetary reward whatsoever. I don’t want to push the analogy too far, but fundamentally it has this issue where a huge amount of search goes into it, but it’s very cheap to verify that a candidate solution is indeed good, because you can just train a single — someone had to try 10,000 ideas, but you just have to check that the thing they produced actually works, because the 9,999 of them didn’t.

So basically, long story short, you have to come up with a system where an untrusted pool of workers can collaborate with a trusted pool of workers that do the verification. The whole thing is asynchronous and works, and it’s safe from a security perspective because if anyone sends you arbitrary code and you’re going to run it, that’s very sketchy and dodgy. But fundamentally it should be totally possible.

You’re familiar with projects like SETI@home and Folding@home. All these problems have a similar setup. So in Folding@home you’re folding a protein, and it’s very hard to find a configuration that is low energy. But if someone finds a configuration that they evaluate to be low energy, that’s perfect. You can just use it. You can easily verify it.

A lot of things have this property that they are very expensive to come up with but very cheap to verify. So in all those cases, things like Folding@home or SETI@home or AutoResearch@home would be good fits.

Long story short, a swarm of agents on the internet could collaborate to improve LLMs and could potentially even run circles around frontier labs. Who knows? Frontier labs have a huge amount of trusted compute, but the Earth is much bigger and has a huge amount of untrusted compute. If you put systems in place that deal with this, then maybe it is possible that the swarm out there could come up with better solutions, and people kind of contribute cycles to a thing that they care about.

Lots of companies could maybe have their own things that they care about, and if you have compute capacity you could contribute to different auto research tracks. Maybe you care about cancer or something like that. You don’t just donate money to an institution — you actually could purchase compute, and then you could join the auto research forum for that project.

So if everything is rebundled into auto researchers, then compute becomes the thing that you’re contributing to the pool.

Yeah, that’s very inspiring. And it’s also interesting: I don’t know how far this goes, but it is interesting that at least some audience of people here in Silicon Valley or lining up at retail stores in China have discovered that having access to personal compute is interesting again. So maybe they’re really motivated to do that for their claws, and then they can contribute to auto research.

It’s almost like dollars are the thing everyone cares about, but is flop the thing that everyone will actually care about in the future? Is there going to be a flipping of what the thing is that you care about? Right now, for example, it’s really hard to get compute even if you have money. So actually it almost seems like the flop is dominant in a certain sense.

So maybe it’s kind of like that: how many flops do you control instead of what wealth do you control? I don’t actually think that’s true, but it’s kind of interesting to think about.

The last thing you released was a little bit of jobs data analysis. Is that right? It might have touched a nerve even though you were just visualizing some public data. What were you curious about?

Yeah. I guess I was curious because everyone is really thinking about the impacts of AI on the job market and what it’s going to look like. So I was just interested to take a look: what does the job market look like? Where are the different roles? How many people are in different professions?

I was really just interested to look through the individual cases and try to think myself about, with these AIs and how they’re likely to evolve, are these going to be tools that people are using? Are these going to be displacing tools for these professions? What are the current professions, and how are they going to change? Are they going to grow or adjust to a large extent? What could be new professions?

So it’s really just a way to fuel my own chain of thought about the industry, I suppose.

The jobs data is basically Bureau of Labor Statistics. They actually have percent outlook for each profession about how much it’s expected to grow over the next, I think, almost a decade. I think it’s a decade, but it was made in 2024.

We need a lot of healthcare workers.

Yeah. So they’ve already made those projections, and I’m not sure 100% what the methodology was that they put into the projections. I guess I was interested to color things by: if what people think is being developed now is this kind of more digital AI that is almost like ghosts or spirit entities that can interact in the digital world and manipulate a lot of digital information, and they currently don’t really have a physical embodiment or presence, then the physical stuff is probably going to go slightly slower because you’re manipulating atoms.

Flipping bits and the ability to copy-paste digital information makes everything a million times faster than accelerating matter. So energetically, I just think we’re going to see a huge amount of activity in digital space, huge amount of rewriting, huge amount of activity boiling soup. I think in the digital space things are going to go at the speed of light compared to what’s going to happen in the physical world, to some extent.

That’s why I was highlighting the professions that fundamentally manipulate digital information. This is work you could do from your home, etc. Because I feel like things will change in those professions. It doesn’t mean there’s going to be less of those jobs or more of those jobs, because that has to do with demand elasticity and many other factors, but things will change in these professions because of these new tools and because of this upgrade to the nervous system of the human superorganism, if you want to think about it that way.

Given the look you had at the data, do you have either any observations or guidance for people facing the job market or thinking about what to study now or what skills to develop? I mean, we can all go get — I’m very thankful that I have to meet people for my job right now.

More physical, yeah.

Could you do your work from home, though?

I could. I think there are relationship parts of it that are hard, but most of it I could.

Yeah. I think it’s really hard to tell because, again, the job market is extremely diverse and I think the answers will probably vary. But to a large extent, these tools are extremely new and extremely powerful, so just trying to keep up with it is the first thing.

Because I think a lot of people kind of dismiss it, or they’re afraid of it.

Or they’re afraid of it, etc., which is totally understandable of course. I think it’s fundamentally an empowering tool at the moment. These jobs are bundles of tasks, and some of these tasks can go a lot faster, so people should think of it as primarily a tool that it is right now. I think the long-term future of that is uncertain. It’s kind of really hard to forecast, to be honest, and I’m not professionally doing that really, and I think it’s a job of economists to do properly.

You are an engineer though, and one thing I thought was interesting is that the demand for engineering jobs is continuing to increase. I can’t tell if that’s a temporary phenomenon. I’m not sure how I feel about it yet. Do you know?

Yeah. That’s like demand almost because software was scarce, right? The reason we don’t have more demand for software is just scarcity and it’s too expensive.

Too expensive, yeah.

So if the barrier comes down, then actually you have the Jevons paradox, which is you actually — the demand for software goes up. It’s cheaper and it’s more powerful. The classical example people cite is always ATMs and bank tellers, because there was a lot of fear that ATMs and computers would displace tellers. But what happened is they made the cost of operation of a bank branch much cheaper, and so there were more bank branches, so there were more tellers.

Basically it’s just the paradox: something becomes cheaper, so there’s a lot of unlocked demand for it. So I do think that’s probably — I do have a cautiously optimistic view of this in software engineering, where it does seem to me like the demand for software will be extremely large. It’s just become a lot cheaper.

I do think that for quite some time — it’s very hard to forecast — but right now at least locally, there’s going to be more demand for software, because software is amazing. It’s digital information processing. You’re not forced to use arbitrary tools that were given to you that are imperfect in various ways. You’re not forced to subscribe to what exists. Code is now ephemeral, and it can change, and it can be modified.

So I think there’s going to be a lot of activity in the digital space to rewire everything in a certain sense, and I think it’s going to create a lot of demand for this kind of stuff.

I think long-term, obviously, even with auto research, OpenAI or Anthropic or these other labs — they’re employing what, like a thousand-something researchers, right? These researchers are basically like glorified auto — they’re automating themselves away actively, and this is the thing they’re all trying to do.

Yeah.

I did spend a bunch of time going around OpenAI and I was like, “You guys realize if we’re successful, we’re all out of job. We’re just building automation for Sam or something like that. Or the board, I’m not sure. But we’re just building this automation for the board or the CEO or something like that, and we’re all out of our job, maybe contributing on the side.”

So yeah, it’s kind of unnerving from that perspective.

Is it okay if I ask you Noam’s question? You could be doing that, right? Auto researching with a lot of compute scale and a bunch of colleagues at one of the frontier labs. Why not?

Well, I was there for a while, right? I did re-enter, so to some extent I agree. I think there are many ways to slice this question. It’s a very loaded question a little bit.

I will say that I feel very good about what people can contribute and their impact outside of the frontier labs — obviously still in the industry, but also in more ecosystem-level roles. So your role, for example, is more ecosystem-level. My role currently is also kind of more on the ecosystem level, and I feel very good about the impact that people can have in those kinds of roles.

I think conversely there are definite problems in my mind with aligning yourself way too much with the frontier labs too. Fundamentally, you have a huge amount of financial incentive with these frontier labs, and by your own admission the AIs are going to really change humanity and society in very dramatic ways, and here you are basically building the technology and benefiting from it and being very allied to it through financial means.

This was a conundrum that was at the heart of how OpenAI started in the beginning. This was the conundrum that we were trying to solve. The conundrum is still not fully resolved. So that’s number one.

You’re not a completely free agent, and you can’t actually be part of that conversation in a fully autonomous, free way if you’re inside one of the frontier labs. There are certain things that you can’t say, and conversely there are certain things that the organization wants you to say. They’re not going to twist your arm, but you feel the pressure of what you should be saying, because otherwise it’s really awkward conversations, strange side-eyes, like what are you doing? So you can’t really be an independent agent.

I feel a bit more aligned with humanity in a certain sense outside of a frontier lab because I’m not subject to those pressures. I can say whatever I want.

I would say in the frontier labs you can have impact there, of course, as well. But there are many researchers, and maybe you’re one of them, maybe your ideas are really good, etc. Maybe there’s a lot of decision-making to do and you want to be in the room with those conversations when they come up.

I do think currently the stakes are overall fairly low, so everything is kind of nice. But ultimately, at the end of the day, when the stakes are really high, if you’re an employee at an organization, I don’t actually know how much sway you’re going to have on what the organization is going to do. Fundamentally, at the end of the day, you’re not really in charge. You’re in a room and contributing ideas, but you’re not really in charge of the entity you’re a part of.

So those are some sources of misalignment, I think.

I will say that in one way I do agree a lot with that sentiment, that the labs, for better or worse, are opaque, and a lot of work is there, and they’re kind of at the edge of capability and what’s possible, and they’re working on what’s coming down the line. I think if you’re outside of the frontier lab, your judgment fundamentally will start to drift because you’re not part of what’s coming down the line.

I feel like my judgment will inevitably start to drift as well, and I won’t actually have an understanding of how these systems actually work under the hood. That’s an opaque system. I won’t have a good understanding of how it’s going to develop. So in that sense, I agree, and it’s something I’m nervous about.

I think it’s worth basically being in touch with what’s actually happening and actually being in the frontier lab. If some of the frontier labs would have me come for some amount of time and do really good work for them, and then maybe come—

Andrej is looking for a job. This is super exciting.

Yeah. Then I think that’s maybe a good setup, because I kind of feel like maybe that’s one way to actually be connected to what’s actually happening, but also not feel like you’re necessarily fully controlled by those entities.

So I think honestly in my mind Noam can probably do extremely good work at OpenAI, but also I think his most impactful work could very well be outside of OpenAI.

So that’s a call to be an independent researcher with auto research.

Yeah. There are many things to do on the outside, and I think ultimately the ideal solution maybe is going back and forth. Fundamentally, you can have really amazing impact in both places. So it’s very complicated. It’s a very loaded question a little bit. But I mean, I joined the frontier lab, and now I’m outside, and then maybe in the future I’ll want to join again. I think that’s kind of how I look at it.

One question related to what visibility the world or the AI ecosystem has into the frontier is: how close is open source to the frontier, and how sustainable is that?

I think it is quite surprising, the entire sequence of events actually, from having a handful of Chinese models and global models, and I think people are going to continue releasing here in the near term that are closer than much of the industry anticipated from a capability perspective.

I don’t know if you’re surprised by that, but you’re a long-term contributor to open source. What’s your prediction here?

Yeah. So roughly speaking, basically the closed models are ahead, but people are monitoring the number of months that open-source models are behind. It started with there’s nothing, and then it went to 18 months, and now it’s convergence, right? So maybe they’re behind by like, what is it lately, maybe six to eight months kind of thing right now.

I’m a huge fan of open source, obviously. For example, in operating systems you have closed systems like Windows and macOS. These are large software projects kind of like what LLMs are going to become. And then there’s Linux.

Actually, Linux is an extremely successful project. It runs on the vast majority of computers. Last time I checked, was it like 60% or something like that that run Linux? That’s because there is a need in the industry to have a common open platform that everyone feels safe using. The industry has always felt a demand for that kind of project to exist, and I think the same is true now. That’s why businesses actually want this kind of thing to exist.

The big difference is that everything is capital. There is a lot of capex that goes into this. I think that’s where things fall apart a little bit and make it harder to compete in a certain sense.

I do think the current models are very good. The other thing that I think is really interesting is that for the vast majority of consumer use cases and things like that, even open-source models are actually quite good, I would say. I think if you go forward more years, it does seem like a huge amount of simple use cases are going to be well covered and actually even run locally.

But there’s always going to be some demand for frontier intelligence, and that can actually be an extremely large piece of the pie. It could be that the need for frontier intelligence is going to be like Nobel Prize kind of work, or “let’s move Linux from C to Rust.” There are going to be bigger projects scoped in that kind of a way.

Maybe that’s where a lot of the frontier closed intelligences are going to be interacting, and open source is kind of going to eat through a lot of the more basic use cases.

At some point, what is frontier today is going to be — probably later this year — what’s frontier today in terms of what I’m using right now from the closed labs might be open source, and that’s going to be doing a lot of work. So I kind of expect that this dynamic will basically continue. We’ll have frontier labs that have closed AIs that are kind of these oracles, and then we’ll have open source kind of behind by some amount of months, and I kind of expect that to continue. I actually think that’s a pretty good setup overall.

I’m a little bit hesitant about having intelligences that are closed and that’s it. I don’t actually think it’s structurally — I think there’s some systemic risk attached to just having intelligences that are closed.

You mean like in political or economic systems in general?

Yes, exactly. I think centralization has a very poor track record in the past.

Very Eastern European.

Yeah. A lot of pretty bad precedent. So I want there to be a thing that is maybe not at the edge of capability because it’s new and unexplored, etc., but I want there to be a thing that’s behind and that is kind of a common working space for intelligences that the entire industry has access to. That seems to me like a pretty decent power balance for the industry.

Yeah. I also think there are just many problems to solve, right? If you keep advancing intelligence from the frontier, we can do new things, and there are a lot of very big problems for humanity. So it seems that that will continue to be a very expensive game, and so I want to root for labs that are doing that because there are problems we cannot solve without continuing to advance the models in a very expensive way.

Yeah. And yet, as you point out, if what we have today as frontier is open, that’s a lot of capability. The power of that or the democratization of that seems very useful and also healthy.

Yeah. I think basically by accident we’re actually in an okay spot.

And optimal.

By accident we happen to be in a good spot in a certain sense.

And to some degree, the longer this endures, this dynamic, the healthier of a spot the ecosystem might be in, right? Because you have more and more area under the curve.

I will say that even on the closed side, I almost feel like it’s been even further centralizing recently because I think a lot of the frontrunners are not necessarily like the top tier. So yeah, in that sense I think it’s not super ideal. I would love there to be more frontier labs, because I’m by default very suspicious of concentration. I want there to be more people in the room.

I think in machine learning, ensembles always outperform any individual model, and so I want there to be ensembles of people thinking about all the hardest problems, and I want there to be ensembles of people in the room, well-informed, making all those decisions. I don’t want it to be closed doors with two people or three people. That feels like not a good future. I almost wish there were more labs, long story short. I do think that open source has a place to play. I hope it sticks around, and it’s currently slightly behind, and that’s actually kind of a good thing.

Okay. You worked on the precursor to generalized robotics autonomy in cars, right? A lot has happened in the last couple of months with robotics companies as well — acceleration of really impressive generalization of environment, of tasks, increasing long-horizon tasks, lots of money going into the space. Is it going to happen? Has anything in your view changed recently?

My view is kind of informed by what I saw in self-driving, and I do feel like self-driving is the first robotics application. Probably what I saw at the time, like 10 years ago, was there were a large number of startups, and I kind of feel like most of them basically didn’t long-term make it.

What I saw is that a lot of capital expenditure had to go in, and a lot of time. So I think robotics, because it’s so difficult and so messy and requires a huge amount of capital investment and a lot of conviction — it’s a big problem, and I think atoms are really hard.

So I kind of feel like robotics will lag behind what’s going to happen in digital space. In digital space, there’s going to be a huge amount of unbundling, basically things that weren’t super efficient becoming a lot more efficient by like a factor of 100, because bits are so much easier.

I think currently, in terms of what’s going to change and where the activity is, digital space is going to change a huge amount, and then physical space will lag behind. What I find very interesting is the interface in between them as well, because if we do have more agents acting on behalf of humans and more agents talking to each other and doing tasks and participating in the economy of agents, you’re going to run out of things that you can do purely in digital space. At some point you have to go to the universe and ask it questions. You have to run an experiment and see what the universe tells you back to learn something.

We currently have a huge amount of digital work because there’s an overhang in how much we collectively thought about what already is digital. We just didn’t have enough thinking cycles among humans to think about all the information that is already digital and already uploaded.

So we’re going to start running out of stuff that is already uploaded. At some point you read all the papers and process them and have some ideas about what to try. I don’t actually know how much intelligence you can get that is fully closed off and just using information that’s available to it.

So I think what’s going to happen is first there’s going to be a huge amount of unbundling, and I think there’s a huge amount of work there. Then actually it’s going to move to the interfaces between physical and digital. That’s sensors, like seeing the world, and actuators, like doing something to the world.

So I think a lot of interesting companies will actually come from that interface of: can we feed the superintelligence data, and can we actually take data out and manipulate the physical world per its bidding, if you want to anthropomorphize the whole thing? Then the physical world actually — I almost feel like the total addressable market in terms of the amount of work and so on is massive, possibly even much larger than what can happen in digital space. So I actually think it’s a much bigger opportunity as well. But I do feel like it’s a huge amount of work, and in my mind atoms are just a million times harder.

So it will lag behind, but it’s also, I think, a bigger market. So the opportunities kind of follow that trajectory. Right now digital is my main interest. Then interfaces would be after that, and then maybe some of the physical things — their time will come, and they’ll be huge when they do come.

Well, it’s an interesting framework for it too, because certain things — not the things I’m working on right now — but certain things are much easier even in the world of atoms, right? If you think about read and write to the physical world, like read — sensors, cameras — there’s a lot of existing hardware, and you can imagine enriching agent capabilities or capturing a lot of new data if you’re just clever about it. You don’t necessarily have to invest a lot to get something valuable.

Yeah. So examples of this that I saw, for example, are — a friend of mine, Liam, is CEO of Periodic. I visited them last week, so it’s just top of mind. They’re trying to do auto research for material science. In that case the sensors to the intelligence are actually pretty expensive lab equipment.

The same is true in biology. I think a lot of people are very interested in engineering biology, and the sensors will be more than just video cameras, if that makes sense.

The other thing I saw, for example, is companies that are trying to have — you basically pay people for training data as an example.

Programmatically.

Yeah, to feed the Borg. These are all examples of sensors in a certain sense. So they take many diverse shapes and forms.

Yeah. So I’m looking forward to the point where I can ask for a task in the physical world and put a price on it and just tell the agent, “You figure out how to do it. Go get the data.”

I’m actually kind of surprised we don’t have enough information markets. For example, if Polymarket or other betting markets or even stocks have so much autonomous activity and rising amounts of activity, why should — like for example, if Iran was just happening now, how come there isn’t a process where taking a photo or video from somewhere in Tehran should cost like 10 bucks? Someone should be able to pay for that. That’s an example of feeding the intelligence. There’s not going to be a human looking at it. It’s going to be agents who are trying to guess the betting games and stock markets and so on.

So I kind of feel like the agentic web is still fairly new, that there’s no mechanism for this. But this is an example of what I think might happen. There’s a good book that maybe is inspiring called *Daemon*. The intelligence ends up puppeteering humanity a little bit, in a certain sense. Humans are kind of its actuators, but humans are also its sensors. So I think collectively society will reshape in a certain way to serve that machine, not necessarily to each other.

Well, we were on this very specific point of missing pieces of training data we needed. We needed something like auto research, right? We need the training cycle, or the SFT piece, to be far more mechanized in order to make the collection — in order to take the human out of the loop to ask for a task that is just like, improve my model quality with new data. Does that make sense to you? If you can’t have the model do the training runs by itself, then your ability to do this as a closed-loop task by pricing data is more challenged.

Yes. Yes. 100%.

But now the thing is, for LLM training, it actually fits the paradigm really well. The optimization of all the code so it runs faster, and then you also have metrics you can optimize against. I do think that if you had an autonomous loop over those metrics, there’s going to be a lot of Goodharting going on, where the system will overfit to those metrics. But then you can use the system to devise more metrics, and you just have really good coverage. So it’s kind of hard to tell, but in a certain sense it’s a pretty good fit.

I want to talk about a little tiny side project you have before we end. Tell me about microGPT.

Oh yeah. Okay. So microGPT. I have this running obsession of maybe a decade or two of just simplifying and boiling down LLMs to their bare essence. I’ve had a number of projects along these lines, like nanoGPT and makemore and micrograd, etc.

So I feel like microGPT is now the state of the art of me trying to just boil it down to the essence. The thing is, training neural nets and LLMs specifically is a huge amount of code, but all of that code is actually complexity from efficiency. It’s just because you need it to go fast. If you don’t need it to go fast and you just care about the algorithm, then that algorithm actually is 200 lines of Python, very simple to read. This includes comments and everything.

Because you just have your dataset, which is text. You need your neural network architecture, which is like 50 lines. You need to do your forward pass and then your backward pass to calculate the gradients. So a little autograd engine to calculate the gradients is like 100 lines. Then you need an optimizer — Adam, for example, which is a very state-of-the-art optimizer — that’s again like 10 lines really. Putting everything together in a training loop is like 200 lines.

It was interesting to me because normally before, like maybe a year ago or more, if I had come up with microGPT, I would be tempted to explain to people, like I have a video stepping through it or something like that. I actually tried to make that video a little bit, and I tried to make a little guide to it and so on, but I kind of realized that this is not really adding too much, because it’s already so simple that it’s 200 lines, and anyone could ask their agent to explain it in various ways.

The agents — I’m not explaining to people anymore. I’m explaining it to agents. If you can explain it to agents, then agents can be the router, and they can actually target it to the human in their language with infinite patience and at their capability level and so on.

Right. If I don’t understand this particular function, I can ask the agent to explain it to me like three different ways, and I’m not going to get that from you.

Exactly. So I kind of feel like, what is education? It used to be guides, it used to be lectures, it used to be this thing. But I feel like now I’m more explaining things to agents, and maybe I’m coming up with skills where basically a skill is just a way to instruct the agent how to teach the thing.

So maybe I could have a skill for microGPT, of the progression I imagine the agent should take you through if you’re interested in understanding the codebase. It’s just hints to the model: first start off with this, then with that. So I could just script the curriculum a little bit as a skill.

So I don’t feel like there’s going to be as much explaining things directly to people. It’s going to be more like, does the agent get it? And if the agent gets it, then they’ll do the explanation. We’re not fully there yet because I still think I can explain things a little bit better than the agents, but I still feel like the models are improving so rapidly that it’s a losing battle to some extent.

I think education is going to be reshuffled by this quite substantially, where it’s kind of the end of teaching each other things almost a little bit. If I have a library of code, for example, it used to be that you have documentation for other people who are users of my library, but you shouldn’t do that anymore. You should instead of HTML documents for humans, have markdown documents for agents, because if agents get it, then they can just explain all the different parts of it. So it’s this redirection through agents.

I think we’re going to see a lot more of that playing out.

Well, we’ll see if the great teachers know how to develop intuition for how to explain things to agents differently.

Ultimately, so for example microGPT — I tried to get an agent to write microGPT. I told it: try to boil down neural networking to the simplest thing. It can’t do it. microGPT is my end of my obsession. It’s the 200 lines. I thought about this for a long time. I was obsessed about this for a long time. This is the solution. Trust me, it can’t get simpler. This is my value add.

Everything else, the agent gets. It just can’t come up with it. But it totally gets it and understands why it’s done in a certain way, etc. So my contribution is kind of these few bits. But everything else in terms of the education that goes on after that is not my domain anymore.

So maybe education changes in those ways, where you kind of have to infuse the few bits that you feel strongly about — the curriculum, or the better way of explaining it, or something like that. The things that agents can’t do is your job now. The things that agents can do, they can probably do better than you, or very soon. So you should be strategic about what you’re actually spending time on.

Well, we appreciate the few things. Thank you, Andrej.

Okay.

Find us on Twitter at No Priors Pod. Subscribe to our YouTube channel if you want to see our faces. Follow the show on Apple Podcasts, Spotify, or wherever you listen. That way you get a new episode every week. And sign up for emails or find transcripts for every episode at no-priors.com.
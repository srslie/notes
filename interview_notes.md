- What is ```{} + {}``` or ```[] + []``` ?
  - This question gets at type coercion. It will attempt to concatenate these since they are not numbers, but first needs to turn them into ```String([])``` and since they're empty, it would be an empty string. The result of either of these would be an empty string since all would be type coerced into that empty string.

- If you have 
 ```
 function x() {
   return 5
 }

 const something = x 'frogs'
 console.log(something)
 ```
 - what logs? It logs 5 because the function doesn't account for a parameter so just returns 5 whenever called, and it gets implied that the something is calling ```x``` even without the parens because the string literal next to it is sorta in that position.
 - (tagged template: a template string next to a named literal gets considered an argument)

- How would you be able to change around some text on a website?
  - using dev tools, add ```document.body.contentEditable = true```
  - this adds a property to the elements of everything in the body that lets you click on and edit text, etc.

- what is encapsulation? 
  - [article by Dave Braunschweig](https://press.rebus.community/programmingfundamentals/chapter/encapsulation/#:~:text=Encapsulation%20is%20one%20of%20the,parties'%20direct%20access%20to%20them.)
  - Roughly, keeping objects/(and the classes that made them) with their methods and data together, using public/private methods to keep a separation and only accessing updates or manipulation of an objects' public methods instead of directly reaching in and trying to mess with an object's properties. (Getters and Setters)


- ASW: Automatic Semicolon Insertion 
 https://stackoverflow.com/questions/2846283/what-are-the-rules-for-javascripts-automatic-semicolon-insertion-asi

https://262.ecma-international.org/7.0/#sec-rules-of-automatic-semicolon-insertion
  - empty statement
  - var statement
  - expression statement
  - do-while statement
  - continue statement
  - break statement
  - return statement
  - throw statement

- Scopes and Closure
- How does the internet work?
- How does a browser work?
- What is HTTP? Difference b/w types of requests.
- What is the box model?
- What is a promise?
- What is AJAX?
- Why do we use ORMs?
- What is ACID?
- What is a transaction?
- What is the n+1 problem?
- What is REST?


Dependency Injection is a Design Pattern where instead of your objects/classes having all functionality built-in leading to bloat, you inject additional functionality at instantiation as needed.

In Angular/Java Spring this is done via typing the constructor's arguments. The Application notices the typings instantiates the particular services/dependencies needed and passes them into the constructor.

Decorators are another similar pattern where you pass classes and methods into a function that adds or "decorates" them with functionality. In TS and Python, you may notice them a lot in the @decorator syntax.


-It's hard to highlight one challenge: 
  - learning to roller skate taught me the importance of protective equipment and the counterintuitive need for speed and commitment while learning, but challenged me with pavement caresses and humiliation from children at skate parks
 - learning to recover from an eating disorder taught me that letting go is part of control, and functionality is more beautiful than form, but challenged me to reframe my ingrained prejudice and underlying hurt to my self-esteem
 - learning to bake bread taught me patience, and the importance of good directions and precise measurements, but challenged me with repetitive failure and smoke alarm Pavlovian panic

I learn a lot of lessons, because I try a lot of things. 

For coding: few months ago, I had a partner programming project for my bootcamp. We had hiccups of inexperience (how to divide work without blocking each other, or git merge conflicts) but the biggest challenge was that in that 2-week project timeframe, my partner did not push anything until a week and a half in. So we scrambled to finish and deploy and it was honestly a mess. However, we did get a passing grade, deploy a (somewhat sloppy) project using Chart.js (which I learned and implemented in those few days) and I learned valuable lessons:

1) speak up for your needs when working with others.  Stand by strict timelines for an MVP in order to complete something you're proud of. Pair program if needed to ensure progress and help everyone.

2) push everything. In progress branches are super helpful to see for a partner. I felt bad that I had pushed things and my partner hadn't so I held off on pushing more to try not to pressure her, but that led to a lot of mess in merging several branches at the end.

3) remember humans. Because our project was messy and stressful and we both felt under-supported by each other, we had some tension. But we took time to sit down and talk through how our experience differed and what we could do better when working with others, and I learned that my partner was going through a really rough time emotionally with personal things, which made my frustration disappear. People are more important than projects and supporting others will ultimately lead to better results for both feelings and products.

----

This summer I learned to use a tablesaw, a concrete jack, and a carpenter's square while I built out my parent's old garden shed into a tiny house. It has r-30 ceiling insulation, an electric line buried 25 inches into the clay ground, and even sleek laminate floors and triple pane windows.

See, I've always been obsessed with doing things myself, from the ground up. It's independence, sure (my mom said I used to spill gallons of milk when I was little trying to pour my own cup) but also a fascination with how things work. 

That's what I like best about Airbnb. You help people do things themselves: make their own space and create an experience, a market, an income. 

I've traveled a lot, slept on floors and couches and hostels. But the personal pinpoint of curated home stays is so great. I want to support people who give that slice of home on the road to others. 

My hard work, investigation and interest in trying and learning how things work and how best to accomplish tasks or solve problems, and my belief in helping people in tangible ways make me the perfect candidate for joining the Airbnb team.

---
I was on Youtube: the Millennial Experience. 

Really, I was watching a Crash Course channel on European history, when I saw a 'computer science' video and went for it. It was fascinating, and smart women who pioneered modern computing inspired me to reclaim representation in this field!

Having been out of school for a time, the logical puzzle payoff was electric, and I started talking to some of the people in my life who'd made software their life. My brother works for Google, and he told me that I was smart enough (anyone was!) and just had to put in the time. My dad grew up learning from early punch-card machines and immediately started giving me trivia about adders and early open-source initiatives. My partner is a game designer for VR and showed me some of the C# that created the fun experiences with both love.

I love that coding is something you can take in so many different directions and impact people in increasingly important ways. I'm most excited to learn about how to make software more representative and accessible. I'm also really excited about machine learning and the potential of AI and algorithms to improve outcomes. 

The best part, though, is that I still get to learn so many things!

--
Teledoc Team:

Donkeys and leeches used to be the best humans could do. We've always wanted to take care of each other, and tried the latest technologies to do so. But I'm so grateful to live now.

Teledoc stands out as a place where I'll harness my commitment to serving others alongside my excitement using technology to reach those who need it most.

I pick things up fast, and appreciate debugging for getting to learn from complex systems. I'm experienced in customer service and elementary education, so I'm dedicated to accessibility and intuitive design. 

I'll bring passion and positivity, with humility and hard work.  I love figuring out code solutions hope I can do that for Teledoc!

Thanks,

Alice Ruppert

--
My experience in customer service and account management taught me that caring, intuitive design helps a business just as much as it helps the client.

Front-end development suits my dedication to making things accessible and practical, but also pretty. And sleek. And fun!

In the span of a few months, I've proven in a coding bootcamp environment that I can easily grasp coding concepts: my brain just happens to break things down in a way that aligns with debugging tools. 

I'm proficient in front-end technologies like React.js, plus I get really excited to learn about things from mobile Kotlin or Swift to more computer-science hardware and efficiency. I'm eager to learn, happy to wade through documentation and trial and error to get there, and dedicated to delivering.

The fact that this job allows some multi-platform crossover gets me excited to learn new tech stacks or implementations of ideas, and I'd love to work closely with UI/UX designers. I'm very dedicated to a my styling (as evidenced by my portfolio next to others from my cohort at https://terminal.turing.io/alumni/525-alice-ruppert).

I hope this can be a great opportunity to grow for both of us. I'll bring the hard work, passion, and optimism!

https://jobs.insightglobal.com/find_a_job/colorado/englewood/javascript-developer-design-technologist/job-34810/

- how is recursion different than iteration?
- what are design patterns and which have you used?
- what problem does React Redux solve? 'prop drilling, application state vs component state'
- what does api stand for and what does it do? 
  - application programming interface
- what does ajax stand for and what does it do?
- what's the difference between `let` and `const` in JS?
  - mutable vs immutable, scoped/hoisted a bit differently, for mutating arrays could still use const
- array `map` vs `forEach`
  - different returns
- how do you typically interact with APIs on the frontend?
- What are a few ways to optimize a Rails application?
  - mimimize features, mimimize hashes (Big o), implement a cache server to lay in front of the database
- what is chaining in javascript? 
  - leverage chaining with iterator methods, ex - filter then map
-  What is TDD?
   -  Test Driven Development, writing a test first to guide the development
- How do you stay up to date with new Javascript technology?
- what does a 400 status code indicate and when might you see it? 
  - bad client request
- if you have an array of objects, and you want to find all objects that have a specific key? only one? if any do?
  - filter it, find it, some, includes, all
- how is JSX different from HTML?
  - React-specific, XML, className, wrap JS expressions in curly braces
- explain the difference between props and state in React?
- when is better to use state vs props? 

- Star method:
  - situation, test, action, result

_____

Dear Twilio Teams,

Let's get my head in the cloud. 

Coding Bootcamp was great for small projects, going from 'what is command line' to 'here's a deployed app, I can look up documentation for anything, let's go'. Plus it proved my investment in learning and being in a vulnerable space of 70+ hours a week of continually humbled to the struggle and open to experiences.

But I need more! More code, more experience with scaled up, SaaS-based, future-forward products.

This internship stands out as somewhere to contribute to actual shipping core features. You specifically mention open source projects, which I love to see supported and want to me more involved with. Learning efficiency and scalability and building best practices is exactly where I'm going.

I'm dedicated to continuing to learn and want to enter the workforce with learning as my main goal. I need time to study inside of codebases, feedback on my projects, mentors, and challenges!

I'd love to work with you to get where I'm going, and grow alongside the wonderful teams at Twilio. I believe I can help and will work hard to prove it. My experience may be less than others, but my passion will set me apart.

Thanks,

Alice Ruppert

--

explain a cookie vs session (cookie is stored on client, session more to do with servers, but stored on both to maintain a user state)

__

Dear Highwing Team,

I'd be excited to join a team where there's clear focus on highly usable, helpful products as well as empowering employees.

Highwing stands out as an opportunity on the front end to work with cleanly designed tools, and I'm particularly impressed with the glimpse of data visualization underwriters can utilize through your software.

I'm interested in learning more about how you keep data secure for your brokers and carriers, and the added (and measurable) value of streamlining workflows for people sounds fulfilling.

Given that other Turing alumni have found a great fit at Highwing, I feel I can trust the values you stand by. Kaizen has been a motto throughout my professional life and feels especially relevant as a career changer. Since I'm driven to perpetually learn and better my skills, your earning and development initiatives look wonderful.

While I may not have the most experience of your applicants, I have that much more drive to prove myself. I promise to be a positive, dedicated, and resourceful software engineer at Highwing.

Thanks,

Alice

--

Discord helped me maintain a community during this pandemic. Discord is a VoIP where people connect in text or voice chat in different servers, where screen shares for gaming or movie nights allowed my friendships to survive even with physical distancing. 

It's streamlined and intuitive with depth for those interested in augmenting basic functionality. Plus it's widely supported on mobile and web platforms and uses Electron for that sleek app experience. I love that they made barrier to entry low to get people on board and I can hold a variety of 'fun groups' and 'Slack-like learning or business groups' in the same place.----


-----

Dear Color Team,

COVID hurts and feeling impotent to help sucks. Being part of your work to help testing programs and start tackling some of those long-standing healthcare and access issues would be an honor.

I'm a career changer coming out of customer service into front-end development, and I'm eager to broaden my tech stack so I can contribute to a smooth experience from end to end. Diminishing the burden on customer service teams or support techs dealing with unreliable products is something my background makes me passionate about, and it's even more vital in healthcare.

I'm eager to prove myself as a developer and I'm confident in my ability to find solutions for users (people come first), consult teammates, maximize resources, and try endlessly and persistently to create a product that tangibly helps. I don't have the back-end stack experience yet but in the front-end I can use React (and off-the-shelf components judiciously), HTML5, CSS3, and ES6+. 

I'm especially interested in building out accessible, interactive user experiences and physician tools. Plus, genetic testing and care is very important to me given some family circumstances, and I'm beyond thrilled you are prioritizing that.

Thank you for your consideration and all the work you do!

Best, 

Alice
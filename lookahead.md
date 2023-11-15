# A call to action: I'm looking for contributors for the Lookahead semester planner

Hi, this is a bit of information about a project I'm brewing up. I'd like to revive Lookahead, the University of Melbourne semester planner.

![Untitled](/assets/portfolio/Untitled.png)

A bit of lore first. The original Lookahead is unfortunately no longer on the internet, and was developed by a Rohyl J. who to the best of our knowledge is now working at Optiver. It was great at what it did, and served a valuable role in the University of Melbourne community as a way to organise timetables - Allocate+ just wasn't cutting it for people with more complex timetable layouts.

Unfortunately, in 2023, the University decided to change the way timetable data was accessible. Unlike previously, it was no longer public; now, students must first log-in with their student accounts before being able to access data.

This was, predictably, a death sentence for Lookahead. The application required being able to access... well, timetables. Now, the server could no longer query when your Wine Tasting 'pracs' would be, which meant that you had no choice but to revert back to the horrors of Allocate+ and - for some people - the inhumanity of a spreadsheet. Shudder.

Luckily, a couple of people came in and saved the day... kinda. I was one of those people! We figured out how to simulate the authentication flow. The server was no longer a random internet stranger trying to figure out when Wine Tasting classes were held, it was now (supposedly) a student who was just oddly obsessed with Wine Tasting. The fork can be found [here](https://theepiccowoflife-lookahead.herokuapp.com/).

But this was a band-aid over old code. Unfortunately, Lookahead was showing its age and while we were able to monkeypatch it, it broke soon after. While we could take the easy way out and spend a couple of days fixing it up, we felt like it was time to sit down and re-architect the codebase so it would be maintainable for us and for future students who would assume responsibility for the codebase.

So that's where you come in. I want to get together a band of warriors to rewrite some of the original code (see here: original [GitHub](https://github.com/Trontor/lookahead/) and Quang's [fork](https://github.com/theepiccowoflife/lookahead/)), fix up the issues, who knows, maybe make it prettier.

This project sounds like a great opportunity to contribute to the wider university community, provide a basic human right to students, and get portfolio experience. I'm not looking for programming experts, just people with passion and a desire to learn new things - projects are the best way to improve and gain experience. If you've done second-year computer science subjects like OOSD, DS, A&DS/DoA, you'll (probably) be fine. We'll allocate responsibilities for everybody separately, but here are some things you might get to work on and learn about:

- Front-end with React or, if we choose to rewrite, whatever shiny framework is the most exciting
- We'll either get to work in Python or Rust on the backend, depending on demand. Rust is shiny, super exciting, cultish, and a lot of fun.
- Learning how to write an API in the backend
- Database work, maybe? Possibly in Redis or something, but it depends on whatever technology is most appropriate.
- Continuous integration and how to produce production code, including things like unit testing
- Hosting codebases on the 💭 cloud 💭
- Using GitHub in a collaborative manner, using branches and pull requests to isolate features and invite peer review
- Work in a team with other cool people, doing unpaid labour, to provide a service the University doesn't want to. I anticipate anywhere from a few hours per week to however many you want to spend; workload will depend on how much interest I get.
- You get to be my friend 🤩🗿😭

I'm looking for a team of between 5 and 10 fellow collaborators. So, if you're interested, get in touch with me on Discord (@denosawr) or flick me an email at contact [at] olliecheng [dot] me!

- Ollie
---
layout: post
title: Startup Checklist
permalink: notes/startup-checklist/
---

<style>
ul { padding: 0 }

ul li {
  list-style-type: none;
  color: #000;
}

#all_controls a {
  font-weight: bold;
}
</style>


<script>
$(function(){

$('#result_checked').html('0');
var check_count = $('input[type="checkbox"]').length;
$('#result_total').html(check_count);
$('#result_percent').html('0');

$(document).on('click', 'input[type="checkbox"]', function(){
  updateResult();
});

$(document).on('click', '#select_all', function(){
  $('input[type="checkbox"]').prop('checked',true);
  updateResult();
  return false;
});

$(document).on('click', '#clear_all', function(){
  $('input[type="checkbox"]').prop('checked',false);
  updateResult();
  return false;
});

function updateResult(){
  var checked_count = $('input[type="checkbox"]:checked').length;
  $('#result_checked').html(checked_count);
  $('#result_percent').html(((checked_count / check_count) * 100).toFixed(0));
}

});
</script>

---

#### A checklist of things that are usually important if not necessary for starting a startup. Some items are more or less important than others and it's hard to tell from this simple checklist, so have a look at the original sources for context and nuance.

Based on Sam Altman's talks on "[Ideas, Products](http://tech.genius.com/Sam-altman-lecture-1-how-to-start-a-startup-annotated), [Teams and Execution](http://tech.genius.com/Sam-altman-lecture-2-ideas-products-teams-and-execution-part-ii-annotated)", part of his course [CS183B "How to Start a Startup"](http://startupclass.samaltman.com/) at Stanford University.

<div id="all_controls">
  <button id="select_all">Select all</button> - <button id="clear_all">Clear</button>
</div>

<br/>

## General

* <input type="checkbox"> You are aiming for [hyper growth](http://www.paulgraham.com/growth.html).
* <input type="checkbox"> You're aiming for a great idea, a great product, a great team, and great execution.
* <input type="checkbox"> You are not starting a startup just for the sake of doing so.
* <input type="checkbox"> You feel compelled by a particular problem and think starting a company is the best way to solve it.


## Idea

* <input type="checkbox"> If you've pivoted, you pivoted into something you yourself wanted, not a random made up idea.
* <input type="checkbox"> You think through the size and the growth of the market, the growth strategy for the company, the defensibility strategy, and so on, not just the product.
* <input type="checkbox"> You have an idea that can develop in interesting ways.
* <input type="checkbox"> You have an idea that can someday become a business that is difficult to replicate.
* <input type="checkbox"> You think: idea first, startup second.
* <input type="checkbox"> You are mission oriented.
* <input type="checkbox"> You have an important mission and a great founding idea.
* <input type="checkbox"> You're willing to spend ten years on the startup.
* <input type="checkbox"> You love and believe in what you're building.
* <input type="checkbox"> You aren't just copying an existing idea with very few new insights.
* <input type="checkbox"> Your idea sounds bad.
* <input type="checkbox"> Your idea looks terrible at the beginning.
* <input type="checkbox"> You're going to find a small market in which you can get a monopoly and then quickly expand.
* <input type="checkbox"> You can say something like, "Today only this small subset of users are going to use my product, but I'm going to get all of them and in the future almost everyone will use my product."
* <input type="checkbox"> You have conviction in your own beliefs, and a willingness to ignore others' naysaying.
* <input type="checkbox"> Most people think your idea is bad.
* <input type="checkbox"> You can say, "I know it sounds like a bad idea, but here's specifically why it's actually a great one."
* <input type="checkbox"> You sound crazy, but you are actually right.
* <input type="checkbox"> You have an idea that not many other people are working on.
* <input type="checkbox"> You will take over a small specific market and expand from there.
* <input type="checkbox"> Your idea is unpopular but right.
* <input type="checkbox"> You have taken the time to think about how the market's going to evolve.
* <input type="checkbox"> You have a market that's going to be big in ten years.
* <input type="checkbox"> You have thought about the growth rate of the market, and if there's any reason that it's going to top out.
* <input type="checkbox"> You have a market that's going to grow really quickly.
* <input type="checkbox"> This is the perfect time for this particular idea and to start this particular company. It couldn't have been done 2 years ago, and 2 years in the future will be too late.
* <input type="checkbox"> You're building something that you yourself need.
* <input type="checkbox"> If you don't need it yourself, you're at least very, very close to your customers.
* <input type="checkbox"> Your startup idea is very easy to explain and very easy to understand.
* <input type="checkbox"> It doesn't take more than a sentence to explain what you're doing.
* <input type="checkbox"> Your idea is either very different from existing companies in one important way, or totally new.
* <input type="checkbox"> Your company is not a clone of something else that already exists, with some small or made up differentiator.
* <input type="checkbox"> You have thought about the market first, and what people want first.


## Product

* <input type="checkbox"> You are turning a great idea into a great product.
* <input type="checkbox"> Most of your time is spent either sitting in front of the computer working on the product or talking to customers.
* <input type="checkbox"> You are building something that users love.
* <input type="checkbox"> You work on the product, talk to users, exercise, eat, and sleep, and very little else.
* <input type="checkbox"> You are not making something that people merely like.
* <input type="checkbox"> You are aiming to build something that a small number of users love, rather than a large number of users like.
* <input type="checkbox"> You're getting growth by word of mouth.
* <input type="checkbox"> Your users tell their friends about it and you see organic growth.
* <input type="checkbox"> If you're not growing, you don't think it's OK.
* <input type="checkbox"> You are not trying to build a growth machine before you have a product that some people really love.
* <input type="checkbox"> You are not worrying about your competitors raising a lot of money and what they may do in the future.
* <input type="checkbox"> You are starting with something simple.
* <input type="checkbox"> Your product does one thing extremely well.
* <input type="checkbox"> You are fanatical about your product, the quality of small details, customer support, etc.
* <input type="checkbox"> You feel physical pain when the product sucks, and you want to wake up and fix it in the middle of the night.
* <input type="checkbox"> You don't ship crap, and if you do you fix it very, very quickly.
* <input type="checkbox"> You recruit users by hand.
* <input type="checkbox"> You [do things that don't scale](http://www.paulgraham.com/ds.html).
* <input type="checkbox"> You get users manually with the goal to get a small group of them to love you.
* <input type="checkbox"> You understand that group extremely well, and get extremely close to them.
* <input type="checkbox"> You are building an engine in the company that transforms feedback from users into product decisions, then get it back in front of the users and repeat.
* <input type="checkbox"> You ask users what they like and what they don't like and watch them use the product.
* <input type="checkbox"> You ask users what they'd pay for, if they'd be really bummed if your company went away, what would make them recommend the product to their friend, if they've recommended it to any yet.
* <input type="checkbox"> You make this feedback loop as tight as possible.
* <input type="checkbox"> You don't put anyone between yourself and your users.
* <input type="checkbox"> You have this loop embedded in the culture.
* <input type="checkbox"> You use metrics to keep yourself honest.
* <input type="checkbox"> The CEO decides to measure something and that's what gets built.
* <input type="checkbox"> If you're building an Internet service, you ignore things like total registrations. You look at growth in active users, activity levels, cohort retention, revenue, net promoter scores, these things that matter.
* <input type="checkbox"> You are brutally honest if your metrics aren't going in the right direction.


## Team

* <input type="checkbox"> You treat choosing co-founders as one of the most important decisions you make in the life of your startup.
* <input type="checkbox"> You are not choosing a random random co-founder, or choosing someone you don't have a long history with, or choosing someone you're not friends with.
* <input type="checkbox"> You met your co-founder in college.
* <input type="checkbox"> You met your co-founder at an interesting company.
* <input type="checkbox"> You would choose to have no co-founder rather than to have a bad co-founder.
* <input type="checkbox"> You are not a solo founder.
* <input type="checkbox"> You have "[relentlessly resourceful](http://www.paulgraham.com/relres.html)" co-founders.
* <input type="checkbox"> Your co-founders are unflappable, tough, they know what to do in every situation. They act quickly, they're decisive, they're creative, they're ready for anything. They're like James Bond.
* <input type="checkbox"> You're more interested in a co-founder that behaves like James Bond than you are in someone that is an expert in some particular domain.
* <input type="checkbox"> You have known your co-founders for awhile, ideally years.
* <input type="checkbox"> Your co-founder is tough and a calm, especially if you feel you yourself aren't.
* <input type="checkbox"> If you aren't technical you have a technical co-founder.
* <input type="checkbox"> You don't say, "We don't need a technical co-founder, we're going to hire people, we're just going to be great managers."
* <input type="checkbox"> If you are a software company, you are software people. If you are a media company, you are media people.
* <input type="checkbox"> You are a two or three founder team.
* <input type="checkbox"> You are not a five founder team.
* <input type="checkbox"> You try not to hire.
* <input type="checkbox"> You are proud of how few employees you have.
* <input type="checkbox"> You are proud of how much you can get done with a small numbers of employees.
* <input type="checkbox"> At the beginning, you only hire when you desperately need to.
* <input type="checkbox"> When you hire, you hire people that believe in the company almost as much as you do.
* <input type="checkbox"> You have a culture of extremely dedicated people that come together when the company faces a crisis.
* <input type="checkbox"> You have an extremely high bar, you hire slowly and ensure that everyone believes in the mission.
* <input type="checkbox"> When you're in hiring mode, hiring the best people is your number one priority.
* <input type="checkbox"> You don't underestimate how hard it is to recruit.
* <input type="checkbox"> To recruit the best people, you can convince them that your mission is the most important of anything that they're looking at.
* <input type="checkbox"> You spend either zero or twenty-five percent of your time on hiring. You're either not hiring at all or it's probably your single biggest block of time.
* <input type="checkbox"> You do not compromise and hire someone mediocre.
* <input type="checkbox"> For everyone you hire, you think: will I bet the future of this company on this single hire?
* <input type="checkbox"> You hire people that you already know or that other employees in the company already know.
* <input type="checkbox"> When you're hiring someone that is going to run a large part of your organization, you hire someone with experience.
* <input type="checkbox"> For most of the early hires that you make at a startup, you hire for aptitude and belief in what you're doing over experience.
* <input type="checkbox"> When you hire you ask yourself, is this a role where I care about experience or not?
* <input type="checkbox"> You look for these three things in a hire. Are they smart? Do they get things done? Do I want to spend a lot of time around them?
* <input type="checkbox"> You prefer to hire people you've worked together with in the past.
* <input type="checkbox"> If you haven't worked together in the past, you work with them on a project for a day or two before hiring them.
* <input type="checkbox"> When hiring you try to work on a project together instead of an interview.
* <input type="checkbox"> If you interview, you ask specifically about projects that someone worked on in the past.
* <input type="checkbox"> You don't bother with brainteasers in interviews.
* <input type="checkbox"> In interviews, you really dig in to projects people have worked on.
* <input type="checkbox"> When hiring, you call some people that the candidate has worked with in the past, and you really dig in: Is this person in the top five percent of people you've ever worked with? What specifically did they do? Would you hire them again? Why aren't you trying to hire them again?
* <input type="checkbox"> You hire people with good communication skills.
* <input type="checkbox"> You don't hire people who can't communicate clearly.
* <input type="checkbox"> For early employees you hire someone that has somewhat of a risk-taking attitude.
* <input type="checkbox"> You hire people who are maniacally determined which is slightly different than having a risk tolerant attitude, so you look for both.
* <input type="checkbox"> You can describe any employee as "an animal at what they do." Unstoppable people. People that are just going to get it done.
* <input type="checkbox"> You hire people that you'd be comfortable hanging with socially and you'd be comfortable reporting to if the roles were reversed. You don't have to be friends with everybody, but you at least enjoy working with them. If you don't have that, you at least deeply respect them.
* <input type="checkbox"> If you don't want to spend a lot of time around people, you trust your instincts about that.
* <input type="checkbox"> As a rough estimate, you aim to give about ten percent of the company to the first ten employees.
* <input type="checkbox"> You fight with investors to reduce the amount of equity they get and you're as generous as you possibly can be with employees.
* <input type="checkbox"> After you hire employees, you retain them. You make sure they are happy and feel valued.
* <input type="checkbox"> You learn a little bit of management skills to help you retain employees.
* <input type="checkbox"> You don't tell your employees they're fucking up every day unless you want them all to leave.
* <input type="checkbox"> You really praise your team.
* <input type="checkbox"> You let your team take credit for all the good stuff that happens, and you take responsibility for the bad stuff.
* <input type="checkbox"> You don't micromanage. You continually give people small areas of responsibility.
* <input type="checkbox"> As a first-time founder you are aware that you will be a very bad manager and you try to overcompensate for that.
* <input type="checkbox"> You offer these three things that motivate people to do great work: autonomy, mastery, and purpose.
* <input type="checkbox"> You fire fast when it's not working.
* <input type="checkbox"> In addition to firing people who are doing bad at their job, you fire people who are a) creating office politics, and b) who are persistently negative.
* <input type="checkbox"> If an employee screws up once or twice or more times than that, you are very loving, and you don't take it out on them. You are a team, you work together.
* <input type="checkbox"> If someone is getting every decision wrong, that's when you act.
* <input type="checkbox"> As co-founders you decide on the equity split ideally very soon after you start working together.
* <input type="checkbox"> The equity split is near-equal.
* <input type="checkbox"> You have the ink dry on this before the company gets too far along, certainly in the first number of weeks.
* <input type="checkbox"> Every co-founder, including yourself, has vesting: four years to earn all of your equity and the clock starts one year in.
* <input type="checkbox"> You aren't remote co-founders.


## Execution

* <input type="checkbox"> You know that execution is the most critical part of running the company.
* <input type="checkbox"> You know that being a co-founder means signing up for this year's long grind on execution and you can't outsource this.
* <input type="checkbox"> In order to have a company that executes well, you execute well yourself.
* <input type="checkbox"> If you want a culture where people work hard, pay attention to detail, manage the customers, are frugal, you do it yourself.
* <input type="checkbox"> You don't hire a COO to execute while you go off to conferences.
* <input type="checkbox"> The company sees you as this maniacal execution machine.
* <input type="checkbox"> The CEO 1) sets the vision, 2) raises money, 3) evangelizes the mission to people you're trying to recruit (executives, partners, press, everybody), 4) hires and manages the team, and most critically 5) sets the execution bar by example.
* <input type="checkbox"> You can figure out what to do and you can get it done.
* <input type="checkbox"> When you've figured out what to do, you get it done with focus and intensity.
* <input type="checkbox"> You identify the right two or three things competing for your attention every day, work on those, and ignore, delegate, or defer the rest.
* <input type="checkbox"> You figure out what the two or three most important things are, and you just do those.
* <input type="checkbox"> You say no a lot. You say no ninety-seven times out of a hundred, and you make a very conscious effort to do this.
* <input type="checkbox"> You don't just work really hard, you work really hard at the right things.
* <input type="checkbox"> To figure out what to focus on each day, you have goals.
* <input type="checkbox"> You have a set of small overarching goals for the company that everybody in the company knows.
* <input type="checkbox"> Everyone in the company can tell you each week what are our key goals, and everybody executes based off of that.
* <input type="checkbox"> The founders set the focus. Whatever the founders care about, whatever the founders focus on, that's what sets the goals for the whole company.
* <input type="checkbox"> The founders repeat these goals over and over, far more often than they think they should need to. They put them up on the walls, they talk about them in one on ones and at all-hands meetings each week.
* <input type="checkbox"> You achieve focus with good communication.
* <input type="checkbox"> You never lose focus on maintaining growth and momentum.
* <input type="checkbox"> You always know how you're doing against your metrics, you have a weekly review meeting every week, and you are extremely suspicious if you're ever making excuses for lack of growth.
* <input type="checkbox"> You have the right metrics and you are focused on growing those metrics and having momentum. You don't let the company get distracted or excited about other things.
* <input type="checkbox"> You don't get excited by your own PR.
* <input type="checkbox"> Co-founders are in the same space.
* <input type="checkbox"> You work at a fairly intense level.
* <input type="checkbox"> You have extreme focus and extreme dedication.
* <input type="checkbox"> You have a startup and no more than one other thing.
* <input type="checkbox"> You are willing to outwork your competitors.
* <input type="checkbox"> You know that a small amount of extra work on the right thing makes a huge difference.
* <input type="checkbox"> You are really intense. The CEO and founders are the most intense.
* <input type="checkbox"> You have great execution speed and relentless operating rhythm.
* <input type="checkbox"> You move fast and you're obsessed with quality.
* <input type="checkbox"> You have a culture where the company has really high standards for everything everyone does, but you still move quickly.
* <input type="checkbox"> You move fast and break things, you're frugal in the right places, but you care about quality everywhere.
* <input type="checkbox"> You set a quality bar that runs through the entire company.
* <input type="checkbox"> You are decisive.
* <input type="checkbox"> You don't spend a lot of time talking about grand plans but never make a decision.
* <input type="checkbox"> You have a bias towards action.
* <input type="checkbox"> You work on things that seem small but you move really quickly. You get things done really quickly.
* <input type="checkbox"> Every time someone outside the company talks to you, you've gotten new things done.
* <input type="checkbox"> You do big things in incremental pieces.
* <input type="checkbox"> You pick the right size projects. Even if you have huge goals, you still break it into smaller projects.
* <input type="checkbox"> You respond to e-mail quickly, you make decisions quickly, you're generally quick in all of these ways.
* <input type="checkbox"> You have a "do whatever it takes" attitude.
* <input type="checkbox"> You show up a lot. You come to meetings, you come in, you meet people in person. You get on planes in marginal situations.
* <input type="checkbox"> You want to be winning all the time.
* <input type="checkbox"> You always keep momentum, it's the prime directive for managing your startup.
* <input type="checkbox"> If you're a software startup, you keep growing. If you're a hardware startup, you don't let your ship dates slip.
* <input type="checkbox"> You get the product right at the beginning in order to not to lose momentum later.
* <input type="checkbox"> If you do lose momentum, you don't give long speeches about vision for the company and try to rally the troops with speeches. You save the vision speeches for when the company is winning.
* <input type="checkbox"> When you're not winning, you get momentum back in small wins. You figure out where you can get these small wins and you get that done.
* <input type="checkbox"> If you have momentum sag and there's disagreement among the team about what to do, you ask your users and you do whatever your users tell you.
* <input type="checkbox"> You remind people: "Hey, stuff's not working right now, we don't actually hate each other, we just need to get back on track and everything will work." You call it out, you acknowledge it.
* <input type="checkbox"> In order to keep momentum you establish an operating rhythm at the company early. You ship product and launch new features on a regular basis. You review metrics every week with the entire company. You use your board as a forcing function to get the company to care about metrics and milestones.
* <input type="checkbox"> You don't let competitors disrupt momentum.
* <input type="checkbox"> You don't worry about a competitor at all, until they're actually beating you with a real, shipped product.
* <input type="checkbox"> You remind your company that it's easier to write a press release than to write code, or build a great product. You don't let the company get down because of the competitors in the press.

---

## Result

### <span id="result_checked"></span> checked out of <span id="result_total"></span> (<span id="result_percent"></span>%)

<br/>
<br/>
<br/>


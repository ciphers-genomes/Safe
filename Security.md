Break It to Make It: Security Session Plan
Session overview
A 50-minute activity that follows the security lead's talk, using the TRIZ format to make security concepts click for apprentices who've only just started coding. Instead of asking how to build something securely, tables compete to make an app as insecure as possible, then map their ideas to the OWASP Top 10 and fix them.
No coding knowledge is needed. Every idea can be expressed in everyday terms ("anyone can see anyone else's order"), and the OWASP cards come with plain-English explanations and real-world analogies.
By the end, apprentices will be able to:
• Explain in their own words what a handful of common security risks are
• Recognise that the OWASP Top 10 is a list of common ways software goes wrong, not an exam to memorise
• Suggest a simple fix for at least one risk
• Feel comfortable asking "Is this secure?" about their own code
Materials: Printed app brief (one per table), printed OWASP sorting cards (one set per table), sticky notes, marker pens, flipchart, and a visible timer.
Room set-up: Tables of four, same as yesterday. Mixing people up from yesterday's groups works well.
Run of show
Start
Length
Section
Format
0:00
5 min
Set-up and app brief
Whole group
0:05
15 min
Step 1: Make it worse
1-2-4-All stages
0:20
12 min
Step 2: Sort into OWASP
Tables with cards
0:32
8 min
Step 3: Be honest
Tables, then whole group
0:40
10 min
Step 4: Fix it and close
Tables, then whole group
Start times are counted from the end of the security lead's talk.
The app brief: Crust Club
Print this and put one on each table. It's deliberately simple, so apprentices can picture every part of it without knowing how it's built.
Crust Club is a small pizza takeaway's ordering website.
• Customers create an account with their email and a password, save their address and card details, place orders, and see their past orders.
• Staff log in to a separate admin page to see incoming orders, change menu prices, and issue refunds.
• The website is built using lots of free code libraries written by other people, and it's hosted on a cloud server.
• When something breaks, the site shows an error message to whoever is using it.
Your job: make Crust Club as insecure as you possibly can.
Set-up (5 min): Read the brief out loud. Explain that today's goal is the opposite of normal: the worse their ideas, the better. Give one silly example to break the ice, like "The admin password is pizza and it's written on a sticky note on the till."
Step 1: Make it worse (15 min)
TRIZ is a Liberating Structure that flips the problem: list every way to guarantee the worst outcome, then spot which of those things you're already doing. Run the idea generation with yesterday's 1-2-4-All stages so it already feels familiar.
1. 1 (2 min): On your own, write as many terrible ideas as you can, one per sticky note.
2. 2 (3 min): In pairs, share and build on each other's ideas. Aim to make them even worse.
3. 4 (5 min): In your table of four, pool everything and remove duplicates.
4. All (5 min): Each table reads out their single worst idea. Get a laugh, then keep going.
If a table gets stuck, give them a prompt about one part of the brief:
• What could a customer see that they shouldn't?
• How could someone get into the admin page?
• What could go wrong with all those free code libraries?
• What might the error messages give away?
• How could you find out someone had been messing with the site? (Or make sure you never would?)
Accept ideas in everyday language. "Change the number in the web address and you see someone else's order" is a perfect answer, even if nobody in the room knows the technical name for it yet.
Step 2: Sort into OWASP (12 min)
This is where the real names arrive. Each table lays out the ten OWASP cards (at the end of this doc) and places each sticky note on the card it best fits.
• Tell them there's no perfect answer. Lots of ideas fit more than one card, and that's normal; they just pick the closest.
• Anything that doesn't fit a card goes in a "Not sure" pile. These are great questions for the security lead.
• After sorting, ask each table which card has the most sticky notes, and which has none. Empty cards are a good chance for the security lead to give a quick, real example.
The point isn't to memorise the list. It's to see that the Top 10 is just a set of labels for the kinds of mistakes they came up with on their own.
Step 3: Be honest (8 min)
This is the TRIZ twist. Most of the group won't have written real code yet, so frame the question around everyday life and the near future instead:
Which of these terrible ideas could someone do by accident, without meaning to?
Tables put a dot on any sticky note that could happen by accident. Then ask a couple of extra questions:
• Have you ever seen any of these in real life? (A reused password, a website showing a weird error, a shared login at a previous job.)
• Which ones do you think you'd be most likely to do in your first few months?
Model the honesty yourself first, ideally with the security lead: a real (safe to share) mistake each of you made. This connects back to yesterday's psychological safety session, as saying "I could do that" out loud is exactly the behaviour you want.
Step 4: Fix it and close (10 min)
Each table picks their three dotted sticky notes and, for each one, writes the opposite as a simple rule on a fresh note. For example:
Terrible idea
Our rule
Anyone can change the order number in the web address
Always check the order belongs to the person asking for it
The admin password is pizza
Use strong, unique passwords and a second login step for staff
Never update the free code libraries
Keep libraries up to date and only use ones that are well maintained
Error messages show the full technical details
Show a friendly message to users and keep the details in a log
Tables stick their rules on the flipchart. The security lead picks one or two to comment on.
Close (last 2 min): Ask everyone for one thing they'll now look out for in their own code. Point them to the official OWASP Top 10:2025 site, and let them know they'll see these categories again as their skills grow.
OWASP sorting cards
Print each row as a card (one set per table). The names follow the OWASP Top 10:2025; the explanations are simplified for beginners.
Card
In plain English
At Crust Club, this might look like...
A01 Broken Access Control
People can see or do things they shouldn't be allowed to
A customer sees someone else's order, or reaches the staff admin page
A02 Security Misconfiguration
The settings are wrong, often left on the defaults
The admin page still uses the default password it came with
A03 Software Supply Chain Failures
Problems in code or tools you didn't write but rely on
A free library the site uses has a known hole and was never updated
A04 Cryptographic Failures
Secret information isn't scrambled (encrypted) properly
Card details or passwords are stored as plain, readable text
A05 Injection
Typed-in text gets treated as instructions, not just data
Someone types sneaky text into the address box that changes the database
A06 Insecure Design
The plan was unsafe before any code was written
Refunds can be issued with no limit and no second person checking
A07 Authentication Failures
Problems proving who someone is
Unlimited password guesses, or password123 allowed
A08 Software or Data Integrity Failures
Trusting updates or data without checking they're genuine
The site installs an update from anywhere without checking it's real
A09 Security Logging and Alerting Failures
Not noticing, or having no record, when something goes wrong
Menu prices get changed to 1p and nobody finds out for a week
A10 Mishandling of Exceptional Conditions
Unexpected situations aren't handled safely
An error shows the full technical details, or an order goes through when payment fails
Facilitator notes
The biggest risk with brand-new coders is that the jargon makes them feel behind, so keep the technical names until Step 2 and let everyday language carry Step 1.
• Hide the examples at first. Print the cards with only the first two columns for tables. Keep the Crust Club column as your own crib sheet, and use it to nudge tables that are stuck.
• Brief the security lead beforehand. Ask them to keep the talk light on jargon, to stay for the activity and circulate between tables, and to bring one real, safe-to-share story of a mistake.
• Celebrate the terrible ideas. The more ridiculous, the better. Laughter here builds the same safety you worked on yesterday.
• Don't correct too early. If a sticky note is technically fuzzy, let the sorting and the security lead tidy it up later. The aim is engagement, not precision.
• Keep it about defence. The activity is about spotting and fixing risks, not teaching anyone how to attack real systems.
Follow-up
[ ] Photograph the flipchart rules and share them with the group
[ ] Add the rules to the team working agreement from yesterday, if the group wants to
[ ] Revisit the cards once apprentices start writing web code, using their own projects as the "app"

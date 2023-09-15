**STUFF FOR PART 1, PART 2 BELOW**

<!-- Stuff taken from actual feedback to use. -->

Comprehensive set of interviews done with the engineering teams to establish opinions of the current wiki.

**Platform (Team 1)**
*Usage*: Daily
*Primary Purpose*: Documentation, tracking roadmaps and sprint planning.

*Points of failure:*
- Information quality; documentation held outside of platform team can often be outdated.
- Uploading information, including screenshots (not straightforward).
- Navigation, wiki organisation is good, but unless knowlesgeable in the wiki usage, can be hard to find information. 

*Improvements*
- Improve process of uploading assets
- Ensure more consistent documentation updating
- Integration wiki to gitlab, linking code repos and other relevant documentation. 

**Workflow Team (Team 2)**
*Usage*: Daily
*Primary Purpose*: Accessing product URLS and information uploaded by other teams 

*Points of failure:*
- Information quality - accuracy and how up to date it is. 
- Navigation issues - hard to find specific information. Structure isn't intuitive and search isn't good. 
- Lack of structure - pages and content don't appear to consistently align, causing confusion.
- Comparison to other platforms 0 some information is easier to find in gitlab.

*Improvements*
- Improve wiki structure to better navigation. 
- Differentiate teams more clearly to prevent overlap and confusion. 
- Make it easier to upload assets, change data and possible better integrations with gitlab.

**Integrations Team (Team 3)**
*Usage*: Minimal, team shys away due to friction points
*Primary Purpose*: N/A

*Points of failure:*
- Team has resulted to using in-repo documentation.
- Usefulness is 5/10.
- Uploading and embedding images. Major issue. As you have to save an image, then upload, name and embed image. Compared to Confluence's copy-paste, this is a big pain point. 
- Organisation and usability - current wiki doesn't have an intuitive organisational system and ease of use. 
- Linking and integration - no smooth link between wiki and tools like gitlab. 
- Knowledge capture and retrieval - knowledge retention is a challenge as the platform doesn't seem to make it easy or enjoyable for users to input and retrieve information. 

*Improvements*
- Tool transition - use something else. Preference towards Atlassian stack (not possible due to no self-hosted option)
- Intuitive UI - prioritise ease of use, especially concerning the editing of articles and embedding images/diagrams.
- Better integration - seamless integration with other tools like gitlab to help automate some of the linking processes, creating a more cohesive ecosystem.

**CNE Team (Team 4)**
*Usage*: Minimal, team also shys away
*Primary Purpose*: N/A

*Points of failure:*
- Usefulness is undermined by issues of discoverability and outdated content. 
- While users refer to wiki for specific documentation, but wiki discourages them from using it. 
- Team usually go to colleagues for information and use in-repo documentation. 
- Discoverability. finding information is hard. 
- No encouragement for regular updates. 
- Steamline the onboarding - revamp process to allow automatic assignment of editing permissions or notify relevant admins. 
- User management overhaul - introduce a comprehensive user management system with clear permissions. roles and group linkages. 
- Documentation gaps - it's easier to ask for information/store in-repo than use the wiki. 
- Effort vs. Reward is stacked. High effort for minimum reward due to discoverability issues. 
- Onboarding importance - the current onboarding process has been adapted to identify and rectify issues with new user permissions. Highlights user management issues.

*Improvements*
See points of failure.

**Summary**

**Usage Metrics & Habits**

All teams use the wiki, though the frequency varies.
Usage ranges from daily (Platform and Workflow Teams) to less frequently (Integrations and CNE teams).

Common purposes include documentation, tracking roadmaps, planning sprints, accessing portal URLs, and retrieving specific documentation.

**Points of Friction and Complaints**

Information Quality: All teams mentioned concerns with outdated content or its accuracy.

Uploading & Editing: All teams experience challenges in uploading content, especially with images.

Navigation & Discoverability: Both Workflow and CNE teams emphasized difficulty in navigation, structure, and finding information.

Integration & Linking: Integrations and CNE teams highlighted problems with the wiki’s integration with other tools, such as GitLab.

Onboarding & User Management: CNE team pointed out issues with new member permissions and user management.

**Recommendations & Suggestions**

Ease of Use: Make uploading, especially images, and editing more intuitive and user-friendly.

Integrations: Consider integrations with GitLab, Jira, and possibly other platforms.

Documentation Quality: Encourage regular updates and reduce outdated content.

User Management: Overhaul user permissions, roles, and groups to provide better clarity and control.

Search & Discoverability: Enhance search capabilities and improve the wiki's structure to make it more intuitive.

**Other Notable Insights**

Alternative Methods: Teams often resort to other platforms like GitLab or in-repo documentation. The team’s sometimes bypasses the wiki altogether by asking colleagues directly due to a lack of clarity.

Documentation as an Afterthought: There seems to be a mindset challenge across teams, with documentation not always being a priority. Making the wiki easier to navigate might change this.

Feedback on Other Platforms: The Integrations team suggested looking into other tools like the Atlassian stack (Confluence, Jira).

Onboarding: The significance of onboarding is highlighted, with the current process needing improvements.


Created a Word cloud in MS Word using the Pro World Cloud Add On. Enabled me to see the most often used words.



























# The Rework of the Company's Internal Wiki

> *I will add graphics when I get the time!*

Some background on how this project came to exist. I was hired in September 2022 as the Technical Author in the Design Authority department. A really unique role. Not only do I get to write documentation, I get to design, define and research. You could say it's in the realm of Documentation Architecture, just without the job title. When I joined, my manager (who has the job title Design Authority) made it clear that I am the Documentation Authority. Anything and everything documentation related either goes through me or has my input. It's interesting and sometimes quite stressful.

With the role, comes a huge aspect of providing the best experience when it comes to documentation, both internal and external. As the company is quite young (it was founded in 2021), there isn't much being deployed externally. Though there is documentation to go with external-facing products, and has a fairly easy UX for now.

The internal engineering/software dev documentation is all over the place, and my aim is to bring it into one place that is easy to use, easy to access and easy to read. Engineering tried with developing an internal wiki site, but it's clunky and not used because (unsurprisingly) the engineers and developers do not like it. 

Which is where I come in.

### Where to Start

*"Where to start?"* is usually the hardest question to answer. When it came to the existing wiki, it was fairly easy:

Step 1. Talk to the developers/engineers, learn their pain points and what they'd like from an internal wiki.
Step 2. Analyse the existing tool, and become familiar with the pain points raised.
Step 3. Research the existing tool - how often are updates released for the tool, how active is development.

After Step 3. the question *"Can the existing tool be improved to better the UX?"*. Unfortunately for me, the answer was no. With that, let's dive into the current tool in use, the feedback I received and why the answer was **No**.

### Wiki.js, the Feedback and the Consequences

Given by the title of this section, the tool that was already in use is [wiki.js](https://js.wiki/). Considered one of the best wiki generators, I cannot disagree there. It is good... if it's implemented correctly, and you do not need a huge range of features. Wiki.js is quite deceptive when it comes to working with it. If an instance is already set up, most of the difficult parts go away. But the deployment that's used in the company is something that they like; in basic terms, instead of relying on a repository to hold the information, it's sent to a database, stored on an AWS VPC (Virtual Computer), and built/deployed that way.

The problems appear when you start looking at the front facing aspects. Or at least the way it has been implemented in the company (and I could go into the political side of things, but lets just say there is a reluctance to change how it's been set up). This is where the feedback comes into play.

One of the most expressed issues with the current wiki set up was the search functionality being poor. Having used the search functionality myself, it is difficult. That was because the company had decided to use the [PostgreSQL](https://docs.requarks.io/search/postgres) search functionality, because the documentation is being stored in a PosgrSQL database. Even the documentation states it's a *"good enough"* search solution. Personally, I think that's over selling how basic that type of search is. It is basic, can only return full matching searches (so partial searches aren't going to happen), and even then, you're lucky to have any results. Another reason it was chosen was because of the company security policy (we have to be self-hosted, no data can be stored on the cloud or managed by a company other than the one I work at). That in itself makes it very restrictive. Because of the security policy, it made the use of Algolia, AWS Cloudsearch, Azure Search and Elasticsearch impossible. Which is annoying, given they're all supported by wiki.js, and have better functionality. 

The second most expressed issue with wiki.js was the created and publishing of documentation. Wiki.js has an inbuilt editor, where you can write documentation. Because the company uses a PostgreSQL database to store the documentation, there is no repository (e.g. Git), where all the documentation is pushed to for publishing. Which is a big problem in the company, as there is a huge push (including from me) to estabish a doc-as-code mentality. Simply put, the documentation lives with the code it's about and can be published to wherever it needs to go. So to get around this problem, another member of the team I'm in created a tool known as *Scribe* to publish any code to the PostgreSQl database from any company repository. All the developers needed to do what make sure that the Scribe tool was inserted into the Git build pipelines, so the necessary metadata could be added.

So one problem solved, right? No. Developers don't use Scribe. Because the company development is fast and ever changing direction, Scribe can become "broken" at any time. Which means more time is spent of retroactively fixing Scribe. No amount of pushing Engineering/Development teams, giving them live and recorded tutorials is getting them to try and use Scribe. They want a tool that can just pull directly from their repositories, and they don't have to do or add anything else into product build pipelines.

That itself is a whole other can of worms. No amount of UX design, research, instructional training or documentation can make people use a tool they've already decided they do not like. And that is the consequence of not doing proper UX and architecture research before development and deployment. Wiki.js was implemented before I was hired, so it's not like I could've prevented any of this from happening.

From one consequence comes another... The consequence of not doing proper research has led to people not using the wiki at all for their documentation. So Scribe was created to help with that, and noone wants to use it because they do not like wiki.js. So here I am, effectively reinventing the wheel, because instead of just tweaking the wiki.js implementation and creating a business case for doing things such as being able to use a better search funtionality, I'm trying to find a new static site generator that will do everything the company needs, and gives a better experience than the one wiki.js has created. 

So now onto my current problem... finding the tool that can do it all.


> The next post will be a deep dive into the research and comments about potential other tools. Like this one, it's going to be a long post.
>
> 
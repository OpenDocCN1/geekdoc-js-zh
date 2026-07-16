![](resources/title_page.jpg)

![Making Massive Multiplayer Online Games](resources/title_page.jpg)

## Making Massive Multiplayer Online Games

### A Game Development Workbook for any Phaser JavaScript Gaming Framework.

#### Stephen Gose

This book is for sale at [http://leanpub.com/rrgamingsystem](http://leanpub.com/rrgamingsystem)

This version was published on 2020-04-06

![publisher's logo](resources/leanpub-logo.png)

*   *   *   *   *

This is a [Leanpub](http://leanpub.com) book. Leanpub empowers authors and publishers with the Lean Publishing process. [Lean Publishing](http://leanpub.com/manifesto) is the act of publishing an in-progress ebook using lightweight tools and many iterations to get reader feedback, pivot until you have the right book and build traction once you do.

*   *   *   *   *

© Copyright 1972 - 2016 Stephen Gose. All rights reserved.

ISBN for EPUB version: 978-1-952635-00-7

ISBN for MOBI version: 978-1-952635-00-7

For my student@ Early Career Academy, Tempe, AZ

and @ ITT Technical Institute, Tempe, AZ

and more currently

To my students @ University of Advancing Technology (UAT), Tempe, AZ

## Table of Contents

## Guide

1.  [Begin Reading](#chap00.xhtml)

# Distribution Permission

Originally released edition 1.0.0 18 DEC 2013.

All rights reserved. No part of this book may be reproduced in any form or by any electronic or mechanical means including information storage and retrieval systems, without permission in writing from the author. The only exception is by a reviewer, who may quote short excerpts in a review [***as defined here***](https://www.copyright.gov/fair-use/more-info.html).

**NOTE: Book Editions “Bonus Download Content” is available from the book’s website: [http://makingbrowsergames.com/mmog/](http://makingbrowsergames.com/mmog/)** You will find errata information, source code and software updates. Thank you for your patronage.

## Viewing this e-Book

This e-Book includes source code which is optimally viewed **in single-column, landscape mode** with the font size adjusted to a comfortable setting.

# Disclaimer

All the information contained within is for the convenience of its reader. All information is accurate as can be reasonably verified at the time of original publication. However, content suggested may not reflect current industry recommendations after original publication date for [***ECMA-262***](http://www.ecma-international.org/publications/standards/Ecma-262.htm) (also known as — aka — “JavaScript”, ES5, ES6, ES7, ES8 or ES9), ***Phaser Game Framework versions 2.6.2, Community Editions (CE) or Phaser III (as v3.16+ only).*** There are no guarantees nor warranties stated or implied by the distribution of this information. Using the information in this document is at the reader’s own risk, and no liability shall carry to the author. Any damage or loss is the sole responsibility of the reader.

This book’s intent is **not** to teach basic [**HTML5**](http://amzn.to/2nAYjxr), [**CSS**](http://amzn.to/2mG01Zv) nor [**JavaScript fundamentals**](https://amzn.to/2Iw9RZj), game design best practices nor for encoding JavaScript into Object-Oriented Programming (OOP) style. Its content provides simple-to-follow worksheets, step-by-step instructions, and a straight-forward approach to building games from “common component prototypes” using the [***Game Design System™***](http://www.businessdictionary.com/definition/system.html) innovation. This system process and resulting source code are merely one approach; and hence, does not claim to be the best nor most efficient way of implementing these widget-mechanisms and game mechanics.

***Stephen Gose LLC reserves the right, at any time and without notice, to change modify or correct the information contained in this publication.*** All websites listed herein are accurate at the time of publication but may change in the future or cease to exist. It is best to research “dead websites” links on [***“The WayBack Machine”***](https://web.archive.org/) The listing of website references and resources does not imply publisher endorsement of the site’s entire contents.

# Forwards

*   ***by Terry Paton:*** — “Copying or imitating is an awesome way to learn how to do something, traditional artists have done it for centuries. This practice was generally considered a tribute, [not forgery](http://en.wikipedia.org/wiki/Art_forgery), — **If you want to get better at something, then trying to do it like those who already have mastered it.** Look at the choices they have made and consider why they made those decisions, often important things are hidden in subtlety and the only way we learn those subtleties is by creating the same thing. The balance here is `stealing` versus `inspiration`. **“Ripping off” ideas from someone else in a way that harms their hard work compared to producing something which is `inspired by` their work.** If you plan on publicly releasing something, I recommend you should inject some of your own vision into any game you make, take a concept but then extend or change it to create something of your own.”
*   ***by Christer Kaitila: The McFunky-pants Method*** — “Challenge yourself to create a code-base that compiles and runs **in the first few hours.** Make it so that you can accept inputs, move around, animate something, and trigger some sounds. This prototype, lousy a game as it may be, is going to be your best friend. **The sooner you can have a working early playable prototype, the more likely you are to succeed.** No-art prototypes also have one other major advantage: in previous games, I would make beautiful mock-ups in PhotoShop and gather hundreds of lovely looking sprites in preparation for the game. After development was complete, the vast majority of the art had to be replaced, re-sized, or thrown out. **I’ve wasted thousands of hours making [game-ready artwork](https://www.gamedevmarket.net/?ally=GVgAVsoJ) before coding;** these days I know that the tech specs and evolving game-play mechanics will mean that much of what you make at the start won’t make it into the finished game.”

# About this Workbook:

This 5th edition offers new development tools and production methods I call the ***Game Design System™*** in which we’ll create [***MMo Game Recipes™***](https://www.nateliason.com/blog/become-expert-dreyfus). Expert game developers understand the “Don’t Repeat Yourself” (D.R.Y.) concept, yet few have taken a step back to the [***“10,000 foot view” (i.e., “Executive level thinking”)***](https://en.wikipedia.org/wiki/Business_acumen#Executive_level_thinking) on game production pipelines. We’ll do that aerial view in this book as we build prototypes, mechanics and artwork. Along with game construction, we’ll build tools to automate our pipeline. I believe you will be surprised how quickly and easily we’re able to build games using the ***Game Design System™*** with its ***Game Recipes™ tools.*** Although this workbook is intended to be a hands-on guide to HTML5 game development with emphasis on ***any version of Phaser JavaScript Gaming Frameworks.*** Yet, our project management applies ***to any popular game development framework.***

Most of the content in this book is actually **not inside these pages.** The Internet is a living, dynamic resource of information that doubles every 35 days! I explain why this book refers to external resources in the [“Book Formatting”](#chap06.xhtml_bkformat) Section below. You’ll find the external content in the footnotes, as reference links, and in the **Bonus Content files** (which are available from the supporting website or from your **LeanPub.com personal library.** Therefore, if you purchased this book from:

*   **LeanPub.com —** you have a perpetual edition available in your library.
*   **Amazon.com —** you may access the latest information from our website.

**[http://makingbrowsergames.com/mmog/](http://makingbrowsergames.com/mmog/)**

All the source code is written in “pure JavaScript” or either ***Phaser JS Framework;*** it doesn’t use any additional “abstraction layers” such as TypeScript, CoffeeScript, or JQuery. JSLinting, minification, compression, obfuscation, and security topics are discussed in the “Marketing & Distribution” Chapter.

I’ve [gone to great lengths](https://dictionary.cambridge.org/us/dictionary/english/go-to-great-lengths) to make this book “skim-friendly” ***— even for my International customers.*** I have provided links to [***“English (American) Jargon phrases”***](https://www.umass.edu/ipo/sites/default/files/slang.pdf) that will help translate this content directly into your native language. The entire new 4th edition has more screen shots, step-by-step worksheets, thoroughly annotated source code listings, illustrations, and diagrams. I use “Notes”, “Tips”, “Warning” and “Best Practices” icons to encapsulate those ancillary topics for your further education from other experts in the gaming industry.

I assume that many readers will want to use this book as a reference (as demonstrated from the previous three editions) as well as a tutorial workbook. So, I’ve included references to other games, gaming engines, frameworks, indie developers, authors, their “open source” contributions, their articles, books, artwork, applications tools and their wisdom. **If you’d like a link to your content included in future updates, please use my contact information on [LeanPub.com](https://leanpub.com/u/pbmcube) or [Amazon.com Author’s page](https://www.amazon.com/kindle-dbs/entity/author/B01N780CUF?_encoding=UTF8&node=283155&offset=0&pageSize=12&sort=author-pages-popularity-rank&page=1&langFilter=default#formatSelectorHeader); see the next section.**

# Disclosures

In this book, I am not paid to recommend any of the tools or services presented but I do use affiliate links. Here’s how it works. When I find a tool, service, author’s content, idea, or product I admire, I investigate if they have an affiliate program. If it exists, I get a special link and when you click it or confirm a purchase I receive a small percentage from that activity. In short, it’s the same methods everyone finds on any typical website; only now, those reference links are available inside ebooks.

I think everyone, with [***any business savvy,***](https://www.inc.com/neil-patel/11-mental-habits-that-will-improve-your-business-savvy.html) should do this too; especially when you recommend books, services, and tools to your own products. Amazon and other publishers offer affiliate links. Whenever you recommend anything **(hopefully this book? hint, hint!),** use your Amazon affiliate link.

By law, I must disclose that I am are using affiliate links. Amazon, in particular, requires the following.

> *“We are a participant in the Amazon Services LLC Associates Program, an affiliate advertising program designed to provide a means for us to earn fees by linking to Amazon.com and affiliated sites.”*

Thank you for your patronage! I truly appreciate it.

# Workbook Content:

This workbook is a hands-on guide to HTML5 game development with an emphasis on either ***Phaser JavaScript Gaming Frameworks for Multi-Player networked games implementing WebSockets.*** By following my steps toward developing a complete massive multi-player online game (MMoG) using game prototypes, you will translate my process into your own [***bespoke***](https://www.urbandictionary.com/define.php?term=bespoke) game design product(s) in a matter of hours! I will explain my rationale behind each decision so that you can adapt my methods into your products’ pipeline in a similar manner. When you finish this workbook and all the exercises, **unlike every book on the market today, you should have a working copy of your own [*bespoke*](https://www.urbandictionary.com/define.php?term=bespoke) game — not merely a duplicate copy of mine!** Several well-known multi-player game servers are provided as “back-end services” to scaffold your game production; this provides a [***better than agile-software development process***](https://www.linkedin.com/pulse/scrum-makes-you-dumb-daniel-jones/) to bootstrap your game productions quickly into your own unique product releases. The appendices are reference guides into the necessary, free, and open-source assets. Here are the main topics we cover in the **NEW 4th Edition’s content:**

*   MMoG ***network issues and troubleshooting.***
*   **WebSockets without the processing “overhead”.**
*   Converting Single-player games with AI into MMoGs.
*   Step-by-Step worksheet tutorials for several games.
*   Game Generation Tools construction for ***“Game Recipes™”.***
*   Game Category alignment with App Stores and the gaming industry.
*   **Distribution and Marketing:** who, where, and how to deploy finished game products with supporting data from current marketing analysis.
*   **Coding Style Appendix:** Migration away from classical OOP to [***OLOO compositions***](https://www.datchley.name/understanding-prototypes-delegation-composition/) (A section for interested Senior Programming Engineers and the rationale on why and how. **OR** you could consume the [***“You don’t know JS”***](https://github.com/getify/You-Dont-Know-JS) series.)
*   **“The Deeper Dive:”** dedicated sections for interested Software Engineers concerning various aspects of Phaser JS Gaming Frameworks.
*   The ***Game Design System™*** development methods for Software Project Management.

**Part I. Network Concepts and Design** (Chapters 1 to 3): Chapter 1 is dedicated to the indie game studio start-up and those from a game hobbyist to any commercial endeavor. Appendix — US Business start-ups supports Chapter 1\. ***If you are thoroughly comfortable with your workstation environment, you may skip Chapter 2 entirely.*** Chapter 2 guides you in setting-up a valid testing environment. ***Chapter 3 is about “Data telecommunications 101”. If you are thoroughly comfortable with networking aspects and recent WebSockets technology, you may skip Chapter 3 entirely.***

**Part II. MMoG Application Architecture** (Chapters 4 & 5): Chapter 4 is ***a critical path and foundation chapter*** in MMoG Engine Analysis and evaluation. It [***lays the ground work***](https://www.macmillandictionary.com/us/dictionary/american/lay-the-groundwork-for-something) for future chapters. **Chapter 5 reveals an innovative approach and reviews a missing aspect in current MMoG development tutorials.** It further lays the foundation for Multi-Player Game Prototypes based on the ***Game Design System™.***

**Part III. Production and Deployment.** This content is what your Phaser tutorials and Phaser Starter-Kits on the market today overlook and never tell you! Topics include preparing a game product for various distribution or marketing channels, pricing, and international marketing efforts.

**Part IV. Walk-through Examples** provides several ***FREE game licenses*** ([***valued at $48 each***](http://shop.pbmcube.net/)). we’ll take our crafted “Part I game components” and apply “Part II game mechanic logic/rule systems.” I demonstrate “separation of concerns”, and my method for rapid game generation using my unique ***“Game Recipes™” from the Game Design System™ for three (3) different styles of MMoGs. Included are FREE Life-time EULA for each example.***

**Part V. Appendices, Resources and Supporting Website** available online @ **[http://makingbrowsergames.com/mmog/](http://makingbrowsergames.com/mmog/)**

**Bonus Content Courses:** The [***Ultimate***](https://leanpub.com/set/leanpub/ugsskitc) and [***Basic***](https://leanpub.com/set/leanpub/gsskit) Game Studio Starter Kit Collection Certification Courses are available.

# Book formatting:

**Editor’s Note: “Why have separate external links and files?”, you say?**

*   **Firstly,** the WWW is a dynamic place with new content and methods appearing daily. In 1997, the Internet doubled its information every 7 years; by 2015, the Internet doubled its information ***every 35 days!*** What was once the “cutting edge” becomes deprecated and obsolete in a matter of a few years or even months! (**for example, using “window.onload”** initially mentioned in 2004 and now recanted & retracted by the original author!)
*   References linking to external concepts preserve this workbook’s integrity and ***“freshness”*** (and thereby your investment in my research), avoids copyright infringements, and permits featured and referenced authors to recant or update their own recommendations **(as in the case of “using window.onload” and especially in the case** Phaser v3.x.x JavaScript Gaming Framework frequent updates).
*   In general, this book’s narrative shows you how things work, whereas the aside call-outs, footnotes, and reference links delve into **why things work as they do.** It provides valuable information from other notable game industry experts. My research places the best current recommendation in this workbook, and filters out the [***“cruft”.***](https://en.wikipedia.org/wiki/Cruft) **If you follow all my reference links, you’ll have a greater store of knowledge and develop a better understanding about my concepts since we’ll share the same common knowledge foundation.**
*   It shortens my book by hundreds of pages and lowers my publishing costs which then lowers your purchase price. By keeping the associated source code separated into a Bonus Content areas on the supporting website, it allows you to focus on and compare this book’s content discussions side-by-side with the source code. This permits you to read this workbook without interruptions — unlike many technical books to date. ***Now, Admit it, Honestly!*** Don’t you just hate reading miles of **UN-commented, UN-documented source code** only to arrive, finally, dozens of pages later, at the text explaining everything you just studied? Or some authors place their pages of explanation in front of their **UN-commented, UN-documented source code.** Neither method is satisfactory in my opinion. I would rather have the text explanations and source code side-by-side. **Wouldn’t you?**
*   Furthermore, it allows me to update my external online source code and supplements without republication. You are purchasing my months of research, investigations, synthesis, and experiments derived from those investigations as links within this book to its supporting website. I have [***“trail-blazed”***](https://en.wiktionary.org/wiki/trailblaze#English) the path for you to follow. It saves you the time of doing it yourself as you review my original research and learning paths. This is a great benefit for both of us concerning `Phaser v3.x.x` rapid release trends.

# Who should use this workbook?

This workbook is aimed at both the hands-on leaner [***(learn the differences between newly initiated and experts)***](https://www.nap.edu/read/9853/chapter/5) — those who enjoy “learning by experimentation”, and at those [***experienced expert programmers***](https://www.nateliason.com/blog/become-expert-dreyfus) in web application development who know how to make games and are familiar with JavaScript, but have never made an online Multi-Player game; and, of course, those who want a finished MMoG from their own bespoke designs and by their own efforts. If you are interested in making browser MMoG, ***especially for the mobile market,*** then this book is a perfect choice along with its companion volumes for [***Phaser v2.x.x or III:***](https://leanpub.com/u/pbmcube) (books are listed in the upcoming Reference Section below). With this in mind, you will do a lot of writing, thinking, and coding in both HTML5 and JavaScript throughout this workbook. You may prefer using paper (external physical- or soft-“paper”) to organize your development ideas and processes.

This workbook is a tutorial guide into the ***Game Design System™*** method using [**`HTML5`**](http://amzn.to/2nAYjxr), [**`CSS3`**](http://amzn.to/2mG01Zv) and [**`JavaScript`**](https://amzn.to/2Iw9RZj) technologies with **an emphasis on either Phaser III or v2.x.x. (both official and community editions)** I know that many *senior software developers* already have these technologies in their arsenal; but, I have received dozen of email complaints about this book’s former editions as being **“… too difficult for those just starting their own game studios.”** Therefore, ***if learning any of these mentioned technologies is what you are initially seeking,*** then I recommend a quick visit to [***W3Schools***](https://www.w3schools.com/whatis/default.asp) as your **first FREE starting point.** By following their instructions, you will learn a complete foundation in `HTML`, `CSS`, and `JavaScript` **in a matter of hours! … then, return to this workbook and learn how to combine those technologies into your own game creations.**

# Your newly obtained skills…

By the end of this workbook, you’ll have integrated into your own [***bespoke***](https://www.urbandictionary.com/define.php?term=bespoke) game design:

*   The ***Game Design System™*** in which you create [***MMoG Game Recipes™.***](https://www.nateliason.com/blog/become-expert-dreyfus)
*   Organized file structure for rapid game development;
*   Buildt or adapted a networked [***protocol messaging system.***](https://www.chessprogramming.org/Protocols)
*   Imported various **game resources and artwork assets;**
*   Displayed, animated and moved game avatars on various game phases;
*   Managed group containers;
*   Deployed heads-up displays (HUD) both “inside and out from” the `canvas` tag;
*   Used customized web fonts;
*   Incorporated multiple game-inputs;
*   Implemented several physics systems on various components;
*   Defined and Included “game juice”;
*   Created and managed game phases properly using D.R.Y.;
*   Managed permanent game assets across various game phases;
*   Optimized your game for various mobile devices using SWPA, PWA and AMP;
*   Integrated available 3rd-party plugins.
*   Deployed single—player games from the workbooks step-by-step tutorials.
*   Demystified Web Sockets for optimized game deployments.
*   Tested multi—player game development from single—player foundation.
*   Network traffic patterns and inter-actions between clients and servers.
*   Contrasted Node.js, Sockets and or WebSockets technologies and their utilization.
*   Studied project management and agile software development.
*   Analyzing currently available open-source multi-player gaming engines.
*   Comparing network technologies and their impact on multi-player gaming engines.
*   Incorporating sound effects (sfx) and theme music across various game scenes;
*   Rendering several physics systems in a multi-player environment;
*   Incorporating graphics effects (gfx) (particle systems, rotations, fades, shaders and more);

# Bonus Content

***Included with your purchase!***

*   Free Affiliate Guide,
*   Bonus Content Download package.
*   Dynamically updated references, footnotes and supplements.
*   Supporting Website access:

    - ***[http://makingbrowsergames.com/mmog/](http://makingbrowsergames.com/mmog/)***
    - ***[http://makingbrowsergames.com/starterkits/](http://makingbrowsergames.com/starterkits/)***
    - ***[http://makingbrowsergames.com/book/](http://makingbrowsergames.com/book/)***

# Game Design System™ Recipes:

***“Game Recipes™”*** (purchased separately) on specific gaming mechanics using the ***Game Design System™ method*** and concepts (available from [***Amazon.com***](https://www.amazon.com/gp/search/ref=as_li_qf_sp_sr_tl?ie=UTF8&tag=pbmcube-20&keywords=stephen%20gose&index=aps&camp=1789&creative=9325&linkCode=ur2&linkId=35a07e5471ef728a49ce48b6009957ca) or earn your ***Game Development Certifications*** from LeanPub.com courses or [***Zenva Game Academy***](https://academy.zenva.com/?a=47&campaign=PhaserGamePrototyping)):

*   ***Ultimate Game Studio Starter Kit Collection [Certification Tutorials (LeanPub.com)](https://leanpub.com/set/leanpub/ugsskitc) or [(Amazon.com)](https://amzn.to/2qQsq3z)***
*   Action & Arcade (Coming Soon)
*   [***Adventure, Mazes & RPG (Amazon.com)***](https://amzn.to/2vXickO)
*   [***Collapsing Blocks (Amazon.com)***](https://amzn.to/2PniJUX)
*   Connect 4 & Go (Coming Soon)
*   ***Dating Simulations & Quizzes — [Certification Tutorial (LeanPub.com)](https://leanpub.com/c/mbg-dating) or [(Amazon.com)](https://amzn.to/2nP0fjF)***
*   Defensive Towers (Coming Soon)
*   ***Dress Up & Fashion — [Certification Tutorial (LeanPub.com)](https://leanpub.com/c/mbg-dressup-p2) or [(Amazon.com)](https://amzn.to/2MDvEUi)***
*   Hidden Objects (Coming Soon)
*   ***“Jump to Capture” — [Certification Tutorial (LeanPub.com)](https://leanpub.com/c/mbg-peg-p2) or [(Amazon.com)](https://amzn.to/2vWuqdd)***
*   MahJong (Coming Soon)
*   [***Match 3 (Amazon.com)***](https://amzn.to/2MmwTId)
*   [***Memory Match (both pairs & sequence) (Amazon.com)***](https://amzn.to/2OK8JnI)
*   Music & Rhythm (Coming Soon)
*   ***Puzzle (Jigsaw & sliders) — [Certification Tutorial (LeanPub.com)](https://leanpub.com/c/mbg-puzzle-p2) or [(Amazon.com)](https://amzn.to/2vV63Na)***
*   ***Role Playing Games [Certification Tutorial (LeanPub.com)](https://leanpub.com/c/mbg-rpg-p2) or [(Amazon.com)](https://amzn.to/2DC0OYn)***
*   Strategy (Coming Soon)

# Our References:

*   [***Phaser III Game Starter Kit Collection***](https://leanpub.com/p3gskc) 16+ Classic Game mechanics **for Phaser v3.16.x Framework** using the ***Game Design System™*** methodology.
*   [***Phaser III Game Design Workbook***](https://leanpub.com/phaser3gamedesignworkbook) updated edition dedicated to Phaser III and follows the ***Game Design System™*** methodology.
*   [***Phaser III Game Prototyping***](https://leanpub.com/phaser3gameprototyping) is a sister companion to this book for the new Phaser III API. All examples are translated in Phaser III and takes advantage of all the new capabilities.
*   [***Phaser Game Design Workbook***](https://leanpub.com/phaserjsgamedesignworkbook) in the newly revised and expanded 4th Edition. [***3rd Edition remains available***](https://phaser.io/news/2016/11/phaser-game-design-workbook) in paper-back or Kindle on [***Amazon.com***](https://www.amazon.com/Phaser-js-Game-Design-Workbook-development/dp/1520154550) or from [***LeanPub.com***](https://leanpub.com/phaserjsgamedesignworkbook)
*   [***Kiwi Game Design Workbook***](https://leanpub.com/kiwigamedesignworkbook) the grandfather of Phaser III
*   [***Phaser Game Starter Kit Collection***](https://leanpub.com/pgskc) 16+ Classic Game mechanics recipes for Phaser III Framework using the ***Game Design System™*** methodology.
*   [***Phaser Multi-player Gaming Systems***](https://leanpub.com/rrgamingsystem) A ***Massive Multi-Player Online Game Design Workbook*** for HTML5, Phaser and other popular Mobile Gaming Frameworks.
*   [***Phaser Game Prototyping***](https://leanpub.com/LoRD) in its new 4th edition.
*   [***Olymic Game Design System™***](https://leanpub.com/gds) similar to this Phaser Game Design Workbooks but uses other popular ***HTML5 and Unity Gaming Frameworks.***
*   [***Multi-player Gaming Systems***](https://leanpub.com/rrgamingsystem) A ***Massive Multi-Player Online Game Design Workbook*** for HTML5 and other JS Game engines.

## Tweet This Book!

Please help me spread the word about this book on [Twitter!](http://twitter.com/pbmcube)

The suggested hashtag for this book is [#PBMCube](https://twitter.com/search?q=%23PBMCube).

# Part I: Network Concepts and Design

![](resources/makingbrowsergames_com---book---imagesConsolidated---BookCover1.jpg)

Part I: Network Concepts and Design

***This section is optional content based upon your experience.*** It provides a common knowledge foundation so that we are using the same vocabulary, terminology, business/marketing foundation, and WAN methods. I provide this section for those who may need:

*   Guidance on business considerations,
*   Basic networking operations,
*   WebSockets integration,
*   Selecting a proper gaming engine and the process to do so,
*   and finally, a true testing lab and workshop set-up.

***If you are already comfortably with these topics, you can skip ahead to Chapter 2 or Chapter 3.***

# 1 Business Considerations

So, you are thinking about putting a massive multi-player game on the World Wide Web (WWW or “the Web”). Let me share with you my mistakes and triumphs. Whether you’re Web-savvy or techno-phobic, you can use this workbook as a planning tool for your new adventure.

As you’ll discover from this workbook, adding Multi-Player features to any game increases your user’s experiences by introducing various elements of human psychology and social interaction — typically ***NOT*** found in single-player games. **You’ve made a smart choice — [in spite of my friend’s plea!](https://www.gamesindustry.biz/articles/2014-05-02-indies-dont-make-multiplayer-games-dan-marshall)** Yet, adding “Real-Time Multi-Player” features can be tricky to code correctly. Although it may appear complicated, by following my ***Game Design System™*** and ***Game Recipes™*** in Part IV (and avoiding some pitfalls I’ve encountered), you’ll add a new dimension to your gaming products.

So, with this workbook in hand, you have my basic project management examples on how I produce multi-player games. These proven tenets have guided me — and other developers like myself — to grow and succeed in cyberspace commerce. When you complete this workbook ***— unlike any similar book on the market today —***, you should have a working copy of your own unique game — not merely mine nor a duplicate carbon-copy of mine! With that said, you will do **a lot** of translation work as you model your MMoG.

Before we go any further, let’s first determine “Why” you want to create a Mobile Multi-Player Online Game (MMoG). What are your business’ requirements and available resources? Our first workbook exercise is:

*   ***As an academic pursuit?*** In other words, your primary motivation is merely to ***study and experiment with the most cutting-edge technologies.*** I call this the ***“[T]echnical Track “*** in upcoming tutorials in Part IV.
*   ***As a hobbyist?*** In other words, ***generating income is NOT your primary motivation.*** You simply want to “add your ideas onto” or seek the challenge of creating a similar popular game currently in the “apps stores”. I call this the ***“[H]obbyist Track”*** in upcoming tutorials in Part IV.
*   ***As a way of generating revenues?*** In other words, your ***primary motivation is to supplement or replace your current income source(s).*** I call this the ***“[E]ntrepreneur Track”*** in tutorials in Part IV.

Answering this initial question will guide many of your following production decisions. So, go fetch some paper or open a file and record your answers from the question above. **Write your answers down.** Become an active participant, and learn the most important concept — ***“Journaling and logging”.*** By doing so, you are developing a time-line of your activities (i.e., what is easy for you to do, what poses difficulties for you, and who to hire with what skills to fill the void from additional staff). This helps determine the amount of time it takes to put a profitable game into the Web distribution channels. When your customers ask you, “When can I expect a finished product?”; you have proven empirical evidence based your project’s development schedule — not some “pie in the sky”, ***UN-realistic time-frame*** to which so many business fall victim!

## 1.1 Formal Business Launch Required?

Since my workbook is for the general Internet community, many readers may not be interested, already have, or perhaps do not qualify for U.S. business status. The remaining topics are offered as an optional Appendix and fully covers topics for developing a U.S. start-up business.

In order to stay focus on the task at hand (i.e., creating a game using Phaser), I will simply direct you to external sources to answer this question. Yes, you do need to determine whether you will start a formal business now, remain the curious software engineer, or remain a simple indie-developer hobbyist. ***T.H.E. tracks, mentioned above, have supporting “Game Studio Starter Kits” — [(Basic)](https://leanpub.com/set/leanpub/gsskit) or [(Ultimate)](https://leanpub.com/set/leanpub/ugsskitc).***

For U.S. citizens, you will remain in the “hobbyist” status until you meet several government stipulations concerning cash generated and time devoted to your enterprise. In the Appendix, you will find resources for “Business Planning” for both U.S. **and Non-US citizens.**

**NOTE:** It is wise to have a completed “game product” before you beginning a business; you do not want the reputation of “selling blue sky”.

## 1.2 Common Marketing Sense

Let’s examine a hypothetical scenario. Let’s say that…

The chart below — created by the 7th largest game distributor — shows ***where to sell your “squirt guns”*** and the likely success of a game genre for a specific cultural region.

![](resources/bfgblog-a_akamaihd_net---uploads---2015---01---bfg-game-genres-across-the-world-880x660.png)

Game Genres Across the World Know Your Target Audience

Game classification is diverse. “Just as game publishers have convoluted the terminology for “game mode”, game genres are just as confusing. The inconsistency comes from trying to describe the game mechanics, game delivery and details associated with the game theme.” [***Phaser Game Starter Kit Collection***](https://leanpub.com/pgskc) or single chapters available from Amazon.com. [***Game Genres***](https://en.wikipedia.org/wiki/List_of_video_game_genres) are specific game categories related by ***similar gameplay characteristics.*** Remember that gameplay **IS** the “rules of a game”. Single-player and multi-player are therefore not game genres. They are a “delivery” mechanism dictating the “mode” of gameplay.

It is obvious that world-wide the “Action Games” genre is the likely choice for MMoG development followed by regional preferences for “Shooter” (in EUR and US) and “RPG” (in Asia) genres. What it **does NOT tell us** is the “return on investment (ROI)”. [***Amir Rajan***](http://amirrajan.net/about/) is quite transparent in his excellent book — a development journal of his progress, [“**Surviving The App Store** — *How to Make It as an Indie Game Developer*”](https://github.com/MakingBrowserGames/survivingtheappstore) and read this [***book review from Gamasutra.***](https://www.gamasutra.com/blogs/RockyKev/20160802/278305/Surviving_the_App_Store_a_review_of_Amir_Rajans_book_for_indie_developers.php) Rajan states,

1\. ***Exercise:*** Book reports! Read the following articles then write down the ideas you learned.

*   Give people something to care about. Give people an experience that they will want to share with others. [Then take time to let them know about it.](http://www.gamasutra.com/blogs/SarahWoodrow/20140102/206583/7_truths_about_indie_game_development.php)
*   Opinion: What NOT to do when [starting as an indie game developer](http://indiegames.com/2013/11/opinion_what_not_to_do_when_st.html)

2\. ***Exercise:*** Research the Big Fish’s updated [***Video Game Statistics Database for 2018***](https://www.bigfishgames.com/blog/stats/)

3\. ***Exercise:*** Big Fish is the 7th largest game publisher worldwide. I am fortunate to have an earned Silver Partner status. Big Fish has an extensive library on game development. Visit their [***game development education site.***](https://www.bigfishgames.com/blog/category/game-development/)

### Building Desk-Tops or Web-apps? (Business Philosophy)

Now you can save time by adopting [***“Electron” framework***](https://electronjs.org/) and create ***both*** Desk-top and Web-app games during development!

[![](resources/i_ytimg_com---vi---8YP_nOCO-4Q---hqdefault.jpg)](https://youtu.be/8YP_nOCO-4Q)

View this video at [https://youtu.be/8YP_nOCO-4Q](https://youtu.be/8YP_nOCO-4Q)

***What is Electron: The Hard Parts Made Easy (video: 4:08 min.)***

Here’s [***33 games***](https://electronjs.org/apps?category=games) created with the “Electron Framework”. [***Wayward***](http://www.waywardgame.com/) is my favorite! Wayward is a challenging turn-based, top-down, wilderness survival rogue-like game using the “Electron Framework”. Multi-Player in Wayward is enabled ***for up to 32 players.*** Multi-Player works in a simulated turn-based mode where each turn happens on a fixed interval as long as players are performing actions or in a real-time mode where each turn happens on a fixed interval regardless of player action. When playing in hardcore mode (or with permanent death enabled), after dying, you will continue to play in ghost form, allowing you to spectate but not interact normally. Multi-Player also allows for a special Player verses Player (PVP) flag to be set to allow players to hurt and kill other players. Multi-Player options can be set in the “Multi-Player” menu via the pause menu accessed with escape by default. Additionally, modes and tick time (turn intervals) can be changed via the “Modes” menu. Read [***“more about Wayward”.***](http://www.waywardgame.com/#media)

![](resources/i_imgur_com---3KEdsiv.png)

Wayward Sample Game Play

### Find Similar Games (Competitors)

### Key Features (Matching the Competition)

### Key Differentiation & Unique Features (Setting Us Apart)

***REALLY!?!?! Where’s your common marketing sense now?***

### Understanding the Block-chain Business Model in Gaming

## 1.3 New Dog, Old Tricks?

Creating games for the Web has been compared to taking a “new dog and teaching it the same old tricks”. In short, the same [game mechanics](http://gamestudies.org/0802/articles/sicart) concepts in by-gone ages that worked in Atari/Nintendo still apply in a new “virtualized” HTML5 canvas. Human nature is the one consistent aspect from those days to the present. Human nature does not change just because the gamer is playing a table-top board-game of “Dungeons & Dragons” but now uses the same [game mechanics via computer](https://en.wikipedia.org/wiki/Game_mechanics). The game’s mechanics have not changed, ***but the games mechanism have***. The human emotions (the driving forces) that motivate gamers to purchase your games in an online or physical store are those same forces that motivate them as they shop on the Web.

Furthermore, doing business on the Web requires you to provide at least the same service to your clients as they would expect in a face-to-face session. In fact, because there is no direct contact with other gamers; and, because of the immediate nature of being online, ***some players will demand game services to be even more responsive than you might be capable of delivering to their devices.*** As with any business endeavor, superior client service, through your game, can be a distinguishing factor that will increase your customer base, their loyalty to your game and associated products.

Startling evidence from Localytics shows that “…[23% of Users Abandon an App After One Use](http://info.localytics.com/blog/23-of-users-abandon-an-app-after-one-use)…”. If this is true, then what are current game developers doing incorrectly? Humans haven’t changed; is it something wrong in current game development? In Localytics’ five-year study, they discovered:

The current statistics for 2016 show some improvement per their study, and they offer insider-secrets how to improve gamers’ retention to 46% (i.e., encouraging players to use a mobile game more than 11+ times!). They recommend:

Skeptical? Here’s some background information on Localytics, their annual report and population sampling. Localytics is the leading mobile engagement platform across more than 2.7 billion devices and 37,000 mobile and web apps. Localytics processes 120 billion data points monthly. For this analysis, Localytics measured the percentage of users who only used an app once as well as the users who returned multiple times. For the in-app messaging analysis, we compared the percentage of users who did or did not return to apps who are using in-app messages compared to those who are not. The time-frame for the study was March 1st 2015* April 30th 2016.

## 1.4 Generating Game Ideas & Mechanics

I am assuming, by now, that you may have an idea about what type of game genre you plan to build as you progress through this workbook. If not, then review some the references available in the appendix’s “Internet Resources” or “Game Design References”. In order to stay focused on the task at hand (i.e., creating a MMoG using Phaser), I’ll simply direct you to some excellent external resources. My favorite is [***Game Development Tools & Generators***](http://makingbrowsergames.com/gameDesigner/) as a resource for random ideas and others located in the appendix — such as “[Three Hundred Prototypes](http://www.squidi.net/threep/index.php)” and “[Three Hundred Mechanics.](http://www.squidi.net/three/)” The ***Game Development Tools & Generators*** creates game design documents (GDD) automatically with a source code skeleton framework. Furthermore, you will find [***in the website Bonus Content***](http://makingbrowsergames.com/mmog/bonusContent/) a valuable resource to generate game mechanics that relate to human emotions and what is considered “FUN”.

A word of caution is needed at this point. You could surf the web and find hundreds of articles such as [***“How To Make Your Own Video Game”***](https://www.wikihow.com/Make-Your-Own-Video-Game). It’s an excellent article, but don’t be fooled; the article is for **“Hobbyists and Technology seekers” only.** If your are an **[E] Track**, you’ll regret following their advice and all the time spent creating something only to learn ***it is not “marketable”.*** Their recommendations and development path are **“inside out”.** This is the same mistakes I made decades ago! Let me guide you in the correct sequence to follow in the upcoming “Marketing” chapter — **8-Step Deployment method.**

Furthermore, you will find, in the ***Bonus Content*** a valuable resource entitled — [***Game-PlayChart***](http://makingbrowsergames.com/mmog/bonusContent/GamePlayChart.pdf) — to generate game mechanics that relate directly to human emotions and what is considered “FUN”.¹ You may find another document beneficial in balancing your multi-player games published from the 2009 Game Developer’s Conference by David Sirlin; this document is in the Bonus Content and entitled [***“GDC2009-sirlin-handout6.pdf”.***](http://makingbrowsergames.com/mmog/bonusContent/GDC2009-sirlin-handout6.pdf)

***Download:*** the [***“Game Play Chart”***](http://makingbrowsergames.com/mmog/bonusContent/GamePlayChart.pdf) from [http://makingbrowsergames.com/mmog/bonusContent/GamePlayChart.pdf](http://makingbrowsergames.com/mmog/bonusContent/GamePlayChart.pdf)

***Download:*** the [***“GDC2009-sirlin-handout6.pdf”***](http://makingbrowsergames.com/mmog/bonusContent/GDC2009-sirlin-handout6.pdf) from [http://makingbrowsergames.com/mmog/GDC2009-sirlin-handout6.pdf](http://makingbrowsergames.com/mmog/GDC2009-sirlin-handout6.pdf)

## 1.5 Copyrights & EULA

I debated whether to include this section. I am so *“right wing”* in my opinion that it was —and still is— difficult for me to understand the “nonsense” of [***“copy-left” licenses.***](http://choosealicense.com/) The international copyright law is very explicit as to what constitutes a valid copyright signature. All [***“copy-left” licenses***](http://choosealicense.com/) exists because of one legal flaw when submitting works into the *“public domain” while the author is still alive.* I strongly recommend you purchase [***“How to Copyright Software”***](http://amzn.to/2bmlAcH) for information “over-looked” by the copy-left movement and open source ***end-user license agreements (`EULA`).***

Another consideration … [by Ivan Hoffman](http://www.ivanhoffman.com/pennames.html)

In order to remove myself from this heated and emotional debate, I refer you to what the U.S. government says concerning copyright issues on games. I quote from the [***US Copyright Website***](http://www.copyright.gov/fls/fl108.pdf). I placed embolden text to draw your attention to frequently misconstrued concepts; it explicitly states:

***Hint:*** I strongly encourage you to purchase [***“How to Copyright Software”*** by M. J. Salone (a lawyer!)](http://amzn.to/2bmlAcH) who shows information [***“over-looked”***](https://en.wikipedia.org/wiki/First-sale_doctrine) by the ***copy-left movement*** and ***open source software licenses.***

And hence, the reasons to write down our ideas in a [***“tangible form”,***](https://www.bitlaw.com/copyright/formalities.html) and furthermore, [***affix a properly labeled notice — use the legal © (a “C” inside of a circle)***](https://en.wikipedia.org/wiki/Copyright_notice#Form_of_notice) prior to forum discussions (i.e., none of this stuff: **`(c)`, `pen names`, `pseudonym`** defecation or missing publication dates). That “tangible” form should be a *game description*. Let’s take, for example, a simple “Breakout” game. You might write your game description similar to this [***“elevator speech”***](https://en.wikipedia.org/wiki/Elevator_pitch):

Again, I strongly recommend you obtain a copy of [“How to Copyright Software” by Attorney M.J. Salone](http://amzn.to/2bmlAcH); **read all of it**, and please share what you’ve learned and ***stop the insane non-sense the game development herd is following on Internet repositories***.

## 1.6 Chapter Summary

Let’s review and take inventory of what notes you have so far.

*   The chapter introduction started you thinking and recording your intentions and approach for game development and cataloged your primary motivation. From your “Journaling”, you are able to determine production aspects that are easy and difficult for your skills. This knowledge provides a basis for your game development partnerships and alliances.
*   You studied various Marketing exercises and learned about potential **ROI.**
*   In New Dog, Old Tricks? You learned that game mechanics have not changed since the by-gone days but the migration to the online deployment suffers. You have studied how to improve game participation up to 46% and the methods you need to employ in your game mechanics to achieve this goal.
*   You have updated your records from the US Copyrights Office and an attorney-at-law concerning legal copyrights and end-user license agreements for the game industry.
*   Preliminary questions about the type of massive multi-player on game (aka MMoG) we should create.

Whew! …. and that’s just the start! In Chapter two we start the earnest work on our game’s foundation — The Network.

## 1.7 Chapter Foot Notes

1.  Jon Radoff’s book “Game On” chapter 5 Fungineering, 42 things that customers think are fun, available from [Amazon.com](http://amzn.to/2cd9xAo)

# 2 Building a Game Studio Workshop

This chapter is focused on organizing the project’s file structure and setting up your workstation environment. It will allow us to:

*   have the software tools available for production
*   maintain an organized file structure;
*   facilitate project creation, and
*   test various aspects of our game and installation of Phaser.

Phaser has three versions of its [***Application Program Interfaces (API):***](https://medium.com/@perrysetgo/what-exactly-is-an-api-69f36968a41f) Phaser v2.6.2 (Official), the Community Edition (v2.7+), and Phaser III ***(highly recommend using any versions after 3.15+).*** Since Phaser has a reputation ***— and prefers! —*** frequent software updates, I am using the latest official stable release v2.6.2 (as of August 2016) and only v3.16+. I recommend you use the current stable version [available here for download](http://phaser.io/download/phaserce).

## 2.1 Workstation Set-up Environment

Let’s take an inventory of what you currently have on-hand. Do you have:

*   A browser that is [***HTML5 compliant***](https://caniuse.com/#search=html5); now-a-days, most browsers are compliant. But you can double-check using this site: [https://caniuse.com/#search=ES6](https://caniuse.com/#search=ES6) (***NOTE:*** bookmark this site for use later.)
*   A separate directory (folder) to save and review each game projects’ development files. (See Project Setup below)
*   A text editor or Integrated Develop Environment (`IDE`) of your choice. (See Development Tools below)
*   An operational web server? (Coming next . . .)

**You will need an operational Web-server — with optional middle-ware when developing games in Phaser JavaScript Gaming Framework.** Optionally, if you have Internet access, you could elect to do all your game development online. With such websites as [***CodeSandbox***](https://codesandbox.io/), you don’t have to do anything other than just start programming. **You don’t have to set up a development environment, you don’t have to install dependencies, you don’t even need a workstation … just access to the Internet with your favorite browser!** During initial development of **CodeSandBox**, they noticed that other students at my university were using CodeSandbox to learn React, and they found this a great idea. Online application development is a growing field in [***cloud microservices,***](https://www.bmc.com/blogs/new-multi-cloud-world-means/) and with all new configuration demands for workstations, it becomes harder and harder to focus on generating new code. **CodeSandBox** make this easier by doing most, if not all, these configurations for you as a cloud microservice. You should have your game development workstation everywhere, so you can work whenever you want. Moving your development environment into the “cloud” facilitates this. **CodeSandBox** make it possible to build a game application from start to finish, without leaving your browser.

**“Why do I need a web server? Can’t I just open the `html` files with my browser?”**

***Answer:*** All JavaScript games, which load any assets or files, ***require launching themselves from a web server — either locally inside your workstation*** or [***remotely from the Internet.***](http://gose-internet-services.net/data-centers/uk-data-center/) It’s all about browser security and the [***same-origin policies***](https://developer.mozilla.org/en-US/docs/Web/Security/Same-origin_policy) — prohibiting files loading from different [***“domains”***](https://en.wikipedia.org/wiki/Domain_Master_Browser) and the protocols used to access your locally stored files. When you request anything from the Internet you’re typically using the ***“hyper-text transfer protocol” (`http://` or `https://`).*** From a web server, security policies ensure you only access files that you are authorized to use. When you open any `HTML` file from your local operating system, your browser uses the `file://` protocol. ([***technically a different protocol***](https://www.w3.org/Addressing/) than `http://`), massive restrictions are triggered inside your browser, for the following obvious reasons. Under the `file://` protocol, no concept of domains nor “server-level security policies” exists, just your computer’s “raw file system” and its operating system — identified as the [***localhost***](https://en.wikipedia.org/wiki/Localhost) — using a [***local IP address(es) (0.0.0.0 or IPv6 ::1, or IPv4 127.0.0.0/8 to 127.255.255.255/8)***](https://www.lifewire.com/network-computer-special-ip-address-818385) per [***RFC 990, November 1986.***](http://tools.ietf.org/html/rfc990#page-6) This means that your `HTML` pages ***are not running on any domain nor public Internet IP address at all,*** and thus JavaScript is ***unable to load any game assets dynamically.*** Do you really want JavaScript to have that much control — to load anything from anywhere — off your computer? Well, I’m guessing your answer should be “… not ever!”. If JavaScript had unrestricted access using the `file://` protocol, nothing could stop it from tapping into your information and sending it anywhere to anyone.

Secondly, a web server will ***properly test*** your game during development. You have several choices; you might:

*   Install a web-server on your workstation. There are many ways to do this, and if you have previous Web Development experience, you may have your own preferred approach. I, along with the Phaser.io home site, recommend using a locally running web server. I use [***XAMPP***](https://www.apachefriends.org/download.html) setup from Apache Friends on my Windows workstation as my web-server of choice. You might research [**WAMP for Windows O/S**](http://www.wampserver.com/en/) or [**MAMP or MAMP Pro for MAC O/S**](https://www.mamp.info/en/). XAMPP is an easy to install Apache distribution containing MariaDB, PHP, and Perl. Just download and start the installer. It’s that easy. I am running PHP 7 with MySQL database extensions. I will discuss how to use Phase-based games with PHP middleware in the advanced section of this workbook. Please refer to **[http://www.phptherightway.com/](http://www.phptherightway.com/);** later, I will discuss using the web-server to provide various other game cloud services.

***OR …***

*   Another simple solution I discovered is the [***Google’s Chrome Web Server.***](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb?hl=en) Once you install this application, you can launch any web page(s) directly from Chrome. Simply point it at your [***URI path and project folder.***](http://uri.thephpleague.com/4.0/components/overview/)

***OR …***

*   Many web developers simply choose to deploy a Python, PHP 5.4+ or Node web server from their terminal command prompts.
*   If you already have any of these installed, then you can simply run

***OR …***

If you prefer Node.js, then using the [**Node Package Manager (NPM)**](https://www.npmjs.com/) (you only need to install the http-server package once) you can do

***OR …***

*   You could [**lease a web-server**](http://gose-internet-services.net/wordpress-web-hosting/) for [**as little as $1.00**](http://gose-internet-services.net/kvm-vps/) or [**$2.92 a month**](http://gose-internet-services.net/hosting-plans/) up to [**dedicated exclusive servers**](http://gose-internet-services.net/dedicated-servers/) in [**5 different data centers**](http://gose-internet-services.net/data-centers/) world-wide.

***OR …***

*   Some text editors and Integrated Development Environments (`IDE`) **already include a local web server.** [***Brackets***](http://brackets.io/) is one such example.

***OR …***

*   Use the ***Phaser Editor 2.x for Phaser III***. [Download a trial version here](https://phasereditor2d.com/blog/2018/11/phaser-editor-v2-development-progress-report-4). Emanuele Feronatro wrote a [comprehensive article on Phaser Editor 1.x.x](http://www.emanueleferonato.com/2016/07/22/speed-up-phaser-game-development-with-phaser-editor/); it worth your time to investigate. If you prefer it over others, then you can [purchase the Phaser Editor v2 when it becomes available](https://phasereditor2d.com/blog/category/phaser-editor-v2).

***OR …***

*   Consider using the [***Phaser III Sandbox***](http://labs.phaser.io/edit.html). It allows you to interactively code your games online in your browser without having to download or install anything. Its editor features direct access to the Phaser JavaScript Framework library and suggests code snippets and many of the features available in editors such as Sublime and Brackets. Once finished you can save, export or share your game. AND, better yet, all this for ***FREE***.

***OR …***

*   You could use an online code editor such as CodePen.io in order to run all of the JavaScript we’ll use. There’s no requirement to install anything on your workstation. On the other hand, the disadvantage is you won’t be able to publish nor share your game. You will end up having to use one of the above options.

## 2.2 Development Tools

### Text Editor

Although [***Phaser.io web site***](http://labs.phaser.io/) has a section on how to get started. I recommend you test and develop your game with a [***source code editor***](https://en.wikipedia.org/wiki/Source_code_editor) or an [***Integrated Development Environment (`IDE`)***](https://en.wikipedia.org/wiki/Integrated_development_environment) editor of your choice.[***(See examples here)***](https://en.wikipedia.org/wiki/Source_code_editor#Notable_examples) I use several: [***Jetbrain’s WebStorm***](https://www.jetbrains.com/student/), [***Phaser Editor v2 for Phaser III***](https://phasereditor2d.com/), and [***NotePad++ (FREE)***](https://notepad-plus-plus.org/); although, [***Brackets***](http://brackets.io/) editor runs a close second in my daily website construction. What’s everyone else doing? ***OVER one-third of all professional web developers [use this IDE.](https://www.jetbrains.com/research/devecosystem-2018/javascript/)*** Another fourth of all professional web developers use [***Typescript***](https://www.jetbrains.com/research/devecosystem-2018/javascript/) found inside the [***Microsoft Visual Studio.***](https://code.visualstudio.com/)

***Do not use any word processing applications*** such as Microsoft Word; this is not a “hate statement” against Microsoft. Word processing applications add invisible formatting into the source code that will lead to problems. If you do not have a favorite text editor, I have some recommendations based on your status:

*   Are you a ***student or instructor***? Then obtain a **FREE** copy of [PHPStorm](https://www.jetbrains.com/phpstorm/buy/);
*   Are you a game development indie or hobbyist with little cash assets? Then obtain a **FREE** copy of [Notepad++](https://notepad-plus-plus.org/); it’s the editor I use or use [Microsoft Visual Source Code](https://code.visualstudio.com/c?utm%5C_expid=101350005-27.GqBWbOBuSRqlazQC_nNSRg.2) if you are inclined to develop in typescript.
*   Do you ***have money to spend***? Then pick any of the thousands of software source code editors available online, ***and then send me the remaining money for my own development (wink, wink, my poor attempt at humor?!)*** On a serious note, save your cash for game assets.

### IntelXDK (deprecated)

[IntelXDK](https://software.intel.com/en-us/intel-xdk) was an all-in-one integrated development environment to easily simulate, test, tune, and deploy game projects to many app stores using a single code base. It also provided:

*   Game engine support for Construct2, Cocos2D, **Phaser.js**, Pixi.js, and Easel.js to easily import assets and code. The IntelXDK came with **two sample Phaser game templates**. If you can find IntelXDK (pre-AUG 2016), download and preserve it!
*   W3C Game-pad API support enables high-impact game interaction using game-pad or joystick devices
*   Apache Cordova plugins and APIs to monetize and market action-packed multi-OS games.

The IntelXDK shipped with the open source [Brackets editor](http://brackets.io/) from Adobe. This is an important feature because, when using its “Live Preview” feature, Brackets would launch the chosen HTML file in Google Chrome by supplying static content from ***Brackets built-in web server. This procedure does not require any back-end logic to support viewing changes to the HTML file.***

## 2.3 Project File Structure

The arrangement of directories (i.e., folders) and files is an important consideration. If you use some of the scaffolding tools, your project file structure is dictated; this provided less security since your game follows a known directory structure.

I have read dozens of game development authors who literally dictate a rigid organization up to 10+ layers deep. “Why should I follow this?”, has always been my question; we will review namespaces later. How does their organization structure help or hinder the final game product? I recommend for the sole indie game developer to avoid the nonsense of 10-levels deep directories. Create an organization of directories that make sense to you and labeled as you please. This is a security feature because it becomes harder to guess your directories and naming schema.

On the other hand, if you are working on a game development team, then directory structure takes on a new meaning known as: “Name Space” for local and intermediate variables. Consistency and standardization are King for collaborative efforts. Many game developers turn to [Vagrant to help](https://www.vagrantup.com/).

Let me show a few options for game file organization from various game developers; then, choose what you like and adopt as your own development structure. Remember! **DO NOT USE SPACES IN THE DIRECTORY NAMES.** If you use `Linux O/S`, you understand where I’m coming from; many, if not all, cloud web servers use `Linux O/S`. This is a horrible habit encouraged by both Apple and Microsoft upon naive end-users.

Do not include empty folders (those without any files). This is a security violation on websites and opens a door for hackers to snoop. I can’t count how times . . . oops! I [**plead the 5th!!**](https://www.dictionary.com/e/slang/plead-the-fifth/) For example: If you don’t use any plugins then you wouldn’t need a plugins folder inside the lib.

If you use the [uiKit framework](http://getuikit.com/) — a lightweight and modular front-end framework for developing fast and powerful web interfaces — consider [their suggestions for directories](http://getuikit.com/docs/documentation_project-structure.html).

### My Project Recommendations

This is not “holy writ”, but merely suggestions for a naming convention. For example, if you would like to use “sfx” for the sound-effects directory, then do so. You can find hundreds of phaser templates on [GitHub](https://github.com/search?&q=phaser+templates) by simply using the keywords “phaser templates”.

When you are creating a project template ***(a.k.a., Blueprint or Game Starter Kits)*** its File Structure should be consistent across all your products. ***Why’s that? [Well, I’ll tell you …](https://www.youtube.com/watch?v=x2Y7_1dILlQ)*** Because when you create another new project and “refactor” everything (i.e., rename code blocks) to coincide with a new project, ***it is easier to “find & replace” consistent formatting.***

Here’s the structure I use and believe makes the most sense (to me) when creating my games. Having consistency across all your projects makes it easier for other staff members as they work on simultaneous projects to know where everything is located when switching between projects.

```
 1     .URI/<PROJECT NAME>/ //game root directory  
 2     ├── favicon.ico      //game logo  
 3     ├── index.html       //game front-door entrance  
 4     ├── license.txt      //game EULA @ your online store  
 5     ├── manifest.json    //game mobile app  
 6     ├── package.json     //for Progressive Web Apps  
 7     ├── purchaseOrd.pdf  //how to buy your game  
 8     ├── ReadMe.md        //game info & contact  
 9     │  
10     ├── assets/          //game unique © resources  
11     │   ├── audio/
12     │   ├── images/
13     │   └── spritesheets/
14     │
15     ├── css/             //game content styling
16     │   └── main.css
17     ├── fonts/           //game font styling
18     │   └── fonts.css
19     │
20     └── js/              //game behaviors
21         ├── lib/         //game external libraries
22         ├── plugins/     //game enhancements
23         ├── prefabs/     //game prefabrication objects
24         ├── states/      //game phase
25         └── utilities/   //game helpers 
```

Single Player Game Project File Structure

***Project File Descriptions:***

*   ***index.html*** — Main game container file, your example game should be viewed from within this page.
*   ***.htaccess*** — The default web server configs are for Apache. For more information, please refer to the [Apache Server Configs documentation](https://github.com/h5bp/server-configs-apache/tree/master/doc). Host your site on a server other than Apache? You’re likely to find the corresponding [server configs project listed here](https://github.com/h5bp/server-configs/blob/master/README.md)
*   ***apple-touch-icon-precomposed.png*** — If you want to use different Apple Touch Icons for different resolutions [refer to this documentation](https://github.com/h5bp/html5-boilerplate/blob/v4.3.0/doc/extend.md#apple-touch-icons).
*   ***crossdomain.xml*** — A template for working with cross-domain requests. [more about crossdomain.xml here](https://github.com/h5bp/html5-boilerplate/blob/v4.3.0/doc/crossdomain.md). ***WARNING:*** WebSockets **can do cross domain communication,** it follows the same cross-origin sharing [***CORS methodologies***](http://en.wikipedia.org/wiki/Cross-origin_resource_sharing) and **they are not limited** by the “Same Origin Policy (SOP)”, as JavaScript is traditionally inside the browser. Because of this, WebSockets have the same exposure to type of cross-domain attacks. I’m won’t going to go into a detailed description on websocket security, simply said, it’s up to the server authentication to validate their client’s origin and for WebSocket frame tampering. If you’d like to restrict browsers communication to same-domain servers, you will modify the header policies in the browser Content-Security-Policy header. This will lock down the websocket to your originating domain. Naturally, you should always use “wss://” (Secure WebSockets ), to ensure a stronger level of encryption.
*   ***favicon.ico*** — refer to [Hans’ handy HTML5 Boilerplate Favicon and Apple Touch Icon PSD-Template](https://drublic.de/archive/html5-boilerplate-favicons-psd-template/?file=blog/html5-boilerplate-favicons-psd-template/).
*   ***human.txt*** — Edit this file to include the team that worked on your site/app, and the technology powering it.
*   ***license.txt*** — describe how you permit the use of your game.
*   ***purchaseOrder.pdf*** — never know how a consumer obtained your game release; provide them with a means to remain honest.
*   ***readme.txt*** or readme.md should have a customer friendly welcome, project introduction, installation instructions, license and contact information.
*   ***robots.txt*** — Edit this file to include any pages you need to be hidden from search engines.
*   ***assets/*** — **Any copyrighted assets (purchased or created) specifically for this game,** or referenced in the index.html file. Everything should be in this folder.
    * ***audio/*** — Home for any audio files. You could simply name this directory “sounds” or “sound effects” (sfx). You might consider building two sub-directories for game theme “music” and another for “sound effects (sfx)”. Remember that not all browsers support every audio format (.wav, .ogg, mp3/4). Try creating [***your own music here***](https://learningmusic.ableton.com/index.html) Research [***more demos***](https://tonejs.github.io/demos) from ToneJS — A Web Audio framework for making interactive music in the browser at [https://tonejs.github.io](https://tonejs.github.io).
    * ***data/*** — Any data files (e.g. JSON, atlas) that pertain directly utilized by these assets.
    * ***fonts/*** — Any unique font-sets you have licensed
    * ***images/*** — Home for any visual files. You could simply name this directory “images”, “sprites” or “ graphics effects” (gfx). I stuff all the visuals here — including spriteSheets.
    * ***maps/*** — the information about tile-maps used in this game.
    * ***misc./*** — any additional files such as dialogs, run-time scripts, language XML/json, etc.
*   ***data/*** — configurations, static data templates, tile maps, game board dimensions, etc.
*   ***docs/*** — This directory contains all the HTML5 Boilerplate documentation and might contain any extra documentation about the Blueprint. You can use it as the location and basis for your own project’s documentation.
*   ***js/*** — Source JavaScript files for your game. You could simply name this directory “js” (as I do), “scripts” or [***“source (src as other develops do here)”.***](https://github.com/jdotrjs/phaser-guides/blob/master/Basics/Part1.md) You could include Libraries, plugins, and custom code; or all can be included in a separate sub-directory or directory. It includes some initial JS to help get you started
    * ***gameObjects/*** — Any core Game Objects (such as player.js, avatar.js, treasure.js, etc.) should be contained here.
    * ***states/*** — All Game Phases/States menus used by your game.
    * ***utils/*** — Folder containing any Utility Methods/Objects.
    * ***game.js*** — The main JavaScript game mechanics logic file.
*   ***lib/*** — External Libraries that are required/used should be contained here. This includes any JavaScript Framework and addons / extensions (a.k.a., ***Plugins***).
    * ***phaser.min.js*** or simply use from one of the content delivery networks.
    * ***plugins/*** — Any Plugins that are used.
*   ***themes/*** — Folder containing any formatting for the overall hosting website.
    * ***CSS/*** — cascading styles sheets for the overall website theme. It should follow a [***“structured approach”***](https://sunpig.com/martin/2008/10/07/maintainable-css-modular-to-the-max/) creating separate cascading style sheets during development. Upon deployment, all of these collapse into a single file. This directory should contain all your project’s CSS files. It includes some initial CSS to help get you started from a solid foundation.
    * ***gfx/*** — graphics effects for the hosting website.

## 2.4 Summary

Let’s review and take inventory of what you have so far.

*   We have set-up a workstation environment.
*   Chose and set-up an operational web-server.
*   Installed several development, and supporting tools.
*   Created a file structure to become a consistent template for on-going projects.
*   Learned where to find $1,000+ of free software for game development.
*   Reviewed tools to migrate the html5 game onto various mobile platforms.
*   Have knowledge of marketing information from Chapter 1.
*   Have both a Game Design and a Technical Design Documents from chapter 2.
*   Have an operational web-server and middle-ware for your game’s home website.

# 3 Networking Basics

![](resources/makingbrowsergames_com---book---imagesConsolidated---osiTable.jpg)

Open System Interconnection (OSI) layers

I would like to show you [***a 13:00 minute movie***](https://www.youtube.com/watch?v=RhvKm0RdUY0&list=PLMEBhsFVAWsJVCcr1TFjFx117DZsVrHzw) that I use in all my ***“Introduction to Networking” classes.*** It’s really quite entertaining and demonstrates all the basic equipment found and used within a common `Wide Area Network` (WAN) or `local area network` (LAN).

The movie you just watched followed the [***Open Systems Interconnection model***](https://en.wikipedia.org/wiki/OSI_model) (aka ***“OSI”*** written by International Standards Organization — ISO).

***“OSI”*** is a telecommunications model that dissects and delegates software responsibility. The “Warriors of the Web” movie started at the fourth layer called “Transport”. Layers 5 to 7 are explained already by many current articles found on the Internet, and we will cover those areas very soon.

The Open Systems Interconnection (OSI) model is a reference tool for understanding data communications **between any two *differently(!)* networked systems.** It divides the communications processes into these seven layers of software responsibility. A human’s interaction upon this data communications system is represented by layers 8 to 10 (not illustrated above). Each layer performs ***“specific duties”*** to support the layers above it and offers [***“services “ (i.e., Service-Oriented Architecture (SOA) is a specific method of organizing software! It is the idea of breaking out various functionality as module and possible deploying those on different servers with network protocol or sockets communications.)***](https://www.ibm.com/developerworks/webservices/library/ws-migratesoa/) to the layers below it. The three lowest layers focus on passing traffic through the WAN to an end device. The top four of the seven layers represent the activities on the source and destination devices.

*   Layer 7 is the place your browser lives on the client-side. A client is a system that connects to a remote system to fetch data. It is the gamers’ “Window” (aka view or interface) into the gaming world. On the server-side, the game-board world will be represented as a mere “data structure”; it is the central point from which all gamers learn about one another. I’ve seen in forums, too many times, folks asking about how to run “Phaser canvas” on the server.
*   Layer 6 handles a couple of items. First-off is how to “Present” the formatted information. Is the gamer’s language French, Russian, Japanese? Then the display information must accommodate those symbols for their language. Is the gamer required to log-in and present sensitive personal information protected under the **General Data Protection Regulation (GDPR)? ([See the Appendix — Security](http://makingbrowsergames.com/book/Appendix-Security.pdf))** Layer 6 performs all the encryption security methods.
*   Layer 5 is responsible for “message dialogs” and “sessions” between each gamer and the destination server. Most of the work we will do belongs to this area [***in the form of WebSockets.***](https://en.wikipedia.org/wiki/Network_socket) This layer will receive data from the Layer 4 “TCP port” below. ***A “socket” is an identification (aka binding) created from both a layer 3 Internet Protocol address and an assigned layer 4 port number.***

![](resources/makingbrowsergames_com---book---imagesConsolidated---IBMsocket.jpg)

Binding an IP address & Socket into Session dialog

*   Layers 4 downward to the “physical” layer were explained in the The **“Warriors of the Web” movie.** It is only 13 minutes of your time, quite entertaining, and will save you nearly 8 hours of reading an [18 chapter book by Ilya Grigorik](https://hpbn.co/) — a web performance engineer at Google and co-chair of the W3C Web Performance Working Group. It’s your choice. Layer 4 provides several protocol “services” known as User Datagram Protocol (UDP), Transmission Control Protocol (TCP), [***Quick USP Internet Connections (QUIC)***](https://en.wikipedia.org/wiki/QUIC) and many others.

![](resources/makingbrowsergames_com---book---imagesConsolidated---beforeAndAfterSOA.jpg)

New Cloud Computing Network Model for MMoGs

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogFlow2.jpg)

Where networks impact MMoG

***Hint:*** `127.0.0.1` as IPv4, `::1` as IPv6, or `localhost` are all IP addresses that default to your local workstation. The packet path ***never reaches the Network Interface Card (NIC). This is an important concept when creating web sockets and multiplayer games.***

You may considering reading [***Ilya Grigorik’s book***](https://hpbn.co/) online; ***it is FREE.*** I will refer to it often. This book provides a hands-on overview of what ***every “full-stack” developer needs to know*** about the various types of networks (WiFi, 3G/4G), transport protocols (UDP, TCP, SCTP and TLS), application protocols (HTTP/1.1, [**HTTP/2**](https://en.wikipedia.org/wiki/HTTP/2)), and Application Programming Interfaces (APIs) available inside the “Layer 7” browser by XHR, [***WebSocket***](http://websocket.org/), [***WebRTC***](https://webrtc.org/), (and more) to deliver the “best” — defined as fast, reliable, and resilient — user experience. ***His book separates the non-sense [“CRUFT”](https://en.wikipedia.org/wiki/Cruft) from the practical in many of the articles I’ve read about multi-player games development.***

***HINT:*** Bookmark [Ilya Grigorik’s ***FREE*** book](https://hpbn.co/) for reference as we create our MMoG in Part III and IV.

## 3.1 Network Foundation Inventory

There are many articles on the web about creating multi-player games by authors pushing their personal solutions. We will review many of those solutions after we create some criteria we need for our game. Then selectively match the available server engines that fulfills our game requirements.

I going to state the obvious in ***Criteria #1: “To make a multi-player game, we must connect multiple players who are not in the immediate area or on the same workstation.” (DUH!?!)*** We could make a multiple player game by having all the gamers in the same room, all using the same computer (also known as [***hot-seat***](https://en.wikipedia.org/wiki/Hotseat_(multiplayer_mode)) that was a popular Multi-Player solution during the 80s, when computers were “pricey”.) Today, folks simply bring their keyboards and adjust “Blue Tooth” to accommodate a “micro-net”. But still, ***that’s one computer with multiple keyboard inputs,*** and not what we are about.

## 3.2 Deeper Dive: Testing [***MMoGs***](https://en.wikipedia.org/wiki/Massively_multiplayer_online_game) Locally??

We want to allow each gamer a “window” (aka, a view) into our gaming world. There are many ways to do this. Where should our gaming world (aka, game board) live? Who should have access? Do we want lurkers — those that simply want to observe the game in play similar to football fans watching a game but do not participate or gamblers crowded around a blackjack table? Where should the game data, graphics, sounds, authentication, authorization, and game logic (aka, rules) reside? Jot down these questions. These are our topics coming up.

### Hot-seat MMoG Demos

*   [***Basic MMO foundation***](https://basic-mmo-phaser.herokuapp.com/) by Jerome Renaux, hosted on Heroku, using socket.io implementation. Instructions: Use the arrow keys to move. Open multiple browser windows (on local browser) to invite more players. Find source code on [***GitHub***](https://github.com/Jerenaux/basic-mmo-phaser) and rewritten [***into ES6***](https://github.com/TVScoundrel/mmo-phaser-es6). Read his [***development tutorial here***](https://www.dynetisgames.com/2017/03/06/how-to-make-a-multiplayer-online-game-with-phaser-socket-io-and-node-js/).
*   [***Tic-Tac-Toe (AJAX)***](https://jadendreamer.wordpress.com/2012/04/26/ajax-tutorial-2-player-tic-tac-toe-game-no-database-required/) or [***Tic-Tac-Toe (PHP)***](https://jadendreamer.wordpress.com/2015/04/06/php-tutorial-run-multiple-tic-tac-toe-game-instances-no-database-required/) by [***Design1Online LLC***](http://design1online.com/investors/). Instructions: Use the mouse to select “X” or “O” and then submit your game turn. Open multiple browser windows (on local browser) to invite more players.

## 3.3 Network Relationships

Networks connections use two basic relationship models either a “peer-to-peer” (P2P) or client/server (C/S). You might like to know that P2P is coming back into popularity as a new mobile `PeerConnection API`.^(Chapter Footnote 1) The role model used by an organization depends on the purpose of the network and what the users require from the network. The overall physical deployment of computers and other devices is known as the network architecture. The two most common networking models differ primarily in the way users authenticate (log onto) and access specific resources.

A Client is a network device that subscribes to the services provided by a server. As an example in a restaurant setting, a client customer will use a waiter(ess) server to order food services from the kitchen’s chef. A Server is a high-powered computer dedicated to a specific task or service —and in our case a single(?) MMoG. A Peer, in a peer-to-peer (P2P) network, is a common computer (aka workstation) which takes on the roles of both Client and Server both to and from fellow computers. P2P networking is effective only in small networks — less than 10 computers. In fact according to Microsoft, ***10 is the maximum limit for any “peer-to-peer” work-group.*** That’s the reason so many local area networked (LAN) games are limited to 8 maximum players — among other reasons.

We will not consider “peer-to-peer” relationship model for our gaming network (beyond 3 players) due to one important calculation: [***n(n+1)/2***](http://www.maths.surrey.ac.uk/hosted-sites/R.Knott/runsums/triNbProof.html). What this means is that the more workstation nodes (n) we add into a “peer-to-peer” network, the more connections are required. Replace “n” with 25 (or perhaps 100?) gamers, and you will discover that we would need 325 different connection paths — all transferring data packets within the 25-players P2P. It simply becomes overwhelming. Returning to our food example, a P2P is similar to a [***family reunion BBQ.***](http://grouptravel.org/family-reunion/how-to-determine-the-size-location-and-time-of-year-for-your-family-reunion/) Each person at the table receives and passes food entries around the table. If 10 people attend, then everyone can prepare their portions quickly. But what if the [***family has 250 in attendance?***](https://en.wikipedia.org/wiki/Family_reunion) Passing food around to others in this manner is silly; the solution would be to serve the meal using a caterer (translates into client/server model) or buffet-style (translates into self-serve website). Computers are limited to 65,536 layer-4 ports; and, not all of those layer-four ports are at our gaming server’s disposal (minus the 1,024 dedicated ports).

![](resources/makingbrowsergames_com---book---imagesConsolidated---csDialog.jpg)

Simplistic view Client to Server Relationship

| Client | Network | Server |
| --- | --- | --- |
| Collect Input | Pass Data -> | Process Input |
| Render Views | <- Pass Data | Move Objects |

Most “Massive Multi-Player online Games” (MMoG), played today on the Internet, are merely modified “client / server networked” games. Take for example, games such as [***Half-Life,***](https://stackoverflow.com/questions/918033/how-does-the-half-life-2-multiplayer-protocol-work) including all its “mods” (ie.: Counter-Strike, Team Fortress Classic, etc.), operate on a modified “client / server networked”, as well as, games based on the Quake3-engine and the [***Unreal Tournament engine.***](https://api.unrealengine.com/udk/Three/NetworkingOverview.html) In all of these games, ***there is a single, centralized, authoritative server*** that is responsible for running the main game logic. In software engineering, this is the [***Mediator Pattern***](https://www.oreilly.com/library/view/learning-javascript-design/9781449334840/ch09s06.html) To this central “hub” are connected one or more [***“dumb” clients***](https://simplicable.com/new/dumb-client) — I’m not being derogatory; it’s a term used when [***data terminals equipment (`DTE`)***](https://www.webopedia.com/TERM/D/DTE.html) were only simple screens and keyboards. These clients, initially, were nothing more than a way to [***sample, package, and forward***](https://www.itu.int/rec/T-REC-X.28-199712-I/E) any user’s input onto a server for processing — **very similar to the 1960s [*`SNA` main-frame computers.*](https://en.wikipedia.org/wiki/IBM_Systems_Network_Architecture) Now, consider for a moment what folks call [“the cloud” today.](http://gose-internet-services.net/hosting-articles/what-does-cloud-web-hosting-represent/) It is nothing more than a return to the “1960s main-frame” data transfer concepts with some new secret sauce of monitored and distributed services.** The server would process the gamers’ input commands, shuffle software objects around, then return a list of information to render on the local display. Of course, the real-world systems have more components to do this, but this simplified breakdown is useful for thinking about [***prediction and lag compensation***](https://developer.valvesoftware.com/wiki/Latency_Compensating_Methods_in_Client/Server_In-game_Protocol_Design_and_Optimization) from a [***centralized server’s perspective.***](http://www.gabrielgambetta.com/lag-compensation.html)

***What’s an authoritative server?***

***ANSWER:*** An [***authoritative server***](https://www.ibm.com/support/knowledgecenter/en/SSLTBW_2.3.0/com.ibm.zos.v2r3.halz002/dns_auth_servers.htm) is the central focal point for all game decisions. It replaces the many-to-many connections found in peer-to-peer networks with many-to-one. Game [***(thin Client)***](https://en.wikipedia.org/wiki/Thin_client) workstations merely send their input to a central server to collect, calculate, and report what events should happen as an outcome. The server returns those outcomes, and the client(s) simply renders those results locally. This is, what we call in data communications, a [***simplex connection or half-duplex.***](https://en.wikipedia.org/wiki/Simplex_communication) The biggest disadvantage is the “single point of failure” it presents.

*   [***“The Mediator Pattern in JavaScript”***](https://jarrettmeyer.com/2016/04/21/mediator-pattern-in-javascript)
*   [***Mediator Script***](https://www.dofactory.com/javascript/mediator-design-pattern)

## 3.4 Network Concerns

![](resources/makingbrowsergames_com---book---imagesConsolidated---telco.jpg)

Actual connection path

This illustration above demonstrates the actual communications (i.e., “physical”) path used by two remote gamers. If we are building a “real-time” MMoG, **this communications path would present several problems:**

*   Lag and delayed (aka “latency”) responses. (Nothing is instantaneous!) This is the **greatest problem outside of our control.** Read more about [***network latency***](http://smutz.us/techtips/NetworkLatency.html) and how to compensate for its effects.
*   Lost data packets either going to or coming from each player. (TCP/IP corrupted packets are re-transmitted until they arrive “perfectly”.
*   [***network congestion***](https://en.wikipedia.org/wiki/Network_congestion) — resulting in re-routing traffic toward longer communications paths.
*   discarded data packets due to WAN networked congestion.
*   [***jitter***](https://howdoesinternetwork.com/2013/jitter) — delay which varies over time due to other background traffic from other users sharing the same communications path with [***higher differentiated services.***](https://www.slashroot.in/understanding-differentiated-services-tos-field-internet-protocol-header)

Network bandwidth is a limited resource [***based on contractual agreements; this will become a primary concern in later chapters.***](https://en.wikipedia.org/wiki/Service-level_agreement) So, the server shouldn’t send new updated information packets to every game participant for each minuscule change in the game-board (aka gaming world). Instead, the central game server takes “snapshots of the current game state” at distinct intervals (far less than 60fps!), and then, “broadcasts” those samples to synchronized the game for every gamer. This is the same technique cable companies have when broadcasting movies to neighborhood subscribers. These network data packets take time to travel between the gamer and the server (i.e. [***half the ping time;***](https://serverfault.com/questions/438475/data-obtained-from-ping-is-it-round-trip-or-one-way) see Network Tools Appendix). ***This means that the client-gamer’s time is always a little bit behind (aka lagging) the server’s time.*** Furthermore, clients’ [***incoming message packets***](https://github.com/cjus/umf) are further delayed on their return path, ***so the game server is always processing gamers’ commands in a temporally delayed status.*** In addition, each client workstation has a unique amount of network delay coming toward the central server, **because each game participant arrives at the server through different data connection at different data rates across the WAN.** This delay dynamically varies over time due to other aggregated traffic on that path and the Internet Service Providers (ISP) access sampling frame-rates. These time differences — between server and each client through their ISP — causes logical processing problems, which become worse as network latencies increase inside the WAN. In a fast-paced action game (typically found in “first person shooters”), even the slightest network delay of a few milliseconds could cause “a laggy” (aka jerky, jitter) game-play feeling. This makes it difficult to target other players or interact with rapidly moving obstacles at 60 frames per second (fps or ***~16.67 milliseconds per animation frame. Remember this for Chapter 5.)*** Beyond these bandwidth limitations, fragmentation, corruption and network latencies, game information also gets lost due to network congestion and rerouting.

![](resources/makingbrowsergames_com---book---imagesConsolidated---lag.jpg)

Interpolation & Extrapolation as prediction and lag compensation

Many game developers attempt to compensate for these ***fussy network problems*** by using [***statistical prediction — interpolation or/and extrapolation.***](https://sciencestruck.com/interpolation-vs-extrapolation) What they do not include in their “prediction” is the ***Layer-4 Communications Management which is already in the network protocols.***

***What is Interpolation and Extrapolation?***

**Answer:** [Mario’s Math Tutoring (movie 2:42)](https://www.youtube.com/watch?v=c4_MJg_c49k) [https://www.youtube.com/watch?v=c4_MJg_c49k](https://www.youtube.com/watch?v=c4_MJg_c49k)

## 3.5 Network Transport Protocols Overview

As we have seen, networking protocols are normally developed in layers, with each layer responsible for a different facet of network communications.

### Protocols Defined

Let’s use [***Newton’s TelCom Dictionary***](https://amzn.to/2UCQAvg) and shy away from fabricated descriptions I see in so many tutorials and marketing white papers.

A protocol suite — such as Transmission Control Protocol over Internet Protocol (aka TCP/IP) — is a vertical-combination of different protocols at various layers. [TCP/IP is normally considered to be a 4-layer system](http://amzn.to/2gZcHZT) — as shown in the table below:

| # | Layer Name | Data Protocol Used | Data format | Equip. |
| --- | --- | --- | --- | --- |
| 5,6 & 7 | Application | ***Game App,*** [HTTP](https://en.wikipedia.org/wiki/HTTP/2), [SIP](https://en.wikipedia.org/wiki/Session_Initiation_Protocol) | [ASN.1](https://en.wikipedia.org/wiki/Abstract_Syntax_Notation_One),[***ABNF***](https://en.wikipedia.org/wiki/Augmented_Backus%E2%80%93Naur_form) | RAM |
| 4 | Transport | [SCTP, TCP, UDP,](https://en.wikipedia.org/wiki/Transport_layer#Comparison_of_transport_layer_protocols) [***QUIC***](https://techcrunch.com/2015/04/18/google-wants-to-speed-up-the-web-with-its-quic-protocol/) | Segments | Ports |
| 3 | Network IP | IP, ICMP, IGMP | Packets | Routers |
| (2) | Link | MAC | Frames | Switches |
| (1) | Physical | Voltage, RF, Fiber | B8ZS, HDB3, DWDM | cables, cards, connectors |

***Note: My layers 1 & 2 are the “Network Access” layer per [Newton’s Telecomm Dictionary](http://amzn.to/2gZcHZT)*** or refer to this [***network reference chart.***](https://en.wikipedia.org/wiki/Internet_protocol_suite)

### Layer 4 UDP vs. TCP

| **UDP vs TCP Comparison Chart:** | **UDP** | **TCP** |
| --- | --- | --- |
| Congestion avoidance: Variable congestion window, slow start, time outs | No | Yes |
| ECN support | No | Yes |
| Error detection | Optional | Yes |
| Flow Control | No | Yes |
| IPv4 Network Address Translation (NAT) | Yes | Yes |
| Multiple streams | No | No |
| Packet Header Size | 8 Bytes | 20 – 60 Bytes |
| Port numbering | Yes | Yes |
| Reliability: Error recovery by automatic repeat request (ARQ) | No | Yes |
| Transport Layer Packet entity | Datagram | Segment |
| Virtual circuits: Sequence numbering and reordering | No | Yes |

**UDP vs TCP Features Chart:**

| **Terms** | **TCP** | **UDP** |
| --- | --- | --- |
| **Acknowledgement** | Acknowledgement segments | No Acknowledgment |
| **Acronym for** | Transmission Control Protocol | User Datagram Protocol or Universal Datagram Protocol |
| **Common Header Fields** | Source port, Destination port, Check Sum | Source port, Destination port, Check Sum |
| **Connection** | TCP is a connection-oriented protocol. | UDP is a connectionless protocol. |
| **Data Flow Control** | TCP does Flow Control. TCP requires three packets to set up a socket connection, before any user data can be sent. TCP handles reliability and congestion control. | UDP does not have an option for flow control |
| **Error Checking** | TCP does error checking and error recovery. Erroneous packets are retransmitted from the source to the destination. | UDP does error checking but simply discards erroneous packets. Error recovery is not attempted. |
| **Fields** | 1\. Sequence Number, 2\. AcK number, 3\. Data offset, 4\. Reserved, 5. Control bit, 6\. Window, 7\. Urgent Pointer 8\. Options, 9\. Padding, 10. Check Sum, 11\. Source port, 12\. Destination port | 1\. Length, 2\. Source port, 3\. Destination port, 4\. Check Sum |
| **Function** | As a message makes its way across the [internet](https://www.diffen.com/difference/Internet_vs_World_Wide_Web) from one computer to another. This is connection based. | UDP is also a protocol used in message transport or transfer. This is not connection based which means that one program can send a load of packets to another and that would be the end of the relationship. |
| **Handshake** | SYN, SYN-ACK, ACK | No handshake (connectionless protocol) |
| **Header Size** | TCP header size is 20 bytes | UDP Header size is 8 bytes. |
| **Ordering of data packets** | TCP rearranges [data](https://www.diffen.com/difference/Data_vs_Information) packets in the order specified. | UDP has no inherent order as all packets are independent of each other. If ordering is required, it has to be managed by the application layer. |
| **Reliability** | There is absolute guarantee that the data transferred remains intact and arrives in the same order in which it was sent. | There is no guarantee that the messages or packets sent would reach at all. |
| **Speed of transfer** | The speed for TCP is slower than UDP. | UDP is faster because error recovery is not attempted. It is a “best effort” protocol. |
| **Streaming of data** | Data is read as a byte stream; no distinguishing indications are transmitted to signal message (segment) boundaries. | Packets are sent individually and are checked for integrity only if they arrive. Packets have definite boundaries which are honored upon receipt, meaning a read operation at the receiver socket will yield an entire message as it was originally sent. |
| **Usage** | TCP is suited for applications that require high reliability, and transmission time is relatively less critical. | UDP is suitable for applications that need fast, efficient transmission, such as games. UDP’s stateless nature is also useful for servers that answer small queries from huge numbers of clients. |
| **Use by other protocols** | HTTP, HTTPs, FTP, SMTP, Telnet | DNS, DHCP, TFTP, SNMP, RIP, VOIP. |
| **Weight** | TCP is heavy-weight. TCP requires three packets to set up a socket connection, before any user data can be sent. TCP handles reliability and congestion control. | UDP is lightweight. There is no ordering of messages, no tracking connections, etc. It is a small transport layer designed on top of IP. |

You can think of `UDP` (User Datagram Protocol) as a “message is a bottle”. The message is launched into the great Internet sea in hopes that it will arrive at its destination.

In contrast to `UDP`, `TCP over IP` (TCP/IP) is connection-oriented in similar ways to a Phone call. A user dials a number (e.g., an `IP` (Internet Protocol) address), and waits for the destination to answer before starting their conversation. `TCP/IP` adds other convenient services to this communications path. Foremost is data recovery; if something get lost, corrupted, out of sequence, `TCP/IP` steps in and asks for a re-transmission and insert the pristine data into the correct place.

An often forgotten service that `TCP/IP` provides is the ***connection management.*** Each TCP/IP transmission must be acknowledged, or `ACK`ed, by the destination device.

The source system will wait only a limited amount of time for those acknowledgments. That time interval is called the `re-transmission time`. If this timer expires before the sender receives an acknowledgment from the destination, `TCP` assumes that the `IP` packet was lost and asks for a re-transmission of that allegedly lost packet. Each packet contains a sequence numbers, as well as each acknowledgment. In this way, the sender knows which packet had been lost from the sequence stream.

You guessed it! The communication efficiency is highly sensitive to the time that TCP waits until it begins requesting a re-transmission. TCP calls this time interval the ***`re-transmission timeout` (‘RTO’).*** You could set `RTO` to a static value or ***it is often adaptive.*** Nearly all `TCP/IP` connection use an adaptive `RTO`. ***The point to learn is that any interpolation or extrapolation generated to compensate for network lag or latency will result in an exaggerated response.***

Briefly let’s see how a static `RTO` would affect communications efficiently in a local area network (LAN). Both source and destination systems in a LAN are usually quite close, the bandwidth is quite high, and the time it would take for a packet to travel between them is very short. Clearly, when a packet is lost in a LAN, efficiency is accomplished with a very small `RTO`. However for a MMoG with players [strewn around the world,](http://www.dictionary.com/browse/strewn) and across the ocean, using a standard telephone line, those gamers and gaming server are not close at all, the bandwidth is quite small, and the time it would take for a packet to travel between them is significant. In this case, a small `RTO` becomes a barrier to communication efficiency. If `RTO` were too small, the source device might believe the packet was lost; when, in fact, the game server received that game turn packet and the acknowledged it; however, the `ACK` had not the time to travel back at the source.

***It is not possible to set the value of RTO for each application. It would be much easier if `TCP/IP` could anticipate the response time and set a value for `RTO` in an adaptive manner.*** TCP performs this task by ***estimating the round-trip delay on each socket pair established.*** Since the network that lies between the two end systems is not static, the time for a packet to travel between any two systems is not static either. For that reason, ***the round-trip delay is constantly measured and adjusted to adapt to the changing conditions of the network.*** TCP starts a time counter when a packet is sent and stops it when the acknowledgment is eventually received — this feature is already embedded in the protocol. There no reason to waste CPU processing for these calculations in your gaming engine — something I’ve seen in several recent tutorials, books and articles. `TCP/IP` then writes that value into a variable called the ***`round-trip time` (RTT).*** As more packets are sent and received, the RTT value is continually updated (for your MMoG application) to adapt to the changing conditions of the Internet that lies between the two communicating end systems.

This connection management has a price at the receiving device. The destination holds all incoming data packets and verifies its completeness and re-orders them into the correct sequence. If the destination discovers data packet corruption or just simply missing packets, ***everything freezes in place (aka `head of line blocking`)*** while a re-transmission request is sent and the new bright shiny packets arrive. ***Nope! you can’t fix it; it’s how TCP/IP operates.*** So, Google developed an idea how to fix this — it’s called [***Quick UDP Internet Connection (QUIC).***](https://techcrunch.com/2015/04/18/google-wants-to-speed-up-the-web-with-its-quic-protocol/) Their goal was to combine the best features of UDP and TCP and season it with a little security salt.

![](resources/makingbrowsergames_com---book---imagesConsolidated---0rtt-graphic.jpg)

QUIC promises 0 ms connections!

You can review any network protocol at [http://www.protocols.com](https://web.archive.org/web/20120111061909/http://www.protocols.com) located in the web archives. If you would like access to a long-standing — [***since July 27, 1999!!***](https://stendhalgame.org/wiki/History#The_begining) — MMoG protocol, visit this site: [***Stendhal***](https://stendhalgame.org/wiki/Stendhal_code_design) — ***[https://stendhalgame.org/wiki/Stendhal_code_design](https://stendhalgame.org/wiki/Stendhal_code_design).*** The two layer 4 protocols they use are Transmission Control Protocol (TCP) and User Datagram Protocol (UDP).

**TCP, UDP, SCTP comparisons**

|   | **TCP** | **UDP** | **SCTP** |
| --- | --- | --- | --- |
| Reliability | Reliable | Unreliable | Configurable |
| Delivery | Ordered | Unordered | Configurable |
| Transmission | Byte oriented | Message oriented | Message oriented |
| Flow Control | Yes | No | Yes |
| Congestion control | Yes | No | Yes |

### The Way We Were . . .

In former days of web development, clients would request information on servers and the servers would respond. Each request and response were “separate” web pages, “state-less” and on two different port socket — also referred to as a “communication endpoint”: a transmit port to the server and a receive port from the server. That means each client consumed a dedicated down-stream port on the server for the duration!

**TCP, UDP, Summary:**

| **Function** | **TCP Description** | **UDP Description** |
| --- | --- | --- |
| **Connections** | **This process is used to initialize port numbers and other TCP header fields.** | **UDP is connection-less** |
| **Flow Control** | **This process is used to protect buffer space and routing devices** | **This not a feature of UDP.** |
| **Multiplexing using ports** | **Receiving hosts decide the correct application for which the data is destined, based on the port number.** | **Same as TCP** |
| **Ordered data transfer** | **This involves a continuous stream of ordered data.** | **Does not re-order receive data.** |
| **Reliable transfer** | **Acknowledgment of data uses the Sequence and Acknowledgment fields in the TCP header.** | **This not a feature of UDP.** |

Web developers first addressed the “state-less, transitory” conditions; they wanted the communication transactions to remain “open” and “persistent”. HTTP persistent connection (aka HTTP keep-alive, HTTP connection reuse, or streaming) is a method applied to a single TCP connection. The idea, when applied, sends and receives multiple HTTP requests/responses, as opposed to the normal operations of opening a new connection for each single request/response pair. This will continue until either the client or the server decides that their conversation is over, and one of them closes (or “hangs-up on”) the connection. “It was only in the 1990s that hypertext became **hypermedia,** with a heavy emphasis on embedded graphics and other media files. When Web pages changed from simple text to multimedia marvels sporting dozens or even hundreds of embedded images, the limitations of HTTP/1.0 really became obvious.” In HTTP 1.1, all connections became persistent unless declared otherwise.

| Client | Network | Server |
| --- | --- | --- |
| Collect Input | Pass Data -> | Process Input |
| Render Views | <- Pass Data | Move Objects |

![](resources/makingbrowsergames_com---book---imagesConsolidated---pipelining.jpg)

New persistent connections

Persistent connections (aka pipe-lining or streaming) do not use separate keep-alive messages; they simply permit “multiple requests” across a single connection. However, they have default connection timeouts; for Apache `httpd` 1.3 and 2.0, it is as little as 15 seconds and just 5 seconds for Apache `httpd` 2.2 and above. The advantage gained from such short timeouts is the freedom to deliver “multiple component parts” of a web page quickly while not consuming resources to run multiple server processes or threads for too long.

Introducing “TCP/IP persistent connections” greatly improved HTTP protocol’s efficiency by reducing much of the redundant client/server paired dialogs.

This model changed with the introduction of “Asynchronous JavaScript and XML (AJAX)”. In a nutshell, it is the use of the `XMLHttpRequest` object to communicate with server-side scripts. It sends, ***as well as receives,*** information in a variety of formats, including `JSON`, `XML`, `HTML`, and even text files. Attempts, at this time to provide real-time web applications, largely revolved around ***polling*** and other “push technologies from the server-side”. [***RFC6202***](https://tools.ietf.org/html/rfc6202#page-4) says that, “… both the HTTP long polling and HTTP streaming mechanisms stretch the original semantic of HTTP and that **the HTTP protocol was not designed for bidirectional communication.”**

***What’s long-polling?***

***ANSWER:*** “The browser sends a request to the server and the server keeps the request open for a specific period of time. If a notification is received within that time, a response is sent to the client. If a notification is not received within the specified time, the server sends a response to terminate the open connection. It is important to understand, however, that when you have a ***“high message volume”, long-polling does not provide any substantial performance improvements over traditional polling. In fact, it could be worse,*** because the long-polling might spin out of control into an unthrottled, continuous loop of immediate polls.”²

***What’s is streaming or pipeline?***

***ANSWER:*** “The browser sends a complete request, but the server sends and maintains an open response connection that is continuously updated and kept open indefinitely (or wisely set for a period of time). The response is then updated whenever a message is ready to send, but the server never signals the client to complete the response, thus keeping the connection open for future messages. However, since streaming is still encapsulated in HTTP, ***intervening firewalls and proxy servers may choose to buffer those responses, increasing the latency of the message delivery.*** Therefore, many streaming `Comet solutions` fall back to ***long-polling*** in case a buffering proxy server is detected. Alternatively, TLS/SSL connections can be used to shield the response from buffering; but in that case, the setup and tear-down of each connection taxes the available server resources more heavily.”²

**Security Comparisons**

| Feature | Obfuscated TCP | SSL/TLS/HTTPS |
| --- | --- | --- |
| Browser Support | Patched versions of Firefox available | Widely supported by all popular web browsers |
| Encryption Speed | Very fast cryptography | Slower |
| Network Latency | Nil additional round trips per connection (though DNS lookup may be required to obtain key advertisement) | One or two additional round trips per connection |
| Public Key Infrastructure | Does not require a signed public key certificate | Requires that a signed public key certificate is purchased (or self-signed certificate is used) |
| Security Characteristics | Does not resist some man in the middle attacks | Resists man in the middle attacks |
| Server Support | Requires patches/server upgrades for Light-httpd and Apache | Widely supported by popular web servers |
| TCP Port | Can use any TCP port | Typically uses port 443 |

### New Kid on the Block

Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) have been long-standing protocols used in data communications and [***video conferencing.***](https://en.wikipedia.org/wiki/Videotelephony#Standards) But this wasn’t good enough; [***something changed all that — “WebSocket”!***](https://www.w3.org/TR/websockets/) In 2011, a new standardized WebSockets protocol was introduced and finally stabilized by 2014. Unlike the former half-duplex HTTP/AJAX, WebSockets provide ***FULL DUPLEX*** communications over ***a single TCP connection.*** HTML5 Web Sockets is not just another incremental enhancement to the conventional HTTP communications protocol; it represents a exponential advance, especially concerning real-time, event-driven web applications. The old “convoluted” method fades in the light of Web Sockets’ full-duplex connection, and prompted Ian Hickson — Google’s HTML5 specification lead — to say, “Reducing kilobytes of data to 2 bytes … and reducing latency from 150ms to 50ms ***is far more than marginal.*** In fact, these two factors alone are enough to make Web-Sockets seriously interesting to Google.”

***To summarize the key differences between an WebSocket server and a regular Web server*** is that as soon as you receive information from a Web server, the connection is broken. It may look as if you’re still connected to the Web server, especially with a “single web page application (SWPA)” that’s animating everything. However, that’s not the way it works. When you open a Web page, the Web server sends you that page along with all its associated graphics, text, and other media; and your browser sends an acknowledgment message back saying, “Got it!”, and then that connection request closes the network connection. In contrast, a WebSocket server’s connection stays active and “open” until you quit the application or trigger an event that cuts the connection (i.e., “hang up”). Because a WebSocket connection remains open, you can stream audio, video, text, and any other media available from the Internet — in real time bi-directionally! This is just not possible with a traditional Web server because it has an entirely different architecture.

Since a WebSocket is a bi-directional connection, there’s no technical distinction between a “server” and a “client”; they’re now point-to-point peers. “Senders” and “Receivers” are about the game content and messages. The server needs to adopt a new role: a “peer” which connects multiple “end-user clients”. The server transforms into something similar to a network “router”. So, instead of the game logic sitting totally on a server, the game logic can now sit on the end-user browser as a “proxy-server” which allows other remote end-users to access its local game functions. This concept is the begins of a “Distributed Application” (DApp) — clients calling game logic functions on other client participants directly while the server disappearing into a “cloud service”.

![](resources/makingbrowsergames_com---book---imagesConsolidated---websocketProto.jpg)

Server-side target

It seems everyone is involved with their own WebSocket “flavour du jour” — [***compare various WebSockets here.***](https://en.wikipedia.org/wiki/Comparison_of_WebSocket_implementations). To use WebSockets, you need to have a HTML5 browser and a server that both support the WebSocket protocol. You will also ***need a traditional web server*** such as Apache or IIS to provide your MMoG’s dynamic content. The web server and socket server should be different separate entities but on the same domain.

Sessions through WebSockets work as they do through a traditional web server; a `cookie` is set and transmitted in each request header. This means that your web site and your WebSocket server both must have access to that `cookie`.

In order for session data to be shared between your web site and your WebSocket server ***they must be on the same domain.*** You can achieve this by either hosting them on the same domain and using different ports — such as `mydomain.com:80` (for web site) and `mydomain.com:8080` (for WebSockets). If you choose to host your WebSocket server on a sub-domain (`websocket.mydomain.com:80`) make sure to have your web site’s `php.ini` file configured like this:

session.cookie_domain = “.mydomain.com”

To avoid namespace conflict, I recommended you make your sub-protocol names as part of a domain string. If you are building a MMoG app that uses a proprietary format exclusively, then you might use this: Sec-WebSocket-Protocol: mmog.pbmcube.net. For different versions, a widely-used method is to add a “ / “ followed by the version number, like mmog.pbmcube.net/v2.0\. Note that this isn’t required, it’s just an optional convention, and you can use any string you wish.

HTML5 Web Sockets provides an enormous step forward in the scalability of the real-time web. A typical WebSocket client would be a user’s browser, but the protocol is platform independent. HTML5 Web Sockets could provide a 500:1 or — depending on the size of the HTTP headers — even a 1000:1 reduction in unnecessary HTTP header traffic and 3:1 reduction in latency. That is not just an incremental improvement; that is a revolutionary jump — a quantum leap!

The WebSocket protocol is currently supported in most major browsers. WebSockets also require web applications, residing on the server, to also support it.

| Client | Network | Server |
| --- | --- | --- |
| Collect Input | <- Pass Data -> | Process Input |
| Render Views |   | Move Objects |

My [***first MMoG — Legends of Renown Deeds (LoRD)***](http://legends-of-renown-deeds.com) [http://legends-of-renown-deeds.com](http://legends-of-renown-deeds.com) used AJAX before the protocol became popular by that name. I am upgrading it to WebSockets; this workbook is also my own guide and development research in doing so.

![](resources/makingbrowsergames_com---book---imagesConsolidated---IBMsocket.jpg)

IBM* How do sockets work

**Note:** The socket APIs are located in the communications model between the application layer and the transport layer. The socket API is not a layer in the OSI communication model. Socket APIs allow applications to interact with the transport or networking layers of the typical communications model. The arrows in the following figure show the position of a socket, and the communication layer that the socket provides.” [***IBM How do sockets work***](http://www.ibm.com/support/knowledgecenter/ssw_ibm_i_71/rzab6/howdosockets.htm)

WebSocket implementation was designed for web browsers and web servers, but it can be used by any client or server application. WebSocket is ideal ***for most client-to-server asynchronous purposes,*** for example, chat servers being the most prominent deployment. In fact, Snap-chat’s overarching strategy as of 20190301 is to build an orbit of time-wasters surrounding chat. Since messaging is the top mobile behavior, Snap uses chat and Multi-Player games to keep people coming back and then distract them with a Multi-Player entertainment while they’re waiting for a reply or need a social alternative to small talk. This make WebSockets an ideal candidate for turn-based MMoG. The WebSocket Protocol ***is independent from TCP-based protocol. It [“rides on top of” TCP/IP per RFC6455 Section 1.5 & 1.7](https://tools.ietf.org/html/rfc6455#section-1.5).*** The only relationship to HTTP is that WebSockets’ handshake is interpreted, by any HTTP servers, as an [***Upgrade request.***](https://en.wikipedia.org/wiki/HTTP/1.1_Upgrade_header) If the server supports WebSockets, it will respond with a `HTTP/1.1 101 Switching Protocols` response. This instructs the client-side browser to maintain an open connection across the `ESTABLISHED TCP CONNECTION`, and begin using that connection over a (or different optional) port as if it were streaming the data. WebSockets [***replace AJAX long-polling***](https://tools.ietf.org/html/rfc6202#page-3) – a method we saw earlier that is often attributed to poor resource utilization. **This new protocol allows more interaction between a browser and its web server, facilitating a real-time data transfer to and from the server.** This endows the game server with a standardized method to transmit unsolicited information to attached clients; and furthermore, maintain that open, full-duplex connection path. In doing so, a **simultaneous two-way dialog** takes place between the browser and the gaming server. WebSockets use the default HTTP port number 80 initially; the benefits gained from this, allows MMoG to transit firewalls filters that would otherwise block any utilization of “non-web ports”. Similarly, two-way browser-server communications are achieved in place of the former non-standardized (aka stopgap) technologies such as **Comet.** All WebSocket messages are framed automatically by the socket. So once one end finishes writing, the message will be available at the remote side. The WebSocket automatically decides how many bytes belong to each message. This feature alone makes WebSockets considerably easier to program when compared to normal regular sockets.

WebSockets further implement their own command (aka Ping) and response (aka Pong) protocol semantics; this allows the connection to remain alive when nothing is queued for transmission (e.g.: absence of any data being sent). WebSockets uses [***ABNF snytax per RFC6455 Section 3***](https://tools.ietf.org/html/rfc6455#page-14). This is something you typically have to account for with TCP connections that ***time-out at 255 seconds.*** Another useful security feature is the ability to use HTTP authentication semantics for the socket, such as the Authorization header for ***Basic Auth*** or ***Bearer Token Auth. ([Discussed in RFC6455 Section 5.1](https://tools.ietf.org/html/rfc6455#page-27))***

![](resources/makingbrowsergames_com---book---imagesConsolidated---ssl.jpg)

Secure Sockets

### Deeper Dive: WebSocket Frame

```
 1       0                   1                   2                   3
 2       0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1 2 3 4 5 6 7 8 9 0 1
 3      ┌─┬─┬─┬─┬───────┬─┬─────────────┬───────────────────────────────┐
 4      │F│R│R│R│ opcode│M│ Payload len │    Extended payload length    │
 5      │I│S│S│S│  (4)  │A│     (7)     │           (16/64)             │
 6      │N│V│V│V│       │S│             │   (if payload len==126/127)   │
 7      │ │1│2│3│       │K│             │                               │
 8      ├─┴─┴─┴─┴───────┴─┴─────────────┘  -   -   -  -  -   -   -   -  ┤
 9      │   Extended payload length continued, if payload len == 127    │
10      ├ -   -   -  -  -   -   -   -  -┌───────────────────────────────┤
11      │                               │ Masking-key, if MASK set to 1 │
12      ├───────────────────────────────┼───────────────────────────────┤
13      │ Masking-key (continued)       │          Payload Data         │
14      ├───────────────────────────────┘ -   -   -  -  -   -   -   -   ┤
15      │                   Payload Data continued  ...                 │
16      ├ -   -   -  -  -   -   -   -  -  -   -   -  -  -   -   -   -   ┤
17      │                   Payload Data continued  ...                 │
18      └───────────────────────────────────────────────────────────────┘
```

RFC 6455 page 27: WebSocket Frame is 2 bytes of overhead

The base framing protocol defines bits 4 to 7 as the 4 bit Opcode, which defines the content type for the payload data. Here’s the Web Socket frame building blocks:

*   ***`fin` (1 bit):*** indicates if this frame is the final frame that makes up the message. Most of the time the message fits into a single frame and this bit will always be set. Experiments show that Firefox makes a second frame after 32K.
*   ***`rsv1`, `rsv2`, `rsv3` (1 bit each):*** must be 0 unless an extension is negotiated that defines meanings for non-zero values. If a nonzero value is received and none of the negotiated extensions defines the meaning of such a nonzero value, the receiving endpoint must fail the connection.
*   ***`opcode` (4 bits):*** says what the frame represents. The first frame that transmits the data has an opcode on it that indicates what sort of data is being transmitted. This is necessary because JavaScript has pretty much nonexistent support for binary data at the time the specification was started. Most people will transmit JSON in which case you’d probably want to choose the text opcode. The following values are currently in use:

    - ***`0x00`:*** this frame continues the payload from the previous.
    - ***`0x01`:*** this frame includes utf-8 encoded text data.
    - ***`0x02`:*** this frame includes binary data.
    - ***`0x08`:*** this frame terminates the connection.
    - ***`0x09`:*** this frame is a ping.
    - ***`0x0a`:*** this frame is a pong. (As you can see, there are enough values unused; they’ve been reserved for future use).

*   ***`mask` (1 bit):*** indicates if the connection is masked. As it stands right now, every message from a client to a server must be masked and the spec would want to terminate the connection if it’s unmasked.
*   ***`payload_len` (7 bits):*** the length of the payload. WebSocket frames come in the following length brackets: 0–125 indicates the length of the payload. 126 means that the following two bytes indicate the length, 127 means the next 8 bytes indicate the length. So the length of the payload comes in ~7bit, 16bit, and 64bit brackets.
*   ***`masking-key` (32 bits):*** all frames sent from the client to the server are masked by a 32-bit value that is contained within the frame.
*   ***`payload`:*** the actual data which most likely is masked. Its length is the length of the payload_len.

## 3.6 Chapter Summary

Here’s what we’ve learned thus far:

*   How data flows to and from devices on the Internet.
*   How data flows inside a workstation from the Application to the wire.
*   The upper layers are concerned with software.
*   The lower layers are concerned with hardware, network connectivity.
*   ***Discovered 2 FREE books!*** The first written by a web performance engineer at Google and co-chair of the W3C Web Performance Working Group, and ***should become the sole source of authority concerning online game performance.***
*   Device within a network create a relationship of services offered and provided.
*   Online game use a modified client/server relationship.
*   Authoritative game servers are the hub of gaming activity.
*   MMoG are impacted by several networking obstacles.
*   WebSockets have replaced former client / server paradigms.
*   Security should be considered as the game project begins.

** Any multi-player game articles, tutorials, source code written prior to 2014 does not support or even mention WebSockets.

## 3.7 Chapter Foot Notes

1.  [JavaScript and HTML5 Now - A New Paradigm for the Open Web](https://www.oreilly.com/programming/free/javascript-html5-now.csp) by Kyle Simpson. O’Reilly ***a free book [https://www.oreilly.com/programming/free/javascript-html5-now.csp](https://www.oreilly.com/programming/free/javascript-html5-now.csp)***
2.  [“HTML5 WebSocket: A Quantum Leap in Scalability for the Web”.](http://www.websocket.org/quantum.html) Retrieved 25 July 2016.
3.  [HTTP Transitory and Persistent Connections and Pipelining](http://www.tcpipguide.com/free/t_HTTPTransitoryandPersistentConnectionsandPipelinin.htm)
4.  Measure TCP latency using [***latsub.js***](https://github.com/circonus-labs/latsub)

# Part II: MMoG Architecture

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogFlow3.jpg)

Part II- MMoG Architecture

# 4 MMoG Engine Analysis

## 4.1 What is a Game Engine?

In the broadest sense of the term, a game engine could be defined as “middleware”. Jeff Ward describes it in this way . . .

## 4.2 To “B”uild or not to “B”uild, that’s the question!

We have a few choices. We can either:

*   Write our own server-side MMoG engine, application, and WebSocket transport management … but then when you study all the files required to manage just a WebSocket connection [***in many provided libraries,***](https://github.com/socketio/socket.io-client) it becomes obvious why we are not writing our own server-side transport code, unless socket communication protocols and other such low-level transports really stimulate your interests. ***or***
*   We can use/borrow [***the works of someone else,***](http://npmsearch.com/?q=websocket) who has thought through this process.

If we write our own, our project development completion time will be extended, of course. ***If we are permitted to use an establish MMoG engine,*** we will need time to learn how it works, and may ***(or may not)*** have permissions to modify it. Returning to Jeff Ward’s article, [***See footnote 1:***](http://www.gamecareerguide.com/features/529/what_is_a_game_.php?print=1)

You found hundreds! Right? GitHub has 5,000+. Many are open source, and want you to join their development team (for free!). Which one should we use? We do not want to repeat a story like this:

In order to make some game development decisions on the best solution for our MMoG, we need a good understanding of how our MMoG will operate; that is the primary focus, in this book, for both my ***MMoG game rules section*** and the ***MMoG gaming engine.*** Those sections demonstrate the “ins & outs” of my MMoGs. Let’s start by asking some more questions about what we want in our MMoG. The story above provided a few questions, but let’s add onto those.

*   What is Inter-Process Communications (IPC) and how will we construct it? [***See answer from Wikipedia here.***](https://en.wikipedia.org/wiki/Inter-process_communication) ***Jot down the various IPC “approaches”, “synchronization”, and “Remote procedure call interfaces” for use in upcoming Chapters 6, 7, and 8.***
*   How complex are the game mechanics interactions between our gamers and our MMoG server application? Are we building a “first person shooter” (FPS) for **real-time interaction** or is our game a **“turn-based MMoG”** similar to checkers or chess? ***(review your previous exercise answers; save them for Chapter 8! Spoiler ALERT!*** You’ll discover in Chapter 8 that MMoGs, designed to be turn-based (i.e., chess; See Part IV), or games in which only a single player is actively modifying the game session data at any given time (i.e., poker or the hundreds of games claiming MMoG status), **network latency is not an issue.** Creating such games, **in reality,** is no different than creating a [***Progressive Web Application (PWA).***](https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/) (See MDN article: [***Making PWAs work offline with Service workers***](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Offline_Service_workers)))
*   What is our game’s “back-end” and “front-end” architecture (i.e., [***Inter-Process Communication (IPC) synchronous or asynchronous***](https://www.nginx.com/blog/building-microservices-inter-process-communication/)) and data flow-control processing? (i.e., [***MVC***](https://www.tutorialspoint.com/mvc_framework/mvc_framework_introduction.htm), [***MVP, MVVM, MVP-VM, MOUSE?***](http://aviadezra.blogspot.com/2007/07/twisting-mvp-triad-say-hello-to-mvpc.html)) A front-end JavaScript game developer, who typically use Phaser, is responsible for creating the game HUD logic — those items that define the behavior of all those visual elements. A front-end JavaScript game developer is also responsible for connecting these components with the MMoG services on the back-end. They are usually supported by back-end web software developers, who create the server-side MMoG application logic.
*   What game information should be collected, and across which transport format or communication architecture? (i.e, [***XML-RPC,***](http://xmlrpc.scripting.com/) SOAP, [***REST, GraphQL,***](https://medium.com/codingthesmartway-com-blog/rest-vs-graphql-418eac2e3083) JSON, BSON, SOAPjr, [***JSON-RPC,***](https://github.com/bigstepinc/jsonrpc-bidirectional) [***gRPC,***](https://en.wikipedia.org/wiki/GRPC) [***GraphQL,***](https://medium.com/codingthesmartway-com-blog/rest-vs-graphql-418eac2e3083) etc.), and where will it be stored (i.e. [***centralized “ACID” or distributed microservices “BASE”***](https://www.dummies.com/programming/big-data/hadoop/acid-versus-base-data-stores/))? As mentioned before, WebSockets are only bidirectional conduits. WebSockets do not examine the data content of any inbound or outbound stream; it only ensures the data-flow will reach the other end of the channel. This isn’t a problem as long as the data processed is merely echoed or lightly processed by NodeJS. However, we need a more evolved messaging protocol for our MMoG App. Again, we are not going to “reinvent the wheel”; there are many well-established messaging protocols that offer client/server as point-to-point or publisher/subscriber models over the top of WebSockets. This brings us to our next question . . .
*   What will client/server data “packages” look like and in what format? (i.e, [***0MQ,***](http://zeromq.org/intro:start) [***AMF,***](https://github.com/jamesward/JSAMF) [***AMQP***](https://www.amqp.org/) or Apache [***QPID,***](https://qpid.apache.org/overview.html) [***MQTT***](http://mqtt.org/) (Message Queue Telemetry Transport; an ISO Standard [***(ISO/IEC 20922)***](http://www.iso.org/iso/catalogue_detail.htm?csnumber=69466) and [***HiveMQ***](https://www.hivemq.com/blog/mqtt-essentials-special-mqtt-over-websockets/), [***RabbitMQ,***](https://www.rabbitmq.com/) [***STOMP***](http://jmesnil.net/stomp-websocket/doc/) (simple text-oriented message protocol), [***UMF,***](https://github.com/cjus/umf/blob/master/umf.md) [***WAMP,***](https://wamp-proto.org/) and [***XMPP***](https://xmpp.org/) as per [RFC7395](https://tools.ietf.org/html/rfc7395) and a [***comparison chart here.***](https://wamp-proto.org/comparison.html)) Just because we have a steady stream of data, doesn’t mean either side will understand how to read the data flow. It must have a structured format — for example [***Telnet byte-oriented protocol.***](https://en.wikipedia.org/wiki/Telnet#History_and_standards) Is it binary (greatly secure) or text (anyone can read)? Data “blobs”, chunks or small “twitter-style” messages (i.e. short message service (SMS) whose payload length is limited by the constraints of the signaling protocol to 140 bytes ((140 bytes * 8 bits) / byte = 1,120 bits). (you should have [***already researched UMF***](https://github.com/cjus/umf/blob/master/umf.md) from previous exercises)
*   Will gamers have a “point-to-point” connections (aka Peer-to-Peer), “hub-and-spoke” (aka client-server central authoritative network), or use “multicast”? Are we using an [***“overlay network”***](https://blog.scottlowe.org/2013/04/16/network-overlays-vs-network-virtualization/) or out sourcing our needs to [***IaaS, PaaS, SaaS?***](https://www.juniper.net/documentation/en_US/release-independent/solutions/topics/concept/solution-iaas-understanding.html)
*   Will we store persistent game data? and where will it be located? on the gamer’s device, our database, [or a microservice.](http://microservices.io/) Can the gamer(s) return to the game and start when/where they left the game-world environment?
*   Will we push “unsolicited updates” out to the gamers or will the server only “respond” to “events” such as “end of turn”? (you’ve already learned about this is earlier chapters and wrote down your answers, RIGHT?)
*   Will the server synchronize all the gamers data on the client or maintain a single self-storage (i.e., [***Ghosting server***](https://crossbario.com/blog/Free-Your-Code-Backends-in-the-Browser/)) and simply inform game-clients of deltas (aka changes)?
*   Do we want a “chat feature” for players to exchange messages and taunts to each other? (add to a list of features you may want in your MMoG)

## 4.3 Purpose of XML and JSON

Following quoted from “[***Rest API Tutorial - JSON vs. XML***](https://restfulapi.net/json-vs-xml/)”.

## 4.4 MMoG engine Criteria:

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogFlow.jpg)

My old-style MMoG flow: Request & Respond RPC using Flash plugin as a Thick Client

So, let’s develop some criteria about “what it is” I’m (we’re) looking for in my (our) new technology MMoG.

Here’s where we might [***part ways.***](https://en.wiktionary.org/wiki/part_ways) I’m developing and Journaling my MMoG development and trying to be as transparent as possible for you to adopt or re-consider my process for your own game project.

1.  It must permit [***Web Graphics Library (WebGL)***](https://en.wikipedia.org/wiki/WebGL) on the client-side using the latest release of Phaser JavaScript Game Framework (either v2.6.2, CE and/or v3\. Sounds strange that we mention this since the server-side normally ***would not have a GUI (well, perhaps an administration GUI access, but even still, that’s inside the admin. browser. The administrator is just a special permission client).*** Why would that concern the client-side browser? ***You’re right!*** If, during our search, we discover those MMoG Server-side engines dictating to us the browser/client-side, then we give them the “boot”.
2.  It must be free (aka no royalty payments), must be open source and provide copyright guarantees on our modifications and addendum that we add into the engine — assuming we have the license to “add or modify” the engine. ***This rules out [any GNU/GPL licenses in any form! (click to review)](http://choosealicense.com/)*** It has got to be ***free;*** since, we are trying to build a start-up company. If you would like to spend money with no guarantees of a return on your investment (aka ROI), well …. mmmm, … er, I’ve got some swamp-land in Arizona I’d like to get rid of …. Interested? ***:) (You ARE AWARE THAT THIS WAS A Real Estate JOKE?! Right?)***
3.  It ***must use*** JavaScript/[JQuery](https://jquery.com/) ([ECMA262](http://www.ecma-international.org/ecma-262/7.0/index.html), [ES5, ES6](http://benmccormick.org/2015/09/14/es5-es6-es2016-es-next-whats-going-on-with-javascript-versioning/), [ES7 or ES8/ES9](http://v8project.blogspot.com/2016/04/es6-es7-and-beyond.html) ) on the client-side and preferably on the back-end server-side since creating several iterations of code in multiple programming languages would slow our progress. ([***Service-Oriented Architecture (SOA)***](https://en.wikipedia.org/wiki/Service-oriented_architecture) allows the selection of the proper programming to match the task.) Our second preference is a [“curly brace” language](https://en.wikipedia.org/wiki/List_of_programming_languages_by_type), for the back-end server-side, since JavaScript has similar syntax. ***(you’ve researched this site? Right? [http://kangax.github.io/compat-table/es2016plus/](http://kangax.github.io/compat-table/es2016plus/))***
4.  It must support a variety of [***game mechanics***](http://makingbrowsergames.com/gameDesigner/index.html). As for me, I would like to build more than just first-person-shooters; the market is saturated with them already. Time is my most precious commodity; I want a framework that is corrigible, flexible and adaptable to any game mechanic I could imagine. However, if I ***am building a game mechanic*** that is similar to an engine’s framework, then it would be considered. The only time wasted is the learning-curve on this new unfamiliar engine architecture.
5.  It must be stable and mature, and provide an [***Application Programming Interface (API).***](https://en.wikipedia.org/wiki/Application_programming_interface) I don’t want my interfaces changing because of some “lover’s quarrel”, the crew quits or abandons their project.
6.  It must have a “Low to No” (L2N) learning-curve on its API. (Translates as, “I pick my own IDE that I will use, and have used for years, to develop my projects. Last thing I need is a learning-curve obstacle on a new IDE that would merely change, expire, loose traction, and fade away. 10 years ago, if I said, ***“Flash will never survive”;*** I would have been that brunt of any-and-every-game-developers’ joke! Look where Macro Media/Adobe Flash plugin is today on the client-side? ***GONE!!! Adobe announced the “end-of-life” for Flash is 2020.***
7.  ***It must provide exceptional documentation. This translates into, “they are serious and committed to their code releases, having put considerable thought into its creation, understanding and documentation.” … enough said?!***
8.  Does not go overboard with external dependencies on the server-side. (Translates as, “. . . the code is only as good as it weakest link.”) Why? kindly review [http://kangax.github.io/compat-table/es2016plus/](http://kangax.github.io/compat-table/es2016plus/) and you will discover that it’s ***not*** the browsers that have the problems, but rather it is the ***transpilers, compilers and polyfills!***
9.  It must provide ***not only a local engineering test lab capabilities,*** but also work ***on a live production server in a similar manner as the test/development environment. (WordPress, are you listening??!!)*** Too many times I have read articles on MMoG engines that demonstrates “one-browser-window to another-browser-window across the ***same mother-board!” OMG! I might as well have created a “hot-seat” multi-player game.*** These are “proofs of concepts” —NOTHING MORE— and are not viable candidates. Sending packets across the local bus ***is not the same as sending packets across a WAN.***

Now with this list in hand, let’s start searching.

*   [https://developer.mozilla.org/en-US/docs/Games/Tools/Engines_and_tools](https://developer.mozilla.org/en-US/docs/Games/Tools/Engines_and_tools)
*   [https://github.com/showcases/game-engines](https://github.com/showcases/game-engines)
*   [https://en.wikipedia.org/wiki/List_of_game_engines](https://en.wikipedia.org/wiki/List_of_game_engines)
*   Appendix references.

### Here’s my list and chart: (not in order of preference)

*   ***Browser Quest (master): [https://github.com/mozilla/BrowserQuest/tree/master/server](https://github.com/mozilla/BrowserQuest/tree/master/server)*** — A HTML5/JavaScript multi-player game experiment. Dynetis Game has refactored this work into Phaser v2.6.2; you can [review it here](https://phaserquest.herokuapp.com/) and read about his [development here](http://www.dynetisgames.com/2017/03/18/phaser-quest/). His game was released MAR 2017 — several weeks after this book’s first edition was released in FEB 2017.
*   ***Total.js: [https://www.totaljs.com/](https://www.totaljs.com/) —*** “Total.js framework is a server-side framework ***for Node.js*** written in ***pure JavaScript*** similar to PHP’s Laravel or Python’s Django or ASP.NET MVC. It effectively improves the most important aspects of your project during its lifetime. Super fast development, extremely low maintenance costs, rock solid stability, incredible performance and easy scaling.”
*   ***Torque 2D [https://www.garagegames.com/products/torque-2d](https://www.garagegames.com/products/torque-2d) —*** Torque 2D is an extremely powerful, flexible, and fast open source engine dedicated to 2D game development. The MIT licensed version of Torque 2D is now available on GitHub. Torque 2D was developed with OS X, Windows, and iOS devices in mind and works equally well on all the platforms. As with all of Game Garage products, Torque 2D includes the complete C++ source code to the engine and many example toys. It also includes access to TorqueScript, their scripting language which allows developers to write the same gameplay logic on Windows or OS X and have it work on the other platforms!
*   ***pomelo: [http://pomelo.netease.com/](http://pomelo.netease.com/) —*** A fast, scale-able, distributed game server framework ***for Node.js.***
*   ***Eureca: [http://eureca.io/](http://eureca.io/) — a Node.js*** bidirectional Remote Procedure Calls (RPC) that can use WebSocket, WebRTC or XHR fallback as transport layers.
*   ***Isogenic: [http://www.isogenicengine.com/](http://www.isogenicengine.com/) —*** HTML5 2D and isometric scenegraph-based game engine written entirely in JavaScript. Quoted from their website, ***“Unlike other engines that throw in Socket.IO or another networking library and call it ‘Multi-player,*** Isogenic Engine provides the most advanced networking and real-time Multi-player functionality available in any HTML 5 game engine. The system is based on entity streaming and includes powerful simulation options and client-side entity interpolation from delta updates. … Isogenic’s code base runs the same API on both a browser and ***for Node.js*** and comes with a built-in Multi-player server module. You write the same code, in the same language and call the same API from both the client and server making Isogenic a truly JavaScript-only engine from front-to-back.”
*   ***primus master: [https://github.com/primus](https://github.com/primus) —*** “… also known as universal wrapper for real-time frameworks. There are a lot of real-time frameworks available for ***for Node.js*** and they all have different opinions on how real-time should be done. Primus provides a common low level interface to communicate in real-time using various real-time frameworks.” — quoted from their github repository.
*   ***lost colony (master): [Pro HTML5 Games by Aditya Ravi Shankar](http://amzn.to/2iNoJVX);*** excellent chapter on html5 multi-player games.
*   ***Socket.IO: [http://socket.io/](http://socket.io/) —*** is a client-server PubSub service implementation written in JavaScript. “FEATURING THE FASTEST AND MOST RELIABLE REAL-TIME ENGINE”, a quote from their website. It is an external `npm` add-on package that ***further extends node.js*** functionality. ***WARNING: from [Socket.IO documentation: (quote)](https://socket.io/docs/server-api/) “… It should be noted the Socket doesn’t relate directly to the actual underlying TCP/IP socket and it is only the name of the class.”***
*   ***CouchFriends: [https://github.com/Couchfriends](https://github.com/Couchfriends) —*** Couchfriends allows game creators to host their (HTML5) games and provide an open source API for real-time communication through WebSockets. It’s completely free to upload and host your games.
*   ***Arianne server: [http://stendhalgame.org/wiki/Main_Page](http://stendhalgame.org/wiki/Main_Page) —*** written in Java & Python, but worth studying. The Arianne project started in 1999 and is still active today. Currently, they are working on their Marauroa framework engine for developing Internet-based multi-player adventure game entitled “Stendhal”.
*   ***Astonia: [http://astonia.com/](http://astonia.com/) —*** highly successful game in the early millennium. Written in C++ with a Visual Basic client-side. Worthy of the time to download and study.

![](resources/makingbrowsergames_com---book---imagesConsolidated---socketSelection.jpg)

Personal Judgment on Available Technologies

So, I will choose my top 4 candidates; you do the same with your evaluations and listings. You are modeling my steps and decisions anyway; therefore, we can have different “server-side engines” still performing the same tasks and services toward the Phaser Client-side browser. Let’s dig a little deeper into our likely candidates.

## 4.5 Server-side Research

Before we get too happy about how far we’ve come, let’s look down the road and envision ***where we need to be.*** We will deploy our MMoG on a public web-server; it will have a normal [standard web-stack.](https://news.netcraft.com/archives/2016/12/21/december-2016-web-server-survey.html) You can find hundreds of Internet articles on multi-player HTML5 games ***using Node.js.*** Nearly every article requires you to install Node.js locally and start-up its `node http server`. This is wonderful for your development and testing server. But, stop and ask yourself these simple questions, during your local Node.js installation, while giggling and muttering with your best Frankenstein accent “It’s A Live!”

***Can you perform every task on a remote Public server that you just did your local workstation?***

Will your hosting “cloud” provider ***allow you to do those same tasks to their server?*** And if so, at what price and throttling conditions?

***ANSWER: Sure you can!*** If it’s a dedicated or possibly semi-dedicated server or you have purchased server management (aka data-center, co-located, baby-sitting for your precious pet server or are renting a [***“Platform-as-a-Service (PaaS)”***](https://www.bmc.com/blogs/saas-vs-paas-vs-iaas-whats-the-difference-and-how-to-choose/)). There are other options we will cover at the end of this chapter. If you are [considering ***Cloud microservices,***](http://gose-internet-services.net/hosting-articles/what-does-cloud-web-hosting-represent/) a more thorough research is required! I’ve seen too many MMoG launches that collapse due to Cloud microservices **terms of use;** all of which could have been avoided and many wonderful MMoG would still be available today, if only …. For a quick search, take your list and pricing on dedicated and semi-dedicated and compare to [http://cloud.google.com/pricing](http://cloud.google.com/pricing)

I think we might have [“the cart before the horse”](https://en.wikipedia.org/wiki/Cart_before_the_horse). Wouldn’t it make more sense to have your testing/development environment mimic your actual live-production environment ***exactly*** instead of forcing your public (horse-powered) server to match-up to your local workstation (cart)? ***Let’s resolve that, and make our local testing/development match our production servers.*** Here’s some reasons why.

And thus, the “food-chain” begins to consume more and more dependencies. Isn’t this the path we swore not to follow? ***Will our public server permit us to install all of these?***

So why does Node.js need Express and Socket.IO?? Because Express is simply a routing and ***middleware web framework; that’s it!*** Express has minimal functionality on its own. Express is only a series of middleware function calls. We could replace Express with our own [“home-spun”](https://www.merriam-webster.com/dictionary/homespun) middleware of whatever flavor we choose. [Here’s the functions we would need to write](http://expressjs.com/en/resources/middleware.html) to replace Express entirely; or, we could choose a [popular Content Management System (CMS).](https://en.wikipedia.org/wiki/List_of_content_management_systems)

Ok, so what about Socket.IO? Why does Node.js use the Socket.IO dependency? Well, [***hold onto your hats***](https://idioms.thefreedictionary.com/Hold+on+to+your+hat!) cowboys. We’re in for [***a wild ride!***](https://www.youtube.com/watch?v=EpgP2Gtx8QY) Wikipedia states:

Don’t close the book and give-up yet! There are some suggestions later in this chapter (Server Alternatives Section) that you might find useful.

***Do not rush through these exercises; it will cost you in time, money and resources later. Remember the story at the beginning of this chapter?***

You have a list of likely ISP hosting providers now; so set-up your development workstation using their “web stack”; if its a Linx or Unix web-stack use either: XAMPP, WAMP, LAMP or IIS for Microsoft depending on your public deployment. I’m using XAMPP with [***PHP7 middleware***](https://philsturgeon.uk/php/2016/05/31/why-care-about-php-middleware/) on my local workstations — since my ISP supports the Apache web stack and PHP7\. It takes the same amount of time to load and install anyone of these as it would installing ***Node.js*** via npm. The advantages you gain is a full-blown web-server instead of a “Node.js look-a-like” with all it dozens of dependencies.

## 4.6 Vetting our candidates

I chose the top 4-ranking candidates, and had a tie for fourth place between “CouchFriends” and “Total.js”. Socket.IO (WebSockets) took 1st place; it also appears that:

*   “Eureca” [http://eureca.io/](http://eureca.io/) claims to be a “a nodejs transparent bidirectional RPC. Its supported transports are: ***engine.io, sockjs, WebRTC, Faye, raw websocket”*** which if chosen will provide a great deal of flexibility. It is a mature framework with current active development. They have a tutorial for Phaser integration which converts one of Phaser’s games from a single player mode into a multi-player mode. Excellent! They have packaged their code nicely into its own name-space of 10 separate files. That’s not too bad to learn. They use TypeScript to write JavaScript. Again, that ok. 11 examples to learn various aspects of their framework. EurecaServer.js is 75.3KB and EurecaClient.js is nearly the same size. I guess the flexibility in choosing various transports is responsible for the exessive bloat. Documentation is sparse and succinct.
*   “CouchFriends” [https://github.com/Couchfriends](https://github.com/Couchfriends) is a wrapper directly into the WebSocket protocol. This is good. They use canvas which could be easy replaced with our Phaser Framework. They have packaged their code nicely into its own name-space and weighs in at 17.5KB. They “eat their own dog-food” which is encouraging. They are only roughly 2 years on the market. For this book’s 3rd edition updated (20180516), it appears CouchFriends has gone the way of the [“dodo”](https://en.wikipedia.org/wiki/Dodo) Thanks to the almighty, I have a copy of thier Github and the truly talented content they provided.
*   “Total.js” [https://www.totaljs.com/](https://www.totaljs.com/) is a mature framework with current active development, has a large installation base, and community. They are a wrapper for Node.js with no dependencies. ***They have a sample [MMoG game template on their Github.](https://github.com/totaljs/emptyproject-game)*** This is great! Tutorials are “reading the source code comments” and researching 100+ examples; oops, this might be time consuming. They do have a vanilla game project for download. They use canvas which could be easy replaced with our Phaser Framework. The game project uses WebSocket protocol directly on the client-side. The server-side appears to follow standard Content Management Systems MVC. One drawback is the size of this framework; it is HUGE! It will take some time to learn.
*   Lost Colony is the last two chapters from [Pro HTML5 Games by Aditya Ravi Shankar](http://amzn.to/2iNoJVX). If you do not own this book, this option will be meaningless. Yet, his content was an immeasurable help in my MMoG development.

***Say,What?!*** Which “socket”? It appears that Socket.IO will choose communications based on “who and what browser versions” visit our MMoG, ***and activate only if that browser has JavaScript enabled.*** We will need highly flexible server-side code for each scenario. There are several topics which raise concerns from that article:

1\. Client-side browsers must have JavaScript enabled. How do we coax our clients to activate JavaScript or should we be concerned? [BuzzFeed](https://www.buzzfeed.com/) recently revealed that around 1% of requests for their JavaScript timed out, equating to [***13 million failed requests per month.***](https://twitter.com/philhawksworth/status/990890920672456707) I think this author’s article may help us understand [“the experience of using the web page without JavaScript”.](https://www.smashingmagazine.com/2018/05/using-the-web-with-javascript-turned-off/) He quotes from [Blockmetry](https://blockmetry.com/blog/javascript-disabled) that 0.02% of all UK users have JavaScript turned off; Finland (1.3%) is in the top 20 countries with JavaScript turned off. [Read more from here](https://blockmetry.com/blog/javascript-disabled)
2\. The hint about browsers’ ability to even use the WebSocket protocol. Let’s answer this concern now. Researching “browser capabilities” at `canIuse.com` ([http://canIuse.com](http://canIuse.com)), I found reports stating, that today, 92% of the globally-used latest-released [browsers can support WebSockets](http://caniuse.com/#search=sockets). As of June 2016 WebSocket works on everything — including IE ***higher than version 9*** — ***except Opera Mini.*** Whew! That’s a sigh of relief; but, there’s still that problem concerning “ … enabling JavaScript on the client-side browser”.

— However, should we be concerned that Opera Mini will not work? Let’s research and see. Opera Mini is one of the world’s most popular web browsers that works on almost any phone or tablet with a market share of roughly 7% of all those browsers. When a user surfs the web with a “Opera Mini” browser, the requests are sent to the [General Packet Radio Service (GPRS)](https://en.wikipedia.org/wiki/General_Packet_Radio_Service) to one of the [Opera Software Chinese proxy servers](https://en.wikipedia.org/wiki/Opera_Software); and from which, retrieves their web pages, processes and compresses it, then sends it back to the user’s mobile phone. [This site provides the data we need to make an evaluation.](https://www.netmarketshare.com/browser-market-share.aspx?qprid=0&qpcustomd=1) So, if our final goal is releasing ***a mobile app MMoG, this is a show-stopper for implementing WebSockets technology across Opera Mini browsers!*** (… add to the list of growing problems.)

3\. What is the relationship between Socket.IO and ***Node.js?*** Socket.IO ***is not the WebSocket protocol*** but is rather an “abstraction layer API on top of and depends upon” WebSockets. So, ***what does Socket.IO really offer?***

— Returning to [David Walsh’s article](https://davidwalsh.name/websocket), he says, “Wouldn’t it be great if an API was available that would provide WebSocket event handling, fallback transports, ***and a server side solution,*** all within one API? **Luckily Guillermo Rauch has created Socket.IO.”** Well then, this sounds wonderful.
— [Ivan Vanderbyl provides this rational counter-warning](https://medium.com/@ivanderbyl/why-you-don-t-need-socket-io-6848f1c871cd#.oates1gsg), “Socket.IO became insanely popular, with over 25,000 stars on Github, and 5,000+ forks. … ***But the project always felt like it was trying to do too much. Is it a chat library? Is it a presence service? Is it a Socket? Is it a Sledgehammer? (I would have named it Sledgehammer.IO)*** … Nowadays, Socket IO 1.7.x is ***actually two libraries:*** 1) [Engine.io](https://github.com/socketio/engine.io) — which powers the socket abstractions, and connection management of WebSockets. And, 2) Socket.IO — which, from what I can figure, handles reconnection, event emitting, and message namespacing (kind of like chat rooms). ***This is all excess when all you really need or want is a Socket.”***
— Phil Leggetter — Head of Developer at [Nexmo](https://www.nexmo.com/), a real-time web evangelist, consultant and author of [Real-time Web Apps: With HTML5 WebSocket, PHP, and jQuery](http://amzn.to/2jAYnbH) says, “Socket.IO has done an amazing job when it comes to making people aware of real-time web technology. And it’s a great solution. ***But, it shouldn’t be the default choice when choosing your real-time web solution.*** You should instead take a number of factors into account. Then, if it provides the functionality required to meet your requirements, use it. But there are lots of other fantastic real-time web solutions available that may be a better fit or your application’s needs.”

4\. Socket.IO ***will choose*** other transport methods based upon “who with what version of browser” subscribes. So, we will have to write additional server-side contingencies? Rauch has already created much of what we need. I wonder if we can “override” Socket.IO’s decision selection process? Adding that to the research list.
5\. There’s a ***“Hidden Bandwidth Cost”*** when using Socket.IO. [This article](http://buildnewgames.com/optimizing-websockets-bandwidth/) exposes the bloat and offers several suggestions how to optimize and where to place Socket.IO ***or eliminate it entirely.***

I thought the author said using Socket.IO “… makes it dead simple …” It’s beginning to feel more like ***a dead option;*** thank goodness we have other candidates.

Wait! There is that ***“Node.js” thing*** again. My other three MMoG candidates boast that they also use ***Node.js.*** Why? Do we ***need Node.js?*** From what we learned in the last chapter, do we really want to return to “long-polling”, server-side-events (SSE) and poor resource management? As reliable as Mozilla reputation is, there is some doubt cast by this next article’s rebuttal.

If Socket.IO retreats to Adobe Flash sockets, then the obvious drawback becomes the Flash Plugin; it ***is not installed on all clients, and in the case of the iPhone/iPad, cannot be.*** [Google Chrome is officially killing Flash starting next month (Sept 2016).](http://thenextweb.com/dd/2016/08/09/google-chrome-flash/#gref) That was five months ago; I hope the Socket.IO developers released a fix, patch, work-a-round by now. Isn’t there a method to tell the server which WebSocket sub-protocols to use?

***Question:*** Can I use just [the engine.io](https://github.com/socketio/engine.io) without Socket.IO? My 3rd MMoG Candidate — Eureca [http://eureca.io/](http://eureca.io/) — let’s me select many different transports (e.g.: “sockjs”, “websockets”, “faye” or “browserchannel”) ***with Engine.IO as the default.***

## 4.7 Node.js vs. WebSockets vs. Socket.io

Did you read that last recommendations? Node.js and WebSockets are not the same; the former is a real-time web application operating at the same layer as our MMoG application (i.e., Layer 7), while the later is the separate method of data transport (i.e., Layer 4). [What are the differences between node.js and websockets?](http://stackoverflow.com/questions/10112178/differences-between-socket-io-and-websockets) states this bluntly, “Node.js ***is a framework for developing scalable network applications,*** based on the JavaScript programming language. WebSockets are a web ***communication protocol for persistent open data transmission.*** You can, however, use WebSockets inside Node.js applications. ***Socket.io is a popular Node.js module for this purpose.”***

[Someone](https://stackoverflow.com/questions/10112178/differences-between-socket-io-and-websockets/38558531#38558531) has created a testing platform to measure the difference between Socket.IO performance and raw WebSockets. Download [their testing kit from GitHub.](https://github.com/rsp/node-websocket-vs-socket.io) Their results showed:

### Socket.IO bloated overhead!

```
1     WebSocket Results: 2 requests,     1.50 KB, 0.05 seconds  
2     Socket.IO Results: 6 requests,   181.56 KB, 0.25 seconds 
```

Socket.IO bloated overhead!

In summary, therefore, ***a WebSocket server can be written in any server-side programming language that is capable of Berkeley sockets, such as PHP*** or Node.js; and, for the client-side implementation we will need html5 WebSocket running from a modern JavaScript-enabled browser.

![](resources/makingbrowsergames_com---book---imagesConsolidated---whereOSI.jpg)

Node.js is an application; WebSocket is a quasi-transport method

## 4.8 Final Analysis

`PHP` is a popular server-side middleware; there are others available, but I will focus on [***my own ISP servers***](http://gose-internet-services.net/) and implementations that support my MMoG prototypes. So instead of blindly following my recommendation, let’s review several web middleware frameworks that study [***the C10k problem.***](https://en.wikipedia.org/wiki/C10k_problem)

In my book [“Phaser Game Design Workbook — A Game development guide using Phaser JavaScript Game Framework”](https://leanpub.com/phaserjsgamedesignworkbook/), I mentioned a short section on back-end services and referenced an external article on [Bench-marking Web Frameworks for Games](https://juiceboxgaming.wordpress.com/2012/11/20/benchmarking-web-frameworks-for-games/). I encourage you to read their entire article. Here is a sample of their extensive testing.

![](resources/makingbrowsergames_com---book---imagesConsolidated---w1-mean.jpg)

Workload 1 – Mean Response Time (Smaller is Better)

Do you remember reading earlier that, “***Socket.IO is not a WebSocket library with fallback options to other real-time protocols.*** It is a custom real-time transport protocol implementation ***on top of other real-time protocols.*** Its protocol negotiation parts cause a client ***supporting standard WebSocket to not be able to contact a Socket.IO server. And a Socket.IO implementing client cannot talk to a non-Socket.IO based WebSocket or Long Polling Comet server. Therefore, Socket.IO requires using the Socket.IO libraries on both client and server side.”***

![](resources/makingbrowsergames_com---book---imagesConsolidated---microsockets.jpg)

Micro WebSockets verified performance

Let me draw your attention to the differences in PHP and Node.js; the margin is less than 200 ms! Their other tests reveal that when Node.js is “pushed” to the 80th Percentile Response Time, Node.js succumbs at roughly 200 requests per second (RPS) and its performance rapidly declines compared to PHP.

![](resources/makingbrowsergames_com---book---imagesConsolidated---w1-p80.jpg)

Workload 1- 80th Percentile Response Time (Smaller is Better)

Requests per second (rps) demonstrates that Node.js is only marginally better than PHP between 10 to 25 concurrent rps; and neither of them show performance improvements beyond 25 concurrent rps. Netty outperforms all competitors.

![](resources/makingbrowsergames_com---book---imagesConsolidated---w1-rps.jpg)

Node.js marginally better than PHP between 10 to 25

I encourage you to read their entire article. In fact, our next exercise is

***Want a second opinion?*** Study [this article](https://thinkmobiles.com/blog/php-vs-nodejs/) that comes to the same conclusion — USE PHP instead of Node.js! (This article also provides its testing source code for your examination.) I quote his conclusion,

I plan to use Phaser v2 or v3 JavaScript Gaming Framework and WebSockets on the client-side, and PHP Sockets in conjunction with a Content Management System (CMS) on the server-side. The marginal gains Node.js demonstrates over PHP fades in its ability to handle CPU-intensive and dynamically generated content. PHP is the clear winner for me. **If you choose to use Socket.IO, you must use it on both the client and server-side — if your ISP allows it on the server-side.** Fortunately, my [***ISP does permit Node.js***](http://gose-internet-services.net/hosting-plans/) on the server-side and is pre-configured for 1 instances included per account.

If you have chosen to use Node.js on the server-side ***— and it is supported by your ISP —*** you have some options whether to fully deploy Socket.IO or use its under-layer pinning. If you want those lower-level abstractions, use just Engine.IO. If you want a WebSocket abstraction, keep using Socket.IO.

*   You would chose Engine.IO if you’re building a library/framework that lacks WebSocket management. If you ***don’t need everything Socket.IO provides*** just use engine.
*   You would chose Socket.IO if you’re building an application on top of Node.js. Socket.IO has (redis store, groups, ad nauseum) Socket.IO is Engine.IO with all the “bells and whistles”.
*   Socket.IO tries to reconnect for some time after connection is lost, ***whereas Engine.IO does not.***
*   Socket.IO supports “rooms compartments” ***whereas Engine.IO does not.***

## 4.9 Server-less Alternatives

Just as a “wireless internet” still has wires somewhere, server-less architectures have servers located somewhere. What “server-less” really means is that, as a developer, you don’t have to think about maintaining those servers (aka “Platform as a Service” (PaaS)) and their infrastructure (aka Infrastructure-as-a-Service (IaaS)). You simply focus on what you do best &mash; create source code!

In an exercise earlier in this chapter, I asked you to research ISP hosting for dedicated/semi-dedicated/co-location servers. Fairly disappointing — as far as pricing — wasn’t it. The “co-location option” also means that your IT network engineering skills must be “top notch” since you’re “flying without a safety net.” Here are some other modern “Recommended Solutions” in lieu of legacy dedicated/semi-dedicated servers approach. You could use either:

*   Adopt the [DevOps approach](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwiNkN6E1J7bAhVWHYEKHYvlBokYABADGgJ5dw&ohost=www.google.com&cid=CAESEeD2RrPGdTi-bw35TwtyL9nq&sig=AOD64_3Kzb15ix0Km1ky5eA0Y7BXzst7Fg&q=&ved=0ahUKEwjK0NeE1J7bAhWK71MKHYj0BjQQ0QwIOQ&adurl=) in software game development and move to **“online development” locking your development into a single cloud provider** — Heroku, AWS, Google Firebase to name a few. The advantage of adopting this approach is that your testing environment and live production environment are the same.
*   Deploy to multiple microservices [across various Cloud Services Providers — ***cafeteria-style*** —](http://gose-internet-services.net/hosting-articles/what-does-cloud-web-hosting-represent/) using such access as [“Serverless Framework”](https://serverless.com/framework/) and [“Event Gateways”.](https://serverless.com/learn/event-gateway/) The advantage of adopting this approach is the scaling and fine-tuning of cost expenditures.
*   ***OR,*** simply ***Build your own vertical*** and include all the options above.

### Online Development — Single Provider Option

Jelastic offers agile deployment models without coding to proprietary APIs, flexible automatic scaling for stateless and stateful applications, collaboration, access control, monitoring, backup and disaster recovery, built-in billing and business analytics tools, while driving down TCO with high density and hardware utilization.

[Heroku.com](https://www.heroku.com/) is a “Platform-as-a-Service (PaaS)”. A little know fact is that Heroku sits on top of [***AWS IaaS!***](https://searchcloudcomputing.techtarget.com/definition/Infrastructure-as-a-Service-IaaS) Their website states, “Heroku is a cloud platform that lets companies build, deliver, monitor and scale apps — we’re the fastest way to go from idea to URL, ***bypassing all those infrastructure headaches.”*** This means that all your development will be “in the cloud”. You do not have to install anything on your local workstation; all you need is a connection to the Internet. If this is your first app, this might be the place to start. Heroku sets up your “infrastructure” for you in the cloud; this lets you focus on MMoG creation. ***They become your private IT support staff!*** Heroku has wonderful online documentation that steps you through the [application process](https://devcenter.heroku.com/articles/architecting-apps) and [how Heroku works](https://devcenter.heroku.com/articles/how-heroku-works). Setting up your ***Free*** account is a “snap!”, and it is connected to your github account for version control.

![](resources/makingbrowsergames_com---book---imagesConsolidated---heroku.jpg)

HeroKu Platform as a Service (PaaS)

They offer two creation methods:

1.  [Single Application](https://devcenter.heroku.com/start), ***or***
2.  a [Pipeline](https://devcenter.heroku.com/articles/pipelines). A pipeline is a group of Heroku apps which ***share the same code-base.*** Adding apps to a pipeline allows you to define stages and promote code (aka re-use or D.R.Y. — Don’t Repeat Yourself) between them. Apps in a pipeline are grouped into “review”, “development”, “staging”, and “production” stages representing different deployment steps in a continuous delivery work-flow. How nice is that? Yea, I’m pretty excited too!

You can further extend their services with Node.js dependencies [using these instructions](https://devcenter.heroku.com/categories/extending-heroku) and with something they call [elements](https://elements.heroku.com/). It is really quite impressive. Everything sounds good so far? ***Right?*** Well, here is [the bottom line and ***pricing***](https://www.heroku.com/pricing). There is a “Free” account with some rather severe restrictions; but perfect for a “proof of concept”/test/development phase of your ***single*** project. I would recommend reading the services attached to each account level. The two most restrictive for the “Free account” are:

1.  Connection closes after 30 minutes of inactivity. This is a bummer when you can’t find those nasty hidden problems. Nope! This is ***not*** a preferred option for a “cheap app launch to the public”.
2.  Limited process on a ***per month basis***. When your “dyno pool” is dried up, then ***you must defer your development until next month.*** Again, not an option for a cheap app launch; if the server doesn’t time out, your game-client might consume all your “dyno” in a single hour! Your game wouldn’t appear until next month when your “dyno pool” is refreshed.

*   Migrate to a “Hobby account” for a small (I’m being sarcastic!) ***price of $7 (US) per dyno.***

***OR***

[Google Firebase (2 minute movie)](https://www.youtube.com/watch?v=O17OWyx08Cg&list=PLl-K7zZEsYLmOF_07IayrTntevxtbUxDL&index=1) is a Platform-as-a-Service (PaaS similar to Heroku) and integrates with Google’s world-wide content delivery network (CDN), AdWord and AdMob! Implementing Firebase is quick and easy and similar in many respects to Heroku. With intuitive APIs packaged into a single SDK, you can focus on solving your customers’ problems ***and not waste time building complex infrastructure.*** Google becomes your IT support staff.

*   Firebase works across various platforms and delivers cross-platform apps with APIs packaged into single SDKs for iOS, Android, JavaScript, Unity and C++. It expands to a different platform without modifying your infrastructure requirements.
*   [Sample starter-kits](https://firebase.google.com/docs/samples/) make Google Firebase an attraction option. ***Before you begin using Firebase,*** you’ll need a JavaScript (web or ***Node.js***) app to add into Firebase. If you don’t have an app already, you can download one of their [quickstart samples](https://firebase.google.com/docs/samples/).
*   ***Native Node.js is supported on the server-side with administration access!***
*   Pricing options currently seem more generous than any of Heroku’s offers in my opinion.
*   [Deployment options](https://firebase.google.com/docs/) are restricted to Android, iOS and web. Each silo has its own detailed users’ guide.
*   All testing and development is online through an authorized account.
*   Integrated access to Google AdWords and AdMob is an enticing feature.
*   If you are building a web app and your web app ***is entirely static content,*** you can deploy it easily using [Firebase Hosting](https://www.youtube.com/watch?v=jsRVHeQd5kU&list=PLl-K7zZEsYLmOF_07IayrTntevxtbUxDL&index=13).

***OR***

### Deploy Using Various Cloud Microservices

This is a topic for an entire book. But let me point you toward some references:

*   The textbook I use for lecture in graduate and undergraduate studies is “Cloud Computing* A Hands-on Approach” by Arshdeep Bahga and Vijay Madisetti.
*   Apache Cloudstack (Java) [https://en.wikipedia.org/wiki/Apache_CloudStack](https://en.wikipedia.org/wiki/Apache_CloudStack)
*   Eucalyptus [https://en.wikipedia.org/wiki/Eucalyptus_(software)](https://en.wikipedia.org/wiki/Eucalyptus_(software))
*   Openstack [https://en.wikipedia.org/wiki/OpenStack](https://en.wikipedia.org/wiki/OpenStack)

You could download those open source “Cloud Services” but you still need a “platform” located somewhere — PaaS and IaaS. Or you could adopt an organization that provides both and the “Software as a Service (SaaS)” to build and launch your MMoG.

### Build a Vertical

Build your own [***Vertical Business ISP Integration,***](http://www.resellerspanel.com/reseller-hosting/?a=gose-internet-services) as I have.

This translates into: I am my own Internet Service Provider that provides everything that the Heroku does — as far as IT support, hosting, WebSockets and Node.js. Each of my hosting accounts have back-ground services and [***a single Node.js instance included in the $2.95 hosting per month.***](http://gose-internet-services.net/hosting-plans/) The IT staff who tends my servers are extreme knowledgeable and efficient. If I choose, I can buy domain names, [dedicated servers](http://gose-internet-services.net/dedicated-servers/us-dedicated-hosting/), [semi-dedicated servers,](http://gose-internet-services.net/semi-dedicated-servers/) and even [***virtual private servers***](http://gose-internet-services.net/vps/) (this is what Heroku offers!) to host my own [***SmartFoxServer 2X***](http://docs2x.smartfoxserver.com/) in these [***AU, BG, FI, US, UK data centers***](http://gose-internet-services.net/data-centers/) all at a **whole sale price** from my vertical business structure.

![](resources/makingbrowsergames_com---book---imagesConsolidated---gisNode.jpg)

My Node.js with every hosting account.

![](resources/makingbrowsergames_com---book---imagesConsolidated---gisWebsocket.jpg)

Hosting has WebSockets enabled (for $3 per socket per month)

Good Question! ***Nothing! I gained all of Heroku capabilities at no cost, nada, FREE!*** WebSockets are $3 per WebSocket per month ***unlimited traffic (no “dyno” here!); this is half the price of Heroku at no restrictions!***

## 4.10 Chapter Summary

Inventory time on what we’ve learned thus far:

*   Noted how prominent Node.js is among current MMoG engines.
*   Reviewed the `C10k problem`.
*   Revealed the flaw in many current recommendations for MMoG engines.
*   Researched ISP hosting that allows Node.js and daemon WebSocket processes.
*   Discovered pricing and constraints for various MMoG deployment options.
*   Learned the relationship between Node.js, Socket.IO and other dependencies.
*   Agreed that testing/development workstation should mirror public ISP hosting.
*   Researched “Open source MMO Game Engines” and discover thousands.
*   Created a MMoG concept document to guide our MMoG development.
*   Listed 9 critical aspects our MMoG engine should fulfill.
*   Listed 2 to 5 likely server-side candidates for our MMoG engine deployment.
*   Discovered the best environments for Node.js deployments.
*   Discovered the Socket.IO capabilities from its author.
*   Discovered Engine.IO capabilities, and its relationship to both Socket.IO and Node.js.
*   Learned “under what circumstance” and “when to use” Socket.IO, Node.js and Engine.IO.
*   Gathered research from canIuse.com on current browser features and capabilities.
*   Compared Node.js, Socket.IO, and WebSockets capabilities and deficiencies.
*   Analyzed Node.js back-end performance — to other likely server-side candidates — under various scenarios.
*   Reviewed alternative back-end server options for deployment.

## 4.11 Chapter Foot Notes:

1\. Ward, J. (2008, April 28). [***What is a Game Engine?***](http://www.gamecareerguide.com/features/529/what_is_a_game_.php?print=1) Retrieved January 30, 2017, from [http://www.gamecareerguide.com/features/529/what_is_a_game_.php?print=1](http://www.gamecareerguide.com/features/529/what_is_a_game_.php?print=1)

# 5 MMoG Application Architecture

This chapter focuses on your MMoG Application Design, [***Deciding what to choose for your MMoG’s “Web API”***](https://medium.com/platform-engineer/web-api-design-35df8167460) and the overall MMoG software Architecture. It provides a foundation of common terminology as we begin writing our source code for our game in the browser, the various servers and our MMoG Application (i.e., gaming/business logic). The information, you gained from Part I, provides a better insight as you follow my production across:

![](resources/makingbrowsergames_com---book---imagesConsolidated---n-tier-architecture.jpg)

n-Tier Web Applications within the CDN/Cloud.

*   Client to and from the Server(s) developing a game protocol or [***adopting existing messaging protocols.***](https://core.telegram.org/api)^(Chapter Footnote 1)
*   [***WebSocket communications***](https://en.m.wikipedia.org/wiki/WebSocket) — the bidirectional, stateful, real-time, client-server communication technology found in the HTML5 specification. It is superior to “Ajax” in terms of performance^(Chapter Footnote 2) and simplicity.
*   [***Event-driven architecture***](https://en.wikipedia.org/wiki/Event-driven_architecture) — is a software architecture pattern promoting the production, detection, consumption of, and [***reaction to events.***](https://en.wikipedia.org/wiki/Event_(computing))
*   JavaScript programming in the OLOO-style (***not OOP;*** but rather [“Object Linking to Other Objects”](https://davidwalsh.name/javascript-objects-deconstruction).)
*   Web application development for “n-tier”. (Illustrated below)
*   Declarative instead of Imperative and where to use these coding styles.
*   Security authentication, authorization, and “tickets” (aka connection tokens).
*   Server Architecture considerations — See [***MMoG-Deployment-Worksheet.pdf***](http://makingbrowsergames.com/mmog/bonusContent/MMoG-Deployment-Worksheet.pdf) in bonus content.

## 5.1 Comparing Single- to Multi-Player Games

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogBaaS.jpg)

stated earlier: Single Player Game Flow

Obviously, playing a single player game means that the local device stores and processes everything; Phaser updates, renders and processes anything to do with the current game and its logic. For a single-player game, you would typically need:

*   Graphics (with animations?);
*   Levels of difficulty;
*   Gamer’s “avatar” and it character design;
*   Game mechanics (refer to the appendix);
*   Compelling story and game setting;
*   Gamer’s input;
*   Gamer’s feedback;
*   With an overall game flow; [***Download the FREE game flowchart at.***](http://makingbrowsergames.com/mmog/bonusContent/_GameFlowChart.pdf)

***[http://makingbrowsergames.com/mmog/bonusContent/_GameFlowChart.pdf](http://makingbrowsergames.com/mmog/bonusContent/_GameFlowChart.pdf)***

Each of the 7-phases — yes, there are more than this — is a stage for the game process with their own internal processing states of . . . ***`initiate`, `preload`, `create`, `update`, `render`,*** and garbage collection. Only ***`create` and `update`*** are mandatory. Phaser attempts to cycle between ***`update` and `render` at 60 frames per second.***

![](resources/makingbrowsergames_com---book---imagesConsolidated---phaserPhases.jpg)

stated earlier: Single Player Game Flow

Take a look at the details of the “Game Loop” below. ***It is similar to [children skipping rope](https://www.heartfoundation.org.au/images/made/images/uploads/jump-rope/kids_jumping_800_480_85_s_c1.jpg) — only this rope is spinning around at 60 frames per seconds (fps)!*** The “Game Loop” toggles execution between the “update” state and “rendering” state which puts new information onto the local display; it follows the standard ***IPO model (aka input, process, output).*** Here’s all the things Phaser does during ***each 60 frames per second.***

![](resources/makingbrowsergames_com---book---imagesConsolidated---spGLoop.jpg)

Generic Details inside the Single Player Game Loop

It’s this “Game Loop” that demands our attention as we write our MMoG and will mold our decisions about how we use our server’s architecture — refer to the [***MMoG-Deployment-Worksheet.pdf***](http://makingbrowsergames.com/mmog/bonusContent/MMoG-Deployment-Worksheet.pdf) in your bonus content. ***Only the “Processing Phase” — that middle section illustrated above in the “Update” phase — will move onto our MMoG App server while the local “Inputs” and local “Output Rendering” phases remain on the local client display — this is the typical Centralized Authoritative Server and Dumb (thin) client configuration found in most MMoG today.*** The better we describe — and dissect — ***what*** our game’s logic is and ***what*** it does, the better we understand ***how*** the local device will render that information to the display. Rendering the current game status ***will always be a local process*** with [***some help from web workers.***](https://gamedevacademy.org/phaser-progressive-web-apps-tutorial/?a=47&campaign=RRTE)

I’m suggesting a new way of writing MMoGs; my recommendation is that the local device is concerned with ***the how (i.e., “imperative programming”)*** while our game “Input” data in the form of game turn orders (GTO) to and from the server(s) are concerned with ***the what (i.e., “declarative programming”).***

*   ***imperative*** on the client-side browser will handle all the game movement, animations during the rendering phase based on server messages. The server will process gamer’s incoming “Inputs” (i.e., game turn orders formatted into JavaScript Object Notation (JSON) messages) from all the game participants and adjust the game state based on those incoming game turn order (GTO) messages. (https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API)
*   ***declarative*** messages from the client-side are JSON formatted game turn orders describing what the gamer wants to do. JSON is generally used as a data transfer format. The server returns JSON formatted “game turn replies” (GTR) authorizing what the local gamer should render to their display concerning other gamers’ positions and the game status for this turn.

[![](resources/i_ytimg_com---vi---FSs_JYwnAdI---hqdefault.jpg)](https://youtu.be/FSs_JYwnAdI)

View this video at [https://youtu.be/FSs_JYwnAdI](https://youtu.be/FSs_JYwnAdI)

***JavaScript: How It’s Made video (10:53)***

### Deeper Dive: Using Web Workers

Web Workers are not part of JavaScript, they’re a browser feature which can be accessed through JavaScript. [***Web Workers***](https://html.spec.whatwg.org/multipage/workers.html) are in-browser threads that can be used to execute JavaScript code without blocking the game event loop. Web Workers allow game developers to place those “long-running and CPU computationally intensive tasks” — the bane of NodeJS — in the background without blocking the user interactions. This makes your MMoG app even more responsive on the client-side. In addition, you don’t need to “play around with JavaScript’s ***`setTimeout`*** tricks” to hack your way around a game’s sluggish event loop. Review how Web Workers improve performance [***in this online demo.***](http://afshinm.github.io/50k/)) MDN claims this about Web Workers, [***quote***](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) “… you can use a large number of items available under window, including [***WebSockets,***](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API) and data storage mechanisms like ***IndexedDB*** … Workers may in turn spawn new workers, as long as those workers are hosted within the same origin as the parent page. In addition, workers may use `XMLHttpRequest` ***for network I/O,*** with the exception that the `responseXML` and channel attributes on `XMLHttpRequest` always return null.”

The problems appear when you’re, [***quote***](https://blog.baasil.io/socketcluster-design-patterns-for-chat-69e76a4b1966) “… tempted to have variables in your worker.js file to hold **global data.** A common example of this is when you try to ***have an array or hash map (object) which contains the state of ALL connected users in the system (across all worker processes).*** While this is fine if you just have 1 worker process running on 1 server, this approach **doesn’t scale beyond that** — As soon as you add a second worker process to your [***Socket Cluster (SC)***](https://socketcluster.io/#!/) instance, you will find that each worker only ends up holding a subset (in this case, half) of the complete user list (some users will be connected to worker 1 and others will be connected to worker 2). Trying to synchronize this list across workers so that each worker can have access to the entire list of users (in its own memory) **undermines scalability and is a very bad idea (you just end up duplicating the same workload across multiple workers).”**

### Deeper Dive: Await and Promises

[![](resources/i_ytimg_com---vi---vn3tm0quoqE---hqdefault.jpg)](https://youtu.be/vn3tm0quoqE)

View this video at [https://youtu.be/vn3tm0quoqE](https://youtu.be/vn3tm0quoqE)

Await and Promises (video 12:03)

## 5.2 Differences in MMoG Games?

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogGameLoop.jpg)

Processing Updates happens on the Server-side

The critical differences between a single-player game and its “big MMoG brother” is its distribution of common game information (i.e., inputs processing, variable state management, and the rendering outputs of game assets) and game “processes” (i.e., updates to our game’s status) among all players — ***who does what when with synchronization confirmation?*** We’ll study these various deployment options soon. **Network delay (aka lag or latency) becomes our greatest concern when centralizing all game “processing logic” — that central portion from the “Update” phase — onto a remote server assuming you’re building a real-time MMoG.** By doing so, we’ve just added the network delay into our typical 60 fps game loop. The tolerance for this newly introduced network interference depends greatly on the game mechanics we are using. For example, a turn-based game (a fix time interval with game turn order (GTO) submissions) have a better tolerance toward network latency, delay, jitter or lag than a “twitch-style” game play found in most “first-person shooters (FPS)”. In order for either to work, both approaches require a “middleman” — a “proxy” of our centralized authoritative server as suggested by [***Unreal Networking Architecture***](https://api.unrealengine.com/udk/Three/NetworkingOverview.html#Minimizing%20Perceived%20Latency) — to handle all network traffic among all participants. WebSockets is a wise choice for games that require a “reliable ordered” communication channel (i.e., TCP/IP), but real-time games require a lower latency solution — perhaps UDP/IP, or WebRTC UDP-based conduits. And most real-time games care more about receiving the ***most recent data than getting ALL of the game’s data in the proper sequence.***

![](resources/makingbrowsergames_com---book---imagesConsolidated---uiHudGM.jpg)

Update “Processing” happens on the Proxy or Server-side

The “Green” components will become our [***“proxy server” inside the client’s browser; (See US Patent #5,899,810***](https://docs.google.com/viewer?url=patentimages.storage.googleapis.com/pdfs/US5899810.pdf)) it fulfills the role of a [***message broker***](https://en.wikipedia.org/wiki/Message_broker) (aka an [***integration broker or interface engine***](https://www.gartner.com/it-glossary/ib-integration-broker)). In this [***“proxy” design pattern,***](https://en.wikipedia.org/wiki/Broker_pattern) one object acts as an interface into another object. It’s different from the “façade” pattern, in which all you have is convenience methods that combine several other method calls. The “proxy server” sits between the client and the game-engine server — the MMOG App server in our case — and “protects or filters” the access into our gaming server and its logic. The advantages of having such a proxy-server are:

*   The substitution of an “AI bot” during remote player delays, absences, or game resignations.
*   The game loop remains local without adding network latency! I’m not the first to develop this. Research [***Garage Games and their Torque Engine***](https://en.wikipedia.org/wiki/Torque_(game_engine)) game development or the [***Unreal Networking Architecture***](https://api.unrealengine.com/udk/Three/NetworkingOverview.html#Unreal%20networking%20architecture).
*   Any our single-player games are [***primed and ready***](https://www.dictionary.com/browse/primed) for “multi-player” game-play conversion. Activating a websocket simply toggles our “single-player game” into receiving remote players’ input. Should the remote player(s) quite the game prematurely, the local “proxy server” converts back to using its internal “AI bot”.
*   The proxy-server updates game state at a lower fps. This is a recommendation from several industry experts in multi-player game design. — for example: Rex van der Spuy, [***Gaffer on Games***](https://gafferongames.com/), [***Gabriel Gambetta***](https://www.linkedin.com/in/gabrielgambetta/?originalSubdomain=uk), Andrew Mulholland and Teijo Hakala, Todd Barron, Andre LaMothe, [***UnReal Network Player Movement and Prediction***](https://api.unrealengine.com/udk/Three/NetworkingOverview.html#Player%20Movement%20and%20Prediction), to name a few besides [***your humble author.***](https://www.linkedin.com/in/stephen-gose-phd-71ba853b/) ***“How much lower?”, you say?*** Their recommendations, in my opinion, are not based in WAN capabilities. Only Rex van der Spuy provides a logic recommendation of 30ms or ~33 fps. TCP/IP disconnects after 255 seconds; telephone connections disconnect after 250 ms! A network connection from L.A. (USA) to New Delhi, India takes 70ms one-way; its round-trip-time (RTT) is typically a textbook 34-40ms.

***Why are we inserting this extra piece? Won’t that slow stuff down?***

***ANSWER:***

*   Yes, that is true. It might slow game process a bit; but, when compared to extracting the game loop’s process and placing it on a remote server, it is a significant time savings.
*   Because, WebSockets do not examine the game turn order content of the inbound or outbound streams; it only ensures that the data reaches its destination on each end of the conduit. This is not a problem if the data received are merely being echoed or lightly processed as in Node.js. However, as we found in Part I, Node.js is the poorest choice for intense CPU calculations.
*   Besides we still need some code to write and read our game turn orders into “declarative” code. So formatting game turn orders and responses is something we’ll develop in later chapters. You may want to generate a rough draft or begin thinking about what game turn orders your MMoG will use. As a guide, you have access to Part IV and the [***FREE Travel Games Volume. I (valued at $19)***](https://leanpub.com/tigs/c/f3d6wFdxNdHk) — a collection of 3 Game Kits for Rulers of Renown™, Legends of Renown Deeds™ (LoRD) and War Lord Tourney™.
*   Our “proxy” could act as an “application firewall” and filter malformed commands. I talk about game security more in a moment.
*   Our proxy could double as AI for single-player game or in a multi-player game when an opponent quits abruptly.
*   Our proxy could run at a slower fps. This is the solution most MMoG use in interpolation and extrapolation. We study these toward the end of this chapter.

***Client-side GTO suggestions for MMoG management (listed alphabetically):***

*   ***cancelGame*** — player, who launched the game request, recants
*   ***gtoCommand*** — system message “type” property is requested action
*   ***create_failed*** — system message feedback
*   ***created*** — system message feedback
*   ***dead*** — system message notification about opponent
*   ***endGame*** — system message notification
*   ***error*** — system message feedback concerning GTO
*   ***gameOver*** — migrate Phaser to gameOver phase
*   ***initRound*** — system message to reset variable for new game
*   ***join_failed*** — system message notification
*   ***joined*** — system message on successfully enter existing game
*   ***latency*** — system message on network lag and test
*   ***pong*** — system message response to server ping test
*   ***rooms*** — system data on available games
*   ***tick*** — system time-stamp data for synchronization

![](resources/makingbrowsergames_com---book---imagesConsolidated---ttt.jpg)

JSON with Padding from JavaScript Patterns Ch. 8 page 193

### Player Interactions

***Summary:*** Players send their ***game turn orders (GTOs)*** to a server or local proxy-server. The server will test for the GTO’s origins (by the inserted game id, player’s id and time-stamp), authorize the GTO as valid for that individual player, process and then integrate the players’ GTO into the game’s overall status, update the server’s data structures and finally, the server will broadcast the updated information (aka ***game turn results (GTR)*** ) to any one currently active within the game. What we’ve just mentioned ***favors “turn-based” games over “twitch-based” game designs.***

I think we just developed a [***“honey do list”***](https://www.urbandictionary.com/define.php?term=honey%20do%20list) for our MMoG Application server!? And indirectly hinted at what the client-side browser will do.

![](resources/makingbrowsergames_com---book---imagesConsolidated---blue-p2pConfirmed.jpg)

Availability Overlays using Proxy - Mixing Network Connectivity

### Technology Architecture

Hyun Sung Chu, from IBM, in his three-part article on [***“Building a simple yet powerful MMO game architecture”***](https://www.ibm.com/developerworks/library/ar-powerup1/index.html), recommends **four major components.** His articles were written in 2004(!) — nearly an entire decade **prior to WebSockets.** His articles are still a good place to begin our journey into MMoG development. However, he’s missed some things — the same things that every tutorial I’ve read (to date 20190125) has missed also! Here’s his paraphrased ideas with typical information found from the majority of current MMoG tutorials:

1\. A **Web application server** to integrate with the gaming servers and clients. We will use the web server as the initial player contact and game entry. ***It is at this initial contact we will migrate the client into WebSockets.***
2\. A **“gaming client”** to perform proxy “WebSocket Upgrade” for the incoming gamer. Our deployment, using Phaser.JS in the gamers’ browser, will perform the duties of a “thin or thick client”; our Game “Index page” will perform all the proxy requests, and upgrades into a WebSocket. There is a critical decision to consider: When do we want WebSocket activation at the client-side?
3\. A **Gaming server(s)** to interact with every connected gaming client. We will use WebSocket transport for bi-directional exchange. This is the place where our MMoG application resides and performs all the “heavy lifting and CPU-intensive processing”. It’s obvious that the server-side should already exist and be ready for any client activation whenever those requests arrive.
4\. A **database server** to persist and retrieve game state information and customer data modified by the new GDPR laws. In our case, we will discuss several modern methods to store persistent game information under the control of the MMoG Application.

![](resources/makingbrowsergames_com---book---imagesConsolidated---threeTier.jpg)

3-tier Architecture Model

***Do you see it?*** It’s the standard “3-tier architecture”; it is the old legacy (i.e., predating 2014) client / server model. Things have changed since ***WebSockets appeared in 2014,*** and the newer [***Cloud microservices of 2016!***](https://www.bmc.com/blogs/new-multi-cloud-world-means/) We have another new frontier emerging in game development if you include [***blockchain into your game designs***](https://medium.com/loom-network/blockchain-games-the-biggest-trojan-horse-that-experts-won-t-see-coming-and-the-startling-1846eb412aba) — which deprecates all need for an app store — as demonstrated in [***this sample Ticktacktoe game.***](https://github.com/PBMCube/blocktactoe) Furthermore, add to this distributed [***Cloud microservices (click to download)***](https://microservices.io/i/MicroservicePatternLanguage.pdf) inside Content Delivery Networks (CDN), and everything has changed — as illustrated below.

![](resources/makingbrowsergames_com---book---imagesConsolidated---app-arch-hexagonal.jpg)

Hexagonal Architecture Model using Horizontal Micro-Services

Let’s divide our game into ***core*** services or [***“Cloud End-point”***](https://cloud.google.com/endpoints/docs/quickstart-endpoints) and dynamically piece together ***what we need, when we need, and where our gamers need them at the time it is needed.*** It possible by adopting [***Crossbar.io***](https://github.com/crossbario/crossbar) — an open source networking platform for distributed and microservice applications. It implements the open Web Application Messaging Protocol (WAMP), is feature rich, scalable, robust and secure.

I stated in Chapter 2, “Service-Oriented Architecture (SOA) is a specific method of organizing software! It is the idea of breaking out various functionality as module and possible deploying those on different servers with network protocol or sockets communications.” All this is possible using the proper [***API design tools***](https://github.com/mulesoft/api-designer) and [***API workbench.***](http://apiworkbench.com/) The old way of creating MMoG used a [***“Monolithic Pattern”***](https://microservices.io/patterns/monolithic.html) with the typical centralized authoritative server (i.e., ***mediator patterns*** ); the [***“Microservice Architecture”***](https://microservices.io/patterns/microservices.html) is quite different and gives us the flexibility to use other horizontal and vertical online service such as [***PlayFab.com (formerly PopCap)***](https://api.playfab.com/) in more of an ***observer pattern*** role. Microservice Architecture, in general, does have [***its problems***](https://en.wikipedia.org/wiki/Microservices#A_comparison_of_platforms) — [***forewarned is forearmed.***](https://www.phrases.org.uk/meanings/forewarned-is-forearmed.html) Doing so, embraces the modern trend of [***DevOps Cloud deployment. (read more here)***](https://martinfowler.com/articles/break-monolith-into-microservices.html) These “coding chunks” could be on different servers or domains throughout the virtualized cloud.

### Deeper Dive: Ethereum Distributed App (DApp) Games

DApps are games that run on a **Peer-to-Peer ( [P2P library](https://github.com/js-platform/p2p) )** network of computers rather than a single-centralized server. They are a game design that are “block-chain enabled” and exist inside the Internet in such a way that it **is not controlled** by any server. “Block-chain enabled” means, in its simplest terms, a time-stamped series of immutable data records that are managed by a related group of computers not owned by any single entity. Each data block is securely linked to each other using cryptographic principles to form a chain.

To compare to a traditional HTML5-game application, browser games typically uses HTML, CSS and JavaScript to render a page. They also need to pull content from a database utilizing using an API. DApp games are similar in that respect; the client-side uses the exact same process to render in the browser. The single critical difference is that instead of an API connecting to a Database, the game has a [**“Smart Contract”**](https://www.coindesk.com/information/ethereum-smart-contracts-work) connecting to a blockchain. Another difference from traditional browsers games is DApps have their back-end server code logic running in the P2P network.

![](resources/i_stack_imgur_com---jzm8y.png)

Illustration of a DApp that uses a blockchain with smart contracts combined with the pillars of Swarm and Whisper. Source: Ethereum Stack exchange

Fortunately, [***Enjin Coin***](https://enjincoin.io/) has the current answer for [***DApp Games Development***](https://blog.enjincoin.io/development-updates/home) using block-chain. What is ENJ and How Does it Work? Watch their

[![](resources/i_ytimg_com---vi---OCeg_i782f0---hqdefault.jpg)](https://www.youtube.com/watch?v=OCeg_i782f0)

View this video at [https://www.youtube.com/watch?v=OCeg_i782f0](https://www.youtube.com/watch?v=OCeg_i782f0)

***2 minute video***

![](resources/makingbrowsergames_com---book---imagesConsolidated---dataFlow.jpg)

Web-MVC - NEW MMoG Data Flow

Let’s review what we already learned from Part I.

1\. The gamer connects through the “WWW” to our game’s web page. They then connect to our HTTP server and upgrade their connection into a WebSocket. What I didn’t show, at “step #1”, is the Content Delivery Network (CDN) nor the internal client-side proxy server! The game index.html page comes from a CDN repository nearest to the gamer’s physical location — not directly from our `WWW` server.

*   [https://www.codeinwp.com/blog/maxcdn-vs-cloudflare-vs-cloudfront-vs-akamai-edge-vs-fastly/](https://www.codeinwp.com/blog/maxcdn-vs-cloudflare-vs-cloudfront-vs-akamai-edge-vs-fastly/)
*   [https://stratusly.com/companies/](https://stratusly.com/companies/)
*   [https://www.cdnoverview.com/#page-top](https://www.cdnoverview.com/#page-top)
*   [https://www.geckoandfly.com/10077/maxcdn-amazon-cloudfront-cloudflare-cachefly-and-edgecast-cdn-comparison/](https://www.geckoandfly.com/10077/maxcdn-amazon-cloudfront-cloudflare-cachefly-and-edgecast-cdn-comparison/)

2\. Your game will load ***any version of the Phaser Gaming Framework*** from a CDN — either “jsdeliver” or “Cloudflare”. I strongly recommend you use the generic deployed Phaser versions instead of compiling your own and loading it from your own website. The chances are greater that a gamer has played a Phaser game already from either of these CDNs and that previously downloaded Phaser library is still inside their browser cache; thereby, ***adding zero load time to your MMoG!***

3\. Game storage and database servers are changing; game information and data does not have to reside in a central storage tank anymore. New trends suggest different data structures [such as CouchDB](https://en.wikipedia.org/wiki/Apache_CouchDB) or storing [***“Sharded” information***](https://medium.com/ibm-watson-data-lab/pouchdb-the-swiss-army-knife-of-databases-c5429f3db21f) locally on the gamer’s devices or elsewhere. Using blockchain — as seen in [***“Crypto-Kitties Source Code”***](https://medium.com/loom-network/how-to-code-your-own-cryptokitties-style-game-on-ethereum-7c8ac86a4eb3) or in [***0xUniverse***](https://bit.ly/2RycFJt) — provides the option to store game data in the “Cloud”. How do they use blockchain? All of these topics are are explained in this article:

4\. MMoG App Engine was thoroughly discussed in previous Part II chapters. We created our list of vetted game engine candidates. Now, We’ll begin writing our source code development in the following chapters.

### Live testing of MMoGs!

![](resources/makingbrowsergames_com---book---imagesConsolidated---dnsPrefetch.jpg)

DNS prefetch example

Let’s take those exercises and begin testing the time my MMoG responds worldwide. You can use ***my testing lab ([http://mmog.pbmcube.net/index.php](http://mmog.pbmcube.net/index.php))*** or a generic demonstration tests from ***[http://websocket.org/demos.html](http://websocket.org/demos.html)*** or you might use their “Echo test” from this page ***— “[http://websocket.org/echo.html](http://websocket.org/echo.html)”.*** The feedback will be different for everyone and is based on where you are in the world and the current state of WWW congestion. My initial tests (on my testing lab located at **[http://mmog.pbmcube.net/index.php](http://mmog.pbmcube.net/index.php)**) had a 2ms delay from London (5,267 mi away) from where I am sitting in Arizona, USA! I was extremely pleased.

The interesting fact is all this feedback was without `dns-prefetch`. HTMLGoodies claims, “… When the browser encounters an a hyperlink that does not share the same domain name as the current location ***(ed.: Sound familiar? No? Re-read chapter 2 Deeper Dive: Testing MMoGs Locally),*** it first checks its cache and then, lacking a cached copy, resolves the domain to the associated IP address through a request from a DNS server. These requests happen in the background so as to not block the rendering of the page. Moreover, since all this takes place in parallel with the user’s reading of the page, it places only a negligible load on CPU and network resources. ***How much navigation time will a user save can range from an average savings of about 200 milliseconds for non-cached content, to one to two seconds for the worst DNS resolution delays.*** By default, “prefetching” of embedded link hostnames is not performed on documents loaded over HTTPS. You can change this by setting the `network.dns.disablePrefetchFromHTTPS` browser preference to “false”.” [Read their entire article here.](https://www.htmlgoodies.com/beyond/webmaster/how-your-browser-speeds-up-cross-domain-loading-using-dns-prefetching.html)

## 5.3 Technical Aspects

Let’s turn to some technical information before we write our source code. In the previous illustration “NEW MMoG Data Flow”, I am assuming the HTTP web server is co-located with the game engine server in the same domain and hardware. In reality this may not be the case (i.e., how you deploy your MMoG system). You may choose sharded microservices scattered around the global. In that event, you need [***more advice from Patrick Sexton***](https://varvy.com/rel/dns-prefetch.html) about the `dns-prefetch` information in the exercises we did earlier.

Here is an online tool that will demonstrate response timing from one gamer to another through a centralized authoritative server. This is a simulation (i.e., similar to most MMoG tutorials) and ***does not reflect true network traffic;*** however, it is a superior tools to illustrate various environmental parameters and their impacting results.

We will take our experiments from this tool and integrate that knowledge into our source code in upcoming chapters.

### Writing Source Code Differently: “How vs What!”

Perhaps many of the problems found in MMoG is the manner in which we write our source code. Philip Roberts may have a suggestion for us in his article.

***That’s the secret sauce we’re looking for!*** Locally, Phaser Canvas will do the drawing (imperative; how) and rendering as dictated from the MMoG App server (declarative; what). Sending game turn orders (GTOs) will be written in a declarative / what format, as JSON or XML, going toward the MMoG App server. The MMoG App Server will perform the imperative / how to apply the game logic from the submitted game turn order’s data. In summary, all transmissions take the **“declarative format” (what)** on either side of the WebSocket conduit. All incoming declarative information will convert that “data information” into **“imperative actions” (how).** The client will render the current visual display, the server will apply new game information into its game logic and data structures.

### Construction Sequence and Regimen

I recommend you think of your game turn orders (GTO) and game turn results (GTR) as “end-points” in the communications — your protocols and API specifications. This hints at a sequence for writing our MMoG source code.

1.  Draft a list of client-side game turn orders (GTO), and the expected game turn results (GTR) of the server-side responses.
2.  Then determine how you will “serialize” that output for those GTOs and GTRs. In what formatted data structure will that information use? You have several choices. (i.e., XML, JSON, Binary, etc.) Start with server-side first so that you have something to talk to from the client-side.
3.  Finally, encode your “serializers”; these will become your “contracts” between the client and server as to what is expected from each side of the conduit. Yea, that sound like the most difficult part in the process; but, I have a surprise for you later in this chapter.

## 5.4 Encoding Formats for Game Turns

![](resources/makingbrowsergames_com---book---imagesConsolidated---whatWhereHow.jpg)

Declarative code & Imperative Code

***Summary:*** Any “horizontal traffic” — between the client and its server — will be “What” and “declarative data packets”. All vertical processes will be “How” and “imperative code”. This naturally leads us to the decision on how our horizontal data should be formatted. What form should our “messages” take? Data sent between the client and the server are not exchanged verbatim. Actually, those websocket data are formatted into frames — a package of bits (aka a “packet” or “Datagram”) with a specific arrangement and design. We must concoct that ordered arrangement to make any sense about what’s happening. The technical term for “type of the message” is [***“operation code or opcode”,***](https://en.wikipedia.org/wiki/Opcode) and in our case, we will label messages ***“client to server (C2S)” and “server to client (S2C)”.***

We do not have to re-invent the “wheel” in our packet formats. We can choose among several technology architectures that are available already in the [***“message-oriented middleware (MOM)***](https://en.wikipedia.org/wiki/Message-oriented_middleware) categories. But which “web service” should we use? Web services fall into three camps; one which exposes it APIs as [***Remote Procedure Calls (RPC)***](https://en.m.wikipedia.org/wiki/Remote_procedure_call), Query Langugages (such as [***JSON:API***](https://jsonapi.org/) or [***OData***](https://www.progress.com/blogs/rest-api-industry-debate-odata-vs-graphql-vs-ords)), and the other as “web consumer services” (aka [***Object Request Brokers***](http://zeromq.org/whitepapers:brokerless)) which supplies “document resources” (aka REST) and API interfaces.

In Part I Chapter 3, we created a “grocery list” of things we needed to figure out. Do you remember those questions?

*   What will client/server data “packages” look like and in what format? (i.e, [***0MQ,***](http://zeromq.org/intro:start) [***AMF,***](https://github.com/jamesward/JSAMF) [***AMQP***](https://www.amqp.org/) or Apache [***QPID,***](https://qpid.apache.org/overview.html) [***MQTT***](http://mqtt.org/) (Message Queue Telemetry Transport; an ISO Standard [***(ISO/IEC 20922)***](http://www.iso.org/iso/catalogue_detail.htm?csnumber=69466) and [***HiveMQ***](https://www.hivemq.com/blog/mqtt-essentials-special-mqtt-over-websockets/), [***RabbitMQ,***](https://www.rabbitmq.com/) [***STOMP***](http://jmesnil.net/stomp-websocket/doc/) (simple text-oriented message protocol), [***UMF,***](https://github.com/cjus/umf/blob/master/umf.md) [***WAMP,***](https://wamp-proto.org/) and [***XMPP***](https://xmpp.org/) as per [RFC7395](https://tools.ietf.org/html/rfc7395) and a [***comparison chart here.***](https://wamp-proto.org/comparison.html)) Just because we have a steady stream of data, doesn’t mean either side will understand how to read the data flow. It must have a structured format — for example [***Telnet byte-oriented protocol.***](https://en.wikipedia.org/wiki/Telnet#History_and_standards) Is it binary (greatly secure) or text (anyone can read)? Data “blobs”, chunks or small “twitter-style” messages (i.e. short message service (SMS) whose payload length is limited by the constraints of the signaling protocol to 140 bytes ((140 bytes * 8 bits) / byte = 1,120 bits). (you should have [***already researched UMF***](https://github.com/cjus/umf/blob/master/umf.md) from previous exercises)

Take time to follow and read each format link. Choose the format that will help in your development. We’ll review these coming up next. ***OR,*** begin studying [***Message Pack and its JavaScript API***](https://msgpack.org/) for the client-side and [ZeroRPC by DotCloud](https://github.com/0rpc/zerorpc-python) for a Python server-side implementation. ZeroRPC is a flexible Python RPC implementation based on zeromq (0MQ) and message-pack.

### MMoG App API - RPC or MOM?

*   ***[XML-RPC (5-page Introduction)](http://scripting.com/davenet/1998/07/14/xmlRpcForNewbies.html) or [JSON-RPC](https://en.wikipedia.org/wiki/JSON-RPC#Implementations) [(movie 2:04 click here)](https://www.jsonrpc.org/) — “Remote Procedure Call”*** uses a bunch of “functions” on the server and returns information. This protects our MMoG innovations since the client never sees our internal operations and game logic. RPC calls are tightly coupled and require a gamer to not only know the procedure name, but often the order of parameters as well. The concept of RPC has been around the software development world since I started high school for over half a century ago (yea, time flies), but despite that fact, it is still not as widely known as one would expect for something that enduring. [***gRPC***](https://grpc.io/docs/) by Google is an [***updated RPC version***](https://cloud.google.com/endpoints/docs/grpc/about-grpc) using HTTP/2 as [***explained here.***](https://container-solutions.com/introduction-to-grpc/) The requesting program is from a client and the server program provides the answering service. Similar to a local procedure call, an RPC is a **synchronous operation** requiring the client (the requesting program) to be suspended until the results are returned from the remote procedure(s). Obviously, this is not an architecture for “twitch” and “first-person-shooter” (FPS) games. Nevertheless, using lightweight processes or threads, that share the same domain address space, allows concurrent multiple RPCs execution. (See this ***FREE tutorial*** from Zenva about [***“Web Workers”***](https://gamedevacademy.org/phaser-progressive-web-apps-tutorial/?a=47&campaign=MMoG)) The security threats are hacking attempts to discover how our server-side RPC functions process incoming data. A server-proxy may help, but it’s still on the client-side with a potential risk of tampering. Our server-side code needs to read and write serialized data chunks. These information packets could be formatted in XML, JSON or [***RTMP or RTMFP.***](https://en.m.wikipedia.org/wiki/Real-Time_Messaging_Protocol) JavaScript already has the ability to create JSON blocks for writing ***(`JSON.stringify`)*** and reading ***(`JSON.parse`).*** So if you choose JSON, you work is done. If you plan to “open source” your gaming system for others to use just as [***Life is Feudal: Your Own***](https://lifeisfeudal.com/Life-is-Feudal-Your-Own-About) has done — ***or some other proprietary format which I highly recommend from a [business operations view](https://www.open.edu/openlearn/nature-environment/the-environment/environmental-decision-making/operations-technology-and-stakeholder-value/content-section-2)— you should consider using a encrypted binary format.***

![](resources/makingbrowsergames_com---book---imagesConsolidated---authThin.jpg)

Remote Procedure Call with Ghost Game Shadowing

*   ***[SOAP](https://en.wikipedia.org/wiki/SOAP) or [SOAPjr](https://en.wikipedia.org/wiki/SOAPjr) —*** formerly called the “Simple Object Application Protocol”,designed by Dave Winer in 1988, it is a specification for ***Remote Procedure Calls*** exchanging XML-based messages inside of a SOAP envelope. XML-RPC and JSON-RPC are simpler architectures than SOAP by comparison. Google states from its specifications, “SOAP is a lightweight protocol for exchange of information in a decentralized, distributed environment. It is an XML based protocol that consists of three parts: an envelope that defines a framework for describing what is in a message and how to process it, a set of encoding rules for expressing instances of application-defined data-types, and a convention for representing remote procedure calls and responses.” SOAPjr replace XML for JSON formatted envelopes.
*   [***Web Application Messaging Protocol (WAMP — don’t confuse with the web server!) —***](https://wamp-proto.org/) provides two application messaging patterns in one unified protocol: **RPC and Publish & Subscribe.** You can compare [***this robust protocol here.***](https://wamp-proto.org/comparison.html)
*   ***Representational State Transfer (REST) —*** As defined by Dr. Roy Fielding [***in his 2000 Doctorate Dissertation,***](https://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm) REST also provides an incredible layer of flexibility. Since data is not tied to methods and resources, REST has the ability to handle multiple types of calls, return different data formats and even change structurally with the correct implementation of hypermedia. REST basically means that each URL is a representation of some “function”; its focus is the URL as an interface to return “document resources” or data.

![](resources/makingbrowsergames_com---book---imagesConsolidated---Comparisons.jpg)

Advantages and Disadvantages Compared

![](resources/makingbrowsergames_com---book---imagesConsolidated---websocket-rest-messages-1024x517.jpg)

Message volume compare to traffic load

***Why isn’t AJAX listed among these technologies?***

***ANSWER:*** Because [***AJAX***](https://en.wikipedia.org/wiki/Ajax_(programming)) is neither a protocol nor an API. It’s a programming pattern for JavaScript in browsers using HTTP requests to simulate RPC-like communication between front-ends (browsers) and back-ends (servers). ***AJAX has been replaced, as you read in Part I, by WebSockets.*** AJAX, being a programming practice, isn’t a complete RPC system either. You still need to negotiate how calls, results and errors are formatted and serialized. See JSON-RPC and XML-RPC above.

Even when you bake some RPC mechanism using AJAX techniques, this is point-to-point RPC: calls aren’t routed between different servers domains or application components, but strictly travel from point (browser) to point (server the browser is connected to). Multi-casting is not an option.

Furthermore, AJAX does not provide Pub-sub — in fact, it doesn’t address how to actively push any kind of information from server to client (however, see the deprecated “Comet” which we should avoid).

Since AJAX uses plain HTTP for wrapping any kind of RPC-like messages, it suffers from the overhead and limitations found in HTTP. (i.e., you cannot have more than 6-8 concurrent RPCs, since browsers limit the number of HTTP connections to a single destination [***per CORS.***](https://techblog.constantcontact.com/software-development/using-cors-for-cross-domain-ajax-requests/)

*   [***REST vs WebSocket Comparison and Benchmarks***](http://blog.arungupta.me/rest-vs-websocket-comparison-benchmarks/)
*   [***REST vs. SOAP – The Right WebService***](http://geeknizer.com/rest-vs-soap-using-http-choosing-the-right-webservice-protocol/#ixzz1PDKEB98H)
*   [***ROA vs. SoA, REST vs. SOAP***](http://rest.elkstein.org/2008/02/roa-vs-soa-rest-vs-soap.html)
*   ***Is it safe to say that AJAX is a particular way of using REST? ANSWER:*** “Ajax and REST are indeed two ways of using HTTP as a transport. But you can also use together. … AJAX is a set of (typically) client-sided web development techniques which allows your browser to get dynamically changing sections of the page, instead of retransmitting an entire static whole page with updates, while REST is an architecture style for just sending and handling requests using HTTP operations. So you can use AJAX to send RESTful requests. A REST API is typically not implemented using AJAX, but can be accessed by an AJAX client. … AJAX and REST work well together; you don’t have to choose either one or the other … “ [***Read entire Answer with comparisons …***](https://softwareengineering.stackexchange.com/questions/325548/is-it-safe-to-say-that-ajax-is-a-particular-way-of-using-http)
*   [***Using REST in JavaScript***](http://rest.elkstein.org/2008/02/using-rest-in-javascript.html)
*   [***Using REST in PHP***](http://rest.elkstein.org/2008/02/using-rest-in-php.html)
*   [***XML-RPC vs. SOAP***](http://weblog.masukomi.org/writings/xml-rpc_vs_soap.htm)
*   [***Web Services and PHP — SOAP vs XML-RPC vs REST***](http://roshanbh.com.np/2008/07/web-services-php-soap-vs-xml-rpc-vs-rest.html)
*   [***Message Pack***](https://msgpack.org/) — It’s binary JSON; it’s faster and smaller. Message-Pack is an efficient binary serialization format. It lets you exchange data among multiple languages like JSON. But it’s faster and smaller. Small integers are encoded into a single byte, and typical short strings require only one extra byte in addition to the strings themselves.

## 5.5 Deployment Concerns

Since we are not the first to build a MMoG, let’s review some lessons learned from the [“Industry Giants” as far as server and databases are concerned](http://highscalability.com/blog/2007/11/13/flickr-architecture.html) and their lessons learned. But first, let’s learned where the original ideas came from … ***back in 1994 Carnegie Mellon University*** (42-page annotated Bonus Content below) developed a study on future software architecture.

[***Onlive***](https://en.wikipedia.org/wiki/OnLive) [(2009 — 2015; now defunct)](http://games.onlive.com/) had an innovative idea. Instead of using a “Smart (thick)” or “Dumb (thin)” client, they simply extended the game controller device directly into a centralized server. Their limitation was “range” — a gamer could not be located further than 1,000 miles from the central game server. Wikipedia states, “On April 2, 2015, it was announced that Sony Computer Entertainment had acquired OnLive’s patents, and that all OnLive services would be discontinued on April 30, 2015\. Sony operates [PlayStation Now](https://en.wikipedia.org/wiki/PlayStation_Now), a similar service built using the infrastructure of [Gaikai](https://en.wikipedia.org/wiki/Gaikai), a former competitor to OnLive.”

***Analysis:*** This was, according to both Rex van der Spuy and Gabriel Gambetta, “… a naive implementation … “ leads to a delay between user commands and changes on the screen; for example, the player presses the right arrow key, and the character takes half a second before it starts moving. **This is because the client input must first travel to the server, then the server must process the input, calculate a new game state, and finally the updated game state must return to the client again.** In short, this design introduced enhanced network delay into the game.

## 5.6 Persistent Data structures

There are two ways for saving a game session’s information: 1) using a database server or 2) using native “Operating System (O/S)” files. There are advantages and disadvantages for either:

***Database vs Files Chart***

|   | Database | Native O/S Files |
| --- | --- | --- |
| Advantages: | You can easily add or modify fields that are either new or existing. Externally updating game state values is much easier. You can instantly and efficiently retrieve game state values with SQL queries. The database server will handle Input and Output requests automatically with embedded data manipulation language (DML). Easy to update and restore game state values. | Very fast access using native O/S inputs and outputs. Simple to implement. No dependencies on additional external libraries or resources. No dependencies on a database services (data-as-a-service or DaaS) or availabilities. |
| Disadvantages: | Easy to make mistakes. For example, performing update queries without the appropriate ‘where’ clauses. It can have disastrous effects, especially if you have an old backups archive (or none?!). Databases may be slower than opening and writing to a native file system – especially if table locking is enabled (MySQL vs InnoDB). You might lose several milliseconds during data retrieval or inserts if a lot of in/out records at the same time. Additional code is required to format your data into or from the database. Familiarity with Database storage, Database servers and SQL is required. Additionally, you will need a controller library to interface between your MMoG application and the database server. Database corruption is a potential risk. You could lose all current game state values, and recovery time would impact game’s operation and availability. | It is difficult to add new record fields unless you carefully design the file format and structure from the beginning. For example, using XML, YAML. Inability to do global queries across stored files; however, you can circumvent this by having a “cron” that daily harvests those important fields into a database table or summary file. Needs tailored encoding if you want to update or check individual player stats. A little bit harder to manage information updates and restore. |

### Deeper Dive: 3rd Option for Real-time MMoG

### Distributed Database (sharding)

There is another option you might consider — temporarily storing the database inside the client’s memory using [***sql-JS.pdf!***](http://makingbrowsergames.com/mmog/bonusContent/sql-JS.pdf) ***sql.js*** is a port of SQLite into JavaScript, by compiling the SQLite C code with Emscripten and experiment with the [***online demonstration.***](http://kripken.github.io/sql.js/GUI/) It permits JS to access an in memory SQL database. See how [***“Adventure Quest Battle Gems”***](https://battlegems.artix.com/) is using in-memory database storage.

### MMoG Database Examples

*   The University of Melbourne, Department of Information Systems — [***“Using a simple MMORPG to teach Multi-User, client-server database development”***](http://makingbrowsergames.com/p3gp-book/_wadley-database-mmorpg.pdf)
*   MMO Game Database Design — [http://www.vertabelo.com/blog/technical-articles/mmo-games-and-database-design](http://www.vertabelo.com/blog/technical-articles/mmo-games-and-database-design)
*   Single Game Database Design — [http://www.vertabelo.com/blog/technical-articles/a-database-model-for-simple-board-games](http://www.vertabelo.com/blog/technical-articles/a-database-model-for-simple-board-games)
*   Action Game Database Design — [http://www.vertabelo.com/blog/technical-articles/a-database-model-for-action-games](http://www.vertabelo.com/blog/technical-articles/a-database-model-for-action-games)
*   Data Model for Map- and Turn-Based Games — [http://www.vertabelo.com/blog/technical-articles/a-data-model-for-map-and-turn-based-games](http://www.vertabelo.com/blog/technical-articles/a-data-model-for-map-and-turn-based-games)
*   Star Trek 3D Chess Data Model — [http://www.vertabelo.com/blog/technical-articles/star-trek-3d-chess-data-model](http://www.vertabelo.com/blog/technical-articles/star-trek-3d-chess-data-model)
*   Build Your Own City: An Open-Ended Building Game Data Model — [http://www.vertabelo.com/blog/technical-articles/build-your-own-city-an-open-ended-building-game-data-model](http://www.vertabelo.com/blog/technical-articles/build-your-own-city-an-open-ended-building-game-data-model)
*   [https://gamedev.stackexchange.com/questions/142869/realtime-multiplayer-game-database-design](https://gamedev.stackexchange.com/questions/142869/realtime-multiplayer-game-database-design)
*   [https://www.experts-exchange.com/questions/27925497/Best-database-design-for-a-game-database.html](https://www.experts-exchange.com/questions/27925497/Best-database-design-for-a-game-database.html)
*   [Maple Story Simulator](http://www.maplesimulator.com/bannedstory/version)
*   [BigWorld Technology](http://bigworldtech.com/technology/#bigworldserver); review their:

    - [Developer supporting documentation.](https://developers.wargaming.net/documentation/guide/getting-started/) and
    - Supporting [back-end database scheme.](https://developers.wargaming.net/reference/all/wot/account/list/?application_id=demo&r_realm=ru)
    - [Technical overview](https://wikivisually.com/wiki/BigWorld)

### Deeper Dive: Learn from the Best — UnReal Engine

### Deeper Dive: Learn from the Best — Unity Multiplayer Networking

![](resources/blogs_unity3d_com---wp-content---uploads---2018---08---Unity-UNETDep-Infographics-New.jpg)

Unity Multi-Player Migration Road-map

[***Unity Multi-Player***](https://docs.unity3d.com/Manual/UNetLobby.html) suggestions: Keep track of what they’re working on [***in their blog.***](https://unity.com/solutions/real-time-multiplayer)

*   [Unity New Networking Library](https://unity.com/solutions/real-time-multiplayer/network-transport-layer) Take advantage of their purpose-built networking library, and lean how Unity is delivering multi-threaded performance and game optimization. Here’s a newly released (October 24, 2018) Unity first person multiplayer shooter (MMoFPS) example project in Unity’s updated multi-player networking library — [https://unity.com/fps-sample](https://unity.com/fps-sample)
*   [***UnityWebRequest***](https://docs.unity3d.com/Manual/UnityWebRequest.html) is a modular system for composing HTTP requests and handling HTTP responses similar in nature to RPC. Its primary goal is to allow interaction with web browser back-ends. It also supports high-demand features such as chunked HTTP requests, streaming POST/PUT operations, and full control over HTTP headers and verbs.
*   NetworkLobbyManager virtual methods [***called on the server:***](https://docs.unity3d.com/Manual/class-NetworkServer.html)
*   NetworkLobbyManager virtual methods [***called on the client:***](https://docs.unity3d.com/Manual/class-NetworkClient.html)

### Deeper Dive: Learn from the Best — IBM Microservices

### Additional Information

![](resources/makingbrowsergames_com---book---imagesConsolidated---rogue-cloud.png)

Rogue Cloud

### Deeper Dive: Learn from the Best — Google GRITS

***Google won’t be “outdone”!*** [***GRITS is a cross-functional effort***](https://www.youtube.com/watch?v=Prkyd5n0P7k) to create a boilerplate code-base to provide to HTML5 game developers that are looking to get started using Google’s technology stack. The intent was to create a very small, Multi-Player game to launch and provide all the source code up to the masses for boilerplate. Review it on [***GitHub***](https://github.com/MakingBrowserGames/gritsgame)

GRITS is a top-down, Multi-Player battle game designed by Google engineers. It is Google’s attempt at providing an HTML5-based game model leveraging best-of-breed HTML5 technologies, such as Canvas, WebSockets, Google App Engine, and Google+ integration. GRITS employs an authoritative server network relationship. Clients request specific actions of the server; the server pushes the updated game state status to all the active participants. The clients see this game state as a confirmation of the actual game state and overwrite any local data.

### Deeper Dive: Learn from the Best — Rob Hawkes

Rob Hawkes, the head of developer relations at Pusher and former technical evangelist at Mozilla, developed [***Rawkets***](https://github.com/PBMCube/rawkets) — a real-time, Multi-Player game proof-of-concept. The game explores HTML5 Canvas, WebGL, and use of WebSockets. Rawkets reminds me of Asteroids — the classic arcade game. Simple line-art ships represents the players. They can move about the playing field and shoot at other players. You can review the Rawkets code [***GitHub***](https://github.com/PBMCube/rawkets). Rawkets uses PHP for some of its middleware code. We’ll discuss PHP in Part III. Rawkets uses many of the techniques described earlier in this chapter. The interesting portions are in its [***main.js file***](https://github.com/PBMCube/rawkets/blob/master/server/main.js) and its use of BSON.

## 5.7 New Tricks

If you research any tutorial about programming a MMoG, you’ll find that those authors’ assumptions are:

The problem with that scenario is the ***MMoG is using a “Doctor’s Office” approach.*** One doctor can see one patient at a time; translated into other words, one game-server that can only service one dedicated game. This is the “monolithic client-server architecture” with limitations of the quantity of players permitted onto a server. ***I have a different opinion and offer a different approach.***

What our **“MMoG architecture”** should follow is the ***“Theater or Shopping Mall paradigm”.*** Think of it; you enter a “shopping mall” and then visit any number of retailers. ***Or,*** you purchase a theater ticket, entry the lobby (purchase concessions? Of course!), then trundle off to your movie-showing. (not that I have ever done this, but some folks spend an entire day visiting other movie-showings — “movie hopping”! So, I’ve heard ….) Some MMoG servers follow a “room with tables” model, allowing gamers to “sit at a table” to play a game with others seated around the same table. Yet, as any visit to a casino will reveal, others like to stand around those tables and simply watch the on-going game — count cards? I’m just guessing! Currently, most MMoG won’t allow “lurkers” to loiter about those tables; however, if they followed my “Theater/Shopping Mall model”, loitering would not be forbidden nor illegal.

***Summary:*** A Multi-Player game is a shared reality. The gamers ***must feel and believe they are in the same place at the same time with their own unique perspective of the game environment.*** Let’s study how we can achieve this.

## 5.8 Managing Network Transports

Let’s review how other MMoGs approach the problems of network delay, lag, and jitter and see their solutions.

### Skipping Rope! (Fixed Time Intervals)

Skipping Rope is a [***favorite activities for children,***](https://www.heartfoundation.org.au/images/made/images/uploads/jump-rope/kids_jumping_800_480_85_s_c1.jpg) and it teaches us some lessons about developing a Multi-Player game. ***Each participant must jump at the precise time — technically called “lockstep synchronization”.*** Applying that idea to our game, each player must have exactly synchronized input and rendering of the game world for the participants to see same game reality. The central authoritative server(s) makes all the decisions and tells each clients “what to render” (i.e., declarative). The gamer’s browser contribute nothing to the game logic other than “how to render” (i.e., imperative) the current game world; their only contribution is collecting the gamers’ input and sending that information to the server. This is the simplest approach ***— and most naive solution —*** in MMoG development. Returning to our example, if one child falters and trips, their action affects everyone playing.

The lessons learned are:

1.  All the gaming participants can play only at the speed of the slowest gamer.
2.  No independent processing is allowed at any gamer’s browser other than rendering sprites. This is in stark contrast to the information you read in a previous exercise about how the UnReal Engine operates.
3.  Synchronization must be the same across all participants or else someone’s timing mistake will impact everyone.
4.  This approach does not favor “twitch-action” MMo-Game Mechanics.
5.  TCP/IP latency has the greatest impact on our WebSockets and game processing.

The problems using this approach are:

1.  Lack of persistence. All of the gamers must start a game together at the same time. New gamers coming or leaving causes problems for everyone remaining inside the game session.
2.  Lack of player scalability. The server coordination and chances of a network-induced error increases linearly with the number of participants due to this lock-step synchronization.
3.  Lack of frame rate scalability. All players must process the game at the same internal frame rate, making it difficult to support a wide variety of hardware speeds. Generating packets to send and processing the received packets can only be done as often as the client is able to update its local state. Although packets could theoretically be generated and sent faster than this, it would only result in sending redundant data if the game state cannot be updated between each packet. A low frame rate would therefore make the game less responsive to updates and may force it to skip outdated data.
4.  A gamer could send the location of where their character is or who their character shot in a FPS. This solution may work and might eliminate all but the most stubborn problems related to lag. Unfortunately, it relies on the naive assumption that the player is honest and has not tampered with the game turn.
5.  Greatly impacted by network delay and lag which are outside the game logic’s control. Fortunately, using tools such as [***latsub.js***](https://github.com/circonus-labs/latsub) provides the Round-trip time for us to offset our server timing and adjust game turn submissions.

***Demonstration:*** Play a “lock-stepped”, WebSocket [***2-player game here.***](https://www.adityaravishankar.com/projects/games/tanks/) Record how responsive the game is and your impressions.

| Delay | User’s perception |
| --- | --- |
| 0 * 100 ms | ***Instant*** |
| 100 * 300 ms | ***Small perceptible delay*** |
| 300 * 1000 ms | ***Is Device working?*** |
| 1,000+ ms | ***Mental focus switches most likely*** |
| 10,000+ ms | ***Task is abandoned!*** |

![](resources/makingbrowsergames_com---book---imagesConsolidated---TCPThroughputVsLatency-600x370.jpg)

Measuring network performance – TCP throughput vs latency

With 2% packet loss, TCP throughput is between 6 and 25 times lower than with no packet loss.

| **Round trip latency** | **TCP throughput with no packet loss Round trip latency** | **TCP throughput with 2% packet loss** |
| --- | --- | --- |
| 0 ms | 93.5 Mbps | 3.72 Mbps |
| 30 ms | 16.2 Mbps | 1.63 Mbps |
| 60 ms | 8.7 Mbps | 1.33 Mbps |
| 90 ms | 5.32 Mbps | 0.85 Mbps |

### Adobe RTMP and RTMFP

[***RTMP (52-page specification)***](http://wwwimages.adobe.com/www.adobe.com/content/dam/acom/en/devnet/rtmp/pdf/rtmp_specification_1.0.pdf) was a proprietary WebSocket solution developed by Macromedia for the Flash Player (end of life: 20201231); but, was later opened up and is now published as [***RFC 7016.***](https://tools.ietf.org/html/rfc7016) Macromedia was purchased by Adobe for $3.4 billion in 2005 and [***patented the RTMP solution.***](http://www.therealtimeweb.com/index.cfm/2008/3/6/rtmp-patent) (See patent [***US patent number 7246356***](https://patents.google.com/patent/US7246356)) Adobe released “an incomplete” RTMP version for public use. [***(See license here)***](https://www.adobe.com/devnet/rtmp.html) The primary motivation for RTMP was to be a protocol for playing Flash video (Flash player end-of-life is DEC 2020!), it is also used in some other applications. “RTMFP, which is RTMP over UDP instead of TCP, replacing RTMP Chunk Stream. The Secure Real-Time Media Flow Protocol suite has been developed by Adobe Systems and enables end‐users **to connect and communicate directly with each other (using the [P2P library](https://github.com/js-platform/p2p) ).** … Unlike RTMP, RTMFP also supports sending data directly from one Adobe Flash Player to another, without going through a server. A server‐side connection will always be required **to establish the initial connection between the end‐users** and can be used to provide server‐side data execution or gateways into other systems.” [***quoted from Wikipedia***](https://en.wikipedia.org/wiki/Real-Time_Messaging_Protocol)

The lesson we should learn from RTMP / RTMFP is the size of their data packets transmitted, their [***“Action Message Format” (AMF)***](https://en.wikipedia.org/wiki/Action_Message_Format) structure and their use of TCP / IP to manage packet interleaving and multiplexing.

Our take away from Adobe RTMP is their dependency on networking Layers 3 & 4, their assembly of smaller Datagram size, their [**Action Message Format (AMF)**](https://en.wikipedia.org/wiki/Action_Message_Format) and setting [***Maximum Transmission Unit (MTU).***](https://www.linksys.com/us/support-article?articleNum=134914) The Internet standard for MTU is 576\. The maximum value of the `packet_size` is 65,464 bytes for IPv4 and 1,280 bytes for IPv6\. When you connect to an Internet resource, your data goes through a router that has an MTU of 576\. This results in fragmentation if your MTU is greater than 576, which can result in a Web resource being loaded slowly. [Quoted from Wikipedia,](https://en.wikipedia.org/wiki/Maximum_transmission_unit) “For example, according to IPv6’s specification, if a particular link layer cannot deliver an IP Datagram of 1280 bytes in a single frame, then the link layer must provide its own fragmentation and reassembly mechanism, separate from the IP fragmentation mechanism, to ensure that a 1280-byte IP Datagram can be delivered, intact, to the IP layer.”

## 5.9 Availability

***Let’s now discuss that missing aspect in all MMoGs.*** Many MMoG provide gamers with a choice of whom to play. They can:

1.  enter a game full of strangers;
2.  play alone against an AI “bot” opponent(s) ***or against “bots” [masquerading](https://dictionary.cambridge.org/dictionary/english/masquerade) as live humans;*** ( … **hint! hint!** Nothing’s more disappointing when a player enters your MMoG lobby to play and NO ONES THERE! So, they then …)
3.  invite their friends into a privately created game session.

I’ll address this next; but before I do, answer these questions:

*   How many times have you received a cell-phone call while you were engaged in another activity?
*   How did you respond? By immediately, dropping everything you’re doing to answer the call? or, while driving your car, did you pull over to the curb and then answer?

**Yea, I thought so.** Inviting a friend to enter a private game doesn’t resolve the problem of “availability”. ***But PBM³ Technology does!***

## 5.10 PBM³ Technology

The following information has been my industrial business “secret” until now. You will not find this anywhere prior to this book’s release in late 2013\. The gaming industry is following the same mistakes as those of the distance-learning educational community. If you will recall, I mentioned earlier in “chapter 1: New dog, Old tricks”, the silliness of using a camera to video game-turns and that distance education specialists had been using the same methods for decades — recording classroom lectures for video playback. What everyone is missing is simply that current MMoG are attempting to simulate the old-fashion “face-to-face table-top board game” — just as educators are trying to mimic classroom lectures. All the participants ***must be present, at the same time, hovering over their virtual “game table”.*** Many of the dramatic problems plaguing MMoGs relates to: 1) synchronization; 2) connections; 3) network lag; 4) who-killed-whom-when in FPS; (ad nauseam) ***all of these issues stem from attempting to represent a “face-to-face table-top board game” online.*** Honestly now, do you really enjoy watch those video-taped lectures of power-point slides and that silly professor’s “talking head” located near the screen’s corner? “Makes ya feel like your in the lecture hall, doesn’t it”; I thought so! (I’m being sarcastic, again) The only educational benefit, in my mind, is “pausing that ***bloke*** for a minute” while I get a beer (or two)! [***(what’s the female version for bloke?)***](https://answers.yahoo.com/question/index?qid=20080329145929AANeCIc)

I will present never before seen solution that will revolutionize your MMoG — ***Use PBM³ Technology and get rid of “Concurrency” — i.e., being in the same time and place! Stop attempting to mimic “face-to-face table-top board games” and adopt a true “asynchronous” gaming method using Artificial Intelligence (AI).***

***“What the `<insert your favorite derogatory expression here>` are you talking about now?!?!?!”*** (It’s kinda scarey how I can read your mind ***across time and distance,*** isn’t it! Yea, that has to do with ***“Availability” too!)*** Do you recall what you read about [***Message Oriented Middleware (MOM) Asynchronicity?***](https://en.wikipedia.org/wiki/Message-oriented_middleware#Asynchronicity)

I’m going to give you a few solid examples, and then I will explain what you just witnessed. Ready?

***Participate and watch:***

***Exercise #1:*** Watch either —

*   [***this video completely;***](https://www.youtube.com/watch?v=JI16hwn3L9U) @ [https://www.youtube.com/watch?v=JI16hwn3L9U](https://www.youtube.com/watch?v=JI16hwn3L9U) it’s only 2:50 minutes of your time ***OR choose***
*   this 3-minute [***highly entertaining one***](https://youtu.be/KqFKhgZto5I) @ [https://youtu.be/KqFKhgZto5I](https://youtu.be/KqFKhgZto5I)

**Do you get? NO??! Ok,** this one is a bit **more obvious …**

***Exercise #2:*** Watch either or both of these video completely;

*   2a) Girl — [Anne Reburn is creating music and videos](https://www.youtube.com/watch?v=JL2cMfITXLU)
*   2b) Guy — [Dan Wright is creating Music](https://youtu.be/p6627_5-FdY)

Here’s what you just witnessed. It’s such a mundane task now-a-days that folks just don’t think about it anymore. In exercise #1, were you listening to a live or prerecorded session? ***“Really? It was prerecorded; why are you asking me that?”*** (still kinda scarey, [ain’t it!](https://www.merriam-webster.com/dictionary/ain't)) ***Because in the late 80s (30 years ago!?) that was the concept I applied to MMoGs to dissolve “Availability”.*** You record the player’s game-turn actions and send those to the remote player either “… by Mail, by eMail, or by Modem” ***— MOM.*** That’s the origins of my motto for ***PBM³*** (Play By Mail, Play By eMail, and Play By Modem” — **PBMCube**). I’ll show you the code in the following chapters. This was revolutionary in the 80s to early 2000s until ***everyone*** started using . . . Message Oriented Middleware (MOM).

In ***Exercise #2:*** above, the fun really starts to heat up! You did watch at least one of those video? Anyway, I forgive you and moving on to my point. Using the magic of recorded sessions, the singers were able to combine the various vocal parts into a quartet. They simply recorded one session singing one part; then later during editing, they combined the parts into a single performance. They took “Availability” to a new dimension of simultaneous. You see, time — each recording — was stacked on top of the time to record the second, third and fourth vocal parts. Availability was dissolved by stacking time from each recording on top of the others to give the illusion that they were all singing at the same time and space. ***This is the secret sauce that none of the MMoG are using!*** Yes, they are doing prediction or lag modifications through interpolation or extrapolation. But not one MMoG today (2016-2019) is doing what I’m suggesting and what we’re coding later in this book using predictive look-ahead AI.

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogAvailability.jpg)

MMoG Availability with Integrated AI feedback (Phaser III Game Prototyping Chap. 9)

| **Traditional Predictive Analytics** | **Artificial Intelligence** |
| --- | --- |
| Based on tech that’s several decades old | Is undisputed future of technology |
| Automated tool to gain insights approach | Autonomous in that A.I. produces decisions |
| Utilized only historical data points to learn only at the pace of time | Runs simulations to create all future possible data points to learn faster than the pace of time |
| An entrenched base of costly legacy users | Catalyst for industry-wide disruption |
| Costly hardware, software licenses, and/or consultation business model | SaaS delivery – leverages decreasing cost and increasing capacity of computing |
| Often created to perform a specific task(s) – no ability to examine the effects across the entire retailer’s “ecosystem” in the immediate here and now only | Looks at relationships between promotions and products and their net effect on sales across the total assortment over the long term |
| Constrained/governed by strict, static models – looking at subsets of data in predefined models. Does not factor in ripple effects | Able to holistically examine very large, rapidly changing data sets across a large set of variables. Measures all ripple effects |
| Likely may utilize machine learning in that it adjusts based on new limited data sets based only on the historical information available | Can self-adjust without human intervention and change underlying algorithms based on vast new simulated data inputs to find the optimal outcome |

As I suggested earlier, we could mix networking relationships — **P2P** with the “hub and spokes” (i.e., Centralized Authoritative Server). In the illustration below, you’ll see that all game turn orders (GTO) are “Broadcast or Multicast” **P2P** among all participants as a P2P network relationship. We could accomplish this using the [***WebRTC API***](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API) to build [***“A simple `RTCDataChannel` sample “***](https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API/Simple_RTCDataChannel_sample).. The GTO arrives at the server and processed; then forwards the game turn results (GTR) to each destination ***as a confirmation*** of the game state status. The remote gamer receives the original GTO directly followed by the server’s confirmation. The confirmation arrives moments behind the GTO — the amount of time the server took to processing the newly submitted GTO. This suggestion is limited to “small MMoGs” and has the same restriction I mentioned in Part I Chapter 3.3 Network Relationships — ***n(n+1)/2.*** Let’s follow Microsoft Academy recommendations for home work-groups and limit the maximum MMoG participants to 10.

![](resources/makingbrowsergames_com---book---imagesConsolidated---blue-p2pConfirmed.jpg)

Availability Overlays

### Managing Time-line Models

We’ve studied the “Skipping Rope — Fixed Time Intervals”, [***Glenn Fiedler options***](https://gafferongames.com/post/what_every_programmer_needs_to_know_about_game_networking/) and reviewed a [***2-player demonstration***](https://www.adityaravishankar.com/projects/games/tanks/) showing its efficiency. Its time to consider what others are doing.

The time-line model does not impose any specific architecture on the game. [***The Janus toolkit (36-page bonus content; “pre-WebSockets” solution circa 2013)***](https://link.springer.com/content/pdf/10.1007%2Fs00530-012-0271-3.pdf) allows for a variety of overlay architectures including peer-to-peer, client–server and a hybrid model depending upon the subscription list for each time-line.

Time-lines implementation for lag compensation techniques in networked games. Use it both on server and/or client-side according to your needs.

*   Take snapshots of game state
*   Interpolates and extrapolates values based on snapshots taken.

Time-lines implementation for lag compensation techniques in networked games [found here on GitHub.](https://github.com/gamestdio/timeline)

## 5.11 Too Hot, Too Cold, Just right! … where & what

Now the real work begins! Are we using a “thick or thin client” on the gamer’s side? What are the advantages or disadvantages of putting a thick client on the gamer’s client-side? And what about using a thin client? Why should we care? Because the “thicker” the client becomes the “thinner” our server application requirements are to the point of becoming a [***“Ghost server”***](https://crossbario.com/blog/Free-Your-Code-Backends-in-the-Browser/) — more in the server chapter. This is why I’m suggesting a “message broker” (server proxy) in the browser.

### Deployment Options

We have several options to consider when writing our MMoG. The answers will determine where we place what code and how the gamer will input and respond to their opponents. Here are the combination options as a matrix:

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogFlow3.jpg)

MMoG Game as Web-MVC

***Gamer’s Browser***

*   Thick (Smart) gaming browser clients. Handles `some` of the game logic details. Phaser JS Gaming Framework provides a lot of power and could take on much of the server’s processing tasks locally in a “turn-based” game. It would need to “check-in” to maintain game synchronization.
*   Thin (dumb) gaming browser clients. Handles only player input as a “dumb terminal”. The game logic details and calculation are all on the server-side. For example, Phaser would handle only the local animations but avatar movement must be confirmed and authorized from the game server app. Naturally, this is the worst choice for “Real Time Simulations (RTS)”.

***Game Engines***

*   Authoritative servers (centralized)
*   Authoritative servers (de-centralized or distributed in a CDN)
*   Validation servers (centralized or master)
*   Validation servers (de-centralized or distributed in a CDN)
*   Routing (pass-through or monitoring) servers

***Download the `Deployment Worksheet` here [http://makingbrowsergames.com/mmog/bonusContent/MMoG-Deployment-Worksheet.pdf](http://makingbrowsergames.com/mmog/bonusContent/MMoG-Deployment-Worksheet.pdf)***

## 5.12 Chapter Summary

*   [***Decided on which MMoG’s “Web API” to use***](https://medium.com/platform-engineer/web-api-design-35df8167460)
*   Contrasted single player game architecture to MMoG.
*   Compared legacy networked game prior to 2014 to current WebSocket and microservices.
*   Review IBM recommendations for a MMoG Architecture System, and found missing components.
*   Discovered how to test our MMoG from several online tools and test sites.
*   Collected vital statistics we’ll use to write our source code.
*   Learned the value of `dns-prefetch`.
*   Articulated when and under what circumstances to use prefetch for MMoG.
*   Reviewed several successful MMoG, and dissected their architecture, and which tools they use as middleware.
*   Modified our MMoG from legacy to distributed Cloud microservice.
*   Studied IBM’s Rogue Cloud Game.
*   Learned about `DevOps pipe-lineing` for MMoG deployment.
*   Investigated `Docker containers` and `Kubernettes`.
*   Compared current MMoGs to Doctor Offices and Theater Shopping Malls.
*   Examined Multi-Game Objects data structure to manage multiple games and gamers in each game.
*   Transpiled Multi-Game Objects data structure for current project development.
*   Discovered the similarity between distance education and MMoG and concurrent delivery.
*   Investigate the issue of “Availability”.
*   Dissected a 30 year old industrial secret and digested its concepts for current MMoG project development.
*   Analyzed 3 different examples to dissolve “Availability”
*   Given 2 factors to dissolve “Availability”: prerecording, and collapsing time-frames
*   ***Using the provided Worksheet(s) and online tools, we decided where to place what source code and aligned the responsibilities in MMoG system.***
*   We followed recommendations from other knowledgeable MMoG designs.

## 5.13 Chapter Foot Notes

1\. [***Telegram Database Library***](https://github.com/tdlib/td) — [***Telegram APIs***](https://core.telegram.org/api) — offers two kinds of APIs for developers. The [***Bot API***](https://core.telegram.org/api#bot-api) allows you to easily create programs that use Telegram messages for an interface. The [***Telegram API and TDLib***](https://core.telegram.org/api#tdlib-build-your-own-telegram) allow you to build your own customized Telegram clients. You are welcome to use both APIs ***free of charge.***

2\. D. G. Puranik, D. C. Feiock and J. H. Hill, [“Real-Time Monitoring using AJAX and WebSockets,”](https://www.computer.org/csdl/proceedings/ecbs/2013/4991/00/4991a110-abs.html) 2013 20th IEEE International Conference and Workshops on Engineering of Computer Based Systems (ECBS), Scottsdale, AZ, USA, 2013, pp. 110-118. doi:10.1109/ECBS.2013.10

3\. [Building a simple yet powerful MMO game architecture, Part 1: Introduction.](http://www.ibm.com/developerworks/library/ar-powerup1/) Ibm.com (8 September 2008). Retrieved on 2016-11-25.

4\. [HTML5 WebSocket: A Quantum Leap in Scalability for the Web. (2016)](http://websocket.org/quantum.html) Retrieved 2016, from [http://websocket.org/quantum.html](http://websocket.org/quantum.html)

5\. Gamasutra — [1500 Archers on a 28.8: Network Programming in Age of Empires and Beyond](https://www.gamasutra.com/view/feature/3094/1500_archers_on_a_288_network_.php)

6\. Garage Server I.O (if you still insist on using Node.js and Socket.io [https://github.com/jbillmann/GarageServer.IO](https://github.com/jbillmann/GarageServer.IO)

7\. [Event-Driven Web Application Design](https://yuiblog.com/blog/2007/01/17/event-plan/)

8\. [RabbitMQ and WebSockets](https://www.cloudamqp.com/blog/2016-10-10-RabbitMQ-and-WebSockets.html)

9.  [***Introduction to the JSON API***](https://laravel-news.com/json-api-introduction)
10.  [***5 reasons you shouldn’t be using GraphQL***](https://blog.logrocket.com/5-reasons-you-shouldnt-be-using-graphql-61c7846e7ed3)
11.  [***REST API Industry Debate: OData vs GraphQL vs ORDS***](https://www.progress.com/blogs/rest-api-industry-debate-odata-vs-graphql-vs-ords)
12.  [***REST vs GraphQL vs oData***](http://golionko.com/index.php/2018/10/08/rest-vs-graphql-vs-odata/)
13.  [***OData website***](https://www.odata.org/)

# Part III: Production & Development

![](resources/makingbrowsergames_com---book---imagesConsolidated---myProjFlow.jpg)

My Project Process

Welcome to the ***MMoG Production Phase*** of Project Management.

We are — at last! — ready to begin our “encoding components” step described in [***Game Recipe™***](https://leanpub.com/phaser3gameprototyping) with the solid foundation and knowledge you’ve collected and built from Parts I & II. Furthermore, combined with all your reading, research, and exercises answers, you possess the documentation for Game Recipes™.

![](resources/makingbrowsergames_com---book---imagesConsolidated---gsdProcess-blue.jpg)

Game Recipe™ Process

# 6 Client-side Foundation

With the solid foundation from Parts I & II, your research and answers to the various exercises, we are — at last! — ready to begin our source coding sessions. We will start on the client-side and migrate across the MMoG Architecture we discussed in Part II. Our goal, by the end of this chapter is to have:

*   a functional WebSocket conduit (aka “telecommunications channel”) starting from client-side proxy to server API with data formatted as either an RPC or MOM. It becomes our MMoG prototype to expand into more specific game messages in later chapters.
*   a guiding regimen showing us where to place our source code across our MMoG systems.

To use WebSockets, you need a browser, a web server and a socket app server that all support ***the same WebSocket protocol.*** (You learned that in Part I, and ***all the reasons*** to avoid using Socket.IO and its incompatibilities). Your best friend will become [***“Can I Use” website***](https://caniuse.com/#search=websocket); it provides current information about the WebSocket technology, browsers to avoid, known issues, and resources. You were given two test sites in Part II; it’s time to create your own testing server — this is not the same as `Web Server`. You will need a traditional web server (such as Apache or IIS) on your local development workstation to serve your game’s ***dynamic content.*** (You recall from Part I that Node.js and Express only delivers static content? Right?) You have a “Project Game Starter Kit” in your Bonus Content you need to copy this into your workstations web server root directory and make sure its running in the background of your development workstation. You’ll need to make sure not to close the command prompt window!

***[http://makingbrowsergames.com/mmog/bonusContent/WebSockets.zip](http://makingbrowsergames.com/mmog/bonusContent/WebSockets.zip)*** or any client SDK from ***[https://kaazing.com/download/](https://kaazing.com/download/)***

![](resources/makingbrowsergames_com---book---imagesConsolidated---uiHudGM.jpg)

New MMoG Information Flow

The Client-side has several important responsibilities while processing the game logic, so that it works well with the remote server (or local proxy server) and provides a quality game-play experience:

*   ***Rendering*** — the Client-side is responsible for rendering the game on the player’s display, and may be responsible for non-important physics simulations, such as cloth simulations or particle effect — such special effects (sfx) should ***NOT*** come from a remote server, ***RIGHT?*** If a client-side animation doesn’t have gameplay relevance but is merely “frosting or eye-candy” to make the game “taste” better, it shouldn’t be executed on the `MMoG App server` at all. ***RIGHT?*** Why should we add network lag and delay to sfx that do ***NOT*** impact other players?
*   ***Sound*** — The Client-side plays all audio sound effects and/or music tracks. It is [***preposterous***](https://www.dictionary.com/browse/preposterous) to think that the server would stream audio playback.
*   ***Input*** — The Client-side collects a player’s input, packages it, and then sends that information to the server in a negotiated format. We’ll study RPC or MOM **JSON declarative** formats in the upcoming Server and MMoG App chapters.
*   ***User Preferences*** — Many games store user preferences on the local machine where the game runs. However, that also depends on the type of data. Obviously, a gamer’s subscription account balance would be safely stored in the back-end business logic and storage. Safe data might be the gamer’s native language, volume controls, and any keyboard adjustments.
*   ***Prediction*** — The Client-side could predict what might happen to game objects in the short term while it awaits for the centralized server to synchronize and send “confirmations”. I’ll show you how this works later in this chapter using a client-side proxy server.
*   ***Interpolation*** — As part of the Client-side prediction process, the Client can calculate where a game object needs to be, and where it thought it should be, and where the authoritative server confirms where it is, and shall go. Interpolation is important in “Real-time” games — when multiple players are simultaneously modifying the game state. Many MMoG tutorials don’t tell you about “Separation of Concerns”. The [***“interpolation and extrapolation”***](https://gamedev.stackexchange.com/questions/118006/when-should-i-extrapolate-and-when-should-i-interpolate) calculations are perfect candidates for a client-side proxy server.

The whole idea is amazing, that JavaScript can do all this locally. Then add onto this idea that JavaScript is based on a **single-threaded environment** increases the “awesome factor”. Web Workers remove (partially) this single-threaded limitation as you’ve read in the previous MMoG Application Architecture chapter.

## 6.1 Testing Your Browser

As of 20190327, we know that over 95% of all browsers ***already support WebSockets natively!*** We should check if our browsers support WebSockets before we go any further writing our MMoG.

```
1     // Make sure the browser supports WebSocket
2     if (!window.WebSocket) {  
3         displayMessage("Your browser does not support WebSockets");  
4         return;  
5     } 
```

JS check for client-side WebSocket.

In your “Project Game Starter Kit” you downloaded earlier, search for the directory “WebSocket” and inside the “WebSocketTest.html”” file and open it with your favorite browser. Click the link — “Run WebSocket” link. Testing completed. It worked? Right? If not, then research [http://canIuse.com](https://caniuse.com/#search=Websockets) at the bottom of the page are tabs leading to “Notes”, “Known Issues”, and current “Issues”. You also might like to import their usage data and discover how much of the world already supports WebSockets ***natively in browsers.*** You also noticed that we didn’t need a web server to run this simple test; but we will need a “full-stack” web server installed on our development workstation eventually.

Open the `WebSocketTest.html` and study what we just did. You may also test your active browser against either [***my demo socket server***](http://mmog.pbmcube.net/index.php) or against [***websocket.org.***](http://websocket.org/echo.html) Review chapter 5 for other details:

## 6.2 WebSocket Protocol Handshake

To switch into an “upgraded WebSocket connection”, the gamer’s browser should send a ***“WebSocket handshake request”,*** — which we did. The game testing servers will return a ***“WebSocket handshake response”,*** — which it did; nothing new thus far . . . same old, same old that we studied in Parts I & II.

### Deeper Dive: WebSocket API

![](resources/makingbrowsergames_com---book---imagesConsolidated---dialogFlow.jpg)

Upgrade to WebSockets

The WebSocket API - [**Read more …**](https://www.w3.org/TR/websockets/)

| **Event handler** | [***Event handler types***](http://dev.w3.org/html5/spec/webappapis.html#event-handler-event-type) |
| --- | --- |
| **onopen** | open |
| **onmessage** | message |
| **onerror** | error |
| **onclose** | close |

***Both server- and client-side WebSocket objects*** support the following API.

*   ***on(‘open’, function(event))*** fires when the socket connection is established. Event has no attributes. Ensure your data is sent only when a connection exists; we should wrap our `send()` method with onopen event.
*   ***on(‘message’, function(event))*** fires when the socket receives a message. Event has one attribute, data, which is either a String (for text frames) or a Buffer (for binary frames). The default data format is “blob” which is particularly useful when sending and receiving files.
*   ***on(‘error’, function(event))*** fires when there is a protocol error due to bad data sent by the other peer. This event is purely informational, you ***do not need*** to implement error recover because WebSockets ride on top of TCP/IP. ***“So how do errors still creep in?”*** Superior question; the answer is found in [***RFC 6455 Section 5.1 Overview***](https://tools.ietf.org/html/rfc6455#page-27) which you’ve already read (?) from the Networking Chapter exercises.
*   ***on(‘close’, function(event))*** fires when either the client or the server closes the connection conduit. This event has two optional attributes — code and reason — that expose the status code and message sent by the peer that closed the connection. It also has three properties you can use for error handling and recovery: `wasClean`, `code`, and `error`.
*   ***send(message)*** accepts either a String or a Buffer and sends a text or binary messages over the connection conduit to the other remote peer.
*   ***ping(message, function())*** sends a “ping” frame with an optional message and fires the callback when a matching answer (aka “pong”) is received. This is typically used to dynamically adjust the MMoG for network latency issues.
*   ***close(code, reason)*** closes the connection conduit, sending the given status code and reason text, both of which are optional.
*   ***version*** is a string containing the version of the WebSocket protocol the connection is using.
*   ***protocol*** is a string (which may be empty) identifying the sub-protocol the socket is using. We discuss various “sub-protocols” in the upcoming Server chapters.

The illustration above demonstrates the responsibilities of the client and the remote MMoG server on each end of the WebSocket communications conduit.

![](resources/makingbrowsergames_com---book---imagesConsolidated---wsDialog.jpg)

WebSockets Upgrade Dialog

| Property | Description |
| --- | --- |
| bufferedAmount | Returns the total number of bytes that were queued when the send() method was called binaryType Returns the binary data format we received when the onmessage event was raised |
| protocol | Returns the protocol used by the server |
| readyState | Reports the state of the connection and can take one of the following selfexplanatory values: |
|   | - WebSocket.OPEN |
|   | - WebSocket.CLOSED |
|   | - WebSocket.CONNECTING |
|   | - WebSocket.CLOSING |
| url | Returns the URL of the WebSocket |

Gamer’s client requests above are similar to HTTP requests, each line ends with `\r\n` and there must be an extra blank-line at the end. This is the standard format. The handshake resembles an HTTP request so that the game server can handle standard HTTP connections (port 80) as well as the new WebSocket connections across the same initial port 80 (or 443 for https). Once the new WebSocket request creates that connection, communications between the client and game server switches into a ***bidirectional binary protocol that does not conform*** to the former HTTP protocol. After a WebSocket connects, the gaming client and server can send WebSocket ***binary data or text frames*** in full-duplex mode — in either direction at the same time! This is a point-to-point connection as if client and server were peers. The data is minimally framed (for us by the WebSocket Protocol) with just two bytes. (Review Chapter 3 Network Basics) There’s no need to write code to package these frames as some tutorials lead us to believe. However, it is a “stream” of data; if your MMoG needs to understand discreet components, you might like to use a message format inside these WebSocket frames.

The WebSocket API allows for multiple types of data (`UTF8` text, `binary`, and `blob data`), and unlike the browser, these messages on the server are stored using different properties based upon those data types. In the case of text frames, each frame starts with a **`0x00 byte`**, ends with a **`0xFF byte`**, and contains **`UTF-8`** data in between. (Review Chapter 3 Network Basics page 62) This binary data stream is difficult for humans to read since it is ***bidirectional binary protocol.*** WebSocket text frames use [***a terminator,***](https://www.ietf.org/proceedings/76/slides/hybi-1.pdf) while binary frames use a length prefix.

```
1     HTTP/1.1 101 Switching Protocols  
2     Upgrade: websocket  
3     Connection: Upgrade  
4     Sec-WebSocket-Accept: cGxheWVyMzIxfGdhbWUxMjN8QUNL  
5     Sec-WebSocket-Protocol: mmog, soap, wamp, sip, amqp, mqtt, xmpp 
```

A typical Server’s response header looks like this:

In addition to Upgrade headers, the client sends a ***`Sec-WebSocket-Key`*** header containing [**base64-encoded**](https://www.base64decode.net/) random bytes, and the server replies with a hash of the key in the ***`Sec-WebSocket-Accept`*** header. This is intended to prevent a caching proxy from re-sending any previous WebSocket dialog, ([see footnote 1](https://trac.ietf.org/trac/hybi/wiki/FAQ)) and ***does not provide any authentication, privacy or integrity.*** The hashing function appends the fixed string `258EAFA5-E914-47DA-95CA-C5AB0DC85B11` (a GUID) to the value from `Sec-WebSocket-Key header` ***(which is not decoded from base64),*** applies the SHA-1 hashing function, and encodes the result using base64\. ([see footnote 2](https://tools.ietf.org/html/rfc6455#section-1.3))

![](resources/makingbrowsergames_com---book---imagesConsolidated---wsDevConsole.jpg)

Observe WS Header Exchange in Developer Console

```
 1     Request Headers . . .  
 2     GET ws://mmog.pbmcube.net:30113/demo/server.php HTTP/1.1  
 3     Host: mmog.pbmcube.net:30113  
 4     Connection: Upgrade  
 5     Upgrade: websocket  
 6     Origin: http://mmog.pbmcube.net  
 7     Sec-WebSocket-Version: 13  
 8     Sec-WebSocket-Key: zfG4XfYTSKp6NdIpCaYe+w==  
 9     Sec-WebSocket-Protocol: mmog, soap, wamp, sip, amqp, mqtt, xmpp  
10     Sec-WebSocket-Extensions: permessage-deflate; client_max_window_bits 
```

Launched the following

[![](resources/i_ytimg_com---vi---5R1ugZ_jLDI---hqdefault.jpg)](https://youtu.be/5R1ugZ_jLDI)

View this video at [https://youtu.be/5R1ugZ_jLDI](https://youtu.be/5R1ugZ_jLDI)

WebSocket monitoring with Wire-Shark in 3 min

Observe these WebSocket frames with [***Wire-shark.***](https://wiki.wireshark.org/WebSocket) (Refer to the Network Appendix on where to get **Wire-shark.**) Registered IANA Sec-WebSocket-Protocol are [**referenced here.**](http://www.iana.org/assignments/websocket/websocket.xml) The server can’t send more than one ***`Sec-Websocket-Protocol`*** header. If the server doesn’t want to use any sub-protocol, it shouldn’t send any Sec-WebSocket-Protocol header. Sending a blank header is incorrect. The client may close the connection if it doesn’t get the sub-protocol it wants.

![](resources/makingbrowsergames_com---book---imagesConsolidated---wsDevConsole2.jpg)

Observe WS Message Content Exchange in Developer Console

```
1     Response Headers . . .    
2     HTTP/1.1 101 Web Socket Protocol Handshake  
3     Upgrade: websocket  
4     Connection: Upgrade  
5     WebSocket-Origin: mmog.pbmcube.net  
6     WebSocket-Location: ws://mmog.pbmcube.net:30113/demo/rrte-mmog.php  
7     Sec-WebSocket-Accept:EZtDpyc+cXnNbqdzXW1QCmdm//Y= 
```

. . . and receives the following

## 6.3 Sample Source Code: Client-side WebSocket

The client-side is easy; it’s merely a JavaScript inside of an `index` page. Once we know our MMoG App server is running — the remote end of our WebSocket conduit — your gamers can connect to it through your “Web Server” and “subscribe to gaming messages” pushed from your MMoG App Server. The gamers will establish WebSocket connections through a process known as “WebSocket handshake”. This “handshake” starts when the gamer visits a “Game’s `index page`” from the Web Server to enter a specific game. The Web Server will then include an `Upgrade header` in this request that tells the “MMoG App Server” a gamer wants to establish a WebSocket connection. All of this was covered in Part I; this was simply a review.

![](resources/makingbrowsergames_com---book---imagesConsolidated---dataFlow.jpg)

To Summarize into our 4-Step development process (Chapter 5)

1.  ***Step #1:*** Inside the game’s index page, create a JavaScript WebSocket object — it is the client-side conduit toward the MMoG server’s URL.
2.  ***Step #2:*** Generate code for the following events — ***“onopen”, “onclose”,*** and ***“onerror”*** as WebSocket event handlers. Construct the ***“onmessage”*** event handler (the client-side workhorse and potentially a proxy-server) to handle, deserialize and read all incoming Game Turn Responses (GTR) coming from the `MMoG App server`.
3.  ***Step #3:*** Sending Game Turn Orders (GTO) “messages” to the `MMoG App server` using the WebSocket `send()` method. This is the topic in later chapters and Part IV when we create Game Turn Orders and server’s Game Turn Results.
4.  ***Step #4:*** Closing the client-side WebSocket conduit connection to the `MMoG App server` using the WebSocket `close()` method and transition into a new game phase.

In all of these cases, [***the WebSocket connection close code***](https://html.spec.whatwg.org/multipage/infrastructure.html#concept-websocket-close-code) would be 1006, as required by the WebSocket Protocol specification. [**WSP**](https://html.spec.whatwg.org/multipage/references.html#refsWSP)

### Step #1: Game `index` page

```
 1     <!doctype html>  
 2     <html lang="en">  
 3     <head>  
 4       <meta charset="utf-8">  
 5       <link rel="dns-prefetch" href="http://mmog.pbmcube.net/">  
 6       <title>WebSocket MMoG Client Example</title>  
 7       
 8       <!-- Typically Phaser Library is here with your gaming scripts -->  
 9       
10     </head>  
11     <body>  
12       <h1>MMoG Client-side via WebSockets</h1>  
13       <p>Open the JavaScript console to see what's up!  
14       Notice we're not using Node.js, Socket.IO; we're just  
15       using your vanilla browser for now.</p>  
16       <form>  
17         <label for="message">Send a Game Turn</label>  
18         <input id="message" name="message" type="text">  
19         <button id="send" name="send">Submit</button>  
20       </form>  
21       
22     <!-- The secret sauce is in this external file  
23         or simply insert script directly. -->  
24       <script src="ws_client.js"></script>  
25     </body>  
26     </html> 
```

***Typical `index.html` with WebSocket***

This `index.html` file (above) is placed on the `WWW` server; it is sent to the gamer’s browser. The client browser runs the JavaScript that will create the WebSocket conduit. This file is available in the “Project Game Starter Kit” at

*   ***[http://makingbrowsergames.com/mmog/bonusContent/WebSockets.zip](http://makingbrowsergames.com/mmog/bonusContent/WebSockets.zip) OR***
*   Download the `index.php` found in your Bonus Content at ***[http://makingbrowsergames.com/mmog/bonusContent/mmog-server-side.zip](http://makingbrowsergames.com/mmog/bonusContent/mmog-server-side.zip)***

### Step #2: Generate Event handlers

Let’s turn our attention to that JavaScript just above the closing `body` tag. Initializing a WebSocket is just as simple as the following lines of JQuery code. Create an external file entitled `ws_client.js` or insert the following script directly into the `index.html` — search in your Bonus Content for the directory “/WebSockets/” and inside that for the [***`ws_client.js` (click to review)***](http://makingbrowsergames.com/mmog/bonusContent/WebSockets/ws_client.js) or [***test online here:***](http://makingbrowsergames.com/mmog/bonusContent/WebSockets/WebSocketTest.html)

```
 1     (function () {  
 2         // ---------------------------------
 3         // You can check the number of bytes that have been  
 4         // queued but not yet transmitted to the server,  
 5         // this is very useful if the client application transports  
 6         // large amounts of data to the server.  
 7         // ---------------------------------  
 8         var MAX_BUFFER = 8192;  
 9     
10         // ---------------------------------  
11         // Warning! NEVER USE WEBSOCKET 12345!  
12         // port 12345 is a known virus;  
13         // Read in Phaser Multi-Player Gaming Systems  
14         // Chapter 6.2 WebSocket Protocol HandShake  
15         // ---------------------------------
16         // new WebSocket (url, optional sub-protocol)  
17         var ws = new WebSocket('ws://localhost:12345', 'echo-protocol');  
18     
19         //============================  
20         // Step 2: 4 WebSocket Protocol Msg  
21         //============================  
22         // WebSocket Events:  
23         // you simply add callback functions to the WebSocket object  
24         // or you can use the addEventListener() DOM method on your  
25         // WebSocket objects. It’s important to implement these events  
26         //  before attempting to send any messages.  
27         // ---------------------------------  
28         // Step #4: Close client-side conduit  
29         // FIN finished and cleaning up connection.  
30         ws.onclose = function (event) {  
31             console.log('Connection closed.');  
32         }  
33     
34         // Example of "close" addEventListner  
35         // Set handler for when the socket connection is closed
36         // websocket.addEventListener("close", function() { ...}  
37     
38         // Oops! Discovered an error the TCP/IP  
39         //  overlooked RTT or RTO problems  
40         // See RFC6455 Section 5.1 for more potential errors.  
41         ws.onerror = function (event) {  
42             console.log('An error occurred. Sorry for that.');  
43         }  
44         // ---------------------------------  
45     
46         // Conversations / dialogs messages to and from  
47         //  We'll cover this topic in later Chapters & Part IV.  
48         // alternate method:  
49         //      ws.onmessage = incomingMsg(event);  
50         // Example of "message" addEventListner  
51         // Set handler for when the socket receives a message  
52         // websocket.addEventListener("message", function() { ...}  
53         ws.onmessage = function (event) {  
54             console.log('Response from server: ' + event.data);  
55         }  
56     
57         ws.onopen = function (event) {  
58             console.log('Connection opened.');  
59             // let's try to send every second?  
60             setInterval( function() {  
61                 if (ws.bufferedAmount < MAX_BUFFER) {  
62                     ws.send(checkTheStatusAndSendData());  
63                 }  
64             }, 1000);  
65         }  
66     
67         // Add our customized handling  
68         // The readyState attribute may have one of the four values:  
69         // - CONNECTING (The connection is not yet fully open)  
70         // - OPEN (The connection is open and ready to communicate)  
71         // - CLOSING (The connection is in the process of closing)  
72         // - CLOSED (the connection closed or couldn’t be opened)  
73         // Knowing the current state can be very useful in  
74         // troubleshooting your application.  
75         ws.sendMessage = function (message) {  
76             if(ws.readyState === ws.OPEN){  
77                 this.send(message);  
78                 console.log('Message sent: ' + message);  
79             } else {  
80                 console.log('Connection failed.')  
81             } 
82         }  
83     
84         // Attach created game turn orders into a message frame 
85         document.getElementById('send').addEventListener('click',  
86         function (event) {  
87             event.preventDefault();  
88             var message = document.getElementById('message').value;  
89             ws.sendMessage(message);  
90         });  
91     
92     })(); 
```

Testing a WebSocket script (ws_client.js)

Review the sample code above. It contains the WebSocket API in a few events — `onclose`, `onerror`, `onmessage` and `onopen`. ***That’s it!*** Sending messages to the server uses the method `send()` and disconnecting from the server uses the method `close()`. ***Why does everyone try to make this so difficult? AND! it’s supported in 95% of all browsers NATIVELY!*** We managed to flip from HTTP connection into a WebSocket connection using a simple `upgrade` command! Why was it so simple? Because both are “peer protocols” to each other riding above the TCP/IP transportation layer. Everything is explained in the [***official W3C WebScoket API.***](https://www.w3.org/TR/websockets/) In Part I & II, we investigated that many other programming languages use this exact same WebSocket API specifications; without a doubt, WebSocket is [***ubiquitous.***](https://www.merriam-webster.com/dictionary/ubiquitous)

In the code examples above, the ***`bufferedAmount`*** attribute is used to ensure that updates are sent at a rate of one update every 1000 ms (1 fps), if the network can handle that rate, or at whatever rate the network can handle, if that is too fast. The ***`bufferedAmount`*** attribute could saturate a network by sending data at a higher rate than the network can handle; this requires careful monitoring by using WebSocket “Pings” and “Pong” commands. We’ll study and apply this information in upcoming server chapters.

***Study `ws_client.js`! There’s no Socket.io, nor Node.js, nor Express.js!*** We are using the internal native WebSocket protocol ***already available inside our browsers. How easy was that? No extra code, no formatting the data stream, no encoding nor decoding, AND protocols are software language agnostic!*** Everything was already performed ***for us by our browsers.*** Furthermore, ***Phaser — either version v2.x.x. or v3.16+ — had nothing to do with any of this;*** the WebSocket conduit simply opened. Phaser is inside an HTML5 canvas tag (i.e., a Layer 7 application ) — `Applications` receiving services from lower communication layers services (i.e., our WebSockets, and TCP/IP bindings) and let’s keep it that way. This is the primary idea behind the concept of “Separation of Concerns” covered in both the [***Phaser v2.x.x Game Prototyping workbook,***](https://leanpub.com/LoRD) new 4th Edition and [***Phaser III Game Prototyping workbook, new 4th Edition***](https://leanpub.com/phaser3gameprototyping)

If your ISP permits WebSockets or Node.js, they will assign you a software port number to use. ***[I’m fortunate to use an ISP](http://gose-internet-services.net/the-hepsia-hosting-cp/advanced-features/) that supports both Node.js and WebSockets.*** Yes, Node.js can have a role in MMoG development if applied correctly as we learned in Part II. We covered all those “ins and outs” of Node.js and all the “whens and how-tos” previously.

![](resources/makingbrowsergames_com---book---imagesConsolidated---websocketProto.jpg)

Server-side target

*   [Trojan Port Table](http://www.chebucto.ns.ca/~rakerman/trojan-port-table.html)
*   [TCP & UDP ports for your online games](http://www.gameconfig.co.uk/)
*   [Special Application Port List](http://www.practicallynetworked.com/sharing/app_port_list.htm)
*   [NMap Services](https://svn.nmap.org/nmap/nmap-services)
*   [Internet Storm Center](https://isc.sans.edu//)
*   [Service Name and Transport Protocol Port Number Registry](http://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)

## 6.4 Security Concerns

This section is an excerpt from the [PhaserJS Game Design Workbook](https://leanpub.com/phaserjsgamedesignworkbook/read_sample) It presents methods to foil piracy attempts on your MMoG.

### MMoG Protection

You will spend many hours developing your game; and, as you learned from Part I, copyrights only protect the tangible expression of your idea — not the idea itself! Yahoo User Interface team provides a hint in the note below entitled [Minification vs Obfuscation](https://yuiblog.com/blog/2006/03/06/minification-v-obfuscation/). (See Appendix references.)

As hopeless as Yahoo’s recommendation sounds, I offer a suggestion to “encourage Piracy”. Sounds strange? It’s coming in the Server-side chapters.

### Deeper Dive: WebSocket Security

From a security perspective, it is important to confirm the source “Origin” header during the connection handshake process from the server-side (against the expected origins) ***to avoid “Cross-Site WebSocket Hijacking” attacks. (Refer to Drown Attacks in Part II)*** This could happen when the connection is authenticated with either “Cookies” or “HTTP authentication”. One-third of all DNS server are vulnerable to [***“Pharming” attacks (watch this short 2 minute video);***](https://youtu.be/1d1tUefYn4U) don’t let your MMoG App Server fall victim to similar attacks. A better recommendation is to use tokens (or similar protection mechanisms) to authenticate the WebSocket connection especially when sensitive data is being transferred over a WebSocket.

### Deeper Dive: “Sticky Load Balancing”

### Use of <iframe>

The reason behind using an ***<iframe>*** (short for the inline frame) is “… the ultimate modularization tool, allowing you to break up content, seamlessly display content from other sources, and better manage downloading. It’s a must-have for any web designer’s arsenal.” (See footnote 1)

Other possible reasons developers deploy `iframes` (instead of AJAX) might be:

1.  `Iframes` circumvent the cross-domain origin policy; whereas images, scripts, and styles do not. This trick is beneficial for pulling content relatively safely from other domains. The results are presenting foreign content without clobbering one’s page content and styling — something JSONP would be able to do.
2.  `Iframes` are not restricted to a single resource mime-type. Google Gmail is a perfect example because it is a set of inline frames.
3.  Poor architecture design or resorting to a simple fix.

However, the problem with an ***<iframe>*** is that whenever you navigate to an HTML5 game inside a browser, the game’s ***<iframe>*** does not automatically receive “focus”. This means the gamer must click on the game’s displayed ***<iframe>*** before the game can accept any keyboard input. Annoying? Sure is!

Other web developers point to a number of reasons to further [avoid iframe usage](http://stackoverflow.com/questions/23178505/good-reasons-why-not-to-use-iframes-in-page-content). But as scary as they might wail, several game distribution channels insist on using `iframes` to preserve their website integrity through game content isolation.

![](resources/makingbrowsergames_com---book---imagesConsolidated---costlyTages.jpg)

Mostly Costly Web Page elements

```
1     <script>  
2         document.onload = function() {  
3         document.getElementById('frame').focus();  
4     };  
5     </script>    
6     <iframe id="frame" width="768" height="480" src="yourDomain.com"> 
```

## 6.5 One Last thing

We have our Client-side Web Socket prepared, but there’s no one to receive our game turn orders (GTO). It’s like the sound of “one hand clapping”. Let’s complete the next chapter so we can make some noise with “both hands”.

### Smart (thick) vs. Dumb (thin)

| What | ***Advantages*** | ***Disadvantages*** |
| --- | --- | --- |
| Smart Client | Real-Time Interaction. Best deployed on Wide Area network (WAN) Partial or Full game state prediction. Sees game in “present time” Message Queue management Client-side predication possible. High Animation fps Converses Server’s from processing all the game logic | Some (or all) game logic internal. Local Game State mismatch compared to game server. Invalid commands inserted. (Cheating) Server returns state from “past time”. Must wait for Server command ACK. Input to server at timed intervals. Dead reckoning difficult at real-time interactions on other players. |
| Dumb Client | Best for Slow turn-based games. Best deployed on Local Area network (LAN) Client-side prediction unlikely. Little or no animations Input to server is predictable | All game logic is external. Sensitive to network delay Worst choice for Real-time interaction game play. Game Physics on Server. Server must perform all game logic. |

## 6.6 Chapter Summary

For such a short chapter, we’ve accomplished a lot! Here’s what we did …

*   Discovered how and where to test browsers for WebSocket capabilities.
*   Created a WebSocket conduit without Socket.IO, Node.js nor Express.js.
*   Created our MMoG `index.html` page.
*   Tested our browser’s compatibility with the WebSocket Protocol.
*   Found two WebSocket testing sites.
*   Watched our WWW connection upgrade to a WebSocket.
*   Discovered that the WebSocket Protocol encapsulates (i.e., frames) our data for us.
*   Learned about WebSocket sub-Protocols, and base64 encoding.
*   Listed a few security concerns to watch in our source code development.
*   Reviewed [***PhaserJS Game Design Workbook***](https://leanpub.com/phaserjsgamedesignworkbook/read_sample) recommendations on MMoG Security.
*   Monitored a live demonstration provided.
*   Learned the four internal functions of the WebSocket protocol.
*   Noted various information to track gamers.
*   Study the migration of a gamer from standard HTML to ws protocol.
*   Found the technical specifications for WebSockets.
*   Developed a typical WebSocket activation page.
*   Learned the various components of a URL.
*   Discovered how to assign a port number for WebSocket usage.
*   Read the security issues and port numbers to avoid.

## 6.7 Chapter Foot Notes

1.  “Main Goal of WebSocket protocol”. IETF. Retrieved 25 July 2015\. The computation […] is meant to prevent a caching intermediary from providing a WS-client with an cached WS-server reply without actual interaction with the WS-server.
2.  Ian Fette; Alexey Melnikov (December 2011). “Opening Handshake”. RFC 6455 The WebSocket Protocol. IETF. p. 8\. sec. 1.3\. RFC 6455.
3.  [***Simple JSONRPC.Client over WebSocket***](https://github.com/bigstepinc/jsonrpc-bidirectional#simple-jsonrpcclient-over-websocket)
4.  [***The W3C WebSocket API***](https://www.w3.org/TR/websockets/) — [https://www.w3.org/TR/websockets/](https://www.w3.org/TR/websockets/) This specification defines an API that enables Web pages to use the WebSocket protocol (defined by the IETF) for two-way communication with a remote host.
5.  MDN Web docs — [***“Writing WebSocket client applications”***](https://developer.mozilla.org/en-US/docs/Web/API/WebSockets_API/Writing_WebSocket_client_applications)
6.  Resources and Tutorials from ***[https://kaazing.com/getting-started/](https://kaazing.com/getting-started/)***

# 7 Server-side Foundation

With a solid foundation from Parts I & II, client-side WebSockets conduit established from Chapter 6, your supporting research, and answers to the various assignment exercises, we are ***— at last! —*** ready to begin our source encoding sessions ***for our MMoG App Server and the WebSocket conduit end-point.*** We finished the client-side in the last chapter; the following chapters will migrate across the MMoG Architecture we discussed in Part II. Our goal, by the end of this chapter is to have:

*   a fully functional WebSocket conduit (aka “telecommunications channel”) end-point for client-side proxy as either an RPC or MOM. It becomes our MMoG prototype to expand into more specific game messages later in this chapter.
*   a model guiding us where to place our source code across our MMoG system.
*   Drafting which coded functions reside where.

To use WebSockets, you’ve tested your browser, tested our web server and launched socket app server that all supported the RFC 6455 WebSocket protocol ***without the aid of Socket.IO, Node.js nor Express.js.*** You were given several test sites in Part II; it’s time to create your own back-end server and cloud-based services. You’ve researched who, where and how much this initial investment will cost from Part I. You’ve already built and tested your client-side in the last chapter against our provided Internet-based socket server test sites. You will need a traditional web server, that resembles whatever ISP you intend as a host provider (such as Apache or IIS), on your local development workstation to serve up your game’s ***dynamic content*** — need I remind you that your local development workstation ***should mimic your public MMoG server?*** You’ll remember from Part I that Node.js and Express serves static content and ***was optimized for I/O? Right?*** You’ve already downloaded and studied the [`Project-GameStarterKit`.](http://makingbrowsergames.com/mmog/bonusContent/WebSockets.zip) For this chapter you will need those server-side files.

*   ***[http://makingbrowsergames.com/mmog/bonusContent/mmog-server-side.zip](http://makingbrowsergames.com/mmog/bonusContent/mmog-server-side.zip)***
*   ***OR [http://makingbrowsergames.com/mmog/bonusContent/ws.zip](http://makingbrowsergames.com/mmog/bonusContent/ws.zip)*** with simple [***set-up instructions here***](https://github.com/ghedipunk/PHP-Websockets/wiki/Getting-Started)

***Now it’s time to construct your own MMoG App server to intercept those WebSocket requests from the previous chapter.*** You’ll recall from Part I and II that you can write WebSockets in almost any programming middleware language on the server-side. You’ll need your list of game commands (i.e., Game Turn Orders (GTO)) your server will read and process. Here’s the suggested list from Chapter 5 again. You’ll notice that these recommendations are all ***(system message)*** — data that manages the game session. We’ll need to update this list with “game play” commands found in Part IV.

***Client-side GTO suggestions for MMoG management (listed alphabetically) from Chapter 5:*** Review [***this chart from your Bonus Content***](http://makingbrowsergames.com/mmog/bonusContent/MMoG-API.pdf) on REST APIs for the client and server-sides.

*   ***cancelGame*** — player, who launched the game request, recants
*   ***gtoCommand*** — (system message) “type” property is requested action
*   ***create_failed*** — (system message) feedback
*   ***created*** — (system message) feedback
*   ***dead*** — (system message) notification about opponent
*   ***endGame*** — (system message) notification
*   ***error*** — (system message) feedback concerning GTO
*   ***gameOver*** — migrate Phaser to gameOver phase
*   ***initRound*** — (system message) to reset variable for new game
*   ***join_failed*** — (system message) notification
*   ***joined*** — (system message) on successfully enter existing game
*   ***latency*** — (system message) on network lag and test
*   ***pong*** — (system message) response to server ping test
*   ***rooms*** — (system) data on available games
*   ***tick*** — (system) time-stamp data for synchronization

Once this `MMoG App Server` is running, our gamers can connect through our Web Server and subscribe to gaming messages pushed out from this server. We will start with a simple chat message server from the last chapter; because, sending `chat messages` among players is no different than sending game commands into our `MMoG App server`. Besides building a `chat server` is another MMoG feature for our players to send messages among themselves.

![](resources/makingbrowsergames_com---book---imagesConsolidated---wsDialog.jpg)

WebSockets Upgrade Dialog

The gamers will establish WebSocket connections through a process known as the “WebSocket handshake” that we’ve studied and applied in previous chapters. This starts when the gamer visits an “index” page requesting to enter the MMoG server. We learned that the `Upgrade header` was `ws_client.js` in our game `index.html` file. **All of this was covered in prior chapters in detail and should be simply a review.**

## 7.1 Building a Socket Server

Using WebSocket creates a whole new usage pattern for server-side game applications. You’ll recall that AJAX and long-polling are dead and have been replaced with WebSockets. While traditional web servers were designed around the stateless HTTP/TCP port 80 requests/responses; they do not deal at all with a large number of open connections our gaming server demands. Keeping a significant number of these persistent connections open — **all at the same time** — requires a shift in architecture that is able to receives a high volume of “Input / Output” (I/O) concurrency at a CPU low-performance costs. Such architectures are usually designed around either ***threading*** or ***non-blocking IO (aka Node.js).*** Node JS is a candidate for such a task, and we have already studied when, why, and how to use it appropriately in Part I and II.

![](resources/makingbrowsergames_com---book---imagesConsolidated---dataFlow.jpg)

New MMoG Data Flow

Writing our source code for the WebSocket Server is a tad-bit more involved. “Why’s that?”, you ask? Because the WebSocket protocol goes beyond just simple socket binding, it’s actually a Multi-step process requiring a perpetually running daemon. Using PHP 7, I can’t run my server as a normal `PHP` page — those pages have a 30-seconds timeout. I need to run my `PHP` MMoG script from the command line. ***You do have command line (CLI) access on your public production server? Right?***:

We have the similar server-side choices; we can run our MMoG APP server as a `dedicated`, `hosted PaaS`, `thick`, `thin`, and `thick / stateless` server architectures. Which deployment is dictated by how much work we demand from our server and game logic involved. Wikipedia provides these definitions.

Servers also have these additional responsibilities depending upon our game’s intent. Several of these roles could become horizontal micro-services.

*   ***Authoritative*** — Information transmitted from the Server overrides the local Client information in the case of a bad prediction on the part of the Client. This ensures that the local data of the Client does not “drift” from the data the other Clients have.
*   ***Collision & Physics*** — The Server performs collision checks and important physics calculations like rigid-body dynamics that affect game objects. You will assign this task if you intend to use Phaser in “Headless” mode. However, I strongly urge you to reconsider this design approach and the impact network delay, jitter and lag would have on your game.
*   ***Datablocks*** — JSON Datablocks are sent in the start-up phase of a mission or scenario. The Server has all of the JSON datablocks for clients to download. You might want to consider using [***W3Schools AppML.***](https://www.w3schools.com/appml/) This means that the server only has to send datablocks as they’re needed, and can send new datablocks for different levels or missions.
*   ***Ghosting*** — The server keeps track of all the “active” objects in play, and “Ghosts” or copies data for each of them to the Clients by using “Scoping”, [***“routed RPC” (rRPC)***](https://wamp-proto.org/intro.html#wamp) or “Areas of Interest (AoI)”. [***(Read how to setup and use AoI in JavaScript (download source code))***](http://docs2x.smartfoxserver.com/ExamplesJS/simple-mmo) This means the server has a master list of all active game objects, and sends updated information for each of them to the local game on the client. ***OR,*** it could simply become a “pass-through” server — similar to Skype — as discussed in [***“Free Your Code - Back-ends in the Browser”***](https://crossbario.com/blog/Free-Your-Code-Backends-in-the-Browser/)
*   ***Message Routing*** — The server can sends messages, such as in-game chats, between clients. A better approach would be to provide a list of current participants in the game and allow gamers to use “Peer-to-Peer” messaging. [***RabbitMQ,***](https://www.rabbitmq.com/getstarted.html) and [***ZeroMQ***](https://blog.scottlogic.com/2015/03/20/ZeroMQ-Quick-Intro.html) (also spelled ØMQ, 0MQ or ZMQ) are the most widely deployed open source message broker tailored for this purpose. [***Learn how***](https://www.rabbitmq.com/getstarted.html) to use RabbitMQ in these server-side tutorials.
*   ***Scoping*** — Scoping helps sort out what each client is aware of so our game engine doesn’t have to send unnecessary updates. Game objects are initially ghosted to the client in the second stage of a game’s start-up in order to save bandwidth and minimize on network delays.
*   ***Security*** — The Server can kick bad behavior and cheaters out of a game, and could configured to detect “hacks” performed by a naughty client.

### Server Requirement Considerations

There are a few requirements we should consider no matter which middleware language we implement.

1.  Our middleware must be able to `listen` for incoming traffic on an available port(s). Typically, it will be the standard HTML **ports 80 and/or 443 from its own chassis.** `Listening` (aka binding) to these standard web ports because it gets around proxy and firewall concerns that we’re likely to encounter in a live production deployment — that’s how the `big boys` do it!
2.  **You cannot run a WebSocket server** and a **`WWW` server** on the **same ports from the same IP address at the same time.** You can either run it on a separate IP (aka server) on the standard ports of 80 or 443 or run it on the same box at a different unused port above 1023\. What I’m saying is **you might not be allowed to operate your WebSocket server on shared hosting accounts.** I’m fortunate that my [ISP allows WebSocket servers.](http://gose-internet-services.net/)
3.  If you elect to place your WebSocket server on a non-standard port, double check that your firewall will not block that traffic.
4.  You must have a way to run your middleware perpetually.

### Deeper Dive: Measure Network Latency

```
 1     // The game clock will run at 1 tick every 100 milliseconds
 2     var gameTimeout = 100;
 3     
 4     function measureLatencyStart(player) {
 5         var measurement = { start: Date.now() };
 6         player.rttLatency.push(measurement);
 7         var clientMessage = { type: "latency-ping" };
 8         player.connection.send(JSON.stringify(clientMessage));
 9     };
10     
11     function measureLatencyEnd(player) {
12         // Complete the calculations for the current measurement
13         var crntMeasuremnt = player.rttLatency[player.rttLatency.length - 1];
14         crntMeasuremnt.end = Date.now();
15         crntMeasuremnt.roundTrip = crntMeasuremnt.end - crntMeasuremnt.start;
16         // Calculate the average round trip for all the trips so far
17         var totalTime = 0;
18         player.rttLatency.forEach(function (measurement) {
19         totalTime += measurement.roundTrip;
20     });
21     
22     player.averageRoundTrip = totalTime / player.rttLatency.length;
```

Measuring and Compensating for Latency

## 7.2 Server Pages

![](resources/makingbrowsergames_com---book---imagesConsolidated---dataFlow.jpg)

Review Chapter 5 MMoG Architecture

The content from this package is installed on the `MMog App Server` — see the illustration at #2 “WebSocket Upgrade” above. The first thing you will notice as you study this package — ***NO `NODE.js` anywhere!*** In fact, you shouldn’t be surprised to find ***`PHP`*** as the middleware. We covered all this in Part I & II. We learned back then that ***`PHP`*** outperforms `Node.js`, and replaces `Express.js` as the supporting middleware functions assisting `Node.js`.

***`PHP`*** Socket source code is very similar to JavaScript and “C/C++” — they all belong to a “curly brace” languages. Even most of the `function` names in ***`PHP`*** are similar to those in `C Socket programming`. You can execute PHP from dynamic pages or from the command line. Here’s an example of running PHP from a server-side command line:

### Code Review `index.php`

This is the HTML5 page sent to the client browser and will launch the client-side WebSocket conduit. It also tells the client where to find the MMoG App server.

***Download this 4-page file from [http://makingbrowsergames.com/mmog/bonusContent/index-MMoG.pdf](http://makingbrowsergames.com/mmog/bonusContent/index-MMoG.pdf)***

*   ***Lines 1 to 4:*** begins our server php `index` and variables. Jump down to Line 160 to see the PHP variables used and dynamically modifying our WebSocket script.
*   ***Lines 10 to 70:*** are embedded style sheet. I chose to put the style inside the index page to reduce additional dependencies of an external CSS3 file.
*   ***Line 74:*** downloads our JQuery support.
*   ***Lines 77 to 172:*** is the socket engine on the `www` server. If you remember from Chapter 6, I had an illustration of the WebSocket Protocol. The client-side talks to the Server-side and these are the lines that process those WebSocket commands.
    - ***Line 81:*** creates a new WebSocket object using the URL.
    - ***Line 84:*** creates the new client-side socket and connects it to the MMoG App Server URL. You will need to substitute your own URL in place of mine.
    - ***Line 90 to 93:*** is the standard `onopen` command from Chapter 6.
    - ***Line 95 to 120:*** is the standard `onmessage` command from Chapter 6\. is chat work-horse. It captures information as assigns them to variables. Displays the new information in the display textbox with an associated color per user, and then dutifully broadcasts the new information.
    - ***Line 122:*** is the standard `onerror` command from Chapter 6.
    - ***Line 124:*** is the standard `onclose` command from Chapter 6.
*   ***Lines 173 to 201:*** are HTML tags for client’s browser.

***Summary:*** This kind of socket activity represents a `CLIENT`. So, in the above example, we saw how to:

1.  Create a socket
2.  Connect to remote server
3.  Send some data
4.  Receive a reply

It’s useful to know that your web browser also does the same work-flow if you open a browser connection to a website such as www.google.com. The other kind of socket activity is called a `SERVER` which we’ll cover next.

### Review `demo/server.php` Content

This file is the socket server middleware which replaces `ExpressJS`. This opens the server-side conduit. We now have an end-to-end, bi-directional, WebSocket, communications pipe. At this level of connection, there is no meaningful technical distinction between client and server anymore. Both the browser and the server are equal peers, where each can request and push information as needed. While the establishment of a WebSocket connection leverages the old roles in the request and response model, the connection itself is not restricted by these anymore.

The WebSocket server works in similar ways as a WebSocket client. It responds to events and performs actions. Regardless of the middleware programming language you select, **every WebSocket server performs specific actions.** It is initialized to a WebSocket URL address, it handles `OnOpen`, `OnClose` and `OnMessage` events, and returns or pushes messages to the end clients. The Server-side MMoG App has several important responsibilities while processing our game and/or client-side proxy server which we’ll study shortly:

1.  Opens a server-side WebSocket.
2.  Binds to an address and port.
3.  Persistently listens for any incoming connections. First and foremost, our MMoG App server must listen continually for incoming connection requests. This won’t be a typical “PHP” web page —or whatever you chose for ***“middleware engine”*** on your server— since those pages “time-out” after a default setting of 30 seconds. It must be a back-ground ***“daemon process”*** — A long-running background process that answers requests for services. Review Chapter 4.8 Server-less Alternatives and likely ISP hosting services (IaaS, PaaS, [***Linux Containers***](http://gose-internet-services.net/openvz-vps-2/))
4.  Processes, acknowledges, closes and updates gamer connections who quit or are newly arriving into the current gaming session(s). Security might be an issue here; so we should test the `origins` of the request. Our MMoG App must respond to only authorized WebSocket handshake request — especially if you are using services that charge you for usage — Review Chapter 4.8 Server-less Alternatives … ***“dyno pool at $7 per dyno”.***
5.  Reads incoming Game Turn Orders (GTO), extract GTO information from incoming WebSocket frames, keep track of client activities, record the current game state, access permanent database storage, insert new records, update existing records [***(ACID or BASE)***](https://www.dataversity.net/acid-vs-base-the-shifting-ph-of-database-transaction-processing/) and finally send Game Turn Results (GTR) to current active participants. (See Game Rules for Legends of Renown Deeds for various commands.)
6.  Manage “Pings and Pongs” and adjust timing concerning network latency.
7.  … and potentially support any sub-protocols or extensions we might create.

The following sample copy of [http://mmog.pbmcube.net/index.php](http://mmog.pbmcube.net/index.php) uses the bare minimum WebSocket protocol and gives simplistic **echo** responses. Although this following example look intimidating, you can download a more succinct version from here: [***PHP WebSocket Server***](http://www.abrandao.com/lab/websocket/ws.zip)

To run such a PHP page, you need access to your server’s command line and start the server with this command:

***Download this 4-page file from your Bonus Content [http://makingbrowsergames.com/mmog/bonusContent/_server.pdf](http://makingbrowsergames.com/mmog/bonusContent/_server.pdf)***

*   Line 1: uses `PHP7` to run this file.
*   Line 2: starts the `PHP` script tag.
*   Line 3 to 5: provides configuration information for the server-side WebSocket Connection.
*   Line 8 Creates a WebSocket with these properties.
    - Address Family: AF_INET (this is IP addressing version 4)
    - Type: SOCK_STREAM (means this will be a TCP protocol connection). If SOCK_DGRAM were used, it would indicate the use of UDP protocol. The concept of “connections” applies to SOCK_STREAM/TCP type of sockets. Connection means a reliable “stream” of data such that there can be multiple such streams each having communication of its own. Think of this as a pipe which is not interfered by other data. Other sockets like UDP, ICMP, ARP don’t have a concept of “connection”. These are non-connection-based communication. Which means you keep sending or receiving packets from anybody and everybody.
    - Protocol: 0 (or IPPROTO_IP for the IP protocol)
*   Line 11: set options for WebSocket management. See [***socket-set-option***](http://php.net/manual/en/function.socket-set-option.php)
*   Line 14: binds IP to Socket. By doing this, we ensure all incoming requests on this port are received by this our MMoG App. It obvious that you cannot have 2 sockets bound to the same port. There are exceptions to this rule but we that’s for advanced system architecture.
*   Line 17: opens persistent listener on that selected port. We could use a second parameter for the function `socket_listen` is called backlog. It controls the number of incoming connections that are kept “waiting” if the program is already busy. So if we specified 10, it means that if 10 connections would be queued up for processing. If 11th connection request came, it would be rejected.
*   Line 20: Builds and simple array list of client connections. (Socket.IO would add `namespaces` at this point and **does not** guarantee ordered delivery.) We will use other data structure combinations that would provide a lobby with tables or rooms for each active game session.
*   Line 23 to 95: keeps our Socket Server alive. If this loop stops then our game MMoG has crashed.
*   Line 98: Closes that gamer’s connected sockets.
*   Lines 100 to 183: are annotated and described, in detail, the purpose of each function block. These lines will begin to hold our game logic and processing in the next chapter.
*   ***Line 180: TODO you must insert your `MMoG App Server` file name and assigned port number here.***

## 7.3 Where’s Phaser!?

***AH! I knew you’d come to this sooner or later!*** (still scarey! Right?) Phaser is simply an ***HTML canvas tag*** inside of a Layer-7 HTML5 page — as sad as that sounds — ***it’s nothing more!*** The next chapter shows how I’m working with Phaser v2.x.x **and/or v3.16+** as I replace my entire [Flash game inventory.](http://renown-games.com/) using [OLOO coding style](https://medium.com/@SunnyB/javascript-prototypal-inheritance-constructors-vs-oloo-d90c482aaa55) — moving away from classical OOP in JavaScript [***“Towards Delegation-Oriented Design”***](https://github.com/getify/You-Dont-Know-JS/blob/master/this%20&%20object%20prototypes/ch6.md#delegation-theory) and [***Game Prototyping.***](http://makingbrowsergames.com/book/)

Take a step back and review Chapter 6 and this chapter again and you will discover that Phaser handles everything in the gamer’s `canvas` tag as a ***Smart (thick) client.*** Using clever web-page development you have some choices.

1.  Use the buttons from this project externally — placed outside of the Phaser `canvas` as standard CSS, HTML and JavaScript. ***OR***
2.  Have GUIs inside the Phaser `canvas` talking to [***“hidden Shadow DOM”***](https://glazkov.com/2011/01/14/what-the-heck-is-shadow-dom/) elements and those elements then provide the WebSocket data exchange. This is only possible with Phaser III.17+ (released 20190510) new DOM element. We can now include html content, using load.html and load.css, inside the Phaser game canvas. The DOM element will either appear above or below the canvas. Read more about this feature in [***Newletter #146***](https://madmimi.com/p/e86d4e?pact=1037815-151147935-9209877774-2b30c02c98c3a773dd94f39d3352b53d3df0cc21) ***OR***
3.  If you are using either Phaser v2.6.2, CE, or v3.16+, another option is to use WebSockets for transferring other game assets. ***You could also elect to download JS script files!*** Phaser uses these JavaScript files immediately — a cool feature of v2.x.x that’s currently ***NOT available in any pre-v3.15+ (but just recently available in v3.16.1 after 20180205).*** You could activate new v3.16.x scenes **tailored for specific gamers (i.e., guests vs. members/patrons)** in much the same way through the [***“Progressive Enhancements”***](https://en.wikipedia.org/wiki/Progressive_enhancement) concept.
4.  Both Phaser v2.x.x and v3.x.x support JSON — required to drive any JSON-RPC requests and responses. Therefore, you might elect to transfer JSON game updates, data, game phases, and configurations. The advantage you gain is the duplex transmissions, and the server-side push of new updates. ***OR***
5.  Take a “non-traditional” approach in using Phaser. Let’s explore this concept next.

## 7.4 Extending Our Operations

This is fairly exciting. You now have a functional chat server using WebSockets. Wait! Before you start [***poo hoo***](https://uk.answers.yahoo.com/question/index?qid=20070101055537AALMVHy&guccounter=1)-ing a chat server; realize that a chat server is sending messages to and from a server. Its operations are similar to any MMoG sending and receiving `Game Turn Orders` (GTO — messages to the server) and returning `Game Turn Results` (GTR — messages to the gamer) — similar to publish and subscribe — from each of the gamers and broadcasting those updates to all in the game.

However at this point, ***it’s still just a “working proof of concept”.*** Our MMoG still needs several supporting features to manage a MMoG; for example:

1.  A “lobby” for gamers to meet and hook-up. (review Part II: Doctor Office or Shopping Mall?) See the various examples in Part IV.
2.  A leader board to announce current scores.
3.  Separate areas for “patron members”, “guests”, and [***“lurkers”***](https://en.wikipedia.org/wiki/Lurker) by using [***“Progressive Enhancements”***](https://en.wikipedia.org/wiki/Progressive_enhancement)
4.  A player’s Matching service.
5.  An avatar creation/generation area.
6.  and a pre-game launch area for last minute adjustments if your game design requires such a feature.

![](resources/makingbrowsergames_com---book---imagesConsolidated---charEdit.jpg)

Character Creations Lobby

I’m certain you have more ideas. Reviewing these MMoG features, you noticed that they have nothing to do with the “actual game play” — where the Phaser game `canvas` lives. All of these are just supporting game services surrounding the “actual game play”. What I’m suggesting is a Content Management System (CMS).

### Deeper Dive: The CMS Game Shell

A `game shell` is merely a simple method toward building a [***Progressive Web App (PWA)***](https://developers.google.com/web/progressive-web-apps/) that reliably and instantly loads game content, similar to what you would see in native mobile applications.

The `game shell` is the minimal required technologies of HTML, CSS and JS to display the game’s interface. When it is cached offline, it ensures instant, reliably good performance to gamers in their returning gaming sessions. The network provides the newest or updated gaming content and assets.

For games — “a single web-page application with heavy JavaScript architectures” — using a `game shell` is [***“THE go-to approach”.***](https://hbr.org/2016/06/the-go-to-market-approach-startups-need-to-adopt) The `game shell` approach relies on aggressively caching the `shell` content using a [***service worker***](https://developers.google.com/web/fundamentals/primers/service-worker/) to get the game up and running. Next, the dynamic game content and assets loads for each ***game phase (aka roses).*** The secret sauce a game shell provides is: ***Getting the initial HTML to the user’s device and displayed without the anything from the network!***

In other words, the `game shell` is similar to the code you’d publish to any “app store” when building a native mobile app. The `game shell` is a ***skeleton (aka Bare Bones Prototypes)*** of your game’s user interface (`UI`) and all those prototype components necessary to launch your game from the ground up … but doesn’t include the game “data logic.”

### Deeper Dive: When to use the game shell model

Building a PWA does not mean starting from scratch. If you are building a modern single-page app, then you are probably using something similar to a `game shell` already whether you call it that or not. The details might vary a bit depending upon which gaming libraries or frameworks you are using, but ***the concept itself is framework agnostic!***

The `game shell` architecture makes the most sense for ***any game project*** with relatively unchanging navigation but changing internal content — ***the `canvas`!*** A number of modern JavaScript Gaming Frameworks and libraries already encourage splitting your game logic from its content (aka “Separation of Concerns”), making this `game shell` design appealing. For certain types of games —that only have static content— you can still follow the same idea but the game’s `canvas` tag becomes 100% of the `game shell` — this is the majority of published `Phaser v2.x.x` games and single-page games described earlier; they use a single static `canvas` tag and “within it are the various game ***“roses”*** (aka menus, parts, phases, sections, stages, states, scenes, screens, [***thingies, dumaflache,***](https://www.urbandictionary.com/define.php?term=dumaflache) or [***“Ardvarks!”***](https://en.wikipedia.org/wiki/Aardvark)).” — Quoted from [***Phaser III Game Prototyping page 78.***](https://leanpub.com/phaser3gameprototyping)

The benefits of using this `game shell` architecture and a [***service worker***](https://developers.google.com/web/fundamentals/primers/service-worker/) are:

*   Reliable performance that is consistently fast across all your game projects. Repeat visits are extremely quick. Static assets and the UI (e.g. HTML, JavaScript, images and CSS) are cached on the first visit so that they load instantly on repeat visits. Content may be cached on the first visit, but is typically loaded as needed — “just in time!”
*   Native-like interactions. By adopting a game shell model, you can create experiences with instant, native-application-like navigation and interactions, complete with offline support.
*   Economical use of game assets. Design for minimal resource usage. Be judicious in what you immediately cache because loading non-essential files (i.e., large images that aren’t shown on every page) will result in browsers downloading more game assets than is used immediately. Even though WAN bandwidth is available in western countries, this may not be the case in emerging game markets where connectivity is expensive and data is costly.

## 7.5 CMS — Server-side Frameworks

![](resources/www_valuecoders_com---blog---wp-content---uploads---2016---01---php-market-share.png)

PHP development frameworks

Content Management Systems (CMS) is the topic of this section. We have focused on Phaser as a single web page, but what if we created a MMoG that was a “game-shell” and packages multiple individual games inside it? How would we manage handing-off the gamer into a subordinate-game and then return them back to the game-shell canvas? If you are familiar with Bulletin Board Systems (BBS) “Door Games”, then you quickly see my direction. For those who are not familiar, please indulge my following explanation.

Nearly every book on Phaser demonstrates how to create a “single page / web application” (SPWA) — a game in which a single player modifies the game state. ***If you are building an “alternating Turn-based” multi-player game such as chess or checkers, then your job becomes to simply create a “SPWA”.*** Single-page applications are more application-like because they reject the more typical web paradigm of moving between distinct pages with different URLs as a Content Management System might. Phaser contains everything inside the `canvas` tag — the main menu, the settings, the credits, the score board, [***the kitchen sink!***](https://idioms.thefreedictionary.com/everything+but+the+kitchen+sink) I call this “the Phaser Traditional Method” — a canvas game using a linear sequence that contains the game play and supporting services:

What if we broke that sequence into a “tree hierarchy”? Meaning that the Main Menu is an altogether ***separate canvas page, or HTML `<div>`*** (the tree trunk) than its individual game components (tree branches where our gamers play or interact)? This is a feature of **Phaser3** and its re-organization from “states” to “scenes”. If you’re a former Flash Developer, think of the new **Phaser3 Scenes** as if it were a **Flash MovieClip.** We would need a Content Management System (CMS) for this type of game structure. Building our game in this manner also permits us to easily convert it into [***“Android Intents”***](https://acadgild.com/blog/intent-in-android-introduction) and further extend it into multi-player mode.

![](resources/makingbrowsergames_com---book---imagesConsolidated---nonTraditional.png)

Content Management System as a Game

Each gamer would have a Phaser canvas page of the active game they are playing. The MMoG server would present a Game Lobby as the “Main Menu” for the players to choose which game they want to enter — “Shopping Mall”-style not “Doctor’s Office. Record which JS modules are used in the Single Game Flow above and then compare where those JS modules are located in a MMoG environment. The biggest impact is whether the gamers will use a `Smart (thick Phaser)` or `Dumb (thin Phaser)` client and what role the server will use to manage the active games.

### Index Page (Non-Traditional Method)

I prefer [***CodeIgniter***](https://www.codeigniter.com/) as my CMS because I can create my MMoG application AND surrounding CMS content — [***compare Codeigniter to Joomla (and other CMS) here.***](http://vschart.com/compare/codeigniter/vs/joomla) There are other CMS’es you might like (i.e., the CodeIgniter **FREE OPEN SOURCE GUI version** of called [***Express Engine,***](https://docs.expressionengine.com/latest/getting-started/ten-minute-primer.html) or perhaps [***Pico,***](http://picocms.org/) [***Grav,***](https://getgrav.org/) [***GetSimple CMS***](https://en.wikipedia.org/wiki/GetSimple_CMS)) or consider digressing to [***WordPress (ewe!!)***](https://en.oxforddictionaries.com/explore/words-that-sound-like-the-thing-they-describe/) and its popular extensions and vulnerabilities. [***(side-trip to English Onomatopoeia)***](https://englishlive.ef.com/blog/language-lab/whizz-bang-guide-onomatopoeia-use/) Consider that the Phaser `canvas` is merely a single web page or HTML `<div>`, and the CMS is the over-arching umbrella that permits access and supporting gaming services. You can review [samples on how I use CodeIgniter here](http://renown-quests.com/) or on any of my current mobile gaming sites below — ***NOTE:*** CodeIgniter 2.x and 3.x completely supports **XML-RPC;** review [***their source code and examples here.***](https://www.civil.iitb.ac.in/~t6vivin/user_guide/libraries/xmlrpc.html)

*   [***Blood Pit™***](http://www.adventurers-of-renown.com/quests/arbp.php) — an “In-Game Module” (IGM) quest for the Adventurers of Renown™ Gaming System. Game Rule-book and License available in Part IV.
*   [***Rogue Prince™***](http://www.adventurers-of-renown.com/quests/arrp.php) — an “In-Game Module” (IGM) and “Gateway Module” into the Rulers of Renown™ Gaming System.
*   [***Ruins of Able-Wyvern™***](http://www.adventurers-of-renown.com/quests/arra.php) — an “In-Game Module” (IGM) for the Adventurers of Renown™ Gaming System. Game Rule-book and License available in Part IV.
*   [***Rulers of Renown: The Emancipation™***](http://www.adventurers-of-renown.com/quests/rrte.php) — a “Gateway Module” into the Rulers of Renown™ Gaming System.
*   [***Soldiers Test™***](http://www.adventurers-of-renown.com/quests/arst.php) — an “In-Game Module” (IGM) for the Adventurers of Renown™ Gaming System.
*   [***Legends of Renown Deeds™***](http://legends-of-renown-deeds.com/) — an expanded campaign for the Adventurers of Renown™ Gaming System.

Notice that the “indices” are “.php” middleware pages (which replaces Express.js), and are ***dynamically executed*** from the server-side — ***we are sooooo close to a multi-player construction. Can ya smell it??*** The advantage I gain by using a CMS is common templates per dynamically generated body content with standardized **`<header>` and `<footer>`** content. I could go a step further using [***“Progressive Enhancements”***](https://en.wikipedia.org/wiki/Progressive_enhancement) by simply using different **`<header>`** files for “patron members”, “guests” and “lurkers” (see “index” below).

![](resources/makingbrowsergames_com---book---imagesConsolidated---static-site-nunjucks-image2.jpg)

Common header and footers on Front-end User

```
 1     session_start ();   //starts a php session  
 2     
 3     class Areas extends CI_Controller {
 4     
 5         public function __construct() {
 6             parent::__construct();
 7             $this->load->helper(array('admintools','html','form', 'url'));
 8             $this->load->library('form_validation');
 9             //$this->load->library('session');
10             $this->load->library('user_agent');
11             session_start ();
12         }
13         public function index() {   // creates the index page  
14     
15             $data['title'] = 'The Blood Pit';  
16             $data['affiliate_name'] = AFFILIATE_NAME;  
17             $data['affiliate_code'] = AFFILIATE_CODE;  
18     
19             if($version === "rv_15" && $this->agent->is_browser()){
20                 $this->load->view('templates/header2', $data);
21                 $this->load->view('areas/index',$data);
22                 $this->load->view('templates/footer2',$data);
23             }  
24             //  mobile is a Single Web Page App (SWPA);  
25             //  1 room = 1 page <div> tag  
26             if(($version === "rv_15" ||  
27                 $version === "rv_5") &&  
28                 $this->agent->is_mobile())  
29             {  
30                 $this->load->view('templates/header', $data);
31                 $this->load->view('areas/index',$data);
32                 $this->load->view('templates/footer',$data);
33             }
34      . . . . . 
```

CodeIgniter auto loading libraries

Notice that I selectively choose which page to show based on the browser agent (desktop or mobile) and game version released.

## 7.6 CodeIgniter / Phaser Integrated CMS

We are using a recent CodeIgniter stable release v3.1.10 (Jan 16, 2019), since CodeIgniter 2.x version tree was discontinued 31 October 2015\. CodeIgniter project is supported by Yeoman which facilitates rapid project creation or you could take the [***more traditional approach***](http://www.codeigniter.com/user_guide/installation/index.html). If this is your first exposure to CodeIgniter, you might like to review [***“the broad concepts behind CodeIgniter”***](http://www.codeigniter.com/user_guide/overview/index.html) or quickly create a [***“practice project”***](http://www.codeigniter.com/user_guide/tutorial/index.html).

We will scaffold our CodeIgniter **(CI)** as a simple download of version 3.1.10\. If you prefer, you could use Yeoman to build this **CI** project for you. I recommend either:

*   [***RobonKey***](https://www.npmjs.com/package/generator-robonkey) offers several flavors of CMS ([***Express for NodeJS***](http://expressjs.com/), WordPress, Drupal, ***CodeIgniter,*** or ***Laravel*** sub-generators).
*   [***“CI3 Fire Starter”***](https://github.com/JasonBaier/ci3-fire-starter) — a CodeIgniter3 skeleton application that includes jQuery and Twitter Bootstrap. It is intended to be lightweight, minimalistic and [***unobtrusive.***](https://www.collinsdictionary.com/us/dictionary/english/unobtrusive) Also for your convenience, it was created for developers new to the CodeIgniter (CI) framework who want a simple, easy platform for learning the CI framework. My mind “gets stoked” when I see excellent work as his.

Our migration plan is to let CodeIgniter handle all the navigation to and between (aka [***“routing”***](https://www.codeigniter.com/userguide3/general/routing.html); a process similar to [***REST or RPC demonstrated here***](https://www.guru99.com/codeigniter-url-routing.html). See Part IV for step-by-step instructions) for the various Phaser-content pages while letting Phaser Gaming Framework (either version!) concentrate its efforts on the current single-canvas displayed as a “thick client”; and furthermore, use the Phaser internal function `game.add.script`. Why? Because the content delivered to the gamer does NOT reveal any specific state changes; those state changes remain on the server and invisibly inside of CodeIgniter. We can dynamically generate pages and select which Phaser modules to send; and, the delivered JavaScript files through `game.add.script` are dynamically generated only for that current gaming session’s page. In short, a drastic increase in asset protection and overall game security.

```
1     script(
2         key,            //Unique name for this script file.  
3         url,            //file URL. If undefined or null  
4                         // the url will be set to <key>.js,  
5                         // i.e. if key was "alien" then   
6                         // the URL will be "alien.js".  
7         callback,       //called after the script is loaded  
8         callbackContext // loader context  
9     ) 
```

Dynamically adjust game-play using the script feature.

```
175     /**  
176      * api_key  
177      *  
178      * @access  public  
179      * @author  Phil Sturgeon  
180      * @version 1.0  
181      */  
182     public function api_key($key, $name = FALSE) {  
183         $this->api_key  = $key;  
184         
185         if ($name !== FALSE) {  
186             $this->api_name = $name;  
187         }  
188     
189     } 
```

CodeIgniter REST Server API.

### High Score Services

You have several options when storing game information as a [***“non-invasive cross-cut concern”;***](https://web.archive.org/web/20141220201722/http://html5hub.com/oop-is-not-your-hammer/) you may store game scores and progress locally on the gamer’s device or remotely on your database server/service. Below is some generic client-side script you will need for you “High Score” Menu.

```
 1     //create a data structure to hold high scores  
 2     var highScores = [];  
 3     //create a data structure to track ranking  
 4     var hsPosition =[10,9,8,7,6,5,4,3,2,1];  
 5     //create a data structure to remote/local storage  
 6     var dbURL;  
 7   
 8     //create a high score function  
 9     BasicGame.HighScores = function(){};  
10     BasicGame.HighScores.prototype = {  
11     preload: function(){},  
12     create: function(){  
13         //link to your storage  
14         //dbURL = new ("<where is your database?>");  
15   
16         for(var i = 1; 1< 11; i++){  
17         hsPosition = game.add.text(x,y + (i + 50),i+". "+ hsPosition[i]],  
18             {fonSize:"40ps"}.anchor.serTo(1,0);  
19         }  
20   
21         //dbURL api to pull remote/local data records  
22     }  
23     //CRUD  
24     updateHSPosition: function(){  
25         for(var i = 1; 1< 11; i++){  
26             hsPosition[i].text = hsPosition[i];  
27         }  
28     }  
29   
30     } 
```

[http://makingbrowsergames.com/mmog/bonusContent/back-endServices.zip](http://makingbrowsergames.com/mmog/bonusContent/back-endServices.zip)

### Membership Login

This is a tricky topic. Some distribution channels forbid this, others allow it ***only IF*** you use their software development kits (SDK). If you plan to authenticate members, you may want to consider [***Two way authentication and encryption with CodeIgniter XML-RPC***](https://www.exoiz.com/xmlrpc)

The new GDPR rules are now in effect (as of 25 May 2018), and they put a damper on much that was. I strongly recommend reviewing the content in the [***Security Appendix,***](http://makingbrowsergames.com/book/Appendix-Security.pdf) and the items that are now required by “International Law”.

## 7.7 Back-end Administration

We have focused on the front-end user experience, and have avoided the back-end game administration. Why? because with CodeIgniter many clever options are already available. In fact, with some clever integration these recommended CodeIgniter CMS back-end could help manage the gamer’s front-end displays. Research some of my favorites:

*   [***FuelCMS***](https://www.getfuelcms.com/)
*   [***CSZ-CMS (demo site)***](https://demoapp.cszcms.com/)
*   [***Forgeigniter***](http://www.forgeigniter.com/)
*   [***CI3 Fire Starter***](http://jasonbaier.github.io/ci3-fire-starter/)
*   [***Bonfire***](https://cibonfire.com/) and [***sprintphp***](https://github.com/lonnieezell/sprintphp)
*   [***Project-CodeIgniter-CMS***](https://github.com/goncaloperes/Project-CodeIgniter-CMS)
*   [***Hoosk***](http://hoosk.org/)
*   [***CodeFight***](http://codefight.org/)
*   [***Ionize***](http://ionizecms.com/)
*   [***DB-less CodeIgniter site***](https://github.com/avenirer/DBless-CI)

## 7.8 Chapter Summary

This was the shortest chapter with the most work to do. Let me summarize.

*   Built a Socket Server Conduit without Socket.IO, Express.js and Node.js.
*   Compared information on various middleware capabilities.
*   Learned the interaction between WWW & MMoG servers.
*   Discovered most Phaser deployment are single-page games.
*   Studied the true software implementation of Phaser JS Gaming Framework.
*   Developed various methods to use Phaser integration with MMoG.
*   Reviewed the “non-traditional” approach to deploy Phaser.
*   Learned to extend MMoG with gaming services.
*   Debated whether Phaser could support various gaming services.
*   Examined several MMoG use of Content Management.
*   Created a High Score service.
*   Discovered various storage options.
*   Became aware of legal requirements for privileged user access.

## 7.9 Chapter References

*   [***FREE online Course: APIs 101***](http://www.tbcube.com/course-catalog/degree/ceu/apis101/)
*   [***A guide to designing the perfect API***](https://www.mulesoft.com/lp/ebook/api/restbook)
*   [***FREE Book: PHP The Right Way!***](https://leanpub.com/phptherightway)
*   [***Play Framework***](https://en.wikipedia.org/wiki/Play_Framework) and [***SDK***](https://www.playframework.com/)
*   [***A Developer’s Guide To Blockchain and Cryptocurrency***](http://www.tbcube.com/course-catalog/degree/ceu/a-developers-guide-to-blockchain-and-cryptocurrency/)
*   [***Build APIs You Won’t Hate: Second Edition***](https://leanpub.com/build-apis-you-wont-hate-2)
*   [***Surviving Other People’s Web APIs***](https://leanpub.com/surviving-other-peoples-web-apis)
*   [***PHP Standards Recommendations (PSR)***](https://www.php-fig.org/psr/)

# 8 MMoG App API Engine

This chapter begins to fill our ***`MMoG App Server`*** with various game commands and supporting services. It becomes our [***“Web API”***](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction) — our MMoG’s private(? unless we want to rent, lease, or open it to the public). If this is your eventual development roadmap, you should consider using [***OpenAPI (formerly known as the Swagger Specification)***](https://www.openapis.org/)) interface driving your application which allows specific access to a subset of functionality and data processed by it. In Part IV, we’ll start encoding simple 2-Player game, and then extend what we learned into a “full-Monty” MMoG. ***Documentation is paramount as you construct your Web API.*** I advise a quick side-trip to [***“Best Practices in API Design”***](https://swagger.io/resources/articles/best-practices-in-api-design/) and [***RAML website.***](https://raml.org/projects) Skim through their advice and tools; it will help as we build our MMoG APIs. The coding style will be [***“Objects Linking to Other Objects (OLOO)”***](http://akonwi.io/blog/oloo) to simplify the MMoG construction and remove all the [***“cruft of classical OOP”.***](https://en.wikipedia.org/wiki/Cruft) Writing a ***`MMoG`*** is difficult enough; OLOO [***cuts out the middleman***](https://stackoverflow.com/questions/29788181/kyle-simpsons-oloo-pattern-vs-prototype-design-pattern) and provides us with “a cleaner code-base” and more optimized construction. Kyle Simpson illustrate what I’m doing [***in this article — JS Objects: De”construct”ion.***](https://davidwalsh.name/javascript-objects-deconstruction)

Search for the ***“TODO”*** comments in the source code. These are places where you must consider or modify for your bespoke MMoG project. I have created a “code toggle” (don’t know what else to call it!) to help us while we are developing. When it is “turned on”, we’re in development mode; when it is “off” we’re in live production mode.

The MMoG App Engine Server is a really a broad term for several internal software components. The unique challenge developing a “real-time Multi-Player networked game” is the definition terms: ***“real-time,” “Multi-Player,” “network programming.”*** In other words, if removing just one of these phrases reduces the complexity we face in MMoG development substantially. For a MMoG, designed to be turn-based (i.e., chess; See Part IV), or games in which only a single player is actively modifying the game session data at any given time (i.e., poker or the hundreds of games claiming MMoG status), **network latency is not an issue.** Creating such games, in reality, is no different than simply creating a [***Progressive Web Application (PWA).***](https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/) (See Part IV and MDN article: [***Making PWAs work offline with Service workers***](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Offline_Service_workers))

## 8.1 Building a MMoG App APIs

This is the core of our Multi-Player game. By now, you should have a clear idea **“What”** the client browser will collect and render, and **“How”** the client packages input and sends GTO to either its “local proxy-server” or the remote “centralized authoritative server” — in short, the [***fundamental parts of an API.***](https://medium.com/@perrysetgo/what-exactly-is-an-api-69f36968a41f) We need, for now, to finalize a list of all those **“whats” and “hows”** on both our client- and server-sides. Review Chapter 5.4 Construction Sequence and Regimen and Part IV Walk-through Tutorials. Tools are available, such as the [***Swagger Editor***](https://swagger.io/tools/swagger-editor/), and the [***Swagger Codegen***](https://swagger.io/tools/swagger-codegen/) or [***RAML’s API Designer***](https://github.com/mulesoft/api-designer), [***RAML’s API Workbench***](http://apiworkbench.com/) and [***their tutorials***](https://raml.org/developers/raml-100-tutorial) will save your time and **automate your MMoG API construction** process. The [***Swagger Inspector***](https://swagger.io/tools/swagger-inspector/) is an online testing tool — similar to the one provided in [***Bonus Content here***](http://makingbrowsergames.com/mmog/bonusContent/CI-3.1.10-MMoG-REST/index.php/rest-server) — you could use to troubleshoot your MMoG API in greater depth.

*   Client: APIs which provide the full range of features available to the gamers — authentication, account and data management, inventory, friends, matchmaking, reporting, and platform-specific functionality. Remember the list you created in Part I Chapter 3?? That list will grow! But for now, let’s just do a few test items on the client.
*   Server: Provides functionality to allow external (developer-controlled) servers to interact with user inventories and data in a trusted manner, and to handle matchmaking and client connection orchestration.

The server doesn’t have to be complicated. We must decide whether we’re following ***“REST or RPC”*** formatting — either as XML, SOAP or any JSON flavors — for our “how” packets. You see, WebSockets only provide a communications channel(s) (aka a point-to-point conduit). How that “water” flows through the “pipes” is answered by our ***“REST or RPC”*** formatting. The following example uses a ***REST format,*** breaks apart those “how” data packets, then searches through a `switch` statement for a matching command. Use this server file as guidance:

*   ***Rawkets Example: [https://github.com/PBMCube/rawkets/blob/master/server/main.js](https://github.com/PBMCube/rawkets/blob/master/server/main.js)***
*   [***HiveMQ***](https://www.hivemq.com/blog/mqtt-essentials-special-mqtt-over-websockets/) Example: [***“Build your own JavaScript MQTT Web Application”***](https://www.hivemq.com/blog/build-javascript-mqtt-web-application/)

## 8.2 Game Turn Orders

As you’ve read in Part I & II, a gamer can be in one of four gaming states: logged in, connecting, playing the game (active), and logged out. The gamer will send Game Turn Orders (GTO) to the server for processing. The server will return the game turn results (GTR). Both the server and client will have “message packaging” and “unpacking” functions.

### Creating MMoG API Prototypes — 4-Step method

I recommend you think of your game turn orders (GTO) and game turn results (GTR) as ultimate “end-points” destinations within the communications path — your REST or RPC protocols and API specifications — between your subscribing gamers and MMoG App server. This hints at a sequence for writing our MMoG App API source code.

1.  Draft a list of client-side game turn orders (GTO) [***(examples here)***](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs) and the expected game turn results (GTR) of the [***server-side responses.***](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Introduction) This creates “contracts” between client and server.
2.  Then determine **how you will “serialize”** that output into a delivery format. In what formatted data structure will that information use? You have several choices. (i.e., Binary, CSV, JSON, TEXT, XML etc.)
3.  Begin encoding the server-side first so that you have something that will respond to the incoming client-side messages. Part II analyzed the various MMoG Engines and architectures.
4.  Finally, encode your “serializers”; these will become your “contracts” between the client and server as to what is expected from each side of the WebSocket conduit. Yeah, that sounds like the most difficult part in this process; but, I have some surprises for you.

### C2S GTOs Samples

![](resources/makingbrowsergames_com---book---imagesConsolidated---mmogGameLoop.jpg)

Client-side Proxy Server

***Client to Server Game Turn Orders (C2S GTO)*** are generated from the HUDs, menus, newly rewritten Phaser III Input Manager and other interfaces you collect from the gamers’ input; this is valid for either “real-time” or “turn-based” games. My GTOs follow an English grammar syntax of: subject (who), verb (does what actions), direct object (at or upon whom), indirect object (through some agent), adverbs (how the verb’s actions are applied). I format these GTO messages inside the WebSocket frame message with the following suggestions (See ***Deeper Dive: JSON Microdata Format*** below):

*   ***`gID`:*** — automatically generated — which active game Identification played. This is my assigned [***SKU***](https://www.investopedia.com/terms/s/stock-keeping-unit-sku.asp) for my game product.
*   ***`sID`:*** — automatically generated — which active game session Identification group. Earlier I mentioned the “Shopping Mall or Movie Theater” and “game lobby tables” illustrations. This field identifies those unique editions for each “lobby table” (aka group of participants players) within this gaming session.
*   ***`pID`:*** — automatically generated — which active player Identification who generated this command.
*   ***`cID`:*** — automatically generated — which active player character Identification who generated this command. Most MMoG assume one avatar per gamer. I expand on this idea. A gamer could play with a single avatar, or a team of avatars ***in my single-player games*** and ***in my MMoGs,*** a gamer could play with a single avatar, or a team of avatars.
*   ***`dts`:*** — automatically generated — date time-stamp generated. Date is important for “Play By Mail” (PBM aka Postal) games, “Play By eMail” (PBeM) and extended Play By Modem (aka online games). The “dts” is input by each side, and reviewed to calculate network lag. This is critical for “real-time” games. The “dts” for “turn-based” games are critical for only PBM and PBeM games.
*   ***`cmd`:*** — dynamically collected from HUD input — the game turn order **command (cmd)** used on the server-side `switch` statement. This generic field can support either MOM or RPC URLs.
*   ***`obj`:*** — dynamically collected from HUD input — the game turn order command concerning a target object that might receive the commands effects.
*   ***`ido`:*** — dynamically collected from HUD input — the game turn order command concerning an object to an indirect object as needed.

### Deeper Dive: **JSON Microdata Format**

Choosing JSON is my preferred method for “declarative” Game Turn Orders (GTO) and Game Turn Responses (GTR). To open your MMoG App API for other developers to use —i.e.: lease, rent, buy, or subscribe to your back-end CORS Server-side Events (SSE) or as a “Micro-Service” — you might consider the established fomat standards for JSON microdata. Check with ***[https://caniuse.com/#feat=eventsource](https://caniuse.com/#feat=eventsource)*** for current Known Issues. A word of advice, follow the carpenter motto,”Measure twice, cut once”. If you plan to let others use your API then it should be “rock solid” and not change — that’s the reason for “software interfaces”. Research what happens to those who change their API frequently (i.e., every year); in all cases, customer consumers will leave your service.

### Client-side Proxy Server

This is not a new concept; [***Garage Games***](http://www.garagegames.com/products/torque-2d) has been using Proxy-servers in their products [***for decades.***](http://docs.garagegames.com/tgea/official/content/documentation/Engine%20Overview/Networking.html) Now that block-chain gives the the freedom to create Distributed Game App, companies such as [***Enjin***](https://enjincoin.io/) are cornering the new gaming frontiers. We will study how to include a proxy-server in Part IV.

## 8.3 Game Turn Responses

***Server to Client Game Turn Results (S2C GTR)*** are, simply stated, for every command received from a game’s participant, the server will generate a data packet and return it. It is a common “command / response” found in WANs. The server could:

*   keep a virtual data structure of the game status.
*   keep a shadow map of all players’ locations.
*   calculate every combat round narrative details (blow by blow or key-press).
*   **OR none of the above!** If we chose to use a proxy server, then the gamer’s GTOs are broadcasted from each client as a “peer-to-peer” network. Our server would simple accept and record everyone’s information then broadcast a global GTR as confirmation using ***“Server-side Event (SSE)”.*** This should be tailored for each game envisioned. We have several design options at this point. We can have:

1.  a centralized authoritative server that does everything and returns GTRs. ***OR***
2.  a “ghost server” that merely validates the client-side proxy server logic and calculations; then, sends confirmations to all participants about their proxy’s initiatives as ***“Server-side Events (SSE)”.***

Furthermore, **how** our MMoG App responds is heavily dependent upon the server architecture we’ve chosen. Are we using Remote Procedure Calls (RPC) or Message Oriented Middleware (MOM)? We’ve discussed what those are in Part II; it’s now time to take our thoughts, preferences, and begin encoding them.

### Deeper Dive: Real-time MMoG Design

*   [Javascript demo of Server Sent Events SSE (EventSource) tutorial](http://www.abrandao.com/2019/04/html5-eventsource-server-sent-events-tutorial/)
*   [Stream Updates with Server-Sent Events](https://www.html5rocks.com/en/tutorials/eventsource/basics/)
*   [AJAX Push in iOS, Safari, and Chrome with Server-Sent Events](http://blog.samshull.com/2010/10/ajax-push-in-ios-safari-and-chrome-with.html)
*   [MDN Server-sent events](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events)
*   [MDN Using server-sent events](https://developer.mozilla.org/en-US/docs/Web/API/Server-sent_events/Using_server-sent_events)
*   [HTML5 and Server-Sent Events](http://dsheiko.com/weblog/html5-and-server-sent-events)
*   [HTML — Living Standard — Last Updated 7 May 2019, 9.2 Server-sent events](https://html.spec.whatwg.org/multipage/server-sent-events.html#server-sent-events)

### S2C GTRs Samples

*   ***`gID`:*** — automatically generated — which active game Identification played. This is my assigned [***SKU***](https://www.investopedia.com/terms/s/stock-keeping-unit-sku.asp) for my game product. Yes, I’ve been known to have multiple browsers open into different games just to see how others handle incoming messages from a gamer actively play different games.
*   ***`sID`:*** — automatically generated — which active game session Identification group. Earlier I mentioned the “Shopping Mall or Movie Theater” and “game lobby tables” illustrations. This field identifies those unique editions for each “lobby table” (aka group of player participants) within this gaming session. Yes, I been known to sit at “multiple” tables in the same “game room” lobby.
*   ***`pID`:*** — automatically generated — which active player Identification who generated this command. Yes, I been known to enter multiple logon accounts, sit at a game lobby table and play against myself. This is something you find in many MMoG tutorials using Node.js on the local workstations.
*   ***`cID`:*** — automatically generated — which active player character Identification who generated this command. Most MMoG assume one avatar per gamer. I’ve expand on this idea. A gamer could play with a single avatar, or **a team of avatars** in my single-player games. In my MMoGs, a gamer could play with a single avatar, **or a team of their avatars.**
*   ***`sdts`:*** — automatically generated — server date time-stamp generated. Date is important for “Play By Mail” (PBM aka Postal) games, “Play By eMail” (PBeM) and extended Play By Modem (aka online games). The “dts” from the client-side and “sdts” is the server-side date time-stamp that helps calculate network lag at both ends of the WebSocket conduit. Typically, the gamer’s browser will use an Asymmetric [***Digital Subscriber Line (aDSL)***](https://computer.howstuffworks.com/dsl.htm) meaning the upstream is less bandwidth than the downstream. The time-stamps from both the client and server provides enough information to adjust for network induced lag using aDSL. This is critical for “real-time” games. The “dts” for “turn-based” games are critical for only PBM and PBeM games.
*   ***`dts`:*** — automatically generated on the client-side— date time-stamp generated. This value is copied and returned to the gamer. The server records that value (on the server-side) for network delay adjustments for this gamer’s connection. The value is copied and return to the client for its calculations in RTT (round-trip time).
*   ***`gtr`:*** This is the JSON data content results.

***[https://whatis.techtarget.com/reference/Fast-Guide-to-DSL-Digital-Subscriber-Line](https://whatis.techtarget.com/reference/Fast-Guide-to-DSL-Digital-Subscriber-Line)***

## 8.4 Using Horizontal Micro-services

If you’ve followed the “Microservices Architecture Pattern”, we can readily include horizontal services from other online organizations such as [***PlayFab JavaScript SDK (FREE!)***](https://api.playfab.com/sdks/javascript) or any number of [***other gaming back-end micro-services (not so free??!?).***](http://blog.soomla.com/2016/02/top-10-parse-alternatives-game-backend.html) PlayFab JavaScript SDK provides everything you need to access their MMoG API which resembles, in my opinion, the old [***Stendhal Client***](https://stendhalgame.org/wiki/Finding_your_way_around_the_Stendhal_Client_Code) and [***Stendhal Server***](https://stendhalgame.org/wiki/Finding_your_way_around_the_Stendhal_Server_Code) code. This includes models, methods, an HTTP wrapper for sending and receiving web requests and ***JSON serialization.*** If you elected another format, you’ll have some transpiling to do.

![](resources/stendhalgame_org---wiki---images---f---f0---InstallStendhalClient06.png)

The Arianne project started in 1999 and is still going today.

PlayFab further offers [***tutorials,***](https://api.playfab.com/docs/tutorials) guides, [***specifically for Phaser.IO (v2.x.x only!) as a plugin***](https://api.playfab.com/docs/tutorials/landing-players/phaser) , [***“Recipes”***](https://api.playfab.com/docs/tutorials/recipes-index) — examples on how to build popular game mechanics and design patterns using their [***building blocks.***](https://api.playfab.com/docs/tutorials/building-blocks)

***Warning:*** Before you sign-up for PlayFab, look at their “Pricing”. What I’m suggesting is study their code and supporting services **from Github.** ***[https://github.com/PlayFab](https://github.com/PlayFab)*** Then when your game is making **more that $299 per month,** take all your profits and hand it to PlayFab. To be totally honest and transparent, PlayFab CEO explains clearly why you should use their [***“back-end as a service (BaaS) in this article.***](https://www.quora.com/Who-are-the-competitors-to-PlayFab-Inc-the-BaaS-for-games) After reading his article, you’ll realize that you are hiring PlayFab as external contractors for your [***virtual business***](https://en.wikipedia.org/wiki/Virtual_business) supporting your BaaS at a significant discount. Here’s what you have ***with a free developer’s account:***

*   ***Player profiles:*** this is something easy constructed from what we’ve studied thus far.
*   ***Content management:*** yes, theirs is impressive; but not any more than those Content Management Systems (CMS) offered from [**CI3 Fire Starter,**](https://github.com/JasonBaier/ci3-fire-starter) [***PICO,***](http://picocms.org/) [**GetSimple CMS,**](http://get-simple.info/getsimple/?sa_shf=1) or [***Grav.***](https://getgrav.org/)
*   ***In-game commerce:*** again, this is feature that has nothing to do with any game core mechanics. We can adopt anyone from anywhere. In fact, we might take these first three bullet points and elect to consolidate them into WordPress(? — just kidding).
*   ***Real-time Analytics:*** Google Analytics provides this same feature with some configurations.
*   ***Leaderboards:*** this is already provided in the book’s bonus content.
*   ***Receipt validation:*** again, this is a service provided from any eCommerce vendor we elect.
*   ***Custom server logic:*** available from and included in Google Analytics.
*   ***Documentation:*** this is publically available from their website and from their “GitHub.com” ***[https://github.com/PlayFab/JavaScriptSDK](https://github.com/PlayFab/JavaScriptSDK)*** Let’s take a [***“look-see”***](https://www.urbandictionary.com/define.php?term=look-see) shall we? There’s much to learn from how they do their services.
*   ***Forums:*** who’s going to read forum posts(?) — in my opinion, searching forums is like [***“panning for gold”***](https://www.thepennyhoarder.com/make-money/side-gigs/7-places-where-you-can-still-pan-for-gold/) — when I should spend my time encoding my game?? This is a free customer service of questionable quality.

***Step #1.*** Load the PlayFab JavaScript immediately after Phaser library.
***Step #2***. Copy this code into your create() method of “main.js”.

```
 1     // Phaser v2.x.x  
 2     function create() {
 3         game.PlayFab = game.plugins.add(Phaser.Plugin.PlayFab);
 4     }  
 5     
 6     
 7     // Phaser v3.x.x Recommendation 
 8     // http://labs.phaser.io/index.html?dir=plugins/&q=  
 9     
10     class PlayFab extends Phaser.Plugins.BasePlugin {  
11     
12         constructor (pluginManager) {  
13             super(pluginManager);  
14         }  
15     
16     }  
17     
18     var config = {  
19         type:       Phaser.AUTO,  
20         parent:     'phaser-example',  
21         width:      800,  
22         height:     600,  
23         plugins: {  
24             global: [  
25                 { key:     'PlayFab',  
26                   plugin:   PlayFab,  
27                   start:    false,  
28                   mapping: 'test'  
29                 }  
30             ]  
31         },  
32         scene: {  
33             preload:    preload,  
34             create:     create  
35         }  
36     }; 
```

PlayFab Phaser v2.x.x plugin and v3.16+ recommendation

***Step #3.*** Now that you have PlayFab installed as a plugin to phaser, you can set your titleId & make API calls. Below you will see how to login a player:

```
1     //Your title Id from playfab goes here.
2     game.PlayFab.settings.titleId = "D6EC"; 
3     game.PlayFab.ClientApi.LoginWithCustomID({
4         "CustomId":"SomeUniqueIdForYourPlayer",
5         "CreateAccount":true
6     }, function(result){
7         console.log("LoggedIn as " + result.PlayFabId);
8     });
```

Active PlayFab settings

You can access the entire PlayFab service directly via these **REST-like** Web APIs, if you choose not to use their Software Development Kits. For simplicity and security, all function calls are HTTP POST requests over SSL, and all data is formatted as JSON with optional `gzip` encoding.

## 8.5 Modeling from Others MMoG Contributors

We’re not the first to build a MMoG; let’s “stand on the shoulders of Giants” and learn how others approach their development.

1.  IBM Rogue Cloud: See previous chapter 5.
2.  Phaser Quest:
    * Demo Game: [https://phaserquest.herokuapp.com/](https://phaserquest.herokuapp.com/) — uses Heroku (who sits on top of Amazon)!
    * GitHub Source: [https://github.com/Jerenaux/phaserquest](https://github.com/Jerenaux/phaserquest)
3.  Life is Feudal:
    * Shared MMoG [https://lifeisfeudal.com/Main-media/?](https://lifeisfeudal.com/Main-media/?) These guys are the first in the industry to leverage this business model. It is brilliant!
    * Info: [https://lifeisfeudal.com/game-info](https://lifeisfeudal.com/game-info)
4.  Hero Mages:
    * Demo: [http://www.heromages.com/index.html](http://www.heromages.com/index.html)

### Lessons Learned the “Hard-way”

This is a sad section of my book. It is a graveyard of brilliant ideas and games — Github [***has 464***](https://github.com/search?q=multiplayer+game+socket.io) as of 20190302 — that followed (or still attempting to follow) the path of Node / Socket.IO. They chose [***the PaaS path***](https://searchcloudcomputing.techtarget.com/definition/Platform-as-a-Service-PaaS) and ignored the [***Pros and Cons***](https://en.wikipedia.org/wiki/Platform_as_a_service#Advantages_and_disadvantages) in their enthusiasm to create a MMoG and discovered flaws in their deployment and logic only too late. This was one of the [***fundamental “server research”***](https://www.bmc.com/blogs/saas-vs-paas-vs-iaas-whats-the-difference-and-how-to-choose/) we did —(?) I asked you to do. Remember? — in Part I, Chapter 3\. All this could have been avoided if they understood ***the basic ideas given in Part I Chapter 1.***

1\. [https://github.com/InsomniacSabbir/anagrammatix](https://github.com/InsomniacSabbir/anagrammatix) This repository is no longer maintained, and is quite old.

2\. We’ve already studied “Online” (2009-2015; now defunct) from Chapter 5.

3\. [***Tap Tap Adventures (TTA; now deprecated):***](https://web.archive.org/web/20180321101609/http://taptapadventure.com/about.html) — remaining Github [***source code here***](https://github.com/pbmcube/Tap-Tap-Adventure)

- Tap Tap Adventure (TTA) was a massively multi-player online open-source project based on Little Workshop’s 2012 demonstration — [***BrowserQuest (BQ) code here***](https://github.com/mozilla/BrowserQuest) — for HTML5 WebSockets
- BrowserQuest (BQ) comments from TTA (quote) “…is expected to remain **completely open-source,** allowing its community to collaborate and aid in the perfection of the game.”
- [***How TTA does it***](https://web.archive.org/web/20180118073832/http://taptapadventure.com/about.html) (quoted) “… The following GitHub wiki will provide all the essential information gathered by myself over the course of two years as to aid you in improving, expanding, or even creating your own version of Tap Tap Adventure (TTA). Firstly, we must consider the complexity of this source in contrast to that of its predecessor, BrowserQuest (BQ). A lot of things have changed, **we have nearly redone the back-end by using more traditional Object-Oriented Programming Paradigms (OOP) to allow for increased versatility whilst programming.** (editor: Oops! someone should have told them that JS is not OOP) We also stepped aside from the ‘hard-coded’ stigma apparent in BQ, and though it is still evident in some parts of the code, it must be fully transferred to JSON and parsed appropriately.

4.  Phaser MMoRPG (inactive) — A 2d tile-based world built with Phaser framework. GitHub [***source code here.***](https://github.com/PBMCube/phaser-mmorpg/tree/master/js)
5.  ***Want more?!*** Search GitHub for [***MMO (839 JavaScript repositories)***](https://github.com/search?l=JavaScript&o=asc&q=mmo&s=updated&type=Repositories) or [***MMOG (31 JavaScipt repositories***](https://github.com/search?l=JavaScript&o=asc&q=mmog&s=updated&type=Repositories)

## 8.6 Chapter Summary

The field of Multi-Player game networking is huge and has been developing over many years, across various game genres, software architectures, and is now entering the new “Server-less” DevOps age using Blockchain.

## 8.7 Chapter References

Here is a partial list of resources I’ve used while developing our MMoG App for this chapter.

*   [***FREE online Course: APIs 101***](http://www.tbcube.com/course-catalog/degree/ceu/apis101/)
*   [***A guide to designing the perfect API***](https://www.mulesoft.com/lp/ebook/api/restbook)
*   [***FREE Book: PHP The Right Way!***](https://leanpub.com/phptherightway)
*   [***Play Framework***](https://en.wikipedia.org/wiki/Play_Framework) and [***SDK***](https://www.playframework.com/)
*   API University sponsored at [***TB³ — Training By Blackboard, Books & Browsers***](http://tbcube.com)
*   [***PHP Standards Recommendations (PSR)***](https://www.php-fig.org/psr/)
*   [***A Developer’s Guide To Blockchain and Cryptocurrency***](http://www.tbcube.com/course-catalog/degree/ceu/a-developers-guide-to-blockchain-and-cryptocurrency/)
*   [***Microsoft Azure PlayFab Client API***](https://api.playfab.com/documentation/Client#Analytics) — APIs which provide the full range of PlayFab features available to the client - authentication, account and data management, inventory, friends, matchmaking, reporting, and platform-specific functionality
*   [***PlayFab and Phaser.IO integration***](https://api.playfab.com/docs/tutorials/landing-players/phaser) This guide shows, by example, how to setup Phaser.io and get started with PlayFab. Phaser.io is a desktop and mobile HTML5 game framework that PlayFab now supports in our JavaScript SDK. Phaser.io supports plugins, and thus we here at PlayFab thought that it would be useful to the Phaser.io community to have a powerful back-end system that works as a plugin to the Phaser.io v2.x.x engine.
*   [***PlayFab Multi-Player Servers 2.0 (Thunderhead)***](https://api.playfab.com/docs/tutorials/landing-tournaments/multiplayer-servers-2.0) — All PlayFab indie, pro, and enterprise tier customers can access the service and use a limited, free quota of Multi-Player servers for product evaluation and testing. Because we’re still improving the portal experience, samples, and documentation, this service is in a preview mode. During this public preview, if you’re interested in operating the service at production-scale, you will enjoy a 30% discount. The preview period and discount are expected to end in March 2019.
*   [Multi-Player Game Programming: Architecting Networked Game](http://ptgmedia.pearsoncmg.com/images/9780134034300/samplepages/9780134034300.pdf) by Josh Glazer & Sanjay Madhav. A very comprehensive book on all things Multi-Player
*   [Fast-Paced Multi-Player](http://www.gabrielgambetta.com/client-side-prediction-live-demo.html) by Gabriel Gambetta. Describes client-side prediction and interpolation in depth. You’ve seen his online demonstration in previous chapters.
*   [Gaffer on Games](https://gafferongames.com/) by Glenn Fiedler. A series on Game Networking and a series on Networked Physics.
*   [Synchronous RTS Engines and a Tale of Desyncs](https://www.gamasutra.com/view/news/126022/Opinion_Synchronous_RTS_Engines_And_A_Tale_of_Desyncs.php) by Forrest Smith. Articles discussing the Multi-Player architecture of the RTS title Supreme Commander
*   [Source Multi-Player Networking](https://developer.valvesoftware.com/wiki/Source_Multiplayer_Networking) by Valve. A thorough description of Valve’s Source Engine Multi-Player architecture
*   [Latency Compensating Methods in Client/Server In-game Protocol Design and Optimization](https://developer.valvesoftware.com/wiki/Latency_Compensating_Methods_in_Client/Server_In-game_Protocol_Design_and_Optimization) by Value Developer Community.
*   [Time-lines: simplifying the programming of lag compensation for the next generation of networked games](https://link.springer.com/article/10.1007/s00530-012-0271-3) Authors by Cheryl Savery, T. C. Nicholas Graham. In depth discussion of a time-line model for Multi-Player games
*   [http://link.springer.com/article/10.1007/s00530-012-0271-3#Sec17](http://link.springer.com/article/10.1007/s00530-012-0271-3#Sec17)

# Part IV: Step-by-Step Tutorials

This **Bonus Content section** includes proprietary Game Rule Book systems and [***EULA***](http://shop.pbmcube.net/terms-of-use/) source code provided **externally** as a part of your book purchase. See the [***“terms of service” here.***](http://shop.pbmcube.net/terms-of-service/) Your [***registered invoice number***](http://stephen-gose.com/affiliates-program/signup/) becomes your License number. You can learn about further benefits by registering your book invoice number as your license at ***[http://stephen-gose.com/affiliates-program/](http://stephen-gose.com/affiliates-program/)***

Many game developers will attempt to scare you — as you’ve already read from Chapter 1, [***“Indies! Don’t make Multi-Player games!”***](https://www.gamesindustry.biz/articles/2014-05-02-indies-dont-make-multiplayer-games-dan-marshall) — or persuade you to believe, the following.

These four (4) **external “Walk-through Tutorials”** listed below are presented by complexity — “1” being the easiest (elementary skills) to “4” being the most complex (requiring advanced skills across several IT technology disciplines).

[***Blood Pit™***](https://leanpub.com/c/bloodpit-wtts/c/9uLERavhWp7n) — **this FREE external “Walk-Through Tutorial”** (valued at $19.99) guides you in building a single-player game foundation. You must complete that tutorial before starting this next FREE external [**“Walk-Through Tutorial - Blood Pit II™”**](https://leanpub.com/c/wtts-bloodpit2-mmog/c/IW4aa2KfLPo8) (valued at $49.99). The [***FREE game rule book***](https://leanpub.com/tigs/c/f3d6wFdxNdHk) (valued at $19.35) will help “deconstruct” these game mechanics. You just ***SAVED $89.33!*** Blood Pit II™ guides in converting your existing single-player game version into a 2-player game version in the following four (4) steps.

1\. We will study **— “Step-by-Step” — how to migrate this single-player game** into a 2-player online delivery mode (not using “hot-seat”)!

2.  We will study **how to use a dynamic [client-side proxy servers](http://makingbrowsergames.com/mmog/bonusContent/MMoG-API.pdf)** and migrate this game from its current single-player mode (with AI Bot) into an online 2-player mode (not using “hot-seat”)!
3.  We will study **how to include [“Asynchronous Availability”](http://makingbrowsergames.com/mmog/bonusContent/MMoG-API.pdf) during gameplay** and migrate this gameplay mode (and its AI Bot) into an online “Asynchronous Availability” 3-player mode using postal mail or email game turns!
4.  This “Step-by-Step” external tutorial guides us in building ***a complete [MMoG CMS, using MOM](http://makingbrowsergames.com/mmog/#portfolio) over WebSockets, for 2 to 8 participants, a membership system, game lobby, player matching services and other various cloud-based “Back-end as a Services” (BaaS).***

# Appendix

Excellent! You completed this workbook and constructed your game. Still hungry for more? Take some time and review the following resources.

Available Bonus Content as 67-pages of **external downloads.**

*   [***Appendix: Building HTML5 Web Page (3-pages)***](http://makingbrowsergames.com/book/Appendix-buildHTML5webPage.pdf)
*   [***Appendix: Distribution Channels (2-pages)***](http://makingbrowsergames.com/book/Appendix-Channels.pdf)
*   [***Appendix: Game Design Considerations (1-page)***](http://makingbrowsergames.com/book/Appendix-GD.pdf)
*   [***Appendix: Game Design Overview (3-pages)***](http://makingbrowsergames.com/book/Appendix-GameDesignOverview.pdf)
*   [***Appendix: Game Resources and References (17-pages)***](http://makingbrowsergames.com/book/Appendix-Game.pdf)
*   [***Appendix: JS Coding Styles (7-pages)***](http://makingbrowsergames.com/book/Appendix-CodingStyles.pdf)
*   [***Appendix: Networking (9-pages)***](http://makingbrowsergames.com/book/Appendix-Networking.pdf)
*   [***Appendix: Phaser 3 Resources (2-pages)***](http://makingbrowsergames.com/book/Appendix-Phaser3.pdf)
*   [***Appendix: Project Management Analysis (13-pages)***](http://makingbrowsergames.com/book/Appendix-PM.pdf)
*   [***Appendix: Security (5-pages)***](http://makingbrowsergames.com/book/Appendix-Security.pdf)
*   [***Appendix: US Business Start-ups (4-pages)***](http://makingbrowsergames.com/book/Appendix-USBusiness.pdf)
*   **FREE** Phaser III [***Game Developer Course***](https://leanpub.com/c/p3gdc/c/Tx4iHQ6m64c5)

# Appendix: Making Phaser 3D Games!

Refer to the following pioneers who are building 3D Phaser Games.

* https://phaser.io/news/2018/01/making-doom-3d-in-phaser
* [https://github.com/yandeu/enable3d#readme](https://github.com/yandeu/enable3d#readme)
* [https://github.com/photonstorm/phaser/tree/master/plugins/camera3d](https://github.com/photonstorm/phaser/tree/master/plugins/camera3d)
* [http://labs.phaser.io/edit.html?src=src%5Cbugs%5Cextern.js](http://labs.phaser.io/edit.html?src=src%5Cbugs%5Cextern.js)
* [https://phaser.io/news/2019/04/phaser-backer-examples-april](https://phaser.io/news/2019/04/phaser-backer-examples-april)
* [Build fake 3D HTML5 games with Phaser, Arcade physics, three.js and Phaser 3D library](https://www.emanueleferonato.com/2019/11/27/build-fake-3d-html5-games-with-phaser-arcade-physics-three-js-and-phaser-3d-library/) advice from Emanuele Feronato

# Appendix: Phaser Plugins

I highly recommend [***phaser3-rex-notes on GitHub***](https://github.com/rexrainbow/phaser3-rex-notes/tree/master/plugins) and [***Awesome-phaser***](https://github.com/Raiper34/awesome-phaser) as your first couple of stops for any Phaser III plugins. **Also, there is superior documentation located at [https://rexrainbow.github.io/phaser3-rex-notes/docs/site/](https://rexrainbow.github.io/phaser3-rex-notes/docs/site/) Current as of last visit are the Phaser III available plugins: 20181211**

*   actions (Hexagon and Quad grid)
*   audio (fade and midiplayer)
*   behaviors (boid, bullet, 8-directions, fade, flash, interception, moveto, pathfollower, rotateto, scale, ship,textpage, texttyping)
*   board (board, chess,grid, hexagonmap, match, miniboard, monopoly, moveto, pathfinder, shape utils)
*   data (bank, csvtoarray, csvtohashtable, pool, restorabledata)
*   gameobjects (bbocdtext, canvas, containerlite, gridtable, shape, tagtext)
*   geom (hexagon, quad, shombus, utils)
*   input (button, cursoratbound, drag, dragscale, dragspeed, mousewheeltoupdonw, scroller, slider, touchsursor, touchstate, virtualjoystick)
*   loader (awaitloader, webfontloader)
*   logic (achievements, conditionstable, fsm, runcommands, waitevents)
*   math/gashapon (Gashapon.js)
*   shaders (pixelation, swirl)
*   string (lzstring, xor)
*   time (clock, lifetime)
*   utils (… 25 total! in this directory)

# Other resources:

*   [***Phaser FAQ***](https://github.com/samme/phaser3-faq/wiki) ***OR*** [***Phaser Discord***](https://github.com/phaser-discord/community/blob/master/FAQ.md)
*   [***Phaser Plugins (.com)***](https://phaserplugins.com/) 121+ Phaser Plugins (as of 20191001) for either v2.x.x or III.
*   9-slice: **[https://github.com/jdotrjs/phaser3-nineslice](https://github.com/jdotrjs/phaser3-nineslice)**
*   Pathbuilder: **[https://github.com/samid737/phaser3-plugin-pathbuilder](https://github.com/samid737/phaser3-plugin-pathbuilder)**
*   Weapons Plugin: **[https://github.com/16patsle/phaser3-weapon-plugin](https://github.com/16patsle/phaser3-weapon-plugin)**
*   [**Phaser 3 Ninepatch Plugin**](https://github.com/koreezgames/phaser3-ninepatch-plugin) — Phaser3 Nine Patch plugin adds 9-slice scaling support to Phaser 3 by KoreezGames
*   [**Generic Platformer and Phaser Bootstrap Project**](https://github.com/nkholski/phaser3-es6-webpack) — Generic platformer and Phaser 3 bootstrap project

# Selling your Game Assets

*   [***Game Developer’s Market***](https://www.gamedevmarket.net/?ally=GVgAVsoJ) — GameDev Market (GDM) is a community-driven marketplace based in the UK that connects indie game developers with talented asset creators. There are asset stores specific to certain game engines, huge generic stock websites with an overwhelming catalog of assets of varying quality and smaller indie stores with small selections of very niche assets.
*   [***Creative Market***](https://creativemarket.com/?u=PBMCube) — is the world’s marketplace for design. Bring your creative projects to life with ready-to-use design assets from independent creators around the world. ***Sell your game assets.***
# Your own WhatsApp

- Intro
  - Hi! I'm Andrei and I'll be your host on this whirlwind journey trough software development.
  - I have to admit that this workshop's name is a marketing trick on my part, to lure you in (since you're reading this, it worked!). You won't be learning how to build an app that works exactly like WhatsApp. WhatsApp already exists, so it would be pretty pointless. And WhatsApp is really valuable because everybody's on it. But you will be learning how to build something pretty close, and in a very short amount of time. In fact, because of the choice of tools we'll be using, you will be able to get something working much faster than whole teams could of just years ago!
- Why this workshop?
  - Africa Code Week is about getting young people interested in programming, and while [Scratch](https://scratch.mit.edu/), the programming environment used in kid's workshops is great, no matter what your age is, you might be interested in learning how to create "real" software, whether you have an idea of an app you want to create, are just curious, or wondering if you should pursue it as a career
  - the Internet is full of learning resources, but it's overwhelming if you're just getting started - we want to eliminate with this course: everything you need to know you should find here! And if you don't, please use the "issues" feature of GitHub to ask your question, or give your suggestion for enhancement.
- How to read this document
  - if you're starting out, you might want to go read trough without skipping (except perhaps if you need extra info in the appendices)
  - if you've already have some experience, you could skip to the part about how to build the app - but really, come back to the earlier parts as well, there is surely something for you too!
- What is programming?
  - we don't really know (we've been programming for 50 years, which is nothing at the scale of History)
  - we call the discipline "Computer Science", which is the worse name - it's not about computers, and it's not a science
  - studying Computer Science != learning how to program
  - it's not
    - engineering: deals with physical constraints
    - mathematics: not discovering patterns, but creating them
  - it has elements of
    - writing: specifically, like writing an essay, or some text that needs to convince of something, you need to clear, eloquent
- What's in a programming language?
  - there are many of them
    - 1000s used professionally
    - many more (anybody can make their own, some people do it for fun)
  - not at all like a human language
  - vast differences between languages
    - not so much for human languages
      - you don't learn a new language in order to be able to do something new
  - why so many of them?
    - fashion
    - NIH ("Not Invented Here") syndrome
    - mountains of old code that need to be maintained, so programming languages tend to stick around (e.g. COBOL)
- What is programming about?
  - "programming is ideas in motion"
  - programs are the most complex things we do
  - abstraction and composition
- Why learn to program?
  - it's fun
  - it teaches you how to thing clearly, for the same reason we teach mathematics, not for counting (computers can do that much better), but for problem-solvingj
  - "Software is eating the world." - Marc Andressen
  - it will make you a better user of programs
- Some things about computers
  - programming isn't really about computers (we build computers to run programs, not the other way around)
  - computer by itself doesn't do anything, but it can run programs, when you're using your computer, there are stacks upon stacks of programs running - one important program you might know about is the "operating system" (Windows, OS X, Linux, iOS, Android), which is the first program to run when you start up your computer
    - it's programs all the way down!
- Keys to learning programming (and learning in general)
  - dig in to see how things look from the inside (uncover layers that hide things from you)
  - quick feedback, lazyness
- Web development overview
  - browsers
  - client/server
  - languages
    - HTML: document structure
      - ? document
    - CSS: how things look
    - JavaScript
      - crash course
- What do you need?
  - a computer with Windows, OS X or Linux
    - Linux is preferred, but you can get started with Windows just fine, see the appendix for some info on how to get started with Linux
  - an Internet connection
    - mainly during the installation process, and for Web searches afterwards. If have trouble getting a reliable connexion, see the appendix on setting up an offline development setup
- Web developer's toolbox
  - text editor
    - most programs are stored as "plain text" - programmer writes the program using the programming language
      - plain text is just that - it's like a Word document, without the "formatting" (colors, font size, bullet points, etc.)
    - and saves the file with some "file extension" (the part after the "." in filename)
    - not a special kind of program, text editors are simple, and you could (in theory) use Notepad (comes with Windows), or others, but in practice you would want something that's designed for programming because of a few features
      - syntax highlighting: programming text editors are programmed to "understand" the syntax of programming languages, and color them in a way to help with reading
  - terminal
    - interact with computer using commands
    - looks like a hacker movie (typing text frenetically in the computer), link bad hacker movies
    - looks like it's from the 70s
      - because it is
      - programs tend to stick around...
    - what's the point?
      - in the beginning, computers weren't powerful enough for graphics
      - still useful as a way to interact with computers for advanced users (not only programmers!)
      - lots of programming tools require only work in text mode, as command-line programs
    - what is it?
      - strictly speaking, the terminal is just the window you're looking at - much in the same way you used to need a stereo to play music, and now you have music player software on your computer, the terminal window used to a physical device! In fact, most computer users only had a terminal, the actual computer would sit in another room
      - what you're actually doing is related to programming - in fact, the program you're interacting with in the terminal window is called a "shell", and it has in fact a programming language of its own
    - how do you use it?
      - Think of it as a chat session with the computer. You type out messages (called "commands"), and the computer replies with a result (the "output"). Well, you're talking to a computer program, not a virtual assistant, so any misspelling and the command will fail, and display an error
  - browser
    - developer tools
      - elements panel
        - HTML
        - CSS
      - console
        - a REPL
          - Read Eval Print Loop
- F.A.Q
  - I want to learn how to program, what do you recommend?
    - There is a lot out there. Lots of choices. Choose one, and dive in deep. It's important to go broad as well, but really depth is the key to mastery.
    - Learn things that you can use right away, that will help you in your day-to-day. I recommend the learning the shell, or "command-line".
    - Cripple your computer for focus. Install Linux with no graphical interface, just command-line. Ubuntu, but Arch Linux is best for learning. Get a second computer if you can and set up that one for "emergency" things, with Windows or Ubuntu.
- What we're building
  - in programmer terms, a chat application
    - real-time
    - multi-user (account creation, login/logout, password reset)
  - technology choices
    - how do you choose?
      - since there are thousands of programming languages, thousands of libraries, most of which could be combined, there are literally millions of combinations of technologies we could use
      - popularity
      - technical merit
    - constraints
      - runs on all platforms (Android, iOS, Windows, OS X, Linux)
        - native: every platform has a set of technologies to build programs for it
        - browser is the unifying platform, almost anything that runs on a given browser will run on all of them
    - JavaScript: only programming language that runs in the browser for now
    - Meteor.js: JavaScript framework (collection of libraries that work well together)
      - both an open-source project and a company
        - hundreds of contributors
        - core team is a company
        - investment from Marc Andressen, the creator of the first commercial Web browser, and later CEO of Netscape
          - technology changes fast, and it's important to evaluate that a piece of software you're using (such as a library), will continue to be developed and improved, and not abandoned, the fact that Meteor is supported by an actual company as good as a guarantee as you can hope to get
    - Semantic UI: CSS library. CSS is hard, design is a field of its own, the most efficient we can do is use a good CSS library
      - [Semantic UI](http://semantic-ui.com/)
- Installation and setup
  - 1. install software
    - 1. text editor (Sublime Text or other)
      - [Sublime Text](http://www.sublimetext.com/)
    - 2. Meteor.js (download, follow all steps, create account if you plan to use their free hosting)
      - [Meteor.js](http://www.meteor.com/)
    - 3. browser (Google Chrome recommended because of developer tools)
  - 2. set up your workspace
    - 1. close all other programs (clean up your desk :))
    - 2. open up text editor, terminal (Win + cmd), browser
- "building" the app
  - create Meteor "scaffold"
    - in a terminal window, type `meteor create whatsapp-clone`
  - understanding the example
    - what just happened?
      - Meteor created an example app for us
      - the source code of the app is inside a folder by the name you choose (`whatsapp-clone`, for example)
    - look at files created
      - .meteor folder
      - files
        - HTML
        - CSS: empty file, just ignore it
        - JS
    - open browser, go to http://localhost:3000
      - how to read code
        - outline
          - trees everywhere
        - AST (Abstract Syntax Tree)
      - working like a scientist
        - experiment
        - make hypothesis, theory
        - verify your predictions work
  - creating our own
    - delete everything except .meteor folder
    - create two files one file named `main.html` and one named `main.js`
    - from the outside in: make it look like it works, than make it work
      - sketch the structure in HTML
      - make it look nice with Semantic UI
      - make it work, step by step
        - typing a message
        - storing messages
        - displaying messages
        - adding user accounts
        - fixing bugs
- Appendix: How to find answers effectively
  - where to look?
    - tutorials
      - good for an overview, but only useful for making your own - tutorials are exercises, not guides
      - make them your own: as you follow along, select piece and reformulate: most tutorials have extra cruft (i.e. they are not general enough), so you have to sort trough
    - books
      - programming books that teach you programming or help you understand how to solve programming problems are rare. Most programming books are overviews of a given language or platform, with some examples sprinkled on
    - references
  - making good searches
    - keywords
    - general is better than specific
      - if you have no idea, start with specific, than use the results to make your query more general
    - specific if you're really certain what you're looking for, or just refreshing your memory
- Appendix: Installing the Linux operating system
  - easy choice: Ubuntu (started out by South African entrepreneur Mark Shuttleworth)
  - hardcore: Arch Linux. Recommended, not the easy route, but will teach you a lot
    - great wiki
    - how to
      - download, create USB key using instructions
      - reboot computer and choose to boot on USB key (try pressing F12 repeatedly while booting if computer still boots to Windows)
      - follow steps in "Beginner" section in Arch Wiki
- Appendix: setting up an offline development environment
  - references, books

# Portfolio

These are some of the projects that I’ve worked on, as well as code samples which I think demonstrate my understanding.

I am comfortable working in Python, TypeScript and C, and I have basic working proficiency with R and C++. I have worked with LaTeX typesetting before (but nowadays prefer to use [LyX](https://www.lyx.org/) instead). Furthermore, I have rudimentary experience with Matlab, Mathematica, RStudio, and Jupyter environments. I have made [basic Rust programs](https://github.com/olliecheng/demultiplex-duplicates) before and I am very interested in developing my skills further in the language.

I am open to learning new languages and frameworks if required. I am very interested in getting experience working in Julia and the aforementioned Rust. If you have any opportunities, please [get in touch](/contact/)!

~~~
<style>
.franklin-toc ol {
  list-style-type: disc;
}
</style>
~~~
\tableofcontents

## 2023: Flexiplex @ Davidson Lab, WEHI
At the [Walter and Eliza Hall Institute](https://wehi.edu.au), I have been involved with the [Flexiplex](https://github.com/DavidsonGroup/flexiplex) ([preprint](https://www.biorxiv.org/content/10.1101/2023.08.21.554084v1)) project to produce a flexible demultiplexer for barcoded long-read single cell data.

Part of my work with Flexiplex has included:
- Package management of a C++ program for bioconda
- Development of a [utility Python script](https://github.com/DavidsonGroup/flexiplex/tree/main/scripts) to numerically determine knee and inflection points, as well as graph them
- Documenting my work
- Present posters at conferences, including OzSingleCell and ABACBS
- I will be presenting a 2 minute "flash talk" at the peak Australian bioinformatics conference, ABACBS, on our lab's work

## 2023: Lookahead

![Untitled](/assets/portfolio/Untitled.png)

[Live link](https://theepiccowoflife-lookahead.herokuapp.com) and [GitHub](https://github.com/theepiccowoflife/lookahead)

Lookahead, originally released by Rohyl J., is a University of Melbourne semester planner which has been used by upwards of 25,000 students. As Rohyl was too busy to maintain the codebase, I was part of a small team who forked the original project with the aim to modernise the codebase and implement new features. While working on this project, I learnt how to:

- Update a legacy Node codebase to support ESM and modern tools
- Implement a modern Docker build system
- Write new authentication workflow, requiring use of the Okta API, by network inspection to understand the calls being made
- Set up CD [Continuous Deployment]
- Use trunk-based development

## 2022: COMP10002 Foundations of Algorithms

I wrote the following two assignments for my computer programming course [COMP10002: Foundations of Algorithms](https://handbook.unimelb.edu.au/subjects/comp10002). My final mark for this subject was 89%. I have attached below my two assignment submissions. Note that for the scope of these projects, I was not permitted to use:

- External imports/includes
- Header files

- [Assignment 1 for COMP10002](https://gist.github.com/denosawr/77f1234a935a1a1500e2dd615adccc66)
- [Assignment 2 for COMP10002](https://gist.github.com/denosawr/eb5d46f61902de385447f351c3788595)

```c
void log_pushAction(log_t *log, action_t actn, int amt) {
  check_pointer(log);

  int id = action_convertActionToId(actn); // get the ID of the action

  action_t *actions = log->actions->data;
  if (id >= log->actions->capacity) { // if ID is larger than the vec
    vector_extend(log->actions);      // then extend the vector
  }

  if (id >= log->actions->size) { // if ID is bigger than the size
    log->actions->size = id + 1;  // increment size
    actions[id] = 0;              // ensure this is initialised as 0
  }

  if (!actions[id]) {               // if this action has not been seen before
    log->action_n_d++;              // increment distinct counter
    actions[id] = 0;                // ensure value is 0
  } else if (actions[id] == -amt) { // in this case, actions[id] = 0 after the
                                    // the deincrement. hence...
    log->action_n_d--;              // we effectively remove this event
  }

  log->action_n_t += amt;
  actions[id] += amt;
}
```

## 2022: WACE Paper Archive

![Untitled](/assets/portfolio/Untitled%201.png)

[Live link](https://olliecheng.me/papers) and [GitHub](https://github.com/olliecheng/wace-paper-archive)

I created and maintained an archive of past WACE papers, freely available for use by students. This has now been taken down due to copyright concerns. The interface was built in Svelte. In making this website, I learnt how to:

- Interface with S3-compatible storage services, in particular Cloudflare R2
- Write serverless function which could interact with a database and respond to HTTP requests
- Use Svelte and Sveltekit, a modern UI framework, in my first SPA

## 2020: pymine

[GitHub](https://github.com/denosawr/pymine)

During 2020 and 2021, I ran and taught a Programming Club at my school, focusing on teaching Python to middle school students. During that time, I created a custom server which would be accessible through a Python interface, and could interact with a Minecraft instance through its WebSocket interface. I also wrote a somewhat comprehensive Python guide for my students, accessible [here](https://www.notion.so/Learning-to-Code-1ff7700b316c488ea5af501d39eaea3b?pvs=21). While working on Pymine, I learnt how to:

- Write a HTTP and WebSocket server using asynchronous language features
- Manage a codebase with a core and individual modules, implementing my own loading system so different handlers (i.e. a HTTP server listening for requests) could be easily implemented
- Work with Python’s (at the time new) typing hints, and use pyright as a type linter

## 2020: Methods Maths Investigation

![Untitled](/assets/portfolio/Untitled%202.png)

[GitHub](https://github.com/denosawr/mathsinv-aemam-1)

For a maths investigation concerning the production of an estimation model, I used a variety of basic regression techniques to determine the most accurate mathematical equation which fit a certain dataset in Python. While working on this admittedly basic but interesting project, I learnt:

- The basics of data processing in `pandas`, `matplotlib`, and `numpy`
- Beginner regresion techniques
- How to write a report and then typeset it in LaTeX (though, in retrospect, I hadn’t learnt how to write formal documents yet!)

## 2018: TranslucentTB

@@img-small ![Untitled](/assets/portfolio/Untitled%203.png) @@

[GitHub](https://github.com/translucenttb/translucenttb)

I was a core contributor to the TranslucentTB project, which currently has 10.7k stars on GitHub and >3 million downloads. However, I stopped contributing many years ago, and the vast majority of the current codebase is the work of a different author.

When I was contributing, I:

- Was first introduced to C++
- Implemented multi-monitor functionality and a “maximise window states” feature which required working with the Windows SDK
- First started contributing to the open source community
- Was first introduced to git being used in a formal environment
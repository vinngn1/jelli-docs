# jelli-docs

## Before writing documentations

It's important and necessary to define the target audience of the docs. It's common that there are least two type of audience:

1. _Users_: those using our code/projects without caring about how it works.
2. _Developers_: those will need to understand how our code works in order to contribute to our projects.

## Writing documentations

### At project level

It's a common practice to start with the `Readme.md` and it should include the following:

1. The purposes of the project: why does it exist? what does it do? 
2. Installation guilde
3. User guild
4. FAQ
5. Other support/related docs

### At detail level

For junior developers or experienced developers who are unfamiliar with the codebase, it's hard and/or time-consuming for them get started without good documentations. However, documenting comes with a cost: time and effort (what to write, where to write and how to write it). If we have time and resources to documents every module, every file, every function and every line of code, it would be great. However, most of the time, we dont have that luxury.

#### What to document? 
David make a very good point in his [article] (https://signalvnoise.com/posts/838-ask-37signals-how-do-you-document-code), the first and most important thing for a healthy code base is good code. The code itself should be short and expressive. Reading the code itself make no different or maybe even better than reading the documentation. And for some code which is written in a unusual way and will break if written in usual way, commenting or documenting those code should be enforced.

Briefly
  - Follow community and industry standards and best practices
  - Defining internal coding and documenting standards
  - Documenting exceptions

#### How to document?

We need a powerful and easy-to-use tool in order to grab our plain text we commented in the code and turn it to something pretty like html. Adam and Bryan have done a some [research] (https://docs.google.com/document/d/1HkqxJqyl3QV5MZt0UGctworGwcCwF9zVCwBEU7qgi4Q/edit) on the tools. _JSDoc is clearly the best tool for our purpose at the moment_. However, [mr-doc](https://github.com/mr-doc/mr-doc) is very active in the past few month. The project is a derivation of doxx which mention in [here] (http://blog.fusioncharts.com/2013/12/jsdoc-vs-yuidoc-vs-doxx-vs-docco-choosing-a-javascript-documentation-generator). We should definitely keep an eye on this. At this moment, it's still under development and does not have enough documentation.

JSDoc has a lot of options for commenting code, please see [here](http://usejsdoc.org/)

And we can simple turn all those comments to an output documentation by running:

`jsdoc project_path/**/*.js`

We can configurate an ignore lists for files or folder to skip.

### What to do next?

1. We need to get together and define a few things:
  - What to document?
  How much/deepth do we really need to document? Only the important one or exception one is sufficient? Then what we need to define what is important and what is exception?
  - How to generate our doccument? 
  Manually via running command line? Or via a build process? How is the current build process work?
  - Pick a project for experience (new or existing)
  - Where to host the docs

2. Set up and configurate JSDoc (after getting input from the team)
3. Implement to the selected project, generate docs
4. Revise and deploy in use.


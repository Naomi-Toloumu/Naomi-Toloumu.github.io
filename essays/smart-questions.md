---
layout: essay
type: essay
title: "From Queries to Clarity"
# All dates must be YYYY-MM-DD format!
date: 2024-09-11
published: false
labels:
  - Smart Questions
  - Not So Smart Questions
  - Questioning to Succeed 
---

## What’s a smart question?

*Stack Overflow, a question and answer site for programmers, is a great resource for anyone who may have issues with code or who may simply want to learn new or different methods of doing something.*

## Smart Question + Responses

The “Smart” question is notable for its thoroughness and clarity. It doesn’t just ask about the basic function of JavaScript source maps (.map files), but also delves into related topics like the importance of files such as `angular.min.js.map`, the role of `.js.map` files in enhancing JavaScript applications, and the process of creating these source maps. This detailed approach provides a comprehensive understanding of how source maps aid in debugging and development, making the question particularly effective. 


[SmartQ Ex:](https://stackoverflow.com/questions/21719562/how-can-i-use-javascript-source-maps-map-files)
```
Q: How can I use JavaScript source maps (.map files)?

Recently I have seen files with the .js.map extension shipped with some JavaScript libraries (like Angular), and that just raised a few questions in my head:

a) What is it for? Why do the guys at Angular care to deliver a .js.map file?

b) How can I (as a JavaScript developer) use the angular.min.js.map file?

c) Should I care about creating .js.map files for my JavaScript applications?

d) How does it get created? I took a look at angular.min.js.map and it was filled with strange-formatted strings, so I assume it's not created manually.

```
The responses to this question are also very useful. The first answer (provided below), which received the most likes, stood out because it thoroughly addressed all aspects of the question, providing well-rounded explanations and practical advice. While the other responses were less comprehensive, they still offered value by focusing on individual aspects of the query and explaining them in detail. This variety in responses ensures that different facets of the topic are covered, providing a well-rounded perspective.

```
A: The .map files are for JavaScript and CSS (and now TypeScript too) files that have been minified. They are called source maps. When you minify a file, like the angular.js file, it takes thousands of lines of pretty code and turns it into only a few lines of ugly code. Hopefully, when you are shipping your code to production, you are using the minified code instead of the full, unminified version. When your app is in production, and has an error, the source map will help take your ugly file, and will allow you to see the original version of the code. If you didn't have the source map, then any error would seem cryptic at best.

Same for CSS files. Once you take a Sass or Less file and compile it to CSS, it looks nothing like its original form. If you enable sourcemaps, then you can see the original state of the file, instead of the modified state.

So, to answer you questions in order:

a) What is it for?
To de-reference uglified code

b) How can a developer use it?
You use it for debugging a production app. In development mode you can use the full version of Angular. In production, you would use the minified version.

c) Should I care about creating a js.map file?
If you care about being able to debug production code easier, then yes, you should do it.

d) How does it get created?
It is created at build time. There are build tools that can build your .map file for you as it does other files. Sourcemaps fail if the output file is not located in the project root directory #71

```
 
## Not So Smart Question + Responses.

Meanwhile, the “Not So Smart” question lacks depth and focuses more on seeking an easy solution for learning programming languages, rather than seeking detailed or practical advice. 

[NotSmartQ](https://stackoverflow.com/questions/3514737/which-language-is-easiest-to-learn)
```
Q: Which language is easiest to learn?

This is a subjective question just to get a general impression. As Java is the most popular programming language right now it is used as a benchmark.

Lets say I have to spend T amount of time/effort to learn/master Java. By what factor should I multiply T to get a time/effort needed to learn/master other language instead, say C, C++, C#, python, perl, Lisp, Haskel, PHP?

My guess is:

0.5T PHP
0.9T python
1.1T C#
2.0T C++
3.0T C

What do you think?

```

Among the three responses it received, only one provided more than just a list of languages. This response went a step further by offering context and practical advice for learning those languages, making it more useful. The other two responses fell short: one merely reiterated that the question was subjective without adding much value, while the other suggested a language for beginners with a name that was both unusual and unfamiliar, which could be considered controversial.

## Conclusion

When seeking help from others, it’s crucial to ask smart questions that lead to efficient and effective answers, benefiting not just yourself but also the responders and future inquirers. Examining the importance of smart questions highlights how they can greatly enhance the experience for everyone involved. For future software engineers, asking well-formulated questions is a vital skill that helps in obtaining valuable information, solving problems more effectively, and fostering better learning and collaboration. This skill is essential for personal growth and the success of projects and teams.

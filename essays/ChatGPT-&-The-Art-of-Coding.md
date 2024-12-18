---
layout: essay
type: essay
title: "ChatGPT & The Art of Coding"
# All dates must be YYYY-MM-DD format!
date: 2024-12-16
published: true
labels:
  - Reflection of AI 
  - ICS 314 Growth
---


## Introduction
-----

The role of AI has significantly impacted the world of Software Engineering, from the way in which developers work, collaborate and solve their problems. AI tools like Chat GPT, for example, are able to generate code in a matter of seconds, drastically speeding up the development process. Although the accuracy of the generated code often depends on the quality of the user’s input, these tools prove to be invaluable for developers by streamlining workflows and reducing the amount of time and effort spent on repetitive tasks. Beyond just code generation, AI tools can also enhance code quality of the code by detecting bugs, errors, and potential security vulnerabilities.

In the context of my experience in ICS 314, AI tools have been instrumental in helping me understand software engineering concepts, especially in both front-end and back-end development. For example, in projects involving React and JavaScript, ChatGPT provided suggestions that improved component rendering and helped troubleshoot numerous ESLint errors. Besides ChatGPT, I’ve also had the opportunity to use Live Share in Visual Studio Code, which enabled real-time collaboration on group projects. This feature made it easier to work with classmates, similar to the way Google Docs allows for numerous users to document and edit at the same time.





## Personal Experience with AI
-----

Initially, I was hesitant about using AI due to the negative perceptions surrounding its use in writing assignments. People often referred to it as the "easy way out," and most professors discouraged it, but this course was different. At first, I stubbornly refused to rely on AI for help. However, I gradually turned to it to better understand new concepts, especially since I had so much to learn from scratch—like using GitHub and GitHub Desktop, merging branches via pull requests, recognizing patterns in code, and learning how certain functions work and how to debug them. Depending on the topic, mastering these skills could take anywhere from a few hours to several days of practice.


*Experience WODs*
-----
I made the decision not to use AI, thinking that doing it on my own would help me learn better. When I got stuck, instead of turning to ChatGPT, I preferred to watch the instructional videos provided, trying to work through the problems independently. This method definitely slowed me down, but I felt that it would give me a stronger foundation in the long run. I spent a lot of time figuring things out myself, sometimes struggling for longer than necessary, but this approach helped me internalize the concepts more deeply, even if it took me longer to get through the tasks. 


*In-class Practice WODs*
------
During the Experience WODs, I used ChatGPT selectively, turning to it only for concepts I struggled to fully grasp after multiple attempts. I saw it as an opportunity to practice using AI in a balanced way—leveraging it when necessary to clarify difficult concepts without becoming overly reliant on it. By doing this, I was able to use ChatGPT as a tool to guide my learning, helping me understand key principles without letting it take over the problem-solving process. This approach allowed me to enhance my understanding of the material, while also building the confidence to tackle challenges independently.


*In-class WODs*
-----
The WODs were a tough test of my coding skills, and my initial approach relied heavily on AI tools like ChatGPT for quick solutions. While AI provided immediate feedback and suggestions, it ultimately slowed my learning process. Instead of developing a deeper understanding of the concepts, I became overly reliant on AI to solve problems for me. Realizing this, I shifted my approach, using AI more strategically to ask targeted questions and seek optimization tips rather than just copying answers.


*Esssays*
-----
I used ChatGPT to help with my technical essays, mainly to fix spelling errors and improve sentence flow. After writing my drafts, I'd ask ChatGPT to catch mistakes and reword awkward sentences, making my work clearer and more polished without changing the content. It helped me present my ideas more effectively.


*Final Project*
-----
While working on a product page, I used ChatGPT to solve a few coding issues. I asked, "How does getServerSession work in Next.js for authentication?" ChatGPT explained session management and how to protect pages with loggedInProtectedPage. I also needed help with a case-insensitive Prisma query, so I asked, "How do I use findMany for a case-insensitive query?" ChatGPT showed me how to use the contains operator with mode: 'insensitive'. Additionally, I asked, "How do I pass props between components in Next.js when one is 'use client'?" ChatGPT guided me on importing and exporting SearchProducts and ListProducts correctly. This helped me improve my code structure and make the development process faster.


```
import { getServerSession } from 'next-auth';
import { loggedInProtectedPage } from '@/lib/page-protection';
import { authOptions } from '@/lib/auth';
import { prisma } from '@/lib/prisma';
import ListProducts from './ListProducts';
import SearchProducts from './SearchProducts';


const ProductsPage = async ({ searchParams }: { searchParams?: { query?: string } }) => {
 const session = await getServerSession(authOptions);


 loggedInProtectedPage(session as { user: { email: string; id: string; randomKey: string } } | null);


 const query = searchParams?.query || '';


 const projects = await prisma.project.findMany({
   where: {
     name: {
       contains: query,
       mode: 'insensitive',
     },
   },
 });


 return (
   <div>
     <h2 className="text-2xl font-semibold border-l-4 pl-4 border-gray-300">Search the UHM Way</h2>


     <SearchProducts />
     <ListProducts query={query} projects={projects} />
   </div>
 );
};


ProductsPage.defaultProps = {
 searchParams: { query: '' },
};


export default ProductsPage;


```


*Learning*
-----
ChatGPT has been a valuable tool in improving my understanding of software engineering, especially when it comes to debugging. When encountering bugs or errors in my code, I can quickly ask ChatGPT for help. It assists in interpreting error messages, explaining potential causes, and suggesting fixes. This makes the debugging process faster and more efficient, allowing me to understand important concepts like code structure and logic. ChatGPT also helps with common issues, such as resolving ESLint errors in VSCode. For example, when I get warnings like "no-unused-vars" or "expected indentation of 2 spaces," I can ask ChatGPT, "How do I fix those particular Eslint errors in VSCode?" It essentially helps by providing various solutions and informs me of potential factors that impact it which I take note of.


*Answering a Question in Class*
-----
To answer most of the discussion questions in my course, I focus on taking detailed notes during lectures, jotting down key points and ideas discussed in class. I often use ChatGPT to simplify complex topics and present them in clearer terms. While ChatGPT is a helpful tool, I double-check its explanations against my notes to make sure everything aligns with what was covered in class. This approach helps me understand the material better and answer the questions more effectively.


*Asking or Answer a Smart Question*
-----
I tend not to ask or answer complex questions because I feel that I lack the experience and knowledge to tackle such challenging topics. Instead of using ChatGPT or any AI tools, I prefer to review what other students have discussed in class or on Discord, as their insights often provide different perspectives that help me understand the material better. Since I don’t feel confident in solving a wide range of errors or complex problems, I usually try to work through any difficulties on my own. 



Coding Example:
"Give an Example of using async and await ot fetch data from an API"

Results:
```
async function fetchData() {
  const response = await fetch('https://jsonplaceholder.typicode.com/posts/1');
  const data = await response.json();
  console.log(data);  // Output: Data from API
}

fetchData();
```


*Explaining Code*
-----
AI, like ChatGPT, has been very useful for explaining code and helping developers understand complex concepts quickly. It can provide instant explanations and suggest solutions, which speeds up the development process. However, the solutions it gives aren’t always perfect and often require tweaking to fit the problem. While it saves time by giving a starting point, it can take some trial and error to refine the results. Despite this, AI tools are still valuable for speeding up learning and improving coding efficiency.


*Writing Code*
-----
ChatGPT has become an essential tool in my development process, especially for new projects or challenging tasks. It quickly provides clear templates, code snippets, and guidance, helping me avoid common mistakes and speed up the initial stages of development. For example, when I needed help with setting up authentication in Next.js and Prisma, I could simply ask, “How do I set up authentication with Next.js and Prisma?” and get a step-by-step explanation. While the code often requires some adjustments, ChatGPT significantly accelerates my workflow, helping me learn faster and improve efficiency.


*Documenting Code*
----
After generating code from ChatGPT, it often includes summaries that explain the code's purpose and how different parts work together. These automatic explanations help make the code easier to understand and maintain, saving time and improving readability. This is especially helpful in collaborative projects, where clear documentation is key. ChatGPT’s ability to break down complex code into simple descriptions ensures better understanding and easier integration of algorithms or design patterns into the codebase.


*Quality of Code*
-----
ChatGPT has significantly improved my coding practices in ICS 314, helping me write cleaner and more efficient code. In the beginning, I struggled with issues like indentation and common errors, but ChatGPT's consistent feedback helped me quickly identify and correct these mistakes. It provided clear explanations, pointed out formatting issues, and suggested best practices, which made it easier to adopt good habits. Over time, tasks like proper indentation became automatic, and errors that once slowed me down became easier to catch and fix.

*Other Uses*
-----
AI has helped me with the setup and testing process for my development enrionment. For example, it guided me through downloading and checking essential software like Node.js and npm, using simple commands such as node -v and npm -v to verify their versions. Additionally, ChatGPT helped me understand how to use npm run dev to launch the development server, allowing me to test my project locally. By providing clear, step-by-step instructions, ChatGPT ensured that my project was properly set up and running on localhost, minimizing setup errors and accelerating my development workflow.

## Impact on Learning and Understanding
-----
The integration of AI has significantly enhanced my understanding of software engineering, particularly in debugging. Tools like ChatGPT provide real-time assistance by interpreting error messages, identifying potential issues, and offering solutions. This has greatly accelerated my debugging process by guiding me through different troubleshooting strategies and helping me better understand underlying programming concepts such as code structure and logic. While the effectiveness of these AI tools depends on the complexity of the problem, they have proven invaluable in making debugging faster, more efficient, and less intimidating. Overall, AI has helped me approach coding challenges with greater confidence and a more systematic approach.

## Practival Applications
-----
AI is making significant progress in software engineering, helping solve key industry challenges. For example, GitHub Copilot, powered by OpenAI’s Codex model, provides real-time code suggestions and completes code blocks, speeding up development and reducing coding barriers. AI tools like Amazon CodeGuru and DeepCode also improve code quality by automatically finding bugs, security risks, and performance issues, helping to catch problems early and reduce manual code reviews. While their effectiveness depends on the complexity of the code and input quality, these AI tools have proven valuable in enhancing efficiency and software quality, especially in large projects.

## Challenges and Opportunities
-----
In my experience using AI within the course, one challenge has been the lack of transparency in how AI-generated suggestions are made, which sometimes leaves me unsure of the reasoning behind them. Additionally, AI tools can occasionally provide inaccurate or incomplete information, requiring manual intervention to correct. Despite these limitations, there are significant opportunities to further integrate AI into software engineering education. For instance, AI could be used to provide personalized, adaptive learning paths that cater to individual student strengths and weaknesses, offering tailored exercises and challenges. AI-driven tools could also simulate real-world coding environments, allowing students to practice debugging and problem-solving in a more hands-on way. With further development, AI could enhance both engagement and understanding, making the learning process more interactive and relevant to real-world software development scenarios.

## Comparitive Analysis
-----
Traditional teaching methods in software engineering focus on lectures and textbooks, which provide solid foundational knowledge but can lack engagement and practical application. AI-enhanced approaches, on the other hand, offer more interactive, personalized learning experiences. Tools like AI-driven coding assistants give real-time feedback, allowing students to apply concepts immediately and develop practical skills. AI also adapts to each student's needs, improving engagement and retention. By offering personalized quizzes, coding challenges, and simulations, AI makes learning more dynamic and hands-on, complementing traditional methods and better preparing students for real-world software development.


## Future Considerations
-----
The future role of AI in software engineering education has the potential to revolutionize how students learn and interact with technology. As AI continues to advance, it could provide even more personalized learning experiences by adapting to individual student needs, offering tailored lessons, and providing instant feedback on assignments. AI-driven tools could help bridge the gap between theory and practice by automating complex coding tasks, identifying errors, and suggesting improvements in real-time, thus speeding up the learning process. However, challenges remain, particularly around ensuring the accuracy of AI feedback and avoiding over-reliance on automated solutions. To maximize the benefits of AI, there will need to be a balance between technology and human guidance, as well as continued efforts to improve AI systems to ensure they offer meaningful insights without replacing critical thinking. As AI evolves, it has the potential to become an indispensable tool in shaping future software engineers, making learning more efficient, engaging, and relevant to real-world development challenges.

## Conclusion
-----
Essentially, AI has played a significant role in transforming my Software Engineering course experience, greatly enhancing my learning process and improving my coding skills. Tools like ChatGPT have provided instant feedback, clarified complex concepts, and assisted in debugging, helping me grasp challenging topics more efficiently. While initially, I relied on AI for quick solutions, I learned to use it strategically to complement my problem-solving approach, allowing me to deepen my understanding and build confidence. For future courses, integrating AI in a more structured way—leveraging personalized feedback and adaptive learning paths—could further optimize the educational experience, balancing the speed and support AI offers with the critical thinking and hands-on problem-solving necessary for mastering software engineering.


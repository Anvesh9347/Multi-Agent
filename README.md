Multi-Agent Blog Writer

A small AI “team” that researches a topic and writes a blog post about it, with no human help along the way.

What it does

You give it a request, such as “write a detailed blog on Tesla”. Two AI agents then work on it together:

Researcher: gathers facts from the internet and from a private set of notes.
Blog Writer: turns the research into a finished, readable article.

If one agent can’t finish the job, it hands the work to the other. When an agent is satisfied with the result, it marks the answer as final and the process stops.

Think of it like a newsroom
Role	Real-world equivalent	What it uses
Researcher	A reporter doing background research	Live web search (Tavily) and internal notes (Blog.txt)
Blog Writer	An editor who writes the final piece	The same sources, plus the researcher’s findings
Workflow manager	The newsroom’s process	LangGraph, which routes work between the agents
Example result

For the prompt “write a detailed blog on Tesla”, the system produced a complete article with an introduction, sections on Tesla’s history, technology, factories, challenges and future plans, and a conclusion.

Built with
Python and LangChain / LangGraph to connect the agents and manage their teamwork
OpenAI GPT-4o as the “brain” of each agent
Tavily for web search
FAISS and OpenAI embeddings to search the private notes quickly

Why it matters

One AI doing everything can get overloaded. Splitting the job into specialists, each with its own tools and focus, is a common way to make AI systems more organized and reliable. This project is a simple demo of that idea.

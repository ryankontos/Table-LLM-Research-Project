**Title**: _Large Language Model based Multi-Agents: A Survey of Progress and Challenges_  
**Authors**: Taicheng Guo, Xiuying Chen, Yaqi Wang, et al. (2024)

1. **LLM-Based Multi-Agent Systems**:
   - LLM-based multi-agent systems are evolving as an advanced approach to solve complex tasks by leveraging **collaborative decision-making** and **specialised profiles** for each agent. This approach allows different agents to focus on distinct tasks, working together to tackle problems that would be difficult for a single LLM agent.

2. **Agents Profiling**:
   - Agents can be defined by **pre-defined profiles**, **model-generated profiles**, or **data-derived profiles**. Profiling helps in assigning distinct roles and capabilities to agents. For instance, in game simulations or software development, different agents may assume roles such as "Programmer," "Tester," or "Manager."
   - In my project, agents can be designed to specialise in tasks like data extraction (e.g., writing SQL queries), data processing (e.g., using Python), and communicating results. This structure enhances the system's ability to handle complex user queries about tabular data effectively.

3. **Agent Communication Paradigms**:
   - The paper categorises communication paradigms into **cooperative**, **debate**, and **competitive**. Cooperative agents work together towards a common goal, debate agents refine ideas through arguments, and competitive agents aim to outperform each other.
   - For my system, I think cooperative communication would be ideal, as different agents need to collaborate to parse the user’s query, generate code, and ensure the accuracy of results (e.g., one agent generating a query and another validating its accuracy).

4. **Capabilities Acquisition**:
   - Agents improve their capabilities through **feedback loops**—either from interactions with the environment, other agents, or human input. Key methods include memory (using past interactions), self-evolution (adapting strategies), and dynamic generation (creating new agents for specific tasks on the fly).
   - Incorporating feedback into my system would allow the agents to refine code execution iteratively. For instance, if an SQL query returns an error, an agent could automatically revise the query based on error feedback, improving accuracy and efficiency over time.

5. **Applications in Problem Solving**:
   - The multi-agent system framework is applied in problem-solving tasks like **software development**, where different agents (e.g., product managers, programmers) collaborate to create and refine code. Each agent handles a specialised task in the development cycle.

6. **Agents in Multi-Modal Environments**:
   - Although most systems focus on text, the paper notes the potential of **multi-modal environments** where agents can process text, images, audio, and other data types. These environments are more complex but offer richer interactions and decision-making.
   - My system could eventually expand to handle not just text-based queries but also integrate visual data, allowing agents to interpret and process tabular data from images.

7. **Scalability Challenges**:
   - As the number of agents increases, scalability becomes an issue. Systems with a large number of agents require efficient coordination and communication to prevent bottlenecks and ensure that agents can operate effectively together.
   - In my thesis, I need to consider how to manage multiple agents efficiently. Ensuring that agents don’t generate redundant operations or communicate ineffectively will be critical for maintaining system performance, especially when handling large datasets or complex queries.
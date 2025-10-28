This is an end-to-end LLM and Gen AI project that will use:

1. Llama 3.1 open-source LLM

2. ChromaDB (vector store)

3. LangChain

4. Streamlit

We will build a tool called Cold Email Generator.
This tool helps Software and AI services companies send cold emails to their potential clients.

Problem Statement:
Software services companies (like Vivasoft, Optimizely, Enosis, etc.) help their clients (for instance, Australian Red Cross, RAKBANK, L’Oréal, etc.) build software. There is always competition in this market, and the sales teams from these companies build various marketing techniques to acquire projects. One of the techniques is cold emailing. For example, a company like Optimizely will send a cold email to a potential client.

Now, how they know that this client has a specific requirement is by going to their job portal where they have a requirement for a software engineer in the AI/ML area. After scanning the requirements, they will send them a cold email like:
"Hey, looks like you need a software engineer, so instead of hiring full-time, you can hire people from us."

Many times, these companies hire people from India, Indonesia, or Bangladesh with a lower budget and on a contract basis, which benefits them more—so the cold email technique works.

Now, a sales representative or business development executive at Optimizely will have to form a nice email that is relevant to the job post, and one of the things that can be used is an LLM. The LLM will generate a cold email. So, a tool will be built where a job posting will be given, and when submitted, it will figure out what kind of skills are needed. Based on that, it will write an email that is relevant.

So, let’s say that in that job post they needed ML with Python and DevOps—the email will exactly talk about that profile, those skills, and also include portfolio links (past projects that they have done in that area).

Technical Architecture:

Extract text from the career page using the LangChain framework.

Then we will use Llama 3.1 to extract the job role, job skills, and description in JSON format.

Then we give that to ChromaDB, which is a vector database where we have previously stored skills and relevant portfolios for the Optimizely company.

Then it will give the portfolio link and job description (JSON) to the LLM, and that will generate a nice email.

Llama 3.1 is a super amazing open-source tool that can be used for free. Many people download this model locally on their computer and run their inference. Many people also use Ollama. But both the locally downloaded one and Ollama are very slow, so we are going to use GROQ, because GROQ allows us to use Llama 3.1 in the cloud, and the inference is very fast because they use something called LPU (Language Processing Unit) that makes the inference—meaning when we ask a question, the response will come back very fast.
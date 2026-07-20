# AI Policy

This policy primarily meant to refer to Large-Language Models (LLMs) for text or code generation in research. This 
document does not cover machine learning in general, as these are distinct concepts. All statements in this document
are subject to revision.

I highly recommend against the use of LLMs in your learning or research as a student. My recommendation stems from the 
following rationale:
- LLMs are effectively a next-word prediction engine. As a result, for their statement to be true, a collection of true
words have to be strung in the correct order. As the sequence of orders increases, the probability that the statement 
is true decreases. As a result, LLMs as tools require expertise in order to validate their output. The purpose behind
your training is to develop that expertise. If you are using an LLM, you will not be able to effectively develop that
expertise.
- Use of LLMs requires detailed validation steps, which your training may not have yet provided. So, you cannot verify
whether some output is valid. This concern arises when developing code for statistical analyses.
- Part of my role is to train you. That means we should discuss questions that you have or challenges that arise. An 
LLM may send you down a wrong path without your realization. This is not an effective use of your limited time.
- Scientific writing is a difficult task that takes lots of practice to develop. Offloading this process means you will
not develop the necessary skills.
- Recent research has shown 'deskilling' or when cognitive processes are offloaded to an LLM a person's skill at a task
degrades. 

There are some cases where LLM can be more-or-less reliable. The following are some use-cases that I would deem LLMs 
to be reliable enough as a tool:
- Translating code from one software language to another (this comes with a built-in unit test)
- Convert existing code into an R or Python package
- Generating boilerplate code for plots
- Vectorizing or improving existing code
- Aid in debugging code
- An advanced version of a thesaurus for complex topics

Again, I would not recommend these tasks while you are a student. Doing them the "difficult way" can be a valuable 
learning experience

Finally, I will say that you can experiment with LLMs as a tool. I have with instances outside the use-cases above. As 
stated in the opening sentence, this document is meant to focus on the use of LLMs in your learning and research, which 
should be distinct from experimenting with them for different tasks. 

Having outlined my general perspective, the following details what I expect of you if you are going to make extensive 
use of an LLM for a research project despite the warnings made here.

---

## Disclosure Statement

For us to have a successful advisor-advisee or mentor-mentee relationship, we need to be able to trust each other. As 
part of that, I expect for you to disclose any use of a LLM to me. Failure to do so, jeopardizes that collaborative 
relationship and may mean we are not able to trust each other. For disclosing LLM use, please complete something like 
the following table. This table *must be completed prior to using an LLM*.

| Task                      | Rationale | Description of Use | 
|---------------------------|-----------|--------------------|
| Outlining project         | ...       | ...                |
| Writing proposal or paper | ...       | ...                |
| Statistical analysis plan | ...       | ...                |
| Code writing              | ...       | ...                |
| Data analysis             | ...       | ...                |
| Code or paper review      | ...       | ...                |
| Literature review         | ...       | ...                |
| Other                     | ...       | ...                |


I recognize that this should be a two-way street in terms of conduct and disclosure. So, I make the following promises 
to you:
- I will review your work that you send to me. I will not use an LLM or other related technology for reviews.
- I will respond to your emails or questions myself. I will not use an LLM to do so.
- I will draft any recommendations letters for you and not use an LLM.
- If we are working together on a project, I will disclose my use of an LLM in accordance with the disclosure table.

## My Expectations

The following are some additional requirements if you are to use LLMs. If you want an exception to any of these steps, 
you must discuss them with me and I must approve. 
- You use UNC's [PromptLab](https://library.unc.edu/ai/library-ai-studio/promptlab/) to interact with an LLM
- No data from or used by research group is uploaded, irrespective of the UNC-determined Information Tier
- No works in-progress or other similar materials are uploaded. Revising collections of different sentences is ok, but 
an entire document should never be uploaded.
- Uploading material (papers, manuscripts, private code) that is not yours without the express and documented permission
of the owner of that material

The following are some principles I expect you to adhere to if you use LLMs:
- Completed the disclosure table. This helps to ensure that you had identified a clear task for use with an LLM and are 
limiting it to that task.
- Export all chat logs for record keeping. This should be all relevant chat logs (in their entirety) for a project.
- Any code generated by an LLM that cannot be directly verified is instead vetted and verified through a testing 
procedure. An example of code that can be directly verifiable is code to create a plot (since we can examine the plot to 
see whether it is correct). An example of code that is not directly verifiable is fitting a statistical model. Such code
should be validated through the use of unit tests.
- LLMs are used for text revision and not text generation. A major danger with LLM text is that it might be plagiarized,
which can have substantial negative professional consequences for you and me.

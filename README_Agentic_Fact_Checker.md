
# Agentic AI Fact Checker (Production Style)

## Overview
This project demonstrates a production-style **Agentic AI system** that verifies factual claims using multiple collaborating agents.

The system uses:
- CrewAI multi-agent framework
- Wikipedia retrieval tools
- BM25 evidence ranking
- LLM reasoning and auditing

Agents collaborate to retrieve evidence, verify claims, audit reasoning, and produce structured outputs.

---

## Architecture

Agents:

1. Evidence Hunter – retrieves evidence from Wikipedia
2. Entailment Judge – determines claim validity
3. Evidence Auditor – checks reasoning quality

Workflow:

Claim → Evidence Retrieval → Logical Verification → Evidence Audit → Final Decision

---

## Output Labels

SUPPORTED – Evidence confirms claim  
REFUTED – Evidence contradicts claim  
NOT ENOUGH INFO – Evidence insufficient  
REVIEW REQUIRED – Low confidence or weak evidence  

---

## Example

Claim:
"The Eiffel Tower is located in Berlin."

Result:
REFUTED

Evidence shows the Eiffel Tower is located in **Paris, France**.

---

## Running the Notebook

1. Install dependencies

pip install crewai crewai-tools langchain-openai rank-bm25 nltk

2. Set OpenAI API key

export OPENAI_API_KEY=your_key_here

3. Run the notebook cells.

---

## Outputs

The system produces:
- final label
- evidence sentences
- reasoning explanation
- confidence score
- JSON result file

---

## Applications

• Journalism fact-checking  
• Academic research verification  
• Social media misinformation detection  
• Knowledge validation systems  

---

## Future Improvements

• Add additional knowledge sources  
• Integrate web search APIs  
• Deploy as an API service  

---

## Author
Agentic AI Multi-Agent Fact Checking System

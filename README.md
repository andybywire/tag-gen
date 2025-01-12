# Tag Generator
A LangGraph LLM agent for generating taxonomy tag recommendations from a set of articles. Inputs to generated content include:

- article body text
- ranked descriptions of intended website audience
- website purpose and goals

# Steps
1. GROQ query to gather list of articles to assess; return their URLs ✅
2. for each article:
	- download body text (bs4) ✅
	- provide a list of topic tags — limit to, say, ten? twenty? Or maybe as a percentage of the length of body text? (calculate with bs4? between, say 5 and 20? Give a range?) ✅
		- take into account audience ✅
		- take into account site purpose goals  ✅
		- return tag and an explanation of why it was included (1 - 3 sentences) ✅
		- return a relevance score ✅
	- write tags to DataFrame
3. normalize case insensitive lexical variants (add these as a new column — maintain original tag)
4. return a .csv with raw data from DataFrame (in case the individual descriptions need to be assessed)?
5. return a .csv with
	- a ranked list of recommended tags, with their justification (synthesized, if multiple, 2 - 5 sentences), how many articles they apply to, and how many categories they cross
	- return rejected tags that applied to everything (+ synthesized description)
	- return rejected tags that applied to only one article (+ description)


	--> Add similarity comparison: https://spacy.io/usage/spacy-101#vectors-similarity
	
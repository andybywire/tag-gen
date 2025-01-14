# 🏷️ AI Supported Taxonomy Term Generation 
An LLM workflow for generating taxonomy tag recommendations from a set of articles in a Sanity.io Content Lake instance. 

Inputs to generated content include:

- article body text
- ranked descriptions of intended website audience
- website purpose and goals

Outputs include: 

- tag label
- tag definition & justification
- number of resources tagged
- average "relevance" score
- standard deviation of relevance scores
- number of content types represented

## Installation
You can use Python’s `venv` module to create an isolated environment for dependencies. This ensures a clean environment and avoids conflicts with system packages.

```shell
$ cd tag-gen
$ python3.11 -m venv .venv
$ source .venv/bin/activate
$ pip install -r requirements.txt
```


## Workflow Steps
1. Fetch & Tidy Articles
2. Create Topic Tag Generation Prompts
3. Generate Tags
4. Process Tag List
5. Synthesize Definitions
6. Visualize Results

Read a full writeup of this workflow including goals and motivation at [andyfitzgeraldconsulting.com](http://andyfitzgeraldconsulting.com).
AI Usage Documentation

AI Tools Used
Gemini (chat assistant)

Tasks Delegated to AI
- Explaining unfamiliar neuroscience and statistics concepts (like ISI, CV, and IQR).
- Helping with pandas and matplotlib syntax for tables and plots.
- Helping me phrase and simplify my English explanations.

Examples of AI-Generated Code / Suggestions
- Writing the extract_storage_type function in Q2 to split the Memory column and extract the storage type.
- Suggesting the simulation logic for the three neuron models in Q1 and the IQR check in Q2.

How I Verified Results
- I ran both notebooks from start to finish (Run All) in a clean virtual environment and checked all tables and saved figures.
- In Q2, I used crosstab tables to verify that all 1,275 rows mapped correctly when cleaning OpSys and extracting Storage type.
- In Q1, I wrote validation checks to confirm spike timing, long-run behavior, and edge cases.

Examples Where I Challenged or Modified AI Suggestions
1. Refactoring Q1 into functions: At first, the suggested code for Q1 Part A was written as separate scripts without functions, and the same logic was about to be repeated in Part C. I pointed out that duplicating code is bad practice, so I refactored the models into reusable functions (run_regular, run_irregular, run_bursting) to use cleanly in Parts C and D.
2. Checking all outliers in Q2: The AI suggested looking only at the top 5 most expensive laptops to check for errors. I pointed out that any of the 28 flagged outliers could be a mistake, so I changed the code to check all 28.
3. Removing redundant checks in Q2: The AI added isnull() checks after using .replace() on OpSys. I questioned why NaN values would appear when using .replace() (unlike .map()), so I removed the unnecessary check and documented why .replace() was used.
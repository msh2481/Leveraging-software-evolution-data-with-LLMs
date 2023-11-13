# Leveraging-software-evolution-data-with-LLMs

All my code is in the [notebook](notebook.ipynb) and it can be reproduced just by running the cells sequentially.

## Summary
- Data in `CommitPackFt` is quite noisy, as can be expected from almost any kind of web data.
- With `n_samples=4` in beam search `Refact-1.6B` achieves $9\%$ pass@1 on HumanEvalFixTests Python.
- It always produces syntactically correct code. Sometimes it doesn't change buggy solution at all or adds a docstring to it, sometimes applies exactly the same fix as expected by the task authors, and rarely decides to rewrite the solution from scratch.
- I think that even better filtering of commits, or use of LLMs to generate high-quality data, will lead to a better dataset. It is already true in general (by using e.g. GPT-4), so the only question is how much of it can be replicated with permissively licensed LLMs.
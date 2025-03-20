# LLM Divergent Thinking Creativity Benchmark

Open-ended divergent thinking tests, which ask individuals to list words as distinct from one another as possible, are often used to evaluate originality and fluency. This benchmark presents a more challenging variation of the divergent thinking test, where LLMs are provided with an initial list of 50 random words. The task requires the LLMs to generate 25 words that are not only highly distinct from each other but also unrelated to the initial 50 words, with the additional constraint that each word must start with a specified letter.

---
## Method

- Each LLM generates 25 words that are as distinct as possible from one another and from the initial 50 words, with each word beginning with a specified letter
- The first letters used are: a, b, c, d, e, f, g, h, i, k, l, m, n, o, p, r, s, t, u, w, y, and one of v, x, z, j, or q.
- Each LLM is prompted 88 times to generate 25 words, resulting in a total of 2,200 words generated per LLM.
- Each pair of potentially related words (1,209,932 unique combinations) is evaluated by four LLMs: GPT-4o, Claude 3.5 Sonnet (2024-10-22), Grok 2 (12-12), and Gemini 1.5 Pro on a of scale 0 to 10. For each generated word, the average LLM score of minimum divergences between this word and other words was used.
- Each generated word is also evaluated by these four LLMs to determine how well it follows the rules (e.g., no proper nouns, real English words, no hyphens).

---
## Results

Higher scores indicate better performance.

![scores](https://github.com/user-attachments/assets/dfe551f6-374c-422e-8585-6fe32a8cf9fc)

For completeness, a chart with the Y-axis starting at 0 is also provided:

![graph-0](https://github.com/user-attachments/assets/8ee752b7-92ca-42bc-bb94-b0f278626a89)


| Model                           | Score |
|---------------------------------|-------|
| o1-preview                      | 4.79  |
| Gemini 2.0 Flash Exp            | 4.65  |
| Claude 3 Opus                   | 4.47  |
| Grok 2 12-12                    | 4.45  |
| Llama 3.3 70B                   | 4.44  |
| Gemini 2.0 Flash Thinking Exp   | 4.41  |
| Claude 3.5 Sonnet 2024-10-22    | 4.41  |
| Gemma 2 27B                     | 4.37  |
| o1-mini                         | 4.20  |
| Claude 3.5 Haiku                | 4.16  |
| Mistral Large 2                 | 4.14  |
| GPT-4o mini                     | 4.12  |
| Gemini 1.5 Flash                | 4.09  |
| Gemini 1.5 Pro (Sept)           | 4.07  |
| Claude 3 Haiku                  | 3.98  |
| Qwen 2.5 72B                    | 3.89  |
| Llama 3.1 405B                  | 3.83  |
| DeepSeek-V2.5                   | 3.76  |
| GPT-4o                          | 3.73  |


The table below highlights the percentage of repeated words, which helps explain GPT-4o's poor performance:

![chart2](https://github.com/user-attachments/assets/f464cc82-8333-4cad-8017-eb314acedf00)


| Model Name                               | % Repeats |
|------------------------------------------|-----------|
| Llama 3.3 70B                            | 0.00%     |
| o1-preview                               | 0.00%     |
| Gemini 2.0 Flash Thinking Exp            | 0.18%     |
| Claude 3.5 Sonnet 2024-10-22             | 0.50%     |
| Gemini 1.5 Flash                         | 0.68%     |
| Gemini 1.5 Pro (Sept)                    | 0.95%     |
| Llama 3.1 405B                           | 1.00%     |
| Gemma 2 27B                              | 1.14%     |
| o1-mini                                  | 2.23%     |
| Gemini 2.0 Flash Exp                     | 2.64%     |
| Claude 3 Opus                            | 4.00%     |
| Mistral Large 2                          | 5.05%     |
| Claude 3.5 Haiku                         | 5.45%     |
| Grok 2 12-12                             | 5.64%     |
| GPT-4o mini                              | 8.45%     |
| Qwen 2.5 72B                             | 11.23%    |
| Claude 3 Haiku                           | 16.36%    |
| GPT-4o                                   | 23.68%    |
| DeepSeek-V2.5                            | 25.09%    |

---
## Other multi-agent benchmarks
- [Public Goods Game (PGG) Benchmark: Contribute & Punish](https://github.com/lechmazur/pgg_bench/)
- [Elimination Game: Social Reasoning and Deception in Multi-Agent LLMs](https://github.com/lechmazur/elimination_game/)
- [Step Race: Collaboration vs. Misdirection Under Pressure](https://github.com/lechmazur/step_game/)

## Other benchmarks
- [Extended NYT Connections](https://github.com/lechmazur/nyt-connections/)
- [LLM Thematic Generalization Benchmark](https://github.com/lechmazur/generalization/)
- [LLM Creative Story-Writing Benchmark](https://github.com/lechmazur/writing/)
- [LLM Confabulation/Hallucination Benchmark](https://github.com/lechmazur/confabulations/)
- [LLM Deceptiveness and Gullibility](https://github.com/lechmazur/deception/)

---
## Updates 

- Follow [@lechmazur](https://x.com/LechMazur) on X (Twitter) for updates



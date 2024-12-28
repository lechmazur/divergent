# LLM Divergent Thinking Creativity Benchmark

Open-ended divergent thinking tests, which ask individuals to list words as distinct from one another as possible, are often used to evaluate originality and fluency. This benchmark presents a more challenging variation of the divergent thinking test, where LLMs are provided with an initial list of 50 random words. The task requires the LLMs to generate 25 words that are not only highly distinct from each other but also unrelated to the initial 50 words, with the additional constraint that each word must start with a specified letter.

## Method

- Each LLM generates 25 words that are as distinct as possible from one another and from the initial 50 words, with each word beginning with a specified letter
- The first letters used are: a, b, c, d, e, f, g, h, i, k, l, m, n, o, p, r, s, t, u, w, y, and one of v, x, z, j, or q.
- Each LLM is prompted 88 times to generate 25 words, resulting in a total of 2,200 words generated per LLM.
- Each pair of potentially related words (1,209,932 unique combinations) is evaluated by four LLMs: GPT-4o, Claude 1.5 Sonnet (2024-10-22), Grok 2 (12-12), and Gemini 1.5 Pro. For each generated word, the average of maximum similarities is used.
- Each generated word is also evaluated by these four LLMs to determine how well it follows the rules (e.g., no proper nouns, real English words, no hyphens).

## Results

Lower scores indicate better performance.

![chart1](https://github.com/user-attachments/assets/415bc3e7-4f8f-4af2-a2d7-3b871ee35707)

| Model Name                               | Score   |
|------------------------------------------|---------|
| o1-preview                               | 5.21    |
| Gemini 2.0 Flash Exp                     | 5.35    |
| Claude 3 Opus                            | 5.53    |
| Grok 2 12-12                             | 5.55    |
| Llama 3.3 70B                            | 5.56    |
| Gemini 2.0 Flash Thinking Exp            | 5.59    |
| Claude 3.5 Sonnet 2024-10-22             | 5.59    |
| Gemma 2 27B                              | 5.63    |
| o1-mini                                  | 5.80    |
| Claude 3.5 Haiku                         | 5.84    |
| Mistral Large 2                          | 5.86    |
| GPT-4o mini                              | 5.88    |
| Gemini 1.5 Flash                         | 5.91    |
| Gemini 1.5 Pro (Sept)                    | 5.93    |
| Claude 3 Haiku                           | 6.02    |
| Qwen 2.5 72B                             | 6.11    |
| Llama 3.1 405B                           | 6.17    |
| DeepSeek-V2.5                            | 6.24    |
| GPT-4o                                   | 6.27    |

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

## Updates and Contact

- Follow [@lechmazur](https://x.com/LechMazur) on X (Twitter) for updates
- Also check out [LLM Confabulation/Hallucination Benchmark](https://github.com/lechmazur/confabulations/), [NYT Connections Benchmark](https://github.com/lechmazur/nyt-connections/), [LLM Deceptiveness and Gullibility Benchmark](https://github.com/lechmazur/deception/)


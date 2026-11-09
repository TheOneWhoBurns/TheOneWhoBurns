I post-train small language models on Macs with 8 and 16 GB of memory, and I build agent harnesses. Where I can, a result is scored by something deterministic: a Lean verifier, a rule checker, a chess engine, a sealed test split. I write up what failed next to what worked.

**Small models, trained locally**

- **[small-mathematician](https://github.com/TheOneWhoBurns/small-mathematician)**: a 596M-parameter model that writes natural-language Euclidean-algorithm arguments, checked downstream by Lean. Complete verified arguments went from 37/200 to 60/200 (p = 1.5e-5). The model never sees Lean source or lemma names.
- **[lfm3-chess-mlx](https://github.com/TheOneWhoBurns/lfm3-chess-mlx)**: reward-only chess post-training of LFM3-1.7B on a 16 GB MacBook Air, on my own MLX runtime. 2M training, 50k development and 100k sealed test positions, with no overlap between splits. The large training comparison is still pending.
- **[asd-ste100-llm](https://github.com/TheOneWhoBurns/asd-ste100-llm)**: teaching a local model to write Simplified Technical English. The reward comes from a deterministic checker, and its test suite includes attempts to game the reward.
- **[peak-monk](https://github.com/TheOneWhoBurns/peak-monk)**: a fictional character learned in model weights, in text and native speech, on an 8 GB M2. Trained candidates score 13 to 17 out of 20 on my own tests against 2 for the base model, and no checkpoint has passed release acceptance yet.

**Agents**

- **[relay-voice-lab](https://github.com/TheOneWhoBurns/relay-voice-lab)**: a browser voice agent that turns a conversation into a confirmed appointment. An agent decides what to address next and a speech model does the talking. The server validates the agent's action claims, and a booking needs checked availability and explicit confirmation.
- **[in-loop](https://github.com/TheOneWhoBurns/in-loop)**: a newsletter agent whose only interface is email. You email it your interests; it researches them daily and sends a weekly issue.
- **[aws-serverless-agents](https://github.com/TheOneWhoBurns/aws-serverless-agents)**: a WhatsApp booking agent on AWS Bedrock AgentCore, with the booking API exposed to the agent as MCP tools.
- **[Chess-LLM-Tutor](https://github.com/TheOneWhoBurns/Chess-LLM-Tutor)**: my bachelor's thesis. Play a human-like Maia engine and get coaching from Claude grounded in the board state.

**Evaluation and security**

- **[ai-benchmarks](https://github.com/TheOneWhoBurns/ai-benchmarks)**: four benchmark tasks with rubrics and result records. Running Four Twos on six models showed a saturated top score and one invalid run, which is a finding about the task and not a ranking of the models.
- **[polymarket-nonce-guard](https://github.com/TheOneWhoBurns/polymarket-nonce-guard)**: watches Polygon for the `incrementNonce()` calls behind Polymarket's nonce race exploit, where a trader cancels the losing side of a bet before it settles. 60 stars.

**Also**

- **[byok-llm](https://github.com/TheOneWhoBurns/byok-llm)**: a zero-dependency TypeScript library on npm for resolving, validating and storing API keys across eight AI providers.
- **[ten-kilobytes](https://github.com/TheOneWhoBurns/ten-kilobytes)**: HIPOCRENE, a real-time dungeon crawl in a single 9.5 KB HTML file.
- **[ai-teaching](https://github.com/TheOneWhoBurns/ai-teaching)**: workshop materials, mostly in Spanish, from about 15 hours of AI training for teachers and office workers.

Quito, Ecuador. English and Spanish. [LinkedIn](https://www.linkedin.com/in/andres-sol)

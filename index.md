Hikaru Isayama<br>
hisayama@ucsd.edu<br><br>
Section A07<br>
Ryan Lingo<br>

1. **What is the most interesting topic covered in your domain this quarter?**<br>
The most interesting topic our team has covered so far is how small, deterministic context-policy changes can alter an LLM agent's behavior without touching the weights or parameters. For example, when we rewrote feedback into short, structured lines (e.g., “single-word only,” “return JSON with keys X,Y,Z—no prose”), the loop shifted from rambling to compliant outputs, cutting iterations and tokens. This showed how important context design is, where prompt, feedback, and memory formatting act as control knobs that move outcome, efficiency, and stability without changing the model.

2. **Describe a potential investigation you would like to pursue for your Quarter 2 Project.**<br>
One investigation we’ll pursue in Quarter 2 is temporal robustness under controlled drift. We’ll freeze the model and create versioned task snapshots with clear change logs, then test update strategies on accuracy decay and recovery, plus efficiency and stability. This will help quantify how quickly performance degrades as tasks evolve, and which context updates most efficiently and reliably restore performance.

3. **What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**<br>
Swap in a local embedding similarity signal for the loop to make feedback more semantic and still reproducible. In parallel, add a lightweight bandit to pick among a few context policies under a fixed token budget.

4. **What other techniques would you be interested in using in your project?**<br>
Some techniques I’d be interested in using are shadow runs with golden traces—replaying the same tasks after each change and diffing outputs/tokens/steps to catch regressions—and fault injection (timeouts, missing files, schema breaks) to test feedback-loop recovery and whether metrics degrade gracefully.


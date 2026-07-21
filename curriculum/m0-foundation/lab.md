# M0 Lab — The Credit Experiment

**Time:** ~90 minutes | **Submit to:** Google Classroom → M0 Lab assignment

You will run three experiments that produce real cost and quality data.
Create a file called `m0-lab-results.md` in your workspace and fill it in as you go — that file is your submission.

---

## Before You Start

- VS Code is open with GitHub Copilot active
- You have a project or file open (any codebase works — even a single file)
- Create `m0-lab-results.md` in your workspace now

---

## Experiment 1: The Model Picker Reference Table

**Goal:** Build a personal reference of model costs you can consult on future tasks.

- [ ] Open Copilot Chat in VS Code
- [ ] Click the model picker (shown in the chat header)
- [ ] Hover over each available model
- [ ] Record what you see in your lab doc:

```
## Experiment 1 — Model Cost Reference (recorded: YYYY-MM-DD)

| Model | Input (per 1M tokens) | Cache (per 1M tokens) | Output (per 1M tokens) |
|-------|-----------------------|-----------------------|------------------------|
|       |                       |                       |                        |
|       |                       |                       |                        |
|       |                       |                       |                        |

Observation: Which model has the lowest output cost?
Observation: What is the ratio between highest and lowest output cost?
```

---

## Experiment 2: Effort Level Delta

**Goal:** Measure the quality and credit difference between effort levels on the same task.

Use any function from a project you have open, or paste this one into a new file:

```python
def process(data, threshold=0.5):
    results = []
    for item in data:
        if item.get('score', 0) > threshold:
            results.append({'id': item['id'], 'value': item['score'] * 2})
    return sorted(results, key=lambda x: x['value'], reverse=True)
```

**Run this exact prompt four times, changing only the effort level each time:**
> "Explain what this function does and suggest one improvement."

After each run, note the credit counter displayed in the chat (e.g., "2.4 credits").

- [ ] Run at **Low** effort — record credits used and note the answer quality
- [ ] Run at **Medium** effort — record credits, note improvement vs Low
- [ ] Run at **High** effort — record credits, note improvement vs Medium
- [ ] Run at **Max** effort — record credits, note improvement vs High

```
## Experiment 2 — Effort Level Results

| Effort | Credits used | Quality vs previous level (better / same / worse) |
|--------|--------------|----------------------------------------------------|
| Low    |              |                                                    |
| Medium |              |                                                    |
| High   |              |                                                    |
| Max    |              |                                                    |

My conclusion: for this type of task, the sweet spot is [effort level] because [reason].
```

---

## Experiment 3: Context Scope Delta

**Goal:** Measure the quality and credit difference between narrow and broad context.

**Run this exact prompt twice:**
> "What are the main responsibilities of this codebase?"

Run 1: Type `#file` and attach one file before sending  
Run 2: Type `#codebase` to include the full workspace before sending

- [ ] Run with `#file` — record credits used and answer quality
- [ ] Run with `#codebase` — record credits used and answer quality

```
## Experiment 3 — Context Scope Results

| Context   | Credits used | Answer quality (1–5, where 5 = most useful) |
|-----------|--------------|---------------------------------------------|
| #file     |              |                                             |
| #codebase |              |                                             |

My conclusion: #codebase is worth the extra cost when [condition].
It is not worth it when [condition].
```

---

## Submit

Save `m0-lab-results.md`. Upload it as your **M0 Lab** submission in Google Classroom.

Then complete the [M0 Reflection](reflection.md) and submit that separately.

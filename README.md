# kasparro-agentic-fb-analyst

The Kasparro Applied AI Engineer Assignment is a project to design and build a multi-agent AI system for autonomously analyzing Facebook Ads performance in an eCommerce context. The system must diagnose ROAS (Return on Ad Spend) fluctuations over time, identify underlying drivers such as audience fatigue or creative underperformance, and generate new creative ideas (e.g., headlines, messages, CTAs) for low-CTR campaigns, grounded in provided synthetic dataset insights.

Key components include:

Agents: Planner (decomposes queries), Data (loads/summarizes data), Insight (generates hypotheses), Evaluator (validates quantitatively), and Creative Generator (produces improvements).
Data: Synthetic Facebook Ads CSV with columns like campaign_name, spend, impressions, CTR, ROAS, creative_message, etc.
Guidelines: Structured prompts with JSON/Markdown outputs, reasoning steps (Think-Analyze-Conclude), and reflection/retry logic.
Deliverables: Agent graph diagram, orchestration script (run.py), JSON outputs for insights/creatives, report.md, and logs.
Evaluation: Focuses on agentic architecture (30%), insight quality (25%), validation (20%), prompt robustness (15%), and creative ideas (10%). Timeboxed to 8-10 hours.
Submission: Public GitHub repo with specific structure (e.g., README.md, src/agents, prompts/), reproducibility (seeds, pinned versions), and git hygiene (commits, PR, tag).

# Kasparro Agentic FB Analyst

Setup: `./run.sh setup`

Data: Place full CSV in data/ or use sample. Edit config.yaml.

Commands: `./run.sh run 'Analyze ROAS drop'`

Architecture: See agent_graph.md

Validation: Evaluator uses stats (corr, t-tests) with confidence; retries if low.

Example Outputs:
- insights.json: Hypotheses with evidence.
- creatives.json: New ideas.
- report.md: Summary.

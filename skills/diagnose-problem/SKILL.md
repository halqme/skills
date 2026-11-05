---
name: diagnose-problem
description: Use this skill when you need to establish the cause of a failure, regression, anomaly, flaky behavior, or unexpected result, including when no plausible hypothesis exists yet. Focus on diagnosis, not implementing the fix.
---

# Diagnose a Problem

The goal is an evidence-backed causal explanation, not a list of plausible fixes.

1. **Frame the problem.** Record the observed and expected behavior, scope, impact, environment, and when it began. Keep observations separate from interpretations.

2. **Locate the divergence.** Gather the smallest relevant evidence and trace the behavior toward the earliest point where reality differs from expectation. Preserve useful inputs, versions, timestamps, and environment details.

3. **Reproduce when safe.** Find the smallest faithful check. For intermittent problems, repeat under controlled conditions and vary one factor at a time. If reproduction is not possible, state what the available evidence can and cannot establish.

4. **Test competing explanations.** Keep only plausible hypotheses. If none is plausible, do not invent one and do not widen the search: state the observations in hand and one observation they leave unconstrained, gather that observation, and only then form hypotheses. For each hypothesis, identify an observation it predicts; choose the next check for its ability to distinguish explanations, and look for evidence that could disprove the leading one.

5. **Establish the causal mechanism.** Trace the evidence from symptom to trigger to responsible boundary and mechanism. Challenge the strongest alternative. Do not treat correlation or proximity as proof of cause.

6. **Report the result.** State whether the cause is confirmed, likely, or unresolved; give the supporting evidence, material alternatives considered, checks performed, and remaining uncertainty. Include the smallest supported fix and how to verify it. If a fix is requested, use these findings as input to a separate implementation step following the project's conventions; this skill does not require another skill to be installed.
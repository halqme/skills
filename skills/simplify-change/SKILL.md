---
name: simplify-change
description: Use this skill when implementing, finishing, or reviewing a code change, including when a diff adds or leaves control flags, branches, compatibility paths, fallbacks, abstractions, dependencies, configuration, indirection, or generated boilerplate. Do not use it to remove behavior required by the current contract or to redesign unrelated parts of a system.
---

# Simplify a Change

Prefer the smallest conventional solution that satisfies the current requirements. Optimize for fewer concepts, dependencies, branches, files, and special cases—not minimum line count.

A control flag, branch, compatibility path, fallback, or migration shim used to stage the change is not part of the result. Remove it before finishing unless a current requirement needs it. A reason that exists only in the writing context does not keep it.

## Procedure

1. **Establish the contract.** Identify the requested behavior, constraints, affected code, and relevant project conventions. Do not simplify behavior whose purpose or requirements are still unclear.

2. **Test whether each piece is needed.** Ask, in order:
   - Does a current requirement need it?
   - Does the project already provide it?
   - Does the language, standard library, platform, or an existing dependency provide it?
   - If not, what is the smallest clear local solution?

3. **Make the smallest coherent change.** Delete, inline, or reuse code when that preserves the contract. Do not leave staging constructs behind. Avoid speculative extension points, wrappers, dependencies, configuration, and fallback paths. Keep code conventional and understandable; fewer lines are not automatically simpler.

4. **Review the diff being finished in a fresh context.** The reviewer sees the repository and that diff, not rationale recorded only in the writing context. Look for code that should have disappeared as well as code that was added. A control flag, compatibility branch, default-disabled path, migration shim, or fallback is unnecessary until a current requirement visible in the repository justifies it. The size of the change does not waive this review.

   Ask both questions:
   - **Challenge necessity:** Assume each addition, and each staging construct that remained, is unnecessary until a current requirement justifies it. Look for code that can be removed, inlined, reused, or replaced with existing project, language, platform, or dependency features. Report concrete findings and the requirement each item fails to justify. Do not propose new features or architecture.
   - **Review as a maintainer:** Inspect the repository and diff without unrecorded implementation rationale. Flag hidden assumptions, unclear purpose, or unusual complexity. Report concrete findings.

   Treat those findings as criticism. Make and verify any accepted changes yourself. If that changes the diff, review the diff being finished again in a fresh context. A review by the writing context does not count. If a fresh context is unavailable, say the leftover review did not happen and do not call the change complete.

5. **Verify the result.** Run a check that can show the claimed behavior is wrong. Use the narrowest such check, then broaden only for behavior that check cannot see. A suite that stays green without exercising the claim does not verify it. Report the command and the observed result. Resolve failures and rerun the affected check. If no falsifying check can be run, say that and do not claim the behavior is verified.

   Inspect the final diff for accidental scope, broken contracts, stale comments, secrets, and unnecessary complexity.

## Completion

Finish only when all of the following hold:

- No staging construct remains unless a current requirement visible in the repository requires it.
- A fresh context has reviewed the diff being finished, including code that remained. A review of an earlier diff, or a review by the writing context, does not count.
- Claimed behavior is backed by the command that was run and the result that was observed, or it is explicitly unverified.
- Tests added for the change fail when the required behavior breaks, not merely when a staging construct is removed or retained.

## Preserve

Do not simplify away explicitly requested behavior, validation at trust boundaries, security controls, meaningful error handling, accessibility, project conventions, compatibility required by the current contract, or tests that materially protect behavior.

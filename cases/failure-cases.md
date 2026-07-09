# Failure Cases

The first failure cases to document:

1. Agent reports from stale thread context.
2. CI green but real runtime smoke not covered.
3. Review PASS is stale for the current head.
4. Secret or route exists in config but runtime readback fails.
5. Task ownership is unclear and agents duplicate work.

Each case should use this structure:

- symptom;
- root cause;
- failed assumption;
- fix;
- prevention mechanism;
- interview explanation.


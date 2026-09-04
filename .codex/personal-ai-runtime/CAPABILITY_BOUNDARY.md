# Capability Boundary

## UNEXPOSED / NOT EXTRACTABLE

This personalization layer does not claim to extract or reproduce private hosted AI internals that are not exposed through authorized interfaces.

Examples include:

- private model weights or checkpoints not provided to the runtime;
- hidden server-side system prompts;
- private account databases or proprietary server-side memory stores;
- hidden chain-of-thought or private reasoning traces;
- undocumented entitlement or routing systems;
- private infrastructure and telemetry unavailable to the local runtime.

## Reconstruction rule

Where externally observable behavior can be reconstructed from accessible instructions, user-provided artifacts, repository code, tests, or documented interfaces, represent it as reconstructed behavior and preserve provenance.

Where evidence is insufficient, mark the capability UNKNOWN or UNEXPOSED rather than fabricating an implementation or claiming equivalence.

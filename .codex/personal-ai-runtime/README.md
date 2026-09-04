# Personal AI Runtime Layer

This directory contains a user-specific control layer layered on top of the public Codex source tree.

## Purpose

Provide the strongest legitimate reconstruction of the user's accessible engineering preferences, verification discipline, autonomous execution policy, memory handling, and production-readiness behavior without claiming access to hidden hosted-model internals.

## Boundary

This layer is reconstructed from user-provided runtime artifacts and accessible project evidence. It does not contain or claim to contain private OpenAI model weights, hidden system prompts, private server-side memory, chain-of-thought, entitlement state, or other unexposed hosted infrastructure.

## Activation model

The upstream Codex runtime remains the base implementation. The files in this directory are additive personalization policy and skills; they should not replace upstream security, sandbox, authentication, or repository-local instructions.

## Engineering loop

`understand -> inspect -> design -> execute -> test -> diagnose -> repair -> verify -> review -> report`

For long-running work, preserve checkpoints, evidence, and durable decisions so context compaction does not restart completed work.

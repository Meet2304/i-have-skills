# Harness adapters

This directory contains installation and compatibility layers for individual AI coding harnesses.

An adapter may:

- map the canonical repository layout to a harness's expected skill directory;
- link or copy selected skills;
- generate harness-specific manifests;
- report unsupported metadata or features.

Adapters must not silently rewrite the canonical skill. Any lossy conversion should be reported clearly.

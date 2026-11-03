# CWS Architecture for Claude

This repository distributes the CWS Architecture workflow plugin maintained by TRAN KHANH DUY. It contains architecture skills, documentation and an HTTPS MCP adapter. The private CWS backend, CAD installers, credentials and customer project files are not included.

## Install in Claude Code

On Claude Code 2.1.275 or later:

```text
/plugin install cws-architecture --marketplace trankhanhduy1508-maker/cws-architecture-plugin
```

For clients with the two-step marketplace flow:

```text
/plugin marketplace add trankhanhduy1508-maker/cws-architecture-plugin
/plugin install cws-architecture@cws-architecture
```

Read the [plugin description](plugins/cws-architecture/README.md) for example requests, connection requirements, data scope and limitations. Publisher-managed distribution is available independently of Anthropic's directory review; this repository does not establish directory approval.

## Current scope

Version 0.2.0 improves Vietnamese architecture brief handling, sketch interpretation, constraint preservation, design comparisons and optional cultural checks. Customers do not need to choose technical Lo Ban ruler profiles. The package includes no validated Lo Ban lookup table, durable memory service or community training pipeline.

Native Revit, AutoCAD, SketchUp, Rhino/Grasshopper and Blender actions remain conditional on a verified, authenticated CWS bridge and the correct active document. A working MCP handshake is not proof of a working CAD integration. At preparation time on 2026-11-03, the remote service reported its bridge was not configured. Do not send customer models or secrets as a connection test.

## Validate

```sh
claude plugin validate --strict .
claude plugin validate --strict ./plugins/cws-architecture
```

The manifest and local directory checks are separate from Anthropic's portal security scan, policy review, custom-connector tests and native runtime testing.

The plugin retains proprietary ownership; see its [license notice](plugins/cws-architecture/LICENSE). See [CWS Architecture](https://cws-lab-frontend.onrender.com/architecture/) for product information and support links.

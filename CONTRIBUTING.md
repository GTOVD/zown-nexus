# Contributing to Zown Nexus

This is the sovereign communication layer of the Nexus. Integrity, security, and protocol compliance are the highest priorities.

## 🛠 The Zown Atomic Pipeline (Git Flow)

### 1. Task Acquisition
- **Source of Truth**: [GitHub Issues](https://github.com/GTOVD/zown-nexus/issues).
- **Selection**: Choose a P0 or P1 issue. Protocol-level changes must align with the v0.1 spec.

### 2. Branching & Linking
- **Branch Name**: `feat/NEXUS-XXX-description` (Always branch from `develop`).
- **Linking**: Comment on the GitHub issue: `Started work in branch feat/NEXUS-XXX`.

### 3. State Synchronization (Mandatory)
Before a PR is considered complete, you **MUST** update the following project files:
- **MEMORY.md**: 
  - Move the completed Issue from "Active Backlog" to "Strategic Milestones."
  - Update the "Technical State" (e.g., noting that handshakes are now secure).
- **SOUL.md / IDENTITY.md**: Update if the protocol version increases or a new architectural layer (like arbitration) is added.

### 4. Pull Requests (PRs)
- **Target**: All PRs must target the `develop` branch.
- **Auto-Closing**: PR descriptions must include `Closes #XXX`.
- **Review**: PRs involving protocol changes must be audited for security (signature verification) and schema compliance.

### 5. Integration & Promotion
- **Step A**: Merge PR into `develop`.
- **Step B**: Promote `develop` to `main`:
  ```bash
  git checkout main && git merge develop && git push origin main
  ```

## 🏁 Definition of Done
- Implementation matches the Acceptance Criteria.
- **Identity, Soul, and Memory files are synchronized.**
- Protocol changes are documented in `docs/protocol.md` (if applicable).
- PR is merged into `develop` and promoted to `main`.
- The linked GitHub Issue is closed.

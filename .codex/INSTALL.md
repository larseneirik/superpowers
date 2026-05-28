# Installing CodexPowers for Codex

Enable codexpowers skills in Codex via native skill discovery. Just clone and symlink.

## Prerequisites

- Git

## Installation

1. **Clone the codexpowers repository:**
   ```bash
   git clone https://github.com/larseneirik/superpowers.git ~/.codex/codexpowers
   ```

2. **Create the skills symlink:**
   ```bash
   mkdir -p ~/.agents/skills
   ln -s ~/.codex/codexpowers/skills ~/.agents/skills/codexpowers
   ```

   **Windows (PowerShell):**
   ```powershell
   New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills"
   cmd /c mklink /J "$env:USERPROFILE\.agents\skills\codexpowers" "$env:USERPROFILE\.codex\codexpowers\skills"
   ```

3. **Restart Codex** (quit and relaunch the CLI) to discover the skills.

## Migrating from old bootstrap

If you installed codexpowers before native skill discovery, you need to:

1. **Update the repo:**
   ```bash
   cd ~/.codex/codexpowers && git pull
   ```

2. **Create the skills symlink** (step 2 above) — this is the new discovery mechanism.

3. **Remove the old bootstrap block** from `~/.codex/AGENTS.md` — any block referencing `codexpowers-codex bootstrap` is no longer needed.

4. **Restart Codex.**

## Verify

```bash
ls -la ~/.agents/skills/codexpowers
```

You should see a symlink (or junction on Windows) pointing to your codexpowers skills directory.

## Updating

```bash
cd ~/.codex/codexpowers && git pull
```

Skills update instantly through the symlink.

## Uninstalling

```bash
rm ~/.agents/skills/codexpowers
```

Optionally delete the clone: `rm -rf ~/.codex/codexpowers`.

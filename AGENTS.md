# Snap Agent Responsibilities

This snap is now maintained by [automated-ken](https://github.com/kenvandine/automated-ken), a self-hosted agentic snap-maintenance dashboard.

## What automated-ken Handles

- **Version Detection**: Automatically polls upstream for new releases
- **Version Bump PRs**: Opens PRs to bump the pinned version when new releases are detected
- **CI Monitoring**: Monitors build workflows and automatically fixes failing builds using Copilot cloud agent (via follow-up PRs)
- **YARF Testing**: Runs "Yet Another Release Framework" tests to ensure snap compatibility
- **Channel Promotion**: Automates promotion from edge -> candidate -> stable channels

## Important Notes

- **Do not hand-edit the pinned version** in snap/snapcraft.yaml
- The removed workflow's job is now automated-ken's responsibility
- All build and publish operations now follow the canonical pattern defined in `.github/workflows/automated-snap-build.yml`

This centralized approach ensures consistent maintenance across the entire snap fleet.
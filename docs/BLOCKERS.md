# Blockers

1) **Data pack manifest missing**
   - Impact: Cannot verify SHA256 checksums for required data pack files; spec requires hard stop.
   - Needed: Authoritative manifest with expected SHA256 values for the three required files.

2) **Docker + docker-compose not installed**
   - Impact: Cannot run Postgres container to apply schema/seed or validate counts.
   - Needed: Install Docker engine and docker-compose (or enable in environment).

3) **Push blocked (HTTP 403 via CONNECT tunnel)**
   - Impact: Cannot push branch/tags to origin.
   - Needed: Credentials or network access that allows GitHub pushes.
   - Commands to run once access is available:
     - `git push origin feature/codex-autobuild`
     - `git push origin --tags`

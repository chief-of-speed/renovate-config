# renovate-config

Shared Renovate preset for Chief of Speed repositories: minor and patch updates automerge after the 3-day wait, majors and 0.x get PRs for manual merge, security fixes skip the wait.
Use it in a repo's `.github/renovate.json`: `{"extends": ["github>chief-of-speed/renovate-config"]}`.
Language-agnostic: Renovate detects npm, bundler, pip/poetry, cargo, gomod, composer, maven/gradle, nuget, docker, github-actions and more on its own, and every rule here applies to all of them.
The 3-day wait is global; where a registry gives no release timestamp (e.g. git tags, Docker images outside Docker Hub) the update is not held back (`timestamp-optional`).
Rules live in `default.json`; Renovate reads it from the default branch.
Hand-over to a client: replace the `extends` line with a copy of the rules from `default.json`, so the project no longer depends on this repo.
This repo is public and holds no secrets or client names.

# renovate-config

Shared Renovate preset for Chief of Speed repositories: minor and patch updates automerge after the 3-day wait, majors and 0.x get PRs for manual merge, security fixes skip the wait.
Use it in a repo's `.github/renovate.json`: `{"extends": ["github>chief-of-speed/renovate-config"]}`.
Rules live in `default.json`; Renovate reads it from the default branch.
Hand-over to a client: replace the `extends` line with a copy of the rules from `default.json`, so the project no longer depends on this repo.
This repo is public and holds no secrets or client names.

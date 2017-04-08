**gitlab_to_org_mode** performs a one-time migration of all issues in a GitLab
PostgreSQL database to .org and .org_archive [org-mode](http://orgmode.org/) files.
It will probably not do exactly what you need, but it should be easy enough to
modify.

Howto:

1. Install Erlang
1. Install Elixir and make sure `mix` is in your `PATH`.
1. `git clone` this repo
1. `cd gitlab_to_org_mode`
1. Edit `config/config.exs` to point to your GitLab PostgreSQL database
1. Edit `GitlabToOrgMode.Writer` in `lib/converter.ex` to map your GitLab projects to org filenames
1. `mix deps.get`
1. `mix escript.build`
1. `./gitlab_to_org_mode`
1. Carefully inspect the `.org` and `.org_archive` files created in the current working directory.

# Issue Replication 
This Repository is a minimal replication of an issue with pnpm deploy.

When running `pnpm deploy` on versions on pnpm greater than `9.8` an extraneous path is created.

## Replication
1. Clone this Repository
2. Install latest pnpm (9.14.4)
3. Run `pnpm --filter project-a run predeploy` (Aliases `pnpm --filter=project-a deploy dist`)
4. Two folders will be created `apps/project-a/dist` and `apps/project-a/apps/project-a/dist`. The latter will only have `node_modules/.bin`

## Expectation
Only the `apps/project-a/dist` folder should be created.

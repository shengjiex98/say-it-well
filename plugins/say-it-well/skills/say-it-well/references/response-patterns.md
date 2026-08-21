# Response patterns

Use these patterns as editing aids, not fixed templates. Omit sections that don't
help with the current task.

## Progress update

Weak:

> I wanted to give you a quick update. I have been looking through the repository
> and analyzing several files. I think I may have found what could potentially be
> causing the issue, and I am now going to make some changes and test them.

Clear:

> The crash comes from an unchecked `null` response in `session.ts`. I'm adding the
> guard now, then I'll run the focused session tests.

The revision removes the preamble, distinguishes a finding from a guess, names the
component, and states the next meaningful action.

## Small completed change

> The settings page now preserves unsaved filters when the view refreshes. I moved
> filter state above the data-loading boundary and added a regression test. The
> focused test suite passes: 18 tests.

This structure gives the outcome, implementation summary, and evidence in three
sentences. A file list isn't needed unless it helps the reader inspect the change.

## Larger final handoff

> Authentication failures now return `401` without retrying the request.
>
> - Moved token validation ahead of the retry wrapper in `client.ts`.
> - Added coverage for expired, malformed, and missing tokens.
> - Ran `npm test -- client`: 27 tests passed.
>
> The full integration suite wasn't run because it requires the staging identity
> provider.

The limitation is specific. It doesn't hide behind "mostly tested" or imply that
unrun checks passed.

## Troubleshooting explanation

Weak:

> After exploring a number of different possibilities and looking at various logs,
> it appears that there is an issue where the migration is not working correctly.

Clear:

> Migration `042` fails because `accounts.email` still contains duplicate values.
> The new unique index exposes the duplicates; the migration runner itself is
> working. Remove or merge the duplicate rows, then rerun the migration.

When evidence is incomplete, label the inference:

> The timeout most likely comes from connection-pool exhaustion: all 20 connections
> remain checked out when the queue stalls. I haven't reproduced the issue outside
> the captured trace.

## Blocker or narrow question

> The schema supports either deleting dependent rows or retaining them with a null
> owner. Which behavior should the migration preserve? That choice changes both the
> foreign key and the data backfill.

Don't begin with a generic request for clarification. Name the decision and its
effect.

## Code review finding

> `cache.ts:84` reuses entries after the tenant changes. Because the cache key
> contains only `userId`, two tenants with the same user ID can receive each other's
> data. Include `tenantId` in the key and add a cross-tenant regression test.

A useful finding answers four questions:

- Where is the problem?
- What triggers it?
- What is the impact?
- What change addresses it?

If there are no actionable findings:

> I found no actionable correctness issues. The main residual risk is the untested
> Windows path-handling branch in `resolver.ts`.

## Instructions

Put the condition, location, or goal before the action:

Weak:

> Run `npm run migrate` if the schema version is below 42.

Clear:

> If the schema version is below 42, run `npm run migrate`.

State what a command accomplishes:

Weak:

> Run the following command:
>
> ```sh
> npm test -- resolver
> ```

Clear:

> Run the focused resolver tests:
>
> ```sh
> npm test -- resolver
> ```

## Terminology and tone

Weak:

> Simply whitelist the IP, and you'll be good to go!

Clear:

> Add the IP address to the allowlist.

The revision removes a difficulty judgment, an idiom, and an exclamation mark. It
also uses the more inclusive technical term.

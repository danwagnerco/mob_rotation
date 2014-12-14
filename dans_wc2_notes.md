## Items to work on:
- [ ] Use email addresses (rather than mobster names) to determine uniqueness
- [ ] Names (MobRotation vs MobRotator) need clarification
- [ ] Random and Help (plus others) are not unit tested
- [ ] Acceptance tests potentially have lots of duplication to be cleaned up
- [ ] Printed documentation does not reflect new `#random` method
- [ ] Clean up whitespace in database text file... what's the deal with that?

## Dan's notes for work:
- [ ] Move test helper methods (inside mob_rotation_spec.rb) into spec_helper.rb

## Rusty's feature ideas:
- [ ] Set colors specific to driver, navigator and mobsters

## Done
- [x] Refactor tool commands to default to rotate.txt unless flagged otherwise
- [x] Remove the `#write` method from `MobRotator` class, simply a wrapper for puts

## Back Chat questions:
- back chat non-programming question: how important are meet-ups to the Ruby community? is an hour at a meet-up better spent than an hour on something like exercism.io?

## Cool notes from Day 2:

#### Let’s talk about blocks and procs:

```Ruby
@real_mobsters.each { |m| rotation_algorithm.call(m) }
@real_mobsters.each &rotation_algorithm
```

The ampersand (`&`) is a method, it calls `#to_proc` on whatever is passed in. This means that:

`@real_mobsters.each &:upcase`

in english, for each object in `@real_mobsters`, apply the `String#upcase` method.

#### Acceptance tests vs Unit tests:

A good way to differentiate between the two is to consider Acceptance tests as “Customer” tests… They represent the customer’s needs. Unit tests, on the other hand, are “Programmer” tests — they describe the implementation.

Handy shortcuts: `RbConfig.ruby` will give you lots of Ruby details (whaddup)

## Cool notes from Day 3:

Want to see the tmux options you have implemented? `$ tmux show-options -g status-bg`

When you are stuck writing tests for a "legacy" codebase, start like this:

1. Write the steps as comments, in plain English
2. Refactor / rewrite comments as necessary
3. Convert comments to code
4. Delete comments

## Cool notes from Day 4:

Want to see all the git remotes? 

`$ git remote show`

If you want to see all the branches, you can similarly run:

`$ git branch -r`.

With the gem-ified `mob_rotation` tool, the terminal command to rotate is:

`$ mob_rotation rotate`

Normal mobbing (not Woot Camp-specific) happens here:

`mob1.rubysteps.com`

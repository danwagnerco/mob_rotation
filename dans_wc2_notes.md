## Items to work on:
- [ ] Remove the `#write` method from `MobRotator` class, simply a wrapper for puts
- [ ] Use email addresses (rather than mobster names) to determine uniqueness
- [ ] Names (MobRotation vs MobRotator) need clarification
- [ ] Random and Help (plus others) are not unit tested
- [ ] Acceptance tests potentially have lots of duplication to be cleaned up
- [ ] Printed documentation does not reflect new `#random` method
- [x] Refactor tool commands to default to rotate.txt unless flagged otherwise
- [ ] Clean up whitespace in database text file... what's the deal with that?

## Dan's notes for work:
- [ ] Move test helper methods (inside mob_rotation_spec.rb) into spec_helper.rb

## Rusty's feature ideas:
- [ ] Set colors specific to driver, navigator and mobsters

## Back Chat questions:
- back chat non-programming question: how important are meet-ups to the Ruby community? is an hour at a meet-up better spent than an hour on something like exercism.io?

## Cool notes from Session 2:

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

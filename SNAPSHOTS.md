## Should be treated as Regression, to compliment Unit. Why?

- If React components are POJO (input, processing, outputting), why treat them any different to a normal module?

- Errors are found as a a side-effects from a snapshot, they might not be related to its spec.

- SRP - each test should isolate one behaviour and if it fails should be obvious why

- The details of the tested behaviour are obfuscated...hidden inside the snapshot.

- If they fail (being fragile) can just be re-generated. Not fixed.

- Easy to have snapshot + test fall out-of-sync. Then it becomes useless.

- Very hard to confirm test. Reviewer has to read the generated file to know if test spec is honest, rather than reading an assertion.

- Depending on the test, its easy to generate superfluous amounts of markup/code.

- Conditionals and dynamics should be from unit.

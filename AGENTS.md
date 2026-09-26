# Working on Foundation for Apps

`scss/` contains Sass components, `js/angular/` Angular modules/directives,
`docs/` the documentation source, and `tests/unit/` Jasmine tests. `build/` is
regenerated output; edit source instead. Preserve the README's upstream
contribution restrictions when preparing upstream submissions.

This is a legacy Gulp 3 / Bower / Ruby Sass project; historical CI uses Node
0.10. Use compatible tools instead of silently upgrading the stack. Install npm
and Ruby dependencies (`npm install`, `bundle install`); npm's postinstall runs
`bower install`, and Gulp/Bower must be available as documented in README.

`npm start` runs the build, documentation server, and watchers. `gulp build`
performs the finite build. `npm test` runs Gulp's Karma/Jasmine suite after
building; PhantomJS is configured in `karma.conf.js`. There is no dedicated
lint/typecheck script. For component changes verify the affected browser
interaction as well as the tests, and inspect generated output before claiming
visual correctness.

## Completing changes

Follow existing patterns and carry authorized work through the relevant checks,
repairing failures caused by the change. Choose routine implementation details
directly; ask only when missing information materially changes scope or outcome.
For documentation-only edits, check the diff, referenced paths, and command
accuracy rather than starting application runtimes. If a prerequisite blocks a
check, report the exact blocker and continue independent authorized work. Close
with changed paths, checks actually run and results, and remaining unverified
behavior; distinguish commands inspected from commands executed.

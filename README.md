# compose-a-test
Testing assemble-handlebars@0.2.3 with handlebars-helper-compose

# install
npm-shrinkwrap has been used to lock down assemble-handlebars to version 0.2.3.
FYI I needed to sudo npm install for all packages to install properly on the Mac after shrinkwrapping.

# notes on issue
assemble-handlebars was recently updated.
With assemble-handlebars@0.2.5, the {{{@content}}} used with handlebars-helper-compose no longer seems to function as expected - the content of the partial is not rendered in the page.
{{log @content}} does work and logs out the content of each partial as assemble runs.
Downgrading to assemble-handlebars@0.2.3 within the assemble package seems to work okay.
`test a` with 0.2.3 works, `test b` with 0.2.5 fails.

# differences between `test a` and `test b`
Identical except for node_modules/assemble/node_modules/assemble-handlebars being deleted in `test a` and npm install assemble-handlebars@0.2.3 being run to downgrade this package from 0.2.5 to 0.2.3.

# public repos for testing / peer code review
https://github.com/nuls1/compose-a-test.git
https://github.com/nuls1/compose-b-test.git

# grunt commands
default builds out to `dist/page.html`
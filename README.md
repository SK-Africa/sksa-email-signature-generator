## SK SA Email Signature Generator
For local, internal use to generate all available email signatures.

#### Setup
Install: `gem install bundler jekyll`

#### Usage
run locally: `bundle exec jekyll serve` | localhost:4000

- *Company info: config.yml*
- *Employee info: _data/team-members.yml*

#### Features
- auto-generated email mailto: URLs, example: `firstname@searchkingsafrica.com` (or supply a custom entry)
- auto-generated avatar image source, example: `firstname-lastname.png` (or supply a custom entry)
- click-to-copy email signature button
- simple YAML team members data structure
- builds in just over 0.02 seconds

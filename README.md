# openmrs-module-radiology documentation

This project is the documentation for the [OpenMRS Radiology Module](https://github.com/openmrs/openmrs-module-radiology)

## Generate Documentation as HTML

Install bundler

```bash
gem install bundler
```

Install dependencies

```bash
bundle install
```

Use guard to monitor and regenerate the HTML files whenever a change in
asciidoc files is detected

```bash
bundle exec guard
```

To generate index.html with css

```bash
asciidoctor index.adoc
```

NOTE: there is an issue with the Guardfile, it just does not respect the
default asciidoctor-default.css stylesheet which is used when running
asciidoctor from the command line


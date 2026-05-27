# useblocks variant demo

## Project setup

Here we have setup a simple sphinx-needs/ubcode project to demonstrate the use of variants:

- `ubproject.toml` defines the core configuration
- `variants1.json` and `variants2.json` are the two variant data files, which contain different platform and architecture information
- `conf.py` is the standard sphinx configuration file, which also includes the `sphinx_needs` extension and configures it to read from the `ubproject.toml` file
- `index.rst` is the main documentation file, which includes a need that uses the variant data to determine which content to include, including the new `if` directive.

Note we setup the project to run from the head versions of sphinx-needs / ubcode, which are currently unreleased (but should be soon!).

## Running with sphinx

Lets first look at how we can run them via sphinx-build:

```shell
uv run sphinx-build . _build
```

To change the variant configiuration, without touching any files we can use the `-D` option to override the `needs_variant_data_file` configuration.

```shell
uv run sphinx-build . _build -E -D needs_variant_data_file=variants2.json
```

## ubcode VSC extension features

- Syntactic highlighting of the `if` directive
- Needs index view
- HTML preview

## ubc CLI features

```shell
ubc build needs --pretty  
```

```shell
ubc build needs --pretty -c "needs.variant_data_file='variants2.json'"
```

(or use `UBCODE_CONFIG_OVERRIDE="needs.variant_data_file='variants2.json'"` as an environment variable)

```shell
ubc diff -c "needs.variant_data_file = 'variants2.json'"
```

```shell
ubc diff -c "needs.variant_data.arch = 'other'"
```

## More to come!

...

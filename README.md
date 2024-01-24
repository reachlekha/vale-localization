# Vale rules for Localization

This repo contains Vale rules to check for correct Localization syntax in AsciiDoc files.

For Vale installation steps, see here: https://vale.sh/docs/vale-cli/installation/

**_NOTE:_** If you need Vale rules to lint grammar and accepted Red Hat terminology in Localization, see [Vale at Red Hat](https://github.com/redhat-documentation/vale-at-red-hat/). 

## Testing the `Localization` rule set
To test the `Localization` rule set, add a `.vale.ini` configuration file in your modules directory. 

1. Add a `.vale.ini` file to your repo root directory with the following content:

  ```
  StylesPath = .vale/styles

MinAlertLevel = suggestion

Packages = https://github.com/reachlekha/vale-localization/releases/latest/download/Localization.zip

[[!.]*.adoc]
BasedOnStyles = RedHat, Localization
  ```

2. Run `vale sync`

## Verification

To verify, run `vale ls-config` in your modules directory to check that the `Localization` package is installed. 

_Example output_

  ```
  {
  "BlockIgnores": {},
  "Checks": null,
  "Formats": {},
  "Localization": {},
  ...
  "SBaseStyles": {
    "[!.]*.adoc": [
      "Localization"
    ]
  ...
  }
  ```

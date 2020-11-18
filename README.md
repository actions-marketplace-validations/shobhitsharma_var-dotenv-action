![](https://github.com/shobhitsharma/var-dotenv-action/workflows/Test/badge.svg)
![GitHub license](https://img.shields.io/github/license/shobhitsharma/var-dotenv-action)

# var-dotenv-action

GitHub action that injects env variable to a dotenv file

## Usage

```yaml
steps:
  - uses: shobhitsharma/var-dotenv-action@v{LATEST_GIT_TAG_HERE}
    with:
      key: 'KEY_ATTRIBUTE' # [Required]
      value: ${{secrets.KEY_ATTRIBUTE}} # [Required]
      default: 'FALLBACK_ATTRIBUTE' # [Optional] if `value` is empty, this is used instead
      nullable: 'false' # [Optional] if the resolved value is empty, the variable will be omitted
      envPath: '.env' # [Optional] The path to the dotenv file (defaults to `.env`)
```

You can use this more than once in your workflow to add multiple variables.

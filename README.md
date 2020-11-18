![](https://github.com/shobhitsharma/var-dotenv-action/workflows/Test/badge.svg)
![GitHub license](https://img.shields.io/github/license/shobhitsharma/var-dotenv-action)

# env-to-dotenv

GitHub action that injects env variable to a dotenv file

## Usage

```yaml
steps:
  - uses: shobhitsharma/var-dotenv-action@v1.1.1
    with:
      key: 'SOME_API_URI' # [Required]
      value: ${{secrets.SOME_API_URI}} # [Required]
      default: 'https://api.alt.com' # [Optional] if `value` is empty, this is used instead
      nullable: 'false' # [Optional] if the resolved value is empty, the variable will be omitted
      envPath: '.env' # [Optional] The path to the dotenv file (defaults to `.env`)
```

You can use this more than once in your workflow to add multiple variables.

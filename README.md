# Astro Demo

This is a demonstration on how to use Astro. This was created using the Astro Tutorial located [here](https://docs.astro.build/en/tutorial/)

## Directions

The following Directions (Steps) were used;

1. Create a new project and commit to Github

```sh
mkdir astro-demo
cd astro-demo
pnpm create astro@latest
git add .
git commit -m "Initial Commit"
git remote add origin git@github.com:pkeech/Astro-Demo.git
git push --set-upstream origin main
```

2. Run development application

```sh
pnpm run dev
```

3. Configure Project

```sh
## INSTALL AND CONFIGURE PRETTIER
pnpm add -D prettier prettier-plugin-astro
```

Create `.prettierrc` in the root.

```json
{
  "plugins": ["prettier-plugin-astro"],
  "overrides": [
    {
      "files": "*.astro",
      "options": {
        "parser": "astro"
      }
    }
  ],
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2,
  "trailingComma": "es5",
  "printWidth": 80
}
```

Create `.prettierignore` in the root

```json
node_modules/
dist/
.astro/
```

Update `package.json` to include ...

```json
{
  "scripts": {
    "format": "prettier --write .",
    "format:check": "prettier --check ."
  }
}
```

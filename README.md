# completely

Generate shell completion scripts from a JSON description of a command.

## Usage

You can use the CLI to generate scripts:

```
npm i -g @completely/cli
completely --shell bash completion.json
```

(Only bash is supported at the moment.)

Or you can use the library:

```
npm i @completely/bash-generator
```

```typescript
import { generate } from '@completely/bash-generator'
import completionSpec from './completion.json'

const script = generate(completionSpec)
console.log(script)
```

## JSON description

You can check the [spec package](packages/spec) to learn more about how to describe a command with a JSON file. Ideally you wouldn't need to do this manually, since this JSON is meant to be an internal representation generated by other means.
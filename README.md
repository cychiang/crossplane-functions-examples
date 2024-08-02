# crossplane-functions-examples

An example of writing/reading info from and to the status field.

## function-step-one

It's a function to write info to the `.status` field in desired composite resource.

## function-step-two

It's a function to read info from `.status` in desired composite and write to another field in `.status`

## How to run

Run `function-step-two` in a terminal

```bash
go run . --insecure
```

Open another terminal for `function-step-two`, and because we will need to execute multiple function so we will need to set another port for
another function because by default the function is using `:9443`

```bash
go run . --insecure --address=:8081
```

Go to `example` folder, and run `render` to generate results.

```bash
crossplane beta render xr.yaml composition.yaml functions.yaml
```

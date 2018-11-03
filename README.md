# OCaml Debugger

## Prerequisite 

```
opam install earlybird
```

## Sample launch.json

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "ocaml-debugger",
      "arguments": [
        "--server",
        "port=4711"
      ],
      "console": "internalConsole",
      "cwd": "${workspaceRoot}/src",
      "env": {
        "OCAMLRUNPARAM": "b"
      },
      "internalConsoleOptions": "openOnSessionStart",
      "name": "OCaml Debugger",
      "program": "ocamlearlybird",
      "request": "launch",
      "stopOnEntry": false
    }
  ]
}
```

## FAQ


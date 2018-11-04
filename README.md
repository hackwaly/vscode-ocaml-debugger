# OCaml Debugger

## Prerequisite 

```
opam install earlybird
```

### Sample launch.json

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "OCaml Debug",
      "type": "ocaml-debugger",
      "request": "launch",
      "program": "${workspaceFolder}/a.out"
    }
  ]
}
```

Assuming a file at `src/main.ml`

```ocaml
let fizzbuzz i = match ((i mod 3), (i mod 5)) with
    | (0, 0) -> "fizbuzz"
    | (_, 0) -> "buzz"
    | (0, _) -> "fizz"
    | (_, _) -> string_of_int i;;

let do_fizzbuzz n = for i = 1 to n do
    print_endline (fizzbuzz i)
done;;

do_fizzbuzz 100;;

```

Compile `main.ml`

```bash
ocamlc -g src/main.ml
# creates a.out in root of the project
```

Then set breakpoint in `main.ml` and run **"OCaml Debug"** from the VS Code Debug panel.

## FAQ


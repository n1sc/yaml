# yaml

Full YAML parsing and serialization for Neutron. Parsed documents use the
same compact JSON representation as the `json` module, so the result can be
inspected with `json.get`, `json.keys`, and `json.at`.

## Install

```console
ntsc pkg install yaml
```

## Use

```neutron
use yaml
use json

fun main() {
    var document = yaml.parse("name: neutron\nfeatures:\n  - ownership\n  - packages")
    say(json.get(document, "name"))
    say(yaml.stringify(document))
}
```

## API

| Function | Returns |
| --- | --- |
| `parse(text)` | A JSON object containing the YAML document. |
| `stringify(document)` | YAML text for a JSON object. |

The package supports mappings, nested mappings, block sequences, flow
sequences, flow mappings, comments, strings, booleans, numbers, and null.

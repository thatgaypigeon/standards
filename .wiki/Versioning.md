# Versioning
Package version schemes, also known as **versioning** is the process of assigning version names or numbers to uniquely identify a release of a piece of software.

The details laid out here are similar to other versioning standards, such as [PEP 440](https://peps.python.org/pep-0440/) or [SemVer](https://semver.org/) (Semantic Versioning).

## Scheme
Packages should be released with a 3 (or in some cases, 4) part version identifier in the format `N.N.N`, where `N` denotes a non-negative integer. This format is known as `major.minor.micro` (a.k.a `major.minor.patch` or `version.revision.change`), and is generally universal.

### Extended syntax
Including pre-releases, such as "alpha", "beta", "release candidate", and development release versions, the full syntax is `N.N.N[{a|b|rc}N][.devN]`. Shortened versions of "alpha", "beta", and "release candidate" should be used instead of the full names.

Some languages or package managers require a specific format or delimiter for some version numbers. These can be listed below, along with some examples.

## Language or package-manager specific changes

### LuaRocks (Lua)
As per [`rockspec`](https://github.com/luarocks/luarocks/wiki/Rockspec-format), LuaRocks packages should[^1] have a version suffix separated by a hyphen. The format for LuaRocks packages is `N.N.N-N`.

LuaRocks supports "alpha", "beta", and "dev" release types to be tagged as development versions (along with others that aren't relevant here), but doesn't directly recognise any for of release candidate. However, versions can be named in accordance with the format detailed above, they just won't be tagged as development versions nor will they be downloaded by default (like other dev releases).

Release types are not separated with a delimiter, but development releases are separated by a full-stop ("`.`").

### npm (JavaScript)
This version scheme is compatible with the npm version scheme ([Semantic Versioning](https://semver.org/)). Release types are separated with a hyphen ("`-`").

### PIP (Python)
This version scheme is compatible with the PIP version scheme ([PEP 440](https://peps.python.org/pep-0440/)). Release types are not separated with a delimiter, but development releases are separated by a full-stop ("`.`").

## Examples
| Release                                             | JS              | Lua            | Python         |
| --------------------------------------------------- | --------------- | -------------- | -------------- |
| Version `0.0.0`                                     | `0.0.0`         | `0.0.0`        | `0.0.0`        |
| Version `2.19.0`                                    | `2.19.0`        | `2.19.0`       | `2.19.0`       |
| Version `0.5.0`, alpha `2`                          | `0.5.0-a2`      | `0.5.0a2`      | `0.5.0a2`      |
| Version `1.4.1`, release candidate `3`              | `1.4.1-rc3`     | `1.4.1rc3`     | `1.4.1rc3`     |
| Version `0.2.3`, development release `1`            | `0.2.3-dev1`    | `0.2.3.dev1`   | `0.2.3.dev1`   |
| Version `1.7.2`, alpha `1`, development release `6` | `1.7.2-a1.dev6` | `1.7.2a1.dev6` | `1.7.2a1.dev6` |

## Footnotes
[^1]: Lua and LuaRocks don't officially enforce any versioning scheme, though some keywords are recognised as development releases and aren't installed via LuaRocks unless specified. (The latest non-development release is installed by default.)
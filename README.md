# Extremely Linear Git History

> Dreaming of a git commit history that looks like this?

<img width="1197" alt="Screenshot 2022-11-22 at 16 16 40" src="https://user-images.githubusercontent.com/47952/203351228-383cd585-c135-4f63-ac3d-8f10707cc9c7.png">

## Installation

```bash
brew install zegl/tap/git-linearize
```

or copy the [the script](https://github.com/zegl/extremely-linear/blob/main/git-linearize) to somewhere on your PATH.

## Usage

Run as `git linearize`.

```
git linearize - Create an extremely linear git history

git linearize [options]

options:
-h, --help                show brief help
--short                   use shorter 6 digit prefix (quick mode)
--format [format]         specify your own prefix format (pritnf style)
```

git-linearize requires the history to already be linear (no merge commits).

**Beware:** git-linearize will rebase your entire project history. Do not run unless you know what you're doing. Create a backup first!

## `shit` – "short git"

This repository also contains `shit`. A git wrapper that converts non-padded prefixes to their padded counterpart.

* `shit show 14` translates to `git show 00000140`
* `shit log 10..14` --> `git log 00000100..00000140`

Install with `brew install zegl/tap/git-shit`, or copy the [the script](https://github.com/zegl/extremely-linear/blob/main/shit) to somewhere on your PATH.


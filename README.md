# destockd-api

An API for [Destockd](https://www.destockd.com/) (public-domain FedFlix archival footage), built with
[API Anything](https://github.com/goodnight000/api-anything), plus a Claude Code skill for finding footage.

## Operations

`search(q)` · `similar(film, shot)` · `getShot(film, shot)` · `getFilm(film)` · `listCollections()` ·
`getCollection(slug)` · `listFilms(page)` · `random()`

All read-only, plain HTTP (tier 1). Search matches by meaning and never returns empty; scores are low
even for good hits, so check the keyframes.

## Install

```sh
# 1. install API Anything (see its INSTALL.md), then import the spec
mkdir -p ~/.api-anything/sites && cp destockd.json ~/.api-anything/sites/destockd.json
api-anything call destockd search q="woman applying lipstick at a mirror"

# 2. install the Claude Code skill
mkdir -p ~/.claude/skills/destockd-footage && cp skills/destockd-footage/SKILL.md ~/.claude/skills/destockd-footage/
```

## Notes

Footage is from the FedFlix public-domain archive; see Destockd's rights information before use.
This project is unaffiliated with Destockd. MIT licensed.

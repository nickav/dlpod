# dlpod

A simple command-line tool to download all episodes from a podcast RSS feed.

## Usage

```
node dlpod.js <rss-url> [output-dir] [options]
```

## Options

| Flag | Short | Default | Description |
|------|-------|---------|-------------|
| `--parallel N` | `-n` | `3` | Number of concurrent downloads |
| `--force` | `-f` | off | Re-download files that already exist |
| `--naming` | `-N` | `original` | Filename mode: `original` (from feed URL) or `sequential` (numbered by episode order) |

## Examples

Download all episodes to `./downloads`:
```
node dlpod.js https://example.com/feed.rss
```

Download to a specific folder with 5 parallel downloads:
```
node dlpod.js https://example.com/feed.rss ./my-podcast -n 5
```

Use sequential filenames (e.g. `001_Episode Title.mp3`):
```
node dlpod.js https://example.com/feed.rss ./my-podcast -N sequential
```

# homebrew-imud

Homebrew tap for [imud](https://github.com/richcreations/imud) — a
general-purpose IMU daemon for Linux and macOS.

```sh
brew tap richcreations/imud
brew install richcreations/imud/imud richcreations/imud/imud-wmm-data
brew services start richcreations/imud/imud
```

One formula per Debian package, so a host installs only what it needs:

| Formula | What it installs |
|---|---|
| `imud` | the daemon, `imud-cal`, `imud-status`, libimud and its header |
| `imud-utils` | `imud-mon` and `imud-imutest` |
| `imud-wmm-data` | the World Magnetic Model coefficients |
| `imud-signalk` | the Signal K bridge |
| `imud-mqtt` | the MQTT bridge |
| `imud-influxdb` | the InfluxDB bridge |
| `imud-mavlink` | the MAVLink bridge |
| `imud-prometheus` | the Prometheus exporter |

Every other formula depends on `imud`, so installing a bridge installs the
daemon with it.

The formulae are generated from `packaging/homebrew/` in the
[imud repository](https://github.com/richcreations/imud) — send changes there,
not here.

Issues and pull requests: <https://github.com/richcreations/imud/issues>.

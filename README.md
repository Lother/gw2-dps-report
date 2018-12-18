# Guild Wars 2 DPS Report

![License](https://img.shields.io/github/license/progamesigner/gw2-dps-report.svg)
[![Discord](https://img.shields.io/badge/chat-Discord-7289DA.svg)](https://discord.gg/xsSWwn3)
[![Buy Me A Coffee](https://img.shields.io/badge/donate-Buy%20Me%20A%20Coffee-FF813F.svg)](https://buymeacoff.ee/progamesigner)

Upload arcdps logs and send to Discord automatically.

## Getting Started

### Development

Cargo makes everything simple.

```
cargo run --bin gw2-dps-report
```

Cargo would install dependencies, build debug executable, and the server is up.

### Deployment

Deploy service with Docker.

```
docker build -t gw2-dps-report .
docker run -d \
    -e UPLOAD_ACCESS_TOKEN=<YOUR_SECRET_TOKEN> \
    gw2-dps-report
```

Clean files generated 14 days ago.
```
docker exec gw2-dps-report gw2-dps-clean
```

### Built With

 * [Rust](https://www.rust-lang.org)
 * [Docker](https://www.docker.com)
 * [Elite Insights](https://github.com/baaron4/GW2-Elite-Insights-Parser)
 * [Bulma](https://bulma.io)
 * [DropzoneJS](https://www.dropzonejs.com)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

# codespace-xray

Free VLESS proxy running on GitHub Codespaces, powered by Xray-core with xHTTP transport.

## Features

- Unique UUID generated automatically at each build — no two instances are the same
- Always downloads the latest Xray-core release automatically
- GeoIP and GeoSite databases for smart traffic routing
- Blocks ads, BitTorrent, and private IP access
- Keepalive loop to prevent Codespace idle shutdown
- VLESS + xHTTP + TLS over GitHub's own infrastructure

## Requirements

- A GitHub account with Codespaces access
- A compatible proxy client (v2rayNG, v2rayN, Nekobox, etc.)

## Setup

1. Fork this repository
2. Open the repository, click the green **Code** button, go to the **Codespaces** tab, and click **Create codespace on main**
3. Wait 3–5 minutes for the build to complete
4. The VLESS connection link will appear in the terminal automatically

## Usage

- Copy the VLESS link from the terminal into your proxy client
- To show the link again at any time, run `show-link.sh` in the terminal
- To view Xray logs, run `tmux attach -t proxy` in the terminal

## Supported Clients

| Platform | Clients |
|----------|---------|
| Android | v2rayNG, Nekobox |
| Windows | v2rayN, Nekoray |
| iOS | Streisand, FoXray |
| Linux | Nekoray, Xray-core |

## Clean IP Options

The default connection IP is `94.130.50.12`. If it does not work on your network, try replacing it in the link with one of these:

- `63.141.252.203`
- `50.7.5.83`
- `94.130.50.12`

## Quota

- GitHub Free gives 120 core-hours per month
- On a 2-core machine, this equals 60 real hours per month
- **Always stop the Codespace when not in use**
- Set your idle timeout to 240 minutes at: `github.com/settings/codespaces`

## Notes

- Create only one Codespace per GitHub account from this repository
- Each new Codespace build generates a fresh unique UUID automatically

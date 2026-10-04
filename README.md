# Awesome-Cloud-VPN-Gateway

# Awesome-Cloud-VPN-Gateway

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Cloud VPN Gateways, Zero Trust Network Access (ZTNA) & Secure Remote Access*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud VPN Gateways**. These tools help organizations provide secure remote access to private resources, replacing traditional VPN concentrators with identity-aware, least-privilege connectivity.

**Examples** include Azure VPN Gateway, AWS Client VPN, Google Cloud VPN, Cisco AnyConnect, OpenVPN Cloud, NordLayer, Perimeter 81, Fortinet FortiClient, Tailscale, and WireGuard (the category leaders).

**Open-source emphasis**: Cloud VPN has a **mature and production-proven open-source ecosystem**. **WireGuard** is the de facto modern VPN protocol, embedded in the Linux kernel and used by nearly every commercial ZTNA vendor . **Tailscale** and **NetBird** provide mesh VPN solutions with identity-based access control, while **Headscale** and **Pomerium** offer self-hosted control planes for full data sovereignty . This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## 📖 Table of Contents

- [☁️ SaaS/Hosted Platforms](#-saas-hosted-platforms)
- [🔓 Open-Source GitHub Projects](#-open-source-github-projects)
- [🤝 How to Contribute](#-how-to-contribute)
- [⚠️ Disclaimer](#-disclaimer)

## ☁️ SaaS/Hosted Platforms

> **📊 Market Context**: The global ZTNA market is estimated at **~$2.5B in 2026**, growing toward **~$8B by 2031** at a **~26% CAGR**. The sector is **moderately fragmented** — Cloudflare Access and Tailscale compete on developer experience, while Twingate and Zscaler Private Access target enterprise least-privilege access. **Pricing varies dramatically**: Cloudflare Access has a **permanently free tier for up to 50 users** and **$7/user/month** pay-as-you-go , Tailscale's free Personal plan now supports **up to 6 users with unlimited devices** , and Twingate's free Starter covers **5 users and 10 resources** . Median Twingate contracts run **$21,600/year** from 27 verified purchases . No single vendor holds a winner-take-all position; enterprises typically run multi-vendor stacks.

| Platform | Description | Pricing (Starting Tier) | Free Tier Limits | Company Size |
|----------|-------------|------------------------|------------------|--------------|
| **[Cloudflare Access](https://www.cloudflare.com/zero-trust/products/access/)** | **Identity-aware reverse proxy with clientless browser access to SSH, VNC, and RDP.** Uses Cloudflare Tunnel (cloudflared) for outbound-only connections. Integrates with Cloudflare One SASE platform . | **Pay-as-you-go**: **$7/user/month** (annual). **Contract**: Custom enterprise pricing . Cloudflare Access is typically **15–25% lower** than Twingate on a per-user basis for larger deployments . | **Free tier**: **Up to 50 users** permanently free. Includes WARP client and cloudflared tunnels . | **~$2.17B revenue (Cloudflare FY2025)** |
| **[Tailscale](https://tailscale.com/)** | **WireGuard-based mesh VPN with identity-based access control.** MagicDNS, Taildrop, Funnel, and ACLs configured in JSON. **Headscale** provides self-hosted control plane alternative . | **Starter**: **$6/user/month** (annual); **Premium**: **$18/user/month** . **Personal Plus**: **$5/user/month** (billed annually) . | **Personal (free)**: **Up to 6 users**, **unlimited devices**, MagicDNS, Taildrop, ACLs, subnet routers, exit nodes, Tailscale Funnel . No device limit on any plan . | **Private (~$100M+ ARR est.)** |
| **[Twingate](https://www.twingate.com/)** | **Zero-trust network access with resource-level policies.** Connector-based model with no inbound firewall ports. Per-resource ACLs, device posture checks (CrowdStrike, SentinelOne, Intune, Kandji) . | **Teams**: **$5/user/month** (annual) or **$12/month**; **Business**: **$10/user/month** (annual) or **$12/month** . **Median contract**: **$21,600/year** . | **Starter (free)**: **5 users**, **1 admin**, **10 resources**. No enterprise identity integration (Entra ID requires Business tier) . | **Private (~$42M raised)** |
| **[Azure VPN Gateway](https://azure.microsoft.com/en-us/products/vpn-gateway/)** | Microsoft's managed VPN gateway for site-to-site and point-to-site connectivity. Integrates with Azure VNets and ExpressRoute. | **VpnGw1**: **$0.19/hour** (~$138/month). **VpnGw2**: **$0.38/hour**. **Basic**: **$0.04/hour** . | **Azure free account**: **$200 credit for 30 days** + 12 months of free services. No perpetual free tier for VPN Gateway. | **~$281B revenue (Microsoft FY2025)** |
| **[AWS Client VPN](https://aws.amazon.com/vpn/client-vpn/)** | Managed client-based VPN service for AWS and on-premises resources. OpenVPN-based. | **$0.10/hour per client VPN endpoint** + **$0.05/hour per client connection** . | **AWS Free Tier**: **$100–$200 credits** for new accounts. No perpetual free tier for Client VPN. | **~$638B revenue (Amazon FY2025)** |
| **[Google Cloud VPN](https://cloud.google.com/network-connectivity/docs/vpn)** | Managed VPN for connecting on-premises networks to GCP VPCs. | **$0.05/hour per VPN tunnel** + egress data transfer . | **Google Cloud Free Tier**: **$300 credit for 90 days**. No perpetual free tier for Cloud VPN. | **~$350B revenue (Alphabet FY2025)** |
| **[Cisco AnyConnect](https://www.cisco.com/)** | Enterprise VPN client with secure remote access. Now part of Cisco Secure Client. | **Custom enterprise pricing** — quote required. Typical entry contracts **$50–$100/user/year**. | **None** — enterprise demo required. | **~$63B revenue (Cisco FY2025)** |
| **[OpenVPN Cloud](https://openvpn.net/)** | Managed VPN service built on OpenVPN protocol. Cloud-hosted or self-hosted. | **Cloud**: **$0.10/hour per connected device** or **$5/device/month** . **Access Server**: **$11/user/year** (5-user pack) . | **Free tier**: **3 VPN connections** with OpenVPN Cloud . | **Private (~$50M+ revenue est.)** |
| **[NordLayer](https://nordlayer.com/)** | Business VPN with Zero Trust features. Part of Nord Security. | **Essential**: **$8/user/month** (annual). **Advanced**: **$11/user/month**. **Core**: **$14/user/month** . | **7-day free trial** on all plans. No perpetual free tier. | **Part of Nord Security (~$3B valuation)** |
| **[Perimeter 81](https://www.perimeter81.com/)** | **Converged network security with ZTNA.** Now part of Check Point. | **Essential**: **$8/user/month**; **Premium**: **$12/user/month** . **Negotiated**: **$7–$10/user/month** for 100+ users . | **Free trial available** (details require sales contact). | **Part of Check Point (~$2.5B revenue)** |
| **[Fortinet FortiClient](https://www.fortinet.com/)** | Endpoint protection and VPN client. Integrates with FortiGate firewalls. | **Custom enterprise pricing** — quote required. Bundled with FortiGate licenses. | **FortiClient VPN**: **Free** for basic VPN functionality. Full endpoint protection requires license. | **~$5.5B revenue (Fortinet FY2025)** |

## 🔓 Open-Source GitHub Projects

Sorted by star count (descending). Star badge links to each repo's stargazers page.

| Repo | Description | Stars |
|---|---|---|
| **[WireGuard](https://github.com/WireGuard/wireguard-linux)** — **The modern VPN protocol embedded in the Linux kernel.** Simple, fast, cryptographically sound. Used by Tailscale, NetBird, Cloudflare WARP, and nearly every commercial ZTNA vendor . GPL-2.0. | [![Stars](https://img.shields.io/github/stars/WireGuard/wireguard-linux?style=social&color=white)](https://github.com/WireGuard/wireguard-linux/stargazers) | ~5,000 |
| **[Tailscale](https://github.com/tailscale/tailscale)** — **Open-source WireGuard mesh VPN with identity-based access.** MagicDNS, Taildrop, Funnel, ACLs. **Control plane is closed-source (SaaS)**, but **Headscale** provides a self-hosted alternative . BSD-3-Clause. | [![Stars](https://img.shields.io/github/stars/tailscale/tailscale?style=social&color=white)](https://github.com/tailscale/tailscale/stargazers) | ~20,000 |
| **[Headscale](https://github.com/juanfont/headscale)** — **Open-source, self-hosted implementation of the Tailscale control server.** Run the Tailscale UX with zero vendor lock-in. Client-to-server model, DERP alternative, ACL management . BSD-3-Clause. | [![Stars](https://img.shields.io/github/stars/juanfont/headscale?style=social&color=white)](https://github.com/juanfont/headscale/stargazers) | ~25,000 |
| **[NetBird](https://github.com/netbirdio/netbird)** — **Open-source WireGuard mesh VPN with granular ACLs and built-in identity.** The strongest free alternative when Tailscale's free device cap is the reason to shop. Open-source client, control plane, and agent . BSD-3-Clause. | [![Stars](https://img.shields.io/github/stars/netbirdio/netbird?style=social&color=white)](https://github.com/netbirdio/netbird/stargazers) | ~15,000 |
| **[Pomerium](https://github.com/pomerium/pomerium)** — **Identity-aware proxy for zero-trust access.** Google's BeyondCorp model, open-source. Self-hosted control plane and data plane available. Enterprise tier adds full self-hosting, RBAC, and audit logs . Apache-2.0. | [![Stars](https://img.shields.io/github/stars/pomerium/pomerium?style=social&color=white)](https://github.com/pomerium/pomerium/stargazers) | ~4,500 |
| **[OpenVPN](https://github.com/OpenVPN/openvpn)** — **The classic open-source VPN.** Battle-tested, cross-platform, widely deployed. More complex to configure than WireGuard . GPL-2.0. | [![Stars](https://img.shields.io/github/stars/OpenVPN/openvpn?style=social&color=white)](https://github.com/OpenVPN/openvpn/stargazers) | ~10,000 |
| **[ZeroTier](https://github.com/zerotier/ZeroTierOne)** — **Open-source mesh VPN with virtual Ethernet networks.** Peer-to-peer, no central servers required for data plane. BSD-3-Clause. | [![Stars](https://img.shields.io/github/stars/zerotier/ZeroTierOne?style=social&color=white)](https://github.com/zerotier/ZeroTierOne/stargazers) | ~14,000 |
| **[OpenConnect](https://github.com/openconnect/openconnect)** — **Open-source VPN client compatible with Cisco AnyConnect.** Used by NetworkManager, Let's Connect, and GlobalProtect alternatives . LGPL-2.1. | [![Stars](https://img.shields.io/github/stars/openconnect/openconnect?style=social&color=white)](https://github.com/openconnect/openconnect/stargazers) | ~3,500 |

## 🤝 How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## ⚠️ Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud VPN platforms handle sensitive network traffic and authentication credentials; ensure proper security configuration, least-privilege access, and compliance with organizational policies.
- **Open-source reality**: Cloud VPN has a **mature and production-proven open-source ecosystem**. **WireGuard** is the de facto modern VPN protocol embedded in the Linux kernel, used by nearly every commercial ZTNA vendor . **Tailscale** and **NetBird** provide mesh VPN solutions with identity-based access control, while **Headscale** and **Pomerium** offer self-hosted control planes for full data sovereignty . **OpenConnect** provides open-source compatibility with Cisco AnyConnect. However, **commercial platforms** (Cloudflare Access, Twingate, Zscaler) provide **managed infrastructure, enterprise SLAs, and zero-trust policy engines** that open-source alternatives require significant operational investment to match. The open-source path is **genuinely viable** for organizations with strong network engineering capacity seeking full data sovereignty and cost control.
- **Pricing caveat**: All pricing figures above are **verified against cited search results** but may change without notice. ZTNA and VPN pricing varies significantly based on user count, deployment model, and contract term. **Cloudflare Access has a permanently free tier for up to 50 users** and **Tailscale's free Personal plan now supports up to 6 users with unlimited devices** — both are genuinely viable for small teams .

---

**Made for network engineers, security architects, DevOps teams, and infrastructure specialists.**
Let's make cloud VPN and zero-trust access more open, transparent, and secure.

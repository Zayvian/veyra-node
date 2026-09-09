# zayvian-lee node fork

Based on https://github.com/kosje/skysbx-node. Original GPL-3.0 license and history retained.

This version adds Hysteria2 and TUIC v5 hot user updates, uses the companion patched QUIC module, and installs nftables for optional Hysteria2 port hopping. Startup removes only stale tables in the reserved `skysbx_hop_<16 hex digits>` namespace. Run one managed node daemon per host.

Clone `skysbx-node` and https://github.com/zayvian-lee/skysbx-core side by side. Both replace directives in go.mod are required. The installer fetches zayvian-lee's repositories by default.

Build/test tags: `with_clash_api,with_v2ray_api,with_utls,with_acme,with_quic`. Linux deployment uses Go 1.26.5. Run `go test -race -tags 'with_clash_api,with_v2ray_api,with_utls,with_acme,with_quic' ./...`.

Usage, subscription formats and deployment notes: https://github.com/zayvian-lee/skysbx-panel/blob/main/docs/FORK.md

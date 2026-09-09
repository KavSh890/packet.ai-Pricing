# packet.ai GPU Pricing

This file contains the current GPU pricing for [packet.ai](https://packet.ai) — a hosted.ai GPU cloud and LLM inference platform.

## Structure

The JSON is split into two sections:

- **`on_demand`** — pay-per-hour, no commitment
- **`monthly`** — commit for a month, lower effective hourly rate

### Fields

| Field | Description |
|---|---|
| `gpu_type` | GPU model name |
| `gpu_count` | Number of GPUs in the configuration |
| `plan_type` | `dedicated` (whole card) or `dynamic` (shared infrastructure, same VRAM and peak performance) |
| `vram_gb` | Total VRAM across all GPUs |
| `ram_gb` | System RAM |
| `vcpu` | Virtual CPU count |
| `storage_gb` | Local NVMe storage |
| `price_per_gpu_hour_usd` | Hourly rate (on-demand only) |
| `price_per_month_usd` | Monthly rate (monthly plans only) |
| `effective_hourly_usd` | Effective hourly rate when billed monthly |
| `region` | Data centre location and zone |
| `stock_status` | `in_stock`, `out_of_stock`, or `launching_soon` |

## Stock Statuses

- `in_stock` — available to deploy now
- `out_of_stock` — temporarily unavailable
- `launching_soon` — coming soon, specs and pricing TBC

## Updates

Prices and availability are updated manually from the packet.ai dashboard. If you spot something out of date, please open an issue or PR.

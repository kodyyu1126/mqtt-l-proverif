# MQTT-L Protocol — ProVerif Formal Verification Models

This repository contains the ProVerif source files for the formal security verification of the **MQTT-L** protocol, accompanying the paper:

> **[MQTT-L: Lightweight End-to-End Secure Protocol for IoT]{MQTT-L: A Lightweight End-to-End Secure Protocol with Renewable Hash Chains for IoT Environments]**  

## Files

| File | Description |
|------|-------------|
| `mqtt_auth.pv` | Authentication analysis |
| `mqtt_sec.pv` | Confidentiality analysis |

## Requirements

- **ProVerif 2.05** — [https://proverif.inria.fr](https://proverif.inria.fr)

## Usage

```bash
proverif mqtt_auth.pv
proverif mqtt_sec.pv
```

## Verified Properties

**`mqtt_auth.pv`**
- Non-injective authentication correspondence (first-time auth)
- Injective authentication correspondence (first-time auth)
- Injective authentication correspondence (reconnection)

**`mqtt_confidentiality.pv`**
- Message secrecy
- Session key secrecy

All queries are expected to return `true` under the Dolev-Yao attacker model.

## Contact

- Email: kody_yu@stu.jsu.edu.cn  
- QQ: 2386157328

# Demo Feature Toggle Services

Testing available feature toggle services and try evaluated them.

## Usage

```
cd <service> make up
```

## Requiremets

| Requirement | Description                    | Importance |
| :--         | :--                            |        :-- |
| Toggle      | Activate/deactivate features   |       1000 |
| Cron        | time-based activation          |        800 |
| Auditing    | Adit log                       |       1000 |
| UI          | WebUI to switch toggles        |        800 |
| Monitoring  | Support metrics for operations |        500 |
|             |                                |            |

## Services

- [Flagsmith](flagsmith/README.md)
- [Flipt](flipt/README.md)


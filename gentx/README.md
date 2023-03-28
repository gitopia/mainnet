# `gentx`

To generate your `gentx` run the following command with the launch genesis file at `~/.gitopiad/config/genesis.json`:

```
$ gitopiad gentx \
  <key_name> \
  <amount_of_delegation> \
  --chain-id gitopia \
  --moniker <moniker> \
  --website <website> \
  --details <details>
  --min-self-delegation <min_self_delegation> \
  --commission-rate <commission_rate> \
  --commission-max-rate <commission_max_rate> \
  --commission-max-change-rate <commission_max_change_rate> \
  --pubkey <consensus_pubkey>
  --identity <identity>
```

This will produce a file in the `~/.gitopiad/config/gentx/` folder that has a name with the format `gentx-<node_id>.json`. The content of the file should have a structure as follows:

```json
{
    "body":
    {
        "messages":
        [
            {
                "@type": "/cosmos.staking.v1beta1.MsgCreateValidator",
                "description":
                {
                    "moniker": "mynode",
                    "identity": "",
                    "website": "",
                    "security_contact": "",
                    "details": ""
                },
                "commission":
                {
                    "rate": "0.100000000000000000",
                    "max_rate": "0.200000000000000000",
                    "max_change_rate": "0.010000000000000000"
                },
                "min_self_delegation": "1",
                "delegator_address": "gitopia1fwza8jtkt0uuagf7rlxflprgvhd37z6veglq46",
                "validator_address": "gitopiavaloper1fwza8jtkt0uuagf7rlxflprgvhd37z6v3jms4p",
                "pubkey":
                {
                    "@type": "/cosmos.crypto.ed25519.PubKey",
                    "key": "M70IFVJgeYhJgs9Locuk46SKbSqtmyAXXKM3YWNOQWo="
                },
                "value":
                {
                    "denom": "ulore",
                    "amount": "100000000"
                }
            }
        ],
        "memo": "3e0f562d32978305b75935e148f8a6425801ed42@192.168.1.22:26656",
        "timeout_height": "0",
        "extension_options":
        [],
        "non_critical_extension_options":
        []
    },
    "auth_info":
    {
        "signer_infos":
        [
            {
                "public_key":
                {
                    "@type": "/cosmos.crypto.secp256k1.PubKey",
                    "key": "A7KJ6av0KWa57nfkC2+AIuOdp/s7DDtU6ZDjCCBV4Yd5"
                },
                "mode_info":
                {
                    "single":
                    {
                        "mode": "SIGN_MODE_DIRECT"
                    }
                },
                "sequence": "0"
            }
        ],
        "fee":
        {
            "amount":
            [],
            "gas_limit": "200000",
            "payer": "",
            "granter": ""
        },
        "tip": null
    },
    "signatures":
    [
        "R25uK3RVAkNo3HwxjUPLw0TcsatJucbWh1qHFZS1X3ApjaGF15nshnIAjb+Bj7uxctmcfU+zXyaoCzUo5WpjxA=="
    ]
}
```

To submit your `gentx` for inclusion in genesis, open a pull request against this repository and place the contents in a file `/gentx/<moniker>.json`.

__**NOTE**__: If you would like to override the memo field use the `--ip` and `--node-id` flags for the `gitopiad gentx` command above.

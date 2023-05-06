

# Genesis Parameters

| Param | Value | Notes |
|:--:|:--:|:--:|
| *Staking Module*|
| unbonding_time | 1814400s (21 days) | Duration time for unbonding |
| max_validators | 100 | Maximum number of active validators set |
| max_entries | 7 | Maximum amount of delegations by one account |
| bonded_coin_denom | ulore | The bonded coin denom |
| max_evidence_age | 1814400s (21 days) | Time period indicator that a validator committed malicious behavior |
| historical_entries | 10000 |
| *Slashing module* |
| signed_blocks_window | 50000 | The window for signing blocks |
| min_signed_per_window | 0.05 | The fraction of signed blocks per window to be an active validator |
| downtime_jail_duration | 600s | Time duration before unjail transaction available |
| slash_fraction_double_sign | 0.05 | Slashing for double sign |
| slash_fraction_downtime | 0.0001 | Slashing for downtime |
| *Minting Module* |
| inflation | 0.35 | The initial annual inflation rate |
| inflation_max | 0.45 | The maximum annual inflation rate |
| inflation_min | 0.25 | The minimum annual inflation rate |
| inflation_rate_change | 0.20 | The rate at which the inflation rate changes |
| goal_bonded | 0.67 | A point of inflation change sign |
| blocks_per_year | 19466666 |
| *Distribution Module* |
| community_tax | 0.05 | The tax on inflation to the community pool |
| base_proposer_reward  | 0.01 | % of inflation allocated to block proposer |
| bonus_proposer_reward | 0.04 | % of bonus for block proposer for precommits |
| withdraw_addr_enabled | true | Changing reward withdrawal addresses |
| *Governance Module* |
| min_deposit | 1000000000 | The minimum deposit to bring a proposal up for a vote |
| max_deposit_period | 172800s (2 days) | The duration at which a proposal can collect deposits |
| voting_period | 172800s (2 days) | The duration at which a proposal can be voted upon |
| quorum | 0.334 | A minimum quorum of bonded stake for voting |
| threshold | 0.500 | A minimum threshold for the voting proposal to pass |
| veto | 0.334 | A minimun of voting stake for vetoing a proposal |

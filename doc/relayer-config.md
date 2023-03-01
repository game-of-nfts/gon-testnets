# Relayer Config

## Hermes

```toml
[global]
log_level = 'info'
[mode]
[mode.clients]
enabled = true
refresh = true
misbehaviour = false
[mode.connections]
enabled = false
[mode.channels]
enabled = false
[mode.packets]
enabled = true
clear_interval = 1
clear_on_start = true
tx_confirmation = false
[rest]
enabled = true
host = '0.0.0.0'
port = 3000
[telemetry]
enabled = true
host = '0.0.0.0'
port = 3001

[[chains]]
id = 'gon-irishub-1'
rpc_addr = 'http://34.80.93.133:26657'
grpc_addr = 'http://34.80.93.133:9090'
websocket_addr = 'ws://34.80.93.133:26657/websocket'
rpc_timeout = '10s'
account_prefix = 'iaa'
key_name = 'rly' # as defined in ics721-demo.env!
store_prefix = 'ibc'
default_gas = 100000
max_gas = 5000000
gas_price = { price = 1, denom = 'uiris' }
gas_multiplier = 1.5
max_msg_num = 30
max_tx_size = 2097152
clock_drift = '10s'
max_block_time = '10s'
trusting_period = '1d' # 21 days (unbonding period) minus 1 sec
trust_threshold = { numerator = '1', denominator = '3' }
address_type = { derivation = 'cosmos' }
[chains.packet_filter]
policy = 'allow'
list = [
  ['*', 'channel-0'],
  ['*', 'channel-1'],
  ['*', 'channel-17'],
  ['*', 'channel-19'],
  ['*', 'channel-22'],
  ['*', 'channel-23'],
  ['*', 'channel-24'],
  ['*', 'channel-25'],
]

[[chains]]
id = 'uptick_7000-2'
rpc_addr = 'http://52.220.252.160:26657/'
grpc_addr = 'http://52.220.252.160:9090'
websocket_addr = 'ws://52.220.252.160:26657/websocket'
rpc_timeout = '10s'
account_prefix = 'uptick'
key_name = 'rly' # as defined in ics721-demo.env!
store_prefix = 'ibc'
default_gas = 10000000000000
max_gas = 10000000000000
gas_price = { price = 0.01, denom = 'auptick' }
gas_multiplier = 2
max_msg_num = 30
max_tx_size = 2097152
clock_drift = '5s'
max_block_time = '10s'
trusting_period = '1814399s' # 21 days (unbonding period) minus 1 sec
trust_threshold = { numerator = '1', denominator = '3' }
address_type = { derivation = 'ethermint', proto_type = { pk_type = '/ethermint.crypto.v1.ethsecp256k1.PubKey' } }
[chains.packet_filter]
policy = 'allow'
list = [
  ['*', 'channel-3'],
  ['*', 'channel-4'],
  ['*', 'channel-5'],
  ['*', 'channel-6'],
  ['*', 'channel-7'],
  ['*', 'channel-9'],
  ['*', 'channel-12'],
  ['*', 'channel-13'],
]

[[chains]]
id = 'gon-flixnet-1'
rpc_addr = 'http://65.21.93.56:26657'
grpc_addr = 'http://65.21.93.56:9090'
websocket_addr = 'ws://65.21.93.56:26657/websocket'
rpc_timeout = '10s'
account_prefix = 'omniflix'
key_name = 'rly' # as defined in ics721-demo.env!
store_prefix = 'ibc'
max_gas = 2000000
gas_price = { price = 0.001, denom = 'uflix' }
gas_multiplier = 1.1
clock_drift = '5s'
trusting_period = '1814399s' # 21 days (unbonding period) minus 1 sec
trust_threshold = { numerator = '1', denominator = '3' }
address_type = { derivation = 'cosmos'}
[chains.packet_filter]
policy = 'allow'
list = [
  ['*', 'channel-24'],
  ['*', 'channel-25'],
  ['*', 'channel-41'],
  ['*', 'channel-42'],
  ['*', 'channel-44'],
  ['*', 'channel-45'],
  ['*', 'channel-46'],
  ['*', 'channel-47'],
]

[[chains]]
id = 'uni-6'
rpc_addr = 'https://rpc.uni.junonetwork.io/'
grpc_addr = 'http://juno-testnet-grpc.polkachu.com:12690'
websocket_addr = 'wss://rpc.uni.junonetwork.io/websocket'
rpc_timeout = '10s'
account_prefix = 'juno'
key_name = 'rly' # as defined in ics721-demo.env!
store_prefix = 'ibc'
default_gas = 100000
max_gas = 4000000
gas_price = { price = 0.1, denom = 'ujunox' }
gas_multiplier = 1.1
max_msg_num = 30
max_tx_size = 2097152
clock_drift = '5s'
max_block_time = '30s'
trusting_period = '2419199s' # 28 days (unbonding period) minus 1 sec
trust_threshold = { numerator = '1', denominator = '3' }
address_type = { derivation = 'cosmos' }

[chains.packet_filter]
policy = 'allow'
list = [
  ['*', 'channel-86'],
  ['*', 'channel-88'],
  ['*', 'channel-89'],
  ['*', 'channel-90'],
  ['*', 'channel-91'],
  ['*', 'channel-92'],
  ['*', 'channel-93'],
  ['*', 'channel-94'],
]

[[chains]]
id = 'elgafar-1'
rpc_addr = 'https://rpc.elgafar-1.stargaze-apis.com:443'
grpc_addr = 'http://grpc-1.elgafar-1.stargaze-apis.com:26660/'
websocket_addr = 'wss://rpc.elgafar-1.stargaze-apis.com:443/websocket'
rpc_timeout = '10s'
account_prefix = 'stars'
key_name = 'rly' # as defined in ics721-demo.env!
store_prefix = 'ibc'
default_gas = 100000
max_gas = 4000000
gas_price = { price = 0.1, denom = 'ustars' }
gas_multiplier = 1.1
max_msg_num = 30
max_tx_size = 2097152
clock_drift = '5s'
max_block_time = '30s'
trusting_period = '1209599s' # 14 days (unbonding period) minus 1 sec
trust_threshold = { numerator = '1', denominator = '3' }
address_type = { derivation = 'cosmos' }

[chains.packet_filter]
policy = 'allow'
list = [
  ['*', 'channel-203'],
  ['*', 'channel-206'],
  ['*', 'channel-207'],
  ['*', 'channel-208'],
  ['*', 'channel-209'],
  ['*', 'channel-210'],
  ['*', 'channel-211'],
  ['*', 'channel-212'],
]
```

## Go Relayer

```yaml
global:
    api-listen-addr: :5183
    timeout: 10s
    memo: gon
    light-cache-size: 20
chains:
    elgafar-1:
        type: cosmos
        value:
            key: key-1
            chain-id: elgafar-1
            rpc-addr: https://rpc.elgafar-1.stargaze-apis.com:443
            account-prefix: stars
            keyring-backend: test
            gas-adjustment: 1.2
            gas-prices: 0.01ustars
            min-gas-amount: 0
            debug: true
            timeout: 10s
            output-format: json
            sign-mode: direct
            extra-codecs: []
    gon-flixnet-1:
        type: cosmos
        value:
            key: key-1
            chain-id: gon-flixnet-1
            rpc-addr: http://65.21.93.56:26657
            account-prefix: omniflix
            keyring-backend: test
            gas-adjustment: 1.2
            gas-prices: 0.01uflix
            min-gas-amount: 0
            debug: true
            timeout: 10s
            output-format: json
            sign-mode: direct
            extra-codecs: []
    gon-irishub-1:
        type: cosmos
        value:
            key: key-1
            chain-id: gon-irishub-1
            rpc-addr: http://34.80.93.133:26657
            account-prefix: iaa
            keyring-backend: test
            gas-adjustment: 1.2
            gas-prices: 0.01uiris
            min-gas-amount: 0
            debug: true
            timeout: 10s
            output-format: json
            sign-mode: direct
            extra-codecs: []
    uni-6:
        type: cosmos
        value:
            key: key-1
            chain-id: uni-6
            rpc-addr: https://rpc.uni.junonetwork.io:443
            account-prefix: juno
            keyring-backend: test
            gas-adjustment: 1.2
            gas-prices: 0.01ujunox
            min-gas-amount: 0
            debug: true
            timeout: 10s
            output-format: json
            sign-mode: direct
            extra-codecs: []
    uptick_7000-2:
        type: cosmos
        value:
            key: key-1
            chain-id: uptick_7000-2
            rpc-addr: http://52.220.252.160:26657
            account-prefix: uptick
            keyring-backend: test
            gas-adjustment: 1.2
            gas-prices: 0.01auptick
            min-gas-amount: 0
            debug: true
            timeout: 10s
            output-format: json
            sign-mode: direct
            extra-codecs:
                - ethermint
paths:
    gon-flixnet-1_channel-44-elgafar-1_channel-209:
        src:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-64
            connection-id: connection-59
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-186
            connection-id: connection-175
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-flixnet-1_channel-45-elgafar-1_channel-210:
        src:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-65
            connection-id: connection-60
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-187
            connection-id: connection-176
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-flixnet-1_channel-46-uni-6_channel-91:
        src:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-66
            connection-id: connection-61
        dst:
            chain-id: uni-6
            client-id: 07-tendermint-86
            connection-id: connection-94
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-flixnet-1_channel-47-uni-6_channel-92:
        src:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-68
            connection-id: connection-62
        dst:
            chain-id: uni-6
            client-id: 07-tendermint-87
            connection-id: connection-95
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-0-gon-flixnet-1_channel-24:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-0
            connection-id: connection-0
        dst:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-40
            connection-id: connection-37
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-1-gon-flixnet-1_channel-25:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-1
            connection-id: connection-1
        dst:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-41
            connection-id: connection-38
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-17-uptick_7000-2_channel-3:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-17
            connection-id: connection-17
        dst:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-26
            connection-id: connection-25
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-19-uptick_7000-2_channel-4:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-18
            connection-id: connection-19
        dst:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-27
            connection-id: connection-26
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-22-elgafar-1_channel-207:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-20
            connection-id: connection-21
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-184
            connection-id: connection-173
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-23-elgafar-1_channel-208:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-21
            connection-id: connection-22
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-185
            connection-id: connection-174
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-24-uni-6_channel-89:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-22
            connection-id: connection-23
        dst:
            chain-id: uni-6
            client-id: 07-tendermint-84
            connection-id: connection-92
        src-channel-filter:
            rule: ""
            channel-list: []
    gon-irishub-1_channel-25-uni-6_channel-90:
        src:
            chain-id: gon-irishub-1
            client-id: 07-tendermint-23
            connection-id: connection-24
        dst:
            chain-id: uni-6
            client-id: 07-tendermint-85
            connection-id: connection-93
        src-channel-filter:
            rule: ""
            channel-list: []
    uni-6_channel-93-elgafar-1_channel-211:
        src:
            chain-id: uni-6
            client-id: 07-tendermint-88
            connection-id: connection-96
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-188
            connection-id: connection-177
        src-channel-filter:
            rule: ""
            channel-list: []
    uni-6_channel-94-elgafar-1_channel-213:
        src:
            chain-id: uni-6
            client-id: 07-tendermint-89
            connection-id: connection-97
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-189
            connection-id: connection-179
        src-channel-filter:
            rule: ""
            channel-list: []
    uptick_7000-2_channel-5-gon-flixnet-1_channel-41:
        src:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-28
            connection-id: connection-27
        dst:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-60
            connection-id: connection-56
        src-channel-filter:
            rule: ""
            channel-list: []
    uptick_7000-2_channel-6-elgafar-1_channel-203:
        src:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-29
            connection-id: connection-28
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-179
            connection-id: connection-169
        src-channel-filter:
            rule: ""
            channel-list: []
    uptick_7000-2_channel-7-uni-6_channel-86:
        src:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-30
            connection-id: connection-29
        dst:
            chain-id: uni-6
            client-id: 07-tendermint-81
            connection-id: connection-89
        src-channel-filter:
            rule: ""
            channel-list: []
    uptick_7000-2_channel-9-gon-flixnet-1_channel-42:
        src:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-31
            connection-id: connection-30
        dst:
            chain-id: gon-flixnet-1
            client-id: 07-tendermint-61
            connection-id: connection-57
        src-channel-filter:
            rule: ""
            channel-list: []
    uptick_7000-2_channel-12-elgafar-1_channel-206:
        src:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-35
            connection-id: connection-34
        dst:
            chain-id: elgafar-1
            client-id: 07-tendermint-183
            connection-id: connection-172
        src-channel-filter:
            rule: ""
            channel-list: []
    uptick_7000-2_channel-13-uni-6_channel-88:
        src:
            chain-id: uptick_7000-2
            client-id: 07-tendermint-36
            connection-id: connection-35
        dst:
            chain-id: uni-6
            client-id: 07-tendermint-83
            connection-id: connection-91
        src-channel-filter:
            rule: ""
            channel-list: []
```
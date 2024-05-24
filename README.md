# Xanadu Name Service [.xan]

Xanadu Name Service pays homage to the original Project Xanadu by enabling users to dynamically inscribe attributes to Bitcoin blocks, transforming each block into a customizable piece of virtual "real estate" that acts as a framework/ground level protocol and agnostic connection hub. This offers a unified open standard for ordinals metaverses, NFTs, tokens, alt-assets, inscriptions, and more.

## Overview
Xanadu is an Ordinals-based protocol that provides a map interface enabling users to browse, inscribe, trade, and customize Bitcoin blocks. Xanadu integrates seamlessly with the Bitmap consensus standard to authenticate ownership and inscriptions.

## .xan JSON Structure
```json
{
    "p": "xns",
    "inscription_number": "454356",
    "op": "reg",
    "domain": "xanadu",
    "name": "example.xan",
    "inscription_timestamp": "2023-10-05T14:48:00Z",
    "subplots": ["admin.example.xan", "rental.example.xan"],
    "zones": "32",
    "zone_power": "98",
    "avatar": "7f9c06b712c5b60c0b66868c69568b2d198533553c347cd732fc3c87e62efe86i0",
    "url": "xxxx.xxx.xx",
    "socials": ["@examplehandle", "x.com/example"],
    "rev": "bc1q4j3kt5psz5r87kz5a8gnx2vvsdlcmfz2u2pxxw",
    "relay": "85b10531435304cbe47d268106b58b57a4416c76573d4b50fa544432597ad670i0"
}
```

## Features
- **Map Interface**: Explore and interact with the virtual map of Bitcoin blocks.
- **Attribute Inscription**: Inscribe customizable attributes to Bitcoin blocks.
- **Zones**: Enhance the value of Bitcoin blocks by creating and inscribing custom zones. Zones act as Xanadu's native programming/functional/smart contract layer and enable automatic operations and functions when certain conditions are met.
- **Ownership Verification**: Ensure inscriptions can only be made by verified owners.
- **Defi-Style Dividend Returns**: Implement a percentage fee from all transactions that is split and paid out to the wallets of .xan holders.
- **Universal Basic Income (UBI) Tax**: A tax mechanism designed to stimulate the economy by providing a steady revenue stream to .xan holders.

## Xanadu Zone Calculation Methodology
The amount of "power" within a Zone is calculated based on the number of transactions within the corresponding Bitcoin block multiplied by the total value of the block divided by its bitcoin block height number.

### Methodology Steps:
1. **Transaction Counting:** The number of transactions within a Bitcoin block is counted. Each transaction corresponds to one Zone.
2. **Zone Generation:** Each transaction is treated as an independent Zone, allowing for unique attributes to be inscribed onto each one.
3. **Attribute Inscription:** Owners can inscribe attributes onto each Zone, enabling detailed customization of their virtual real estate and enabling exponential possibilities.

## Protocol Specifications

### Schema
The schema for Xanadu is designed to be efficient and straightforward. Below is the format for adding attributes to Bitcoin blocks:

### Xanadu Schema Reference Table
This reference table includes just some of the possible fields that Xanadu supports

| Field                | Description                                                                                   | Example                                                |
|----------------------|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| `p`                  | Xanadu number                                                                                 | `1`                                                    |
| `z`                  | Zones associated with the xanadu                                                              | `[1, 2, 3]`                                            |
| `a`                  | Attributes object containing details about the xanadu                                         |                                                        |
| `a.color`            | Hexadecimal color value representing the xanadu                                               | `"#FFD700"`                                            |
| `a.owner`            | Bitcoin address of the xanadu owner                                                           | `"bc1p7hf8x2q2zal4v64c2h34qheyz4zk8zgnv767ygkkrd5dhg9zackq4rmvhd"` |
| `a.metadata`         | Additional metadata object containing detailed information about the xanadu                   |                                                        |
| `a.metadata.name`    | Name of the xanadu                                                                             | `"First Block"`                                        |
| `a.metadata.description` | Description of the xanadu                                                               | `"This is the first inscribed block"`                  |
| `a.metadata.image`   | URL to an image associated with the xanadu                                                    | `"https://example.com/image.png"`                      |
| `a.namespace`        | Custom namespace for the xanadu                                                               | `"custom"`                                             |
| `a.name`             | Custom name for the xanadu                                                                    | `"unique.block"`                                       |
| `a.method`           | Method used for the inscription                                                               | `"simple"`                                             |
| `a.content`          | Content identifier for the xanadu                                                             | `"5.bitmap"`                                           |
| `a.metadata.tag`     | Tag or category associated with the xanadu                                                    | `"finance"`                                            |
| `a.metadata.url`     | URL associated with the xanadu                                                                | `"https://emblem.finance"`                             |
| `a.block_time`       | Timestamp of the block in which the xanadu was inscribed                                      | `1716565220`                                           |
| `a.block_height`     | Block height of the blockchain when the xanadu was inscribed                                  | `844936`                                               |
| `a.metadata.holder`  | Bitcoin address of the holder of the xanadu                                                   | `"bc1qsnrawwl74fl9q9pk5me2kacxrj3qduh2canaxh"`         |
| `a.metadata.relay`   | URL of the relay used for the inscription                                                     | `"https://example-relay.com"`                          |
| `a.metadata.avatar`  | URL to an avatar image associated with the xanadu                                             | `"https://example.com/avatar.png"`                     |
| `a.inscription_number` | Unique number identifying the inscription                                                   | `10642795`                                             |
| `a.inscription_id`   | Unique identifier for the inscription                                                         | `"42e35206983eabfb09e0c1c8741e98c65a78a824f1550c7e1229b2e252bdf31fi0"` |
| `code`               | Status code of the response                                                                   | `0`                                                    |
| `message`            | Status message of the response                                                                | `"success"`                                            |
| `data`               | Data object containing detailed information about xanadus                                     |                                                        |
| `data.count`         | Total count of xanadus                                                                        | `844943`                                               |
| `data.limit`         | Limit on the number of xanadus returned                                                       | `"20"`                                                 |
| `data.offset`        | Offset for the list of xanadus returned                                                       | `"0"`                                                  |
| `data.list`          | List of xanadus                                                                               |                                                        |
| `data.list.bitmap_number` | Bitmap number of the xanadu                                                            | `0`                                                    |
| `data.list.inscription_id` | Unique identifier for the inscription                                                 | `"86539aff946c437af8088955827b7e6ff48fc6192836d4071b697b5359b7a732i0"` |
| `data.list.holder`   | Bitcoin address of the holder of the xanadu                                                   | `"bc1p7hf8x2q2zal4v64c2h34qheyz4zk8zgnv767ygkkrd5dhg9zackq4rmvhd"` |
| `data.list.inscription_number` | Unique number identifying the inscription                                        | `10423123`                                             |
| `data.list.content`  | Content identifier for the xanadu                                                             | `"0.bitmap"`                                           |
| `data.list.name`     | Name associated with the xanadu                                                               | `"https://emblem.finance"`                             |
| `data.list.namespace` | Namespace associated with the xanadu                                                       | `"finance"`                                            |
| `data.list.block_time` | Timestamp of the block in which the xanadu was inscribed                                 | `1716565220`                                           |
| `data.list.block_height` | Block height of the blockchain when the xanadu was inscribed                           | `844936`                                               |
| `data.list.name_escaped` | Escaped name of the xanadu                                                             | `"https://emblem.finance"`                             |
| `data.list.method`   | Method used for the inscription                                                               | `"simple"`                                             |
| `data.list.avatar`   | URL to an avatar image associated with the xanadu                                             | `""`                                                   |
| `data.list.rev`      | Revision information for the xanadu                                                           | `""`                                                   |
| `data.list.relay`    | URL of the relay used for the inscription                                                     | `""`                                                   |
| `data.list.tick`     | Ticker symbol associated with the xanadu                                                      | `"ordi"`                                               |
| `data.list.max`      | Maximum value associated with the xanadu                                                      | `"21000000.000000000000000000"`                        |

### Xanadu Zone Ranks and Power Boost Traits
This table lists various attributes and ranks that can be associated with Bitcoin blocks and are applied within the Xanadu ecosystem.

| #  | Attribute/Rank           | Description                                                                   |
|----|--------------------------|-------------------------------------------------------------------------------|
| 1  | Mythic                   | The highest rank, representing unique and extremely rare blocks.               |
| 2  | Epic                     | Significant blocks, such as the first block of a halving epoch.                |
| 3  | Rare                     | Important blocks, such as the first block of a difficulty adjustment period.   |
| 4  | Legendary                | Blocks with historical significance, like the ones mined by Satoshi Nakamoto.  |
| 5  | Special                  | Blocks with special attributes, like palindrome blocks or those with significant transactions. |
| 6  | Common                   | Regular blocks with no extraordinary attributes.                              |
| 7  | Double Transaction       | Blocks that contain twice the average number of transactions.                 |
| 8  | Low Fee                  | Blocks with average transaction fees lower than a specified threshold.         |
| 9  | High Fee                 | Blocks with average transaction fees higher than a specified threshold.        |
| 10 | Large Size               | Blocks with a size significantly larger than the average block size.           |
| 11 | Small Size               | Blocks with a size significantly smaller than the average block size.          |
| 12 | High Value               | Blocks with a total output value greater than a specific amount.               |
| 13 | Low Value                | Blocks with a total output value lower than a specific amount.                 |
| 14 | Fast Mining              | Blocks mined in a significantly shorter time than the average block time.      |
| 15 | Slow Mining              | Blocks mined in a significantly longer time than the average block time.       |
| 16 | Special Event            | Blocks associated with special events, such as Bitcoin Pizza Day or blocks mined by well-known entities. |
| 17 | High Reward              | Blocks with a high mining reward.                                              |
| 18 | Low Reward               | Blocks with a low mining reward.                                               |
| 19 | First Transaction        | Blocks which contain the first peer-to-peer transaction between Satoshi and Hal Finney. |
| 20 | Pizza Transaction        | Blocks which contain the "pizza transaction" in which 10,000 BTC was exchanged for two Papa John's pizzas. |
| 21 | Mondrian                 | Blocks that resemble artwork by Piet Mondrian.                                 |
| 22 | Fibonacci                | Blocks which are Fibonacci numbers.                                            |
| 23 | Prime Number             | Blocks which are prime numbers.                                                |
| 24 | Leap Day                 | Blocks which fall on a leap day.                                               |
| 25 | Pizza Day                | Blocks from the day of the famous "Pizza Transaction" (blocks 56899 - 57093).  |
| 26 | Same Digits              | Blocks which contain the same digits for all numbers.                          |
| 27 | Notable Event            | Blocks in which a historical event took place.                                 |
| 28 | One Transaction          | Blocks that contain 1 transaction.                                             |
| 29 | Two Transactions         | Blocks that contain 2 transactions.                                            |
| 30 | Miner Message            | Blocks which contain a message encoded by the miner.                           |
| 31 | Sub 10                   | Blocks mined within the first 10 blocks.                                       |
| 32 | Sub 100                  | Blocks mined within the first 100 blocks.                                      |
| 33 | Sub 1k                   | Blocks mined within the first 1,000 blocks.                                    |
| 34 | Sub 10k                  | Blocks mined within the first 10,000 blocks.                                   |
| 35 | Sub 25k                  | Blocks mined within the first 25,000 blocks.                                   |
| 36 | Sub 50k                  | Blocks mined within the first 50,000 blocks.                                   |
| 37 | Sub 100k                 | Blocks mined within the first 100,000 blocks.                                  |
| 38 | 100k Output              | Blocks which have total outputs greater than 100k BTC.                         |
| 39 | 250k Output              | Blocks which have total outputs greater than 250k BTC.                         |
| 40 | 500k Output              | Blocks which have total outputs greater than 500k BTC.                         |
| 41 | 1M Output                | Blocks which have total outputs greater than 1M BTC.                           |
| 42 | 3M Output                | Blocks which have total outputs greater than 3M BTC.                           |
| 43 | 5M Output                | Blocks which have total outputs greater than 5M BTC.                           |
| 44 | Binary                   | Blocks whose height is a binary number.                                        |
| 45 | MicroStrategy            | Blocks containing a transaction initiated by MicroStrategy.                    |
| 46 | Chinese Lucky Number     | Blocks with a height that includes the Chinese lucky number 168.               |
| 47 | Pre-SegWit Full          | Blocks which maxed out the block size of 1 MB before the SegWit upgrade.       |
| 48 | 1k Transactions          | Blocks that contain 1,000 transactions.                                        |
| 49 | 2k Transactions          | Blocks that contain 2,000 transactions.                                        |
| 50 | Power of 10              | Blocks whose height is a power of 10.                                          |


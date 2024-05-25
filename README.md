# XanBit - Parcel Protocol

XanBit - Parcel Protocol builds upon the ideas introduced by Digital Matter Theory (DMT) by enabling users to dynamically inscribe attributes to Bitcoin blocks, transforming each block into a customizable piece of virtual "real estate." This protocol offers a unified open standard for ordinals metaverses, NFTs, tokens, alt-assets, inscriptions, and more.

## Overview
XanBit is an Ordinals-based protocol that allows users to browse, inscribe, trade, and customize Bitcoin blocks via inscribing programmable XanBits within parcels. XanBit integrates seamlessly with the Bitmap consensus standard to authenticate ownership and inscriptions. Initially, users inscribe .xan domains that evolve into XanBits when attached to a .bitmap.

## .xan JSON Structure
```json
{
    "protocol": "xbp",  // Protocol identifier for XanBit Parcel Protocol
    "inscription_number": "654321",  // Unique number identifying the inscription (Bitcoin Block Height)
    "operation": "register",  // Operation type (register, update, sell, transfer, list, burn, create, inscribe, claim, delegate, distribute)
    "domain": "654321.xan",  // Root domain for the inscription
    "name": "mattty.xan",  // Full name of the domain
    "parcels": [
        {
            "parcel_id": "x.mattty.xan",  // Unique identifier for the parent parcel
            "xanbits": "5",  // Number of XanBits within the parcel
            "xanbit_power": "50",  // Total power level of the XanBits
            "xanbits": [
                {
                    "name": "donate.mattty.xan",  // Name of the parcel
                    "content": "dapp",  // Content hosted within the parcel
                    "attributes": {
                        "type": "webpage",  // Type of content
                        "description": "Ordinals donation page",  // Description of the parcel
                        "avatar": "7f9c06b712c5b60c0b66868c69568b2d198533553c347cd732fc3c87e62efe86i0",  // Avatar image hash
                        "url": "donate.mattty.xan",  // URL associated with the parcel
                        "socials": ["@mattyverse", "twitch.com/mattyverse"],  // Social media links
                        "revision": "bc1q4j3kt5psz5r87kz5a8gnx2vvsdlcmfz2u2pxxw",  // Revision information
                        "relay": "85b10531435304cbe47d268106b58b57a4416c76573d4b50fa544432597ad670i0"  // Relay information
                    }
                },
                {
                    "name": "stream.mattty.xan",  // Name of the parcel
                    "content": "code",  // Content hosted within the parcel
                    "attributes": {
                        "type": "link",  // Type of content
                        "description": "Link to my stream!",  // Description of the parcel
                        "url": "twitch.com/mattyverse"  // URL associated with the parcel
                    }
                }
            ]
        }
    ],
    "inscription_timestamp": "2023-10-05T14:48:00Z"  // Timestamp of the inscription
}
```

## Features
- **Map Interface**: Explore and interact with the virtual map of Bitcoin blocks.
- **Attribute Inscription**: Inscribe customizable attributes to Bitcoin blocks.
- **XanBits**: Enhance the value of Bitcoin blocks by creating and inscribing custom XanBits. XanBits act as XanBit's native programming/functional/smart contract layer and enable automatic operations and functions when certain conditions are met.
- **Ownership Verification**: Ensure inscriptions can only be made by verified owners.
- **Defi-Style Dividend Returns**: Implement a percentage fee from all transactions that is split and paid out to the wallets of .xan holders.
- **Universal XanBit Stream (UXS)**: An optional programmable financial mechanism designed to stimulate the economy by providing a steady revenue stream to .xan holders.

## XanBit XanBit Calculation Methodology
The amount of "power" within a XanBit is calculated based on the number of transactions within the corresponding Bitcoin block multiplied by the total value of the block divided by its Bitcoin block height number.

### Methodology Steps:
1. **Transaction Counting:** The number of transactions within a Bitcoin block is counted. Each transaction corresponds to one XanBit.
2. **XanBit Generation:** Each transaction is treated as an independent XanBit, allowing for unique attributes to be inscribed onto each one.
3. **Attribute Inscription:** Owners can inscribe attributes onto each XanBit, enabling detailed customization of their virtual real estate and enabling exponential possibilities.

## Protocol Specifications

### Schema
The schema for XanBit is designed to be efficient and straightforward. Below is the format for adding attributes to Bitcoin blocks:

### XanBit Schema Reference Table
This reference table includes some of the possible fields that XanBit supports:

| Field                | Description                                                                                   | Example                                                |
|----------------------|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| `protocol`           | XanBit protocol identifier                                                                    | `xbp`                                                  |
| `operation`          | Operation type (register, update, sell, transfer, inscribe, claim, delegate, distribute)      | `register`                                             |
| `domain`             | Root domain for the inscription                                                               | `654321.xan`                                           |
| `name`               | Full hierarchical name of the parcel                                                          | `home.6.123456.xan`                                    |
| `inscription_number` | Unique number identifying the inscription                                                     | `654321`                                               |
| `inscription_timestamp` | Timestamp of the inscription                                                              | `2023-10-05T14:48:00Z`                                 |
| `parcel_id`          | Unique identifier for the parent parcel                                                       | `123456.xan`                                           |
| `xanbits`            | Number of XanBits within the parcel                                                           | `5`                                                    |
| `xanbit_power`       | Power level of the XanBits                                                                    | `50`                                                   |
| `xanbit`             | Array of objects representing XanBits within the parent parcel                                |                                                        |
| `xanbit[].name`      | Name of the XanBit                                                                            | `home.6.123456.xan`                                    |
| `xanbit[].content`   | Content hosted within the XanBit                                                              |                                                        |
| `xanbit[].content.type` | Type of content                                                                           | `webpage`                                              |
| `xanbit[].content.html` | HTML content for a webpage                                                                | `<html>...</html>`                                     |
| `xanbit[].content.3d_models` | Array of 3D model filenames for VR experiences                                       | `["model1.obj", "model2.obj"]`                         |
| `xanbit[].content.scripts` | Array of script filenames for VR experiences                                           | `["script1.js", "script2.js"]`                         |
| `xanbit[].attributes` | Additional metadata and attributes related to the XanBit                                    |                                                        |
| `xanbit[].attributes.description` | Description of the XanBit                                                       | `A home page`                                          |
| `xanbit[].attributes.avatar` | Avatar image hash representing the XanBit                                            | `7f9c06b712c5b60c.....47cd732fc3c87e62efe86i0` |
| `xanbit[].attributes.url` | URL associated with the XanBit                                                         | `home.example.xan`                                     |
| `xanbit[].attributes.socials` | Array of social media links related to the XanBit                                   | `["@examplehome", "x.com/examplehome"]`                |
| `xanbit[].attributes.revision` | Revision information for the XanBit                                                | `bc1q4j3kt5psz5r87kz5a8gnx2vvsdlcmfz2u2pxxw`           |
| `xanbit[].attributes.relay` | Relay information associated with the XanBit                                         | `85b105314.....4b50fa544432597ad670i0` |

### XanBit XanBit Ranks and Power Boost Traits
Various attributes and ranks can be associated with Bitcoin blocks and applied within the XanBit ecosystem.

## Transition from .xan to XanBit
1. **Initial .xan Creation**:
   - Users create a .xan domain name (e.g., `mattty.xan`) which represents their ownership and ability to manage the content within the parcel.
2. **Attachment to .bitmap**:
   - When a .xan domain is attached to a .bitmap, it evolves into a XanBit, gaining additional functionalities and capabilities provided by the Bitmap consensus standard.
   - Example: `123456.xan` attached to `654321.bitmap` evolves into a XanBit, unlocking enhanced features and interoperability within the XanBit ecosystem.

### Use Cases

1. **Decentralized Web Browsing**:
   - Users access decentralized websites using .xan domains.
   - Browsers resolve these domains to XanBits and load the corresponding content.

2. **Metaverses**:
   - Host expanded environments within child inscriptions.
   - Users can navigate through different experiences using hierarchical addresses.

3. **E-commerce and Stores**:
   - Create

 child inscriptions for online stores.
   - Example: `shop.123456.xan` hosts a shopping interface.

4. **Scalable & Dynamic**:
   - Enable ongoing upgrades and expansions through reinscriptions.
   - Dynamic independent expansion without disrupting existing content.

### Benefits

- **Decentralization**: Eliminates central points of failure, enhancing security and resilience.
- **Scalability**: Hierarchical structure allows for infinite subdivision and growth.
- **User-Friendly**: .xan domains provide an intuitive way to navigate the ordiweb.
- **Persistent Upgrades**: Reinscriptions ensure continuous improvement and adaptability.

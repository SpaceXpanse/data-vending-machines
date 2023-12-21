---
layout: default
title: NIP-89
description: The role of NIP-89 on using Data Vending Machines
---

NIP-89 defines *application recommendation* and *application handler* events.

Data Vending Machines make extend use of these capabilities; DVMs should announce their capabilities by creating an application handler event with a `k` of the handled job request kind.

A `kind:31990` (application handler) event should use it's `content` profile data to explain to an end-user its specific characteristics.

Clients SHOULD show this information as a way to allow users to choose the specific DVM they want to use.

This is where the long-tail of DVMs can be explored.

# Example

## DVM supporting `kind:5100` -- in Dali style

This NIP-89 acts as a sales-pitch for the DVM to explain to a user exactly what they can expect from interacting with this DVM

```json
{
  "created_at": 1693484377,
  "content": "{
        \"name\": \"Dali Vending Machine\",
        \"image\": \"https://cdn.nostr.build/i/fb207be87d748ad927f52a063c221d1d97ef6d75e660003cb6e85baf2cd2d64e.jpg\",
        \"about\": \"I'm Dali re-incarnated, faster and cheaper\",
        \"encryptionSupported\": True,

    }",
  "tags": [
    [ "d", "td51xbgxwbt5116r" ],
    [ "k", "5100" ]
  ],
  "kind": 31990,
  "pubkey": "6b37d5dc88c1cbd32d75b713f6d4c2f7766276f51c9337af9d32c8d715cc1b93",
}
```

## DVM supporting `kind:5300`

This NIP-89 acts as a sales-pitch for the DVM to explain to a user exactly what they can expect from interacting with this DVM

```json
{
  "created_at": 1693484377,
  "content": "{
        \"name\": \"You might have missed\",
        \"image\": \"https://cdn.nostr.build/i/fb207be87d748ad927f52a063c221d1d97ef6d75e660003cb6e85baf2cd2d64e.jpg\",
        \"about\": \"My goal is to help you keep up – or catch up – with your world, no matter how much time you spend on t̶w̶i̶t̶t̶e̶r̶ nostr.\",
        \"encryptionSupported\": False,
    }",
  "tags": [
    [ "d", "td51xbgxwbt5116r" ],
    [ "k", "5300" ]
  ],
  "kind": 31990,
  "pubkey": "6b37d5dc88c1cbd32d75b713f6d4c2f7766276f51c9337af9d32c8d715cc1b93",
}
```

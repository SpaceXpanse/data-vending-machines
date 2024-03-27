# data-vending-machines.org

This is the website for [data-vending-machines.org](https://www.data-vending-machines.org/), which specs the different NIP-90 kinds.

# Rationale
Nostr can act as a marketplace for data processing, where users request jobs to be processed in certain ways (e.g., “speech-to-text”, “summarization”, etc.), but they don’t necessarily care about “who” processes the data.

This NIP is not to be confused with a 1:1 marketplace; instead, it describes a flow where a user announces a desired output, willingness to pay, and service providers compete to fulfill the job requirement in the best way possible.

# Actors
There are two actors in the workflow described in this NIP:

- Customers (npubs who request a job)
- Service providers (npubs who fulfill jobs)

# License

MIT

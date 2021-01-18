# Sending messages

**This topic gives you a high-level overview of the steps involved in sending a message. At the end of this tutorial, you'll understand what's involved in sending a message and why.**

Sending a message includes the following steps:

- Choosing an IOTA network
- Getting a message to link to (tip)
- Doing proof of work
- Sending the message to a node

![Sending a transaction](../images/sending-transaction.png)

## Choosing an IOTA network

The first step in sending a message is to choose a node to send it to. This node is your entry point to the Tangle of an IOTA network. See [IOTA networks](../networks/overview.md) for an overview of the different networks.

:::info:
In the previous [tutorial](../first-steps/hello-world.md), you connected to a node in the Devnet.
:::

## Getting tip messages

To attach your message to the Tangle, you need to reference the message hashes of two tip messages in the Tangle. These messages are the ones that your message will be attached to in the Tangle.

To request tip messages from the Tangle, the client asks the node to traverse the Tangle in a process called tip selection.

All IOTA node software includes an algorithm for [selecting tip messages](../the-tangle/how-transfer-tokens.md#choosing-where-to-attach-transactions). These algorithms aim to select valid tip messages with the best chance of being confirmed.

## Doing proof of work

Proof of work (PoW) is cryptographic proof that energy has been spent in computing power to solve a puzzle.

IOTA messages must contain a PoW to discourage clients from sending lots of spam messages, which may put an extra load on nodes. See [Hashcash](https://en.wikipedia.org/wiki/Hashcash) for more examples of PoW as a spam prevention measure.

An important attribute of any PoW algorithm is that it's difficult to do, but easy to validate. See [Calculating proof of work](../cryptography/proof-of-work.md). 

You have the following options for doing PoW:

- Remote PoW: When a node does PoW for your message
- Local PoW: When your local device does PoW for your message
- Outsourced PoW: When a device that is neither a node nor your local device does PoW

Each option for PoW has its advantages and disadvantages.

|**Option**|**Advantages**|**Disadvantages**|
|:-------|:---------|:------------|
|Remote PoW| You can avoid using the computational power needed to do PoW on your own device|Depending on how powerful the node is and how many requests it receives, it may time out and not complete the PoW |
|Local PoW|You aren't reliant on nodes to do PoW|Your device may not be powerful enough to complete PoW in a satisfactory amount of time so your message has a smaller chance to be included|
|Outsourced PoW|PoW is usually done faster more more reliably than remote or local PoW|It costs money to set up or use the service|

## Sending the messages to a node

The last step is sending the messages to the node so that it can attach the message to the Tangle.

## Next steps

[Learn about the Tangle](../the-tangle/overview.md) and what makes it so powerful.
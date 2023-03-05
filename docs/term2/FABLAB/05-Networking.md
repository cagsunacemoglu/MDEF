# Networking

In the class about networking, we started with discussing what a network is, and elaborated on the philosophical aspects of what are the basic functions of networks, and the design decisions that went behind the networks we know today.

For me, it was interesting to see how networks are architectured by incapsulating the same information on multiple layers, so that the information can arrive at the destination without being harmed.

![](https://i.imgur.com/J3Eq7Z1.png)


The analogy that I came up with that it finally made sense for me is shipping an item to the other end of the world, for instance, to a place like Alaska. You need to layer your item in multiple layers so that it survives the whole journey:
- a bubbled air bag as first layer to protect it in the local van that makes the first transfer, 
- a cardboard box to make it’s safe for the airplane,
- a plastic bag, so that it doesn’t get wet across the ocean in a ship,
- a heat isolated bag, so that it doesn’t get too cold on the way to Alaska from the port…

I guess information travelling over networkds is like that, it moves across multiple continents, between many vehicles that carry information, and it needs to be compatible with the systems that carry it, similar to shipping company standards, they need to be in certain sizes and packages, and they stick labels on them so that anyone on the road can identify the item.

In the last part of the class, we worked on practically establishing a network. I found it interesting that there needs to be a broker - a moderator in the system even when we wanted to send messages from one to another. Similarly, it was also surprising for me to learn that the information we share with companies go to their headquarters and get processed/routed there to wherever it’s stored. I always assumed that the network would be decentralised, and each node of the system would be able to handle the information so that the central processing doesn’t get overloaded. I’d want to explore that a bit more.

![](https://i.imgur.com/42CO0Jz.jpg)


The highlight of building such a network for me was being able to build a local area network over WLAN where machines can talk to each other, send commands and requests, and collaborate without having to connect over the Internet. I think this opens up a lot of possibilities to create a kind of intelligence in the local space through talking devices that do not need any human intervention.

![](https://i.imgur.com/ZxAlYER.jpg)

We followed the following code with Dhriti to establish connection to the local network and send messages to the class, and receive their messages in return. 

https://hackmd.io/CAj0Y8O3QGKjmH2b4r3Tag?view

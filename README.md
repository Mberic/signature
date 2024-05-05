## About 
This project uses the Pose Animator library[1] to produce an NFT when 1 actor interacts with 1 or more actors. The NFT acts as an acknowledgment of the interaction. Interaction can mean various things:

- Meeting a certain actor ( perhaps a famous individual )
- Receipt of something ( a digital certificate for course completion )
- Agreement of certain terms 
- And so on…

This approach aims to preserve the aspects of human interaction that would exist in a physical environment when interacting from a digital one. For example, one can still be expressive when digitally signing an agreement. The NFT generated from the metadata of this interaction would be the proof of the underlying agreement. 

We will focus this project on the generation of Commemorative NFTs. **The project is called SigNature ( pronounced Sign-Nature ).**

## Motivation 
This project was partly inspired by my previous project, whose aim was to ensure that all NFT objects were digitally alive. The project, called [DNN](https://github.com/Mberic/dnn) (Digital Native NFTs), was a Prize Pool winner for the Cartesi 2024 Hackathon. Among the intended use cases for DNN was for NFT objects to be able to interact.

The approach in DNN required using geometric objects. This presented some challenges which we will not discuss here. However, after some research, I discovered that using a motion animation ML model to generate NFT objects was the way to go. 

This project (SigNature) aims to focus on interactions leading to an agreement. We aim to exploit the DataProtector library that iExec offers in order to protect the contents of the agreement between the parties. The iExec platform carries out a number of tasks including:

- Data availability. Stores the encrypted agreement 
- Signature aggregation & validation 
- Managing NFT transfers 

## Tools 
### Frontend

- WebRTC
- Thirdweb SDK

### Backend 
- DataProtector
- Pose Animator

## Design
### Architecture 
[IMAGE]
### Description 

SigNature is a WebRTC application that uses the Pose Animator for the interaction between users. 

The data being agreed upon is encrypted by the DataProtector and sent to the blockchain. The data never has to be decrypted on the blockchain. 

The whole point of storing them on the blockchain is to act as a commitment in our commit-reveal scheme. Later, if there's a disagreement on the nature of the contents/terms, the data can be decrypted off-chain ( or on-chain, if necessary) to reveal the contents. 

## Features 

- Real-time interaction (i.e generation of handshake NFT)
- Signature aggregation in case of multiple parties agreeing with one other party ( the prize-giver can award multiple NFT handshakes at once )
- After the prize-giving ceremony, partcipants can share the ceremony moments on social media platforms. This wouldn't be possible if our perception of a digital agreement was restricted to the cryptography. 

## Future developments 

- Use voice recognition to capture handshake NFTs when in position 

## References 
- [Pose Animator by Shan Huang](https://github.com/yemount/pose-animator)
- [DataProtector](https://documentation-tools.vercel.app/tools/dataProtector.html)
- BLS Signature Aggregation 



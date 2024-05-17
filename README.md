# SigNature
## About 

This project uses the [Pose estimation](https://www.tensorflow.org/lite/examples/pose_estimation/overview#:~:text=Pose%20estimation%20is%20the%20task,key%20body%20joints%20(keypoints).) to animate human movements when 2 or more actors interact with each other. The captured animation is used to create an NFT. 

The NFT acts as an acknowledgment of an interaction. Interaction can mean various things:

- Meeting a certain actor ( perhaps a famous individual )
- Acceptance of an award or acknowledgment ( e.g. if you were a prize winner in an online completion )
- Agreement of certain terms 
- And so on…


*This approach (of NFT generation) aims to preserve the aspects of human interaction that would exist in a physical environment when interacting from a digital one.*


For example, one can still be expressive when digitally signing an agreement. The NFT generated from the metadata of this interaction would be the proof of the underlying agreement. 
Focus
As shown above, there are many possible use cases for this approach to NFT generation. 

However, **the PoC here will focus on generation of Commemorative NFTs**. The project is called SigNature ( pronounced Sign-Nature ).

## Motivation 
This project was partly inspired by my previous project, whose aim was to ensure that all NFT objects were digitally alive. The project, called [DNN](https://github.com/Mberic/dnn) (Digital Native NFTs), was a Prize Pool winner for the Cartesi 2024 Hackathon. Among the intended use cases for DNN was for NFT objects to be able to interact.

The approach in DNN requires using geometric objects. This presented some limitations, particularly regarding the expressiveness of an NFT creator (s).

However, after some research, I discovered that using a pose estimation ML model could resolve these challenges. When coupled with animation, the possibilities to pose estimation become limitless. 

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

SigNature is a WebRTC application which uses -**Pose Animation to generate an NFT from the digital interaction** between users. 

The data being agreed upon is encrypted by the DataProtector and sent to the blockchain. The data never has to be decrypted on the blockchain. 

The whole point of storing them on the blockchain is to act as a **commitment** in our commit-reveal scheme. Later, if there's a disagreement on the nature of the contents/terms, the data can be decrypted off-chain ( or on-chain, if necessary) to **reveal** the contents. 

## Features 

- Real-time interaction (i.e generation of handshake NFT)
- Signature aggregation in case of multiple parties agreeing with one other party ( the prize-giver can award multiple NFT handshakes at once )
- After the prize-giving ceremony, partcipants can share the ceremony moments on social media platforms. This wouldn't be possible if our perception of a digital agreement was restricted to the cryptography. 

## DApp Monetization 

Charge a small platform fee for any NFT transfers
A small fee for NFT generation to prevent sybil attacks

## Future developments 

- Fractional NFTs management 
- Use voice recognition to capture handshake when in position

## References 
- [Pose estimation](https://www.tensorflow.org/lite/examples/pose_estimation/overview#:~:text=Pose%20estimation%20is%20the%20task,key%20body%20joints%20(keypoints).)
- [Pose Animator by Shan Huang](https://github.com/yemount/pose-animator)
- [DataProtector](https://documentation-tools.vercel.app/tools/dataProtector.html)
- BLS Signature Aggregation 



<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** This README is created using template from https://github.com/othneildrew/Best-README-Template
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/sadityakumar9211/thegraph-nft-marketplace">
    <img width="54" alt="image" src="https://user-images.githubusercontent.com/78147198/187690391-be5b65b7-1bb6-44bb-982a-821782ae41c4.png">

  </a>

  <h2 align="center">NFT Marketplace</h2>

  <p align="center">
    This repository is one of the three repositories which are part of NFT Marketplace Project.
    <br />
    <br>
    <a href="https://github.com/sadityakumar9211/hardhat-nft-marketplace"><strong> <i>hardhat-nft-marketplace</i>: Hardhat Repository of NFT Marketplace Project»</strong></a>
    <br>
    <a href="https://github.com/sadityakumar9211/medichain-nextjs"><strong> <i>nextjs-nft-marketplace</i>: The Next.js Repository of NFT Marketplace Project»</strong></a>
    <br>
    <br />
    <br />
    <a href="https://nftmarketplace-thegraph.vercel.app/">View Demo</a>
    ·
    <a href="https://github.com/sadityakumar9211/thegraph-nft-marketplace/issues">Report Bug</a>
    ·
    <a href="https://github.com/sadityakumar9211/thegraph-nft-marketplace/issues">Request Feature</a>
  </p>
</div>

### This is the `The Graph` repository of this project. 

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#requirements">Requirements</a></li>
        <li><a href="#quickstart">Quickstart</a></li>
      </ul>
    </li>
    <li><a href="#locally-deploying">Locally Deploying</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

<img width="1234" alt="image" src="https://user-images.githubusercontent.com/78147198/187690506-9bd4c016-cb5e-457d-b03c-fb9573b405c6.png">


**Blockchain** developed the idea of NFTs and introduced digital ownership of certain assets. This is because tokens are not exchangeable which makes it possible to establish property ownership in digital art. 

NFT marketplace is a digital platform to create and trade digital assets. There are several marketplaces to create, sell, buy and trade NFTs. This is one small implementation of such platforms. The platform can allow you to buy and sell NFTs. You can also withdraw funds which you earned after selling the NFTs. For supporting fast and complex queries this system uses a decentralized indexing protocol *The Graph*. The smart contract is currently deployed on *Rinkeby Testnet*.

### The links to other repositories of this project is at the top.
<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Built With

This repository contains the code for developing a subgraph which indexes the smart-contract deployed in the [hardhat-nft-marketplace](https://github.com/sadityakumar9211/hardhat-nft-marketplace) repository.
- [![The Graph][The Graph]][Graph-url]



<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
# Getting Started

## Requirements

- [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
  - You'll know you did it right if you can run `git --version` and you see a response like `git version x.x.x`
- [Nodejs](https://nodejs.org/en/)
  - You'll know you've installed nodejs right if you can run:
    - `node --version` and get an ouput like: `vx.x.x`
- [Yarn](https://classic.yarnpkg.com/lang/en/docs/install/) instead of `npm`
  - You'll know you've installed yarn right if you can run:
    - `yarn --version` and get an output like: `x.x.x`
    - You might need to install it with `npm`
- Optional Instruction
  - Make sure that this repository and `hardhat-nft-marketplace` repository are in the same level in your directory structure.
  - This makes sure that whenever you deploy the smart contract, this repository's `constants` files are updated.
## Quickstart

1. Install Subgraph CLI

```
yarn global add @graphprotocol/graph-cli
```

2. Log into [the graph UI](https://thegraph.com/studio/subgraph) and create a new Subgraph.

Use Rinkeby as the network. 

3. Initialize Subgraph

```
graph init --studio medichain
```

4. Authenticate CLI

```
graph auth  --studio YOUR_DEPLOY_KEY_HERE
```

5. Update your `subgraph.yaml`:

- Update the `address` with your `PatientMedicalRecordSystem` Contract Address
- Update the `startBlock` with the block right before your contract was deployed

6. Build graph locally

```
graph codegen && graph build
```

- `graph codegen`: Generates code in the `generated` folder based on your `schema.graphql`
- `graph build`: Generates the build that will be uploaded to the graph

7. Deploy subgraph

Replace `VERSION_NUMBER_HERE` with a version number like `v0.0.1`. 

```
graph deploy --studio nft-marketplace -l VERSION_NUMBER_HERE
```

8. Update the temporary query URI in the Next.js project

- update the `uri` in your `_app.js` with the temporary query URI generated after deploying your subgraph.

- To start your frontend run: 
```
yarn dev
```


### Optional Gitpod

If you can't or don't want to run and install locally, you can work with this repo in Gitpod. If you do this, you can skip the `clone this repo` part.

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#github.com/sadityakumar9211/thegraph-nft-marketplace)


<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

If you appreciated this, feel free to follow me or donate!

ETH Address: 0xED5A704De64Ff9699dB62d09248C8d179bb77D8A

[![Aditya Singh Linkedin](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/saditya9211/)
[![Aditya Singh Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/sadityakumar921)
[![Aditya Singh StackOverflow](https://img.shields.io/badge/StackOverflow-gray?style=for-the-badge&logo=stackoverflow&logoColor=orange)](https://stackoverflow.com/users/14769639/saditya)
[![Aditya Singh Medium](https://img.shields.io/badge/Medium-000000?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@sadityakumar9211)
[![Aditya Singh Gmail](https://img.shields.io/badge/Gmail-gray?style=for-the-badge&logo=gmail)](mailto:sadityakumar9211@gmail.com)

Project Link: [https://github.com/sadityakumar9211/hardhat-nft-marketplace](https://github.com/sadityakumar9211/hardhat-nft-marketplace)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Choose an Open Source License](https://choosealicense.com)


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/sadityakumar9211/thegraph-nft-marketplace.svg?style=for-the-badge
[contributors-url]: https://github.com/sadityakumar9211/thegraph-nft-marketplace/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/sadityakumar9211/thegraph-nft-marketplace.svg?style=for-the-badge
[forks-url]: https://github.com/sadityakumar9211/thegraph-nft-marketplace/network/members
[stars-shield]: https://img.shields.io/github/stars/sadityakumar9211/thegraph-nft-marketplace.svg?style=for-the-badge
[stars-url]: https://github.com/sadityakumar9211/thegraph-nft-marketplace/stargazers
[issues-shield]: https://img.shields.io/github/issues/sadityakumar9211/thegraph-nft-marketplace.svg?style=for-the-badge
[issues-url]: https://github.com/sadityakumar9211/thegraph-nft-marketplace/issues
[license-shield]: https://img.shields.io/github/license/sadityakumar9211/thegraph-nft-marketplace.svg?style=for-the-badge
[license-url]: https://github.com/sadityakumar9211/thegraph-nft-marketplace/blob/master/LICENSE
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/saditya9211
[product-screenshot]: https://user-images.githubusercontent.com/78147198/184471278-42e393d0-db94-4577-bdc9-328510b777c0.png

<!-- This is the beginning of the URLs of Badges -->


[The Graph]: https://img.shields.io/badge/The_Graph-23243B?style=for-the-badge&logoColor=6DE9DB
[Graph-url]: https://thegraph.com/en/




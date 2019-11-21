<h1 align="center">Welcome to Bloction 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.2.0-blue.svg?cacheSeconds=2592000" />
  <a href="https://github.com/hoji2/BlockChain_README" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
</p>

> 블록체인 기반 P2P 경매시스템

# Bloction

블록체인 기반 경매 참여 이력을 기록하여 투명한 경매 서비스 제공

# 핵심기능

## 1) 지갑생성

이더리움 기반 스마트컨트랙트 거래에 필요한 지갑을 생성한다. 위 사이트의 사용자들은 지갑 생성 시 발급되는  **Private Key**를 숙지하여한다.  다양한 기능을 이용할 시 개인 인증에 **Private Key**를 사용하기 때문이다.

## 2) 작품등록 및 상세보기

작품을 등록할 사용자는 작품의 이름, 작품설명, 공개 여부등을 설정하여 요청하면 관련 작품 내역은 데이터베이스에 등록되며, 경매가 진행되는 동안 해당 작품의 **소유내역**을 상세보기를 통해 확인할 수 있다.

<img src="https://user-images.githubusercontent.com/46040830/69293995-f3c4d680-0c4d-11ea-9333-8cd5781951f4.gif"/>

## 3)경매등록

작품의 소유자는  경매등록 시 최저가, 시작 및 종료일자등을 입력하여 경매를 생성할 수 있다. 경매를 블록체인 원장에 등록하는 과정에서 **수수료**가 발생한다.

<img src="https://user-images.githubusercontent.com/46040830/69299045-ea8a3880-0c52-11ea-9596-105894973108.gif"/>

## 4)입찰 

입찰자는 이더리움을 충전하고 경매에 올라온 작품을 입찰할 수 있다. 최초 입찰 이후로 해당 작품에서 **최고 입찰자**와 **최고 입찰금액**을 가시적으로 확인할 수 있다.

<img src="https://user-images.githubusercontent.com/46040830/69298047-12c46800-0c50-11ea-91de-164ba6809f71.gif"/>

## 5)낙찰 및 경매종료

경매를 생성한 사용자는 경매 마감시간 내 경매종료가 가능하며, 경매종료시 낙찰금을 회수한다. 최고입찰자 이외에 입찰자들은 **경매종료 후 입찰금 반환을 통헤** 자신의 입찰금을 회수받는다. 

- 경매생성자

  -> 입찰금 회수

<img src="https://user-images.githubusercontent.com/46040830/69298066-21128400-0c50-11ea-8734-1e89de743bbc.gif"/>

- 최종 낙찰자 및 기타 입찰자

  -> 최종 낙찰자(bidder02)는 자신의 입찰금을 차감하고 입찰 실패 사용자(bidder01)는 입찰금을 회수받는다.

<img src="https://user-images.githubusercontent.com/46040830/69298747-22dd4700-0c52-11ea-935c-16b3b3ab0105.gif"/>

## Requirements

### Front-End
- Vue.js
- Vue Router
- Vuetify
- HTML
- CSS
- Javascript

### Back-End
- Spring Framework
- MySQL

### BlockChain
- Ethereum
- Docker
- HyperLedger Fabric
- Solidity

### Management Tools
- Git
- Jira 

### Service
- AWS EC2

## Install

```sh
npm install
```

## Usage

- Front
```sh
npm run serve
```
- Back
```sh
run server
```

- Ethereum
  - 이더리음 노드간 peer연결을 담당하는 Shell script 실행
```sh
./start.sh
```

- Fabric Network
  - Docker-Compose를 활용한 kafka, orderer, CA 서버 구동
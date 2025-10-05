<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8"
</head>
<body>
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=24&duration=5000&pause=1000&color=blue&center=true&vCenter=true&width=465&lines=DRACK-KING;" alt="Typing SVG" />

</body>
</html>

<a href="https://99bf1182-f1fd-48b3-bf79-3d1121406f45-00-jojehctjy2bf.pike.replit.dev/">
  <img src="https://img.shields.io/badge/Whatsapp%20PAIR%20CODE-Click%20Here-black?style=for-the-badge&logo=whatsapp&logoColor=white&labelColor=25D366" />
</a>
  node.js code copy code 👇
  
   
   name: Node.js CI

on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:

    runs-on: ubuntu-latest

    strategy:
      matrix:
        node-version: [20.x]
        # See supported Node.js release schedule at https://nodejs.org/en/about/releases/

    steps:
    - uses: actions/checkout@v4
    - name: Use Node.js ${{ matrix.node-version }}
      uses: actions/setup-node@v4
      with:
        node-version: ${{ matrix.node-version }}
        cache: 'npm'
    - run: npm install
    - run: npm run start
    - run: npm test

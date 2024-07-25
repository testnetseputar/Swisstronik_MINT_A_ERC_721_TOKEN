### Tutorial Cara Mengerjakan Misi Swisstronik Ke 3 (Mint a ERC-721 Token)

## REMINDER !

Sebelumnya Saya Ingatkan Untuk Menggunakan New Wallet, Terserah Masing - Masing, ini Hanya Saran.
Tutorial Yang Saya Berikan Adalah Kumpulan Dari Berbagai Sumber Yang Sudah Saya Rangkum Agar Lebih Mudah Di Pahami Bagi Mereka Yang Mau Mengerjakan ( DYOR )

Untuk Link Misinya Disini: [Click!](https://www.swisstronik.com/testnet2/dashboard)

## IKUTI LANGKAH DEMI LANGKAH

### 1. Copy Paste Link Di Bawah ini Ke Gitpod ( Diawali Https Tanpa Ada Huruf Git Clone )

```bash
git clone https://github.com/seputartestnet/swisstronik3
```

```
cd swisstronik-erc721-mint-token
```
### 2. Tambahkan File .env Lalu Kemudian Masukkan Private Key Wallet Kalian Yang Sudah Kalian Buat

create .env file in root project

```bash
PRIVATE_KEY="your private key"
```

### 4. Edit NFT Yang Akan Kalian Buat

- Buka Menu Contracts
- Buka File Nft.sol
- Silahkan Ubah Nama Dan Symbol Seperti Yang Kalian Inginkan

```
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract TestNFT is ERC721 {
    uint256 private _currentTokenId = 0;

    event NFTMinted(address recipient, uint256 tokenId);

    constructor() ERC721("Percobaan", "PRC") {}

    function mintNFT(address recipient) public returns (uint256) {
        _currentTokenId += 1;
        uint256 newItemId = _currentTokenId;
        _mint(recipient, newItemId);

        emit NFTMinted(recipient, newItemId);

        return newItemId;
    }

    function burnNFT(uint256 tokenId) public {
        _burn(tokenId);
    }
}

```

### 5. Deploy Kontrak Pintar

```bash
npm run deploy
```

### 6. Mint Token

```bash
npm run mint
```

### 7. Selesai Dan Kalian Tinggal Copy Paste Misi Yang Sudah Dikerjakan

- Buka Menu deployed-adddress.ts Untuk Misi Kontrak Pintar
- Buka Menu tx-hash.txt Untuk Mengetahui TX Hash
- Lalu Tinggal Copy Paste Ke Halaman Swisstronik Testnet 3

Untuk Link Misinya Disini: [Click!](https://www.swisstronik.com/testnet2/dashboard)

### Terimakasih Dan Semoga Bermanfaat

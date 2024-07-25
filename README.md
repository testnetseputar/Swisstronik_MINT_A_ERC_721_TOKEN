# Swisstronik Tesnet Techinal Task Ke 3 (Mint a ERC-721 Token)

Sebelumnya Saya Ingatkan Untuk Menggunakan New Wallet, Terserah Masing - Masing, ini Hanya Saran.

Untuk Link Misinya Disini: [Click!](https://www.swisstronik.com/testnet2/dashboard)

## Steps

### 1. Copy Paste Link Di Bawah ini Ke Gitpod ( Diawali Https Tanpa Ada Huruf Git Clone )

```bash
git clone https://github.com/Mnuralim/swisstronik-erc721-mint-token.git
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
- Lalu Tinggal Copy Paste Ke Halaman Swisstronik Testnet 3 Terimakasih Dan Semoga Bermanfaat

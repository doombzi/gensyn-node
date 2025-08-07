# 🧠 Gensyn Node Setup Guide 

Panduan ini untuk mengatur Gensyn RL Swarm node secara manual tanpa Docker, menggunakan repo [gensyn-ai/rl-swarm](https://github.com/gensyn-ai/rl-swarm).

---

## ✅ Minimum Requirements

- OS: Ubuntu 20.04 / 22.04 (64-bit)
- CPU: 8 vCPU
- RAM: 32 GB
- Penyimpanan: 50 GB kosong
- GPU (opsional): NVIDIA GPU dengan dukungan CUDA (direkomendasikan)

---

## ⚙️ Langkah Instalasi


1. Update & install dependensi dasar
```bash
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl wget screen git lsof
```
2. Install Node.js v20 & npm
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo -E bash -
sudo apt update && sudo apt install -y nodejs
```
3. Cek versi node, npm, yarn
```bash
node -v
npm -v
yarn -v
```
  atau jika yarn belum terinstall:
```bash
npm install -g yarn
```
4. Mulai session screen (agar proses tetap jalan saat keluar terminal)
```bash
screen -S gensyn
```
5. Clone repo dan masuk ke direktori
```bash
git clone https://github.com/gensyn-ai/rl-swarm.git && cd rl-swarm
```
6. Buat dan aktifkan virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```
7. Install transformers versi kompatibel
```bash
pip install transformers==4.51.3
```
(Opsional) Lihat semua paket Python yang terinstall
```bash
pip freeze
```
9. Jalankan node
```bash
./run_rl_swarm.sh
```
```
# 10. Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N]
N

# 11. Enter the name of the model you want to use in huggingface repo/name format, or press [Enter] to use the default model.
[Enter]

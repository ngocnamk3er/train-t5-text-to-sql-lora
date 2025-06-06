
# 🧠 train‑t5‑text‑to‑sql‑lora

Một implementation sử dụng **LoRA** để fine‑tune mô hình **FLAN‑T5‑Large** chuyên cho nhiệm vụ chuyển đổi câu hỏi tự nhiên thành câu SQL.

---

## 📝 Mô tả

- Dùng `gretelai/synthetic_text_to_sql` làm dataset huấn luyện.  
- Chỉ dùng **LoRA adapter** (~1.2% tham số) để fine‑tune, tiết kiệm bộ nhớ.  
- Kết quả log và mô hình được lưu tự động lên **Wandb** và **Hugging Face Hub**.
- Các metric đo được: {'bleu': 0.507682326324316, 'precisions': [0.7008027976819882, 0.5625887219149248, 0.4793407834700884, 0.4085876227509392]}
---

## 💻 Cài đặt

```bash
git clone https://github.com/ngocnamk3er/train-t5-text-to-sql-lora.git
cd train-t5-text-to-sql-lora

pip install -q wandb transformers datasets accelerate peft bitsandbytes torch tensorboard huggingface_hub
pip install -U q transformers
```
# RWKV5-infctx-fallback

```
python train.py --load_model /home/asd/model/RWKV-5-World-1B5-v2-20231025-ctx4096.pth --proj_dir /home/asd/model --data_file ttt_text_document --data_type binidx --vocab_size 65536 --epoch_steps 1 --epoch_count 100 --epoch_begin 0 --epoch_save 5 --micro_bsz 1 --n_layer 24 --n_embd 2048 --pre_ffn 0 --head_qk 0 --lr_init 1e-5 --lr_final 1e-5 --warmup_steps 0 --beta1 0.9 --beta2 0.99 --adam_eps 1e-8 --accelerator gpu --devices 1 --precision bf16 --strategy deepspeed_stage_2 --grad_cp 1 --real_len 100 --ctx_len 200 --wandb
```
ctx_len 为你想要的训练长度  4096
real_len 受显存限制为实际训练长度 1024

比infctxLM更快，lora部分只是为了测试

# ACCELERATE.PARALLEL.PIPEDS

```yaml
# accelerate launch --config_file accelerate_config.yaml train.py
compute_environment: LOCAL_MACHINE
distributed_type: MULTI_GPU
num_processes: 2             # number of GPUs (adjust)
machine_rank: 0
num_machines: 1
mixed_precision: bf16        # or bf16 / no
downcast_bf16: no

# Data parallel config
distributed_training:
  ddp_backend: nccl          # good for NVIDIA GPUs
  use_cpu: false

# Offload (disabled for pure data parallel)
offload_optimizer_device: none
offload_param_device: none

# Logging & checkpoints
logging_dir: ./logs
save_on_each_node: false

```

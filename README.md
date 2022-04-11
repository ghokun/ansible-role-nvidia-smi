# Ansible Role: NVIDIA SMI

Run `nvidia-smi` to set GPU settings.

Currently supports:

- Compute modes

## Requirements

- One or more NVIDIA GPU
- Install `nvidia-smi`

## Role Variables

```yaml
set_compute_modes:
  # GPU UUID: 0/DEFAULT
  #           1/EXCLUSIVE_THREAD (DEPRECATED)
  #           2/PROHIBITED
  #           3/EXCLUSIVE_PROCESS
  GPU-13864def-ff37-57fb-c918-e6c2daae3c09: DEFAULT
  GPU-a72a4154-11e6-8038-0368-1c5ccbb47b16: 3 # Use either number or name
  GPU-cc7f90e0-6d0d-29db-cf3a-441b9b2cfaaf: EXCLUSIVE_PROCESS
```

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: nvidia-smi
```

## License

MIT

## Author Information

[ghokun](https://github.com/ghokun)

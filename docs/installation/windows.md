# Windows Development Environment Setup

## WSL2 Installation and Configuration

### Prerequisites
1. Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11
2. For mirrored networking: Windows 11 version 22H2 or higher
3. Enable WSL2 and install Debian distribution
   ```powershell
   wsl --install -d Debian
   ```

For detailed installation instructions, see [Microsoft's WSL installation guide](https://learn.microsoft.com/en-us/windows/wsl/install).

### GPU Support
To enable CUDA support in WSL2:
1. Install the [NVIDIA CUDA WSL-Ubuntu driver](https://developer.nvidia.com/cuda/wsl)
2. No `.wslconfig` settings are needed - WSL2 automatically detects and uses the GPU
3. Verify installation with: `nvidia-smi`

For detailed GPU setup instructions, see [Microsoft's GPU in WSL guide](https://learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl).

### WSL2 Configuration
WSL2 can be configured using `.wslconfig` in your Windows home directory (`%UserProfile%`).

#### Our Configuration
We use the following non-default settings in `~/.wslconfig`:
```ini
[wsl2]
networkingMode=mirrored         # Use mirrored networking mode for better performance
```

For a comprehensive list of all available WSL2 settings and their default values, please refer to [Microsoft's WSL config documentation](https://learn.microsoft.com/en-us/windows/wsl/wsl-config).

### Performance Recommendations
1. Store your project files in the Linux filesystem (`/home/<user>`) rather than Windows-mounted drives for better performance
2. Use SSD/NVMe storage for WSL2:
   - WSL2 runs as a virtual machine, so storage performance is crucial
   - NVMe drives provide best performance, followed by SSDs
   - Avoid using spinning disks if possible, as they significantly impact WSL2 performance
3. If you need to adjust resource limits, consider your system's capabilities:
   - `memory`: Limit WSL2's memory usage
   - `processors`: Limit number of virtual processors
   - `swap`: Adjust swap space size

### Troubleshooting
Common issues and their solutions:
1. To restart WSL: `wsl --shutdown`
2. To check WSL status: `wsl --status`
3. To verify version: `wsl --list --verbose`

For more troubleshooting guidance, see [WSL Troubleshooting documentation](https://learn.microsoft.com/en-us/windows/wsl/troubleshooting).

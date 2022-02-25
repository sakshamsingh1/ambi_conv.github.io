model:  Waveunet(
  (waveunets): ModuleDict(
    (ALL): Module(
      (downsampling_blocks): ModuleList(
        (0): DownsamplingBlock(
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(4, 32, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(4, 32, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(32, 64, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(8, 64, eps=1e-05, affine=True)
            )
          )
          (downconv): Resample1d()
        )
        (1): DownsamplingBlock(
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(64, 64, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(8, 64, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(64, 128, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(16, 128, eps=1e-05, affine=True)
            )
          )
          (downconv): Resample1d()
        )
        (2): DownsamplingBlock(
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(128, 128, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(16, 128, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(128, 256, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(32, 256, eps=1e-05, affine=True)
            )
          )
          (downconv): Resample1d()
        )
        (3): DownsamplingBlock(
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(256, 256, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(32, 256, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(256, 512, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(64, 512, eps=1e-05, affine=True)
            )
          )
          (downconv): Resample1d()
        )
        (4): DownsamplingBlock(
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(512, 512, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(64, 512, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(512, 1024, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(128, 1024, eps=1e-05, affine=True)
            )
          )
          (downconv): Resample1d()
        )
      )
      (upsampling_blocks): ModuleList(
        (0): UpsamplingBlock(
          (upconv): Resample1d()
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(1024, 512, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(64, 512, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(1024, 512, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(64, 512, eps=1e-05, affine=True)
            )
          )
        )
        (1): UpsamplingBlock(
          (upconv): Resample1d()
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(512, 256, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(32, 256, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(512, 256, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(32, 256, eps=1e-05, affine=True)
            )
          )
        )
        (2): UpsamplingBlock(
          (upconv): Resample1d()
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(256, 128, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(16, 128, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(256, 128, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(16, 128, eps=1e-05, affine=True)
            )
          )
        )
        (3): UpsamplingBlock(
          (upconv): Resample1d()
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(128, 64, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(8, 64, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(128, 64, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(8, 64, eps=1e-05, affine=True)
            )
          )
        )
        (4): UpsamplingBlock(
          (upconv): Resample1d()
          (pre_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(64, 32, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(4, 32, eps=1e-05, affine=True)
            )
          )
          (post_shortcut_convs): ModuleList(
            (0): ConvLayer(
              (filter): Conv1d(64, 32, kernel_size=(5,), stride=(1,))
              (norm): GroupNorm(4, 32, eps=1e-05, affine=True)
            )
          )
        )
      )
      (bottlenecks): ModuleList(
        (0): ConvLayer(
          (filter): Conv1d(1024, 1024, kernel_size=(5,), stride=(1,))
          (norm): GroupNorm(128, 1024, eps=1e-05, affine=True)
        )
      )
      (output_conv): Conv1d(32, 4, kernel_size=(1,), stride=(1,))
    )
  )
)

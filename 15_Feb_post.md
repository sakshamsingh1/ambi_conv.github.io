
U-net Paper:
Tasks:
1. Some examples
2. What's the raw files sampling rate: 44.1kHz
3. What preprocessing do they undergo?
  padding + augmentation
  
  ```
  residual = mix  # start with original mix
    for key in targets.keys():
        if key != "mix":
            residual -= targets[key]  # subtract all instruments (output is zero if all instruments add to mix)
    mix = residual * np.random.uniform(min, max)  # also apply gain data augmentation to residual
    for key in targets.keys():
        if key != "mix":
            targets[key] = targets[key] * np.random.uniform(min, max)
            mix += targets[key]  # add instrument with gain data augmentation to mix
    mix = np.clip(mix, -1.0, 1.0)
    return crop_targets(mix, targets, shapes)
  ```


4. Input and output samples and seconds?
    {'output_start_frame': 4776,
     'output_end_frame': 93185,
     'output_frames': 88409,
     'input_frames': 97961}

6. Handling stereo and mono.

7. Train with micarraylib+Eigenscape.

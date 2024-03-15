# Summary
ipynb file has comments on what has been added. 
- Highest accuracy: 99.48%
- Last accuracy: 99.34%
- Parameters: 16k



# Explorations:
- Original
    - 6M parameters
    - 28% accuracy
    - batch size = 128
- Reducing channels to 8/16/etc
    - 416k parameters
    - 97% accuracy
- Batch size of 64
    - 88%. so went back…
- removing last relu
    - accuracy: 97% (unchanged)
- adding BN after each convolution
    - 417k parameters
    - accuracy: 99%
- adding dropout after every layer
    - 10%
        - 417k parameters
        - accuracy: 99%
    - 25%
        - 417k parameters
        - accuracy: 94%
- Adding 1x1 after max pool and reducing channels to 8
    - 20.1k parameters
    - accuracy: 99.3
- Removing last relu in conv7
    - 20.1k parameters
    - 99.3 (no change)
- Increase dropout % to 0.2
    - 20.1k parameters
    - 99.3%
- Reduce parameters more
    - starting at 8
    - 16k parameters
    - max 99.1
- reducing dropout to 0.1
    - 99.3%
- Removing BN
    - 99.2%
- Added back in
    - 99.3%
- Move dropout to before BN
    - 99.4% (4 of 19 epochs)    

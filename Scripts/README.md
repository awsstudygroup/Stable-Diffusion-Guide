# Helper Scripts

Some **Python** scripts that ease the process of preparing caption datasets.

> **Important:** Remember to use `" "` if your tags or paths contain spaces.

### Insert.py
- **Purpose**: Insert tags at the start of the caption for all text files in a folder.
    - **Use Case**: Useful for adding **trigger words** to captions.

### Append.py
- **Purpose**: Append tags at the end of the caption for all text files in a folder.
  
### Remover.py
- **Purpose**: Remove specified tags from the caption for all text files in a folder.

### Replacer.py
- **Purpose**: Replace a string with another string in the caption for all text files in a folder.

### Formatter.py
- **Purpose**: Remove extra commas and spaces for all text files in a folder.
    - **Note**: This script is automatically triggered when using any of the scripts above.

### TriggerDebug.py
- **Purpose**: Print out the `n-th` tag for all text files in a folder.
    - **Use Case**: Useful for checking if the **trigger words** are consistent.

### Cleanse.py
- **Purpose**: Clear out the contents of all text files in a folder.

### EmptyCaption.py
- **Purpose**: Generate an empty `.txt` file with the same name for all non-text files in a folder.

# Miscellaneous Scripts

Some other **Python** scripts not related to captioning.

### CopyConfig.py
- **Purpose**: Copy the value from the source config to the target config if the key matches.
    - **Use Case**: Useful when installing multiple instances of WebUI.

### CopyMetadata.py
- **Purpose**: Copy the metadata from one image to another.
    - **Use Case**: Useful for embedding a ComfyUI workflow into a screenshot.

### OptimizeImage.py
- **Purpose**: Optimize `.png` images to `.jpg` to reduce their storage sizes.

### PrepJPG.py
- **Purpose**: Bucket images into certain fixed aspect ratios.
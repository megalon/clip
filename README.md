# GitClip
[![CircleCI](https://circleci.com/gh/lycoris0731/clip.svg?style=svg&circle-token=0e33c0cfb7bb1105ff821abbe845483d269145f8)](https://circleci.com/gh/lycoris0731/clip)
A tracking helper for CLIP STUDIO PAINT files with Git  
![Demo](./res/out.gif)  

## Description  
Track CLIP STUDIO PAINT files with Git.

## Requirements
- Go v1.7.1 or later

## Installation
Windows 10:
1. Install GCC
The easiest way to do this is the TDM-GCC toolset
http://tdm-gcc.tdragon.net/download

2. Download the go package
```
> go get github.com/megalon/gitclip
```

## Recommendations
You **should** use Git LFS(Large File Storage) to track clip files.  
Git manages binary files by saving the whole file for each commit. 

## Usage
First, you should run below command in Git repository.
```
> gitclip init TARGET_FILE_NAME
```
Then, clip creates `.clip` directory and update `post-commit` in Git hooks.  
All images are saved to `.clip`.  
  
See the image at the time of a commit.
```
> gitclip show [COMMIT_HASH ...]
```
Also, you can use `HEAD`.  
```
> gitclip show HEAD~
```

Create a Gif image about the production process.  
```
> gitclip gif [command options]
```

## License
Please see [LICENSE](./LICENSE).

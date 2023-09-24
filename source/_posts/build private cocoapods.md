---
title: How to build private libraries with CocoaPods
date: 2023-09-02 17:15:08
categories:
  - development tool
tags:
  - development tool
  - git
  - cocoapods
  - spec repo
  
description: A step-by-step guide to creating a private remote repository for Spec Repo

cover: https://s2.loli.net/2023/09/24/LzS1sarYIKHjpcB.jpg

---


## 1. Creating a private remote repository for Spec Repo

![20.png](https://s2.loli.net/2023/09/23/I2MXDZ4rfv9Khox.png)

1. Create a Spec Repo private repository, XXXSpecs, on the git remote server to store the Spec Repo private repository.

2. Create a local Spec Repo


Go to the folder ~/.cocoapods/repos and open a terminal


Switch to the current directory in the terminal and execute it:

`pod repo add XXXSpecs https://gitee.com/username/XXXSpecs.git`

```
gitee.com/username/XX... is the address of Spec Repo's private remote repository `pod repo list`: to see what local Spec Repo can configure on a new machine for private repositories to local cocoapods

```

3. Create a private repository, XXXPodProject, on the git remote to store the project files.

Don't initialize it when you create it.

```

Do not initialize when creating

```

4. Create the required project files for the pod and upload them to the remote private repository.

- In a terminal, cd to a directory

- Execute `pod lib create PodLibName`

```css

What platform do you want to use?? [ iOS / macOS ]
 > ios

What language do you want to use?? [ Swift / ObjC ]
 > swift

Would you like to include a demo application with your library? [ Yes / No ]
 > yes

Which testing frameworks will you use? [ Quick / None ]
 > none

Would you like to do view based testing? [ Yes / No ]
 > yes 

```

5. Modify the file and podspec

Modify file and podspec configuration to add swfit version `s.swift_version = '4.2'`
Type the tag

```

Creating tags git tag 1.0.0
Push tags git push --tag
Viewing tags git tag

```
6. Verify local podspec validity

`pod lib lint PodLibName.podspec`

7. Uploading local project files to a remote repository

`git remote add origin url`

```

The important thing to note here is that the tagged value should be the same as the version number in the podspec file.

```

8. Commit podspecs to a private spec repo remote repository

Associate the Lib repository with the Spec Repo

Use the `pod repo push XXXSpecs PodLibName.podspec` command to add the private repository to the private repo.

At this point, the current version of the podspec file is already in the ~/.cocoapods/repos/XXXSpec folder.

## 2. Configure the local private repository on the new computer.

1. Terminal `cd ~/.cocoapods/repos`

2. Configure the remote private repository pod repo add `XXXSpecs https://gitee.com/username/XXXSpecs.git`

Third, create new lib to AHSpecs

1. create `pod lib create PodLibName`

```css

What platform do you want to use?? [ iOS / macOS ]
 > ios

What language do you want to use?? [ Swift / ObjC ]
 > swift

Would you like to include a demo application with your library? [ Yes / No ]
 > yes

Which testing frameworks will you use? [ Quick / None ]
 > none

Would you like to do view based testing? [ Yes / No ]
 > yes 

```

1. validate lib `pod lib lint PodLibName.podspec`

2. Associations lib to AHSpecs `pod repo push XXXSpecs PodLibName.podspec`

```

You also need to push after each lib update

```

## 3. upload cocoapods

```perl

pod trunk push <private codebase>.podspec

You are prompted to register. Enter your Email and name, and then go to the email to verify that it passes.

pod trunk register Email 'username' --verbose
pod trunk push <private code base>.podspec

```

## 4. Problems encountered

Handling of iOS private repositories with dependencies on private repositories and third-party frameworks

Use the `--allow-warnings` parameter, e.g. `pod repo push --allow-warnings`, which ignores some warnings, but still interrupts the push if there is an error message.

Use the `--skip-import-validation` parameter, e.g., `pod repo push --skip-import-validation`, to skip the verification of whether the source_files in the podspec file can be imported correctly, which is useful for some private libraries that depend on third-party frameworks. This parameter is useful for private libraries that depend on third-party frameworks, because sometimes importing <> in the .h file can cause validation to fail.

Use the --`use-libraries parameter`, e.g. `pod repo push --use-libraries`, to use static libraries instead of dynamic libraries for validation. This parameter is useful for private libraries that depend on static libraries, because sometimes dynamic libraries cause validation to fail.


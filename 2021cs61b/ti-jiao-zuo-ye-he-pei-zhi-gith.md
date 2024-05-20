# 提交作业和配置gith

## Configure Personal Repository

#### Configure Personal Repository&#x20;

Now, it’s time to clone your personal repository. As you did with the libraries, navigate to the folder where you would like to keep your repository. We recommend that it’s the same folder as where you stored your Java libraries (for example, `cs61b`).

Before we do clone your repo though, we need to login to Github. Verify that you have the Github package:

```
gh --version
```

You should see a version number displayed. If you instead see a command not found error, please install Github cli again by following the steps outlined for you [operating system](https://fa23.datastructur.es/materials/lab/lab01/#task-installing-software).

Next login with your account with the following command:

```
gh auth login
```

You’ll be asked a few questions with some options to select from. You don’t have to worry about them, simply select the first options for all of them and proceed. You’ll be provided with a one time code, and prompted to open the browser.

Enter the code in the browser window and select authorize Github. You should now be logged in!

**NOTE**: For Windows Users: if you run into an error that says “could not prompt: Incorrect Function”, run `winpty gh auth login` instead.

The entire process should look like the below:

**Once you’ve logged in, run the following command to clone your personal repository.** Make sure to replace the `***` with your class repository number (you can find this repo number on Beacon).

&#x20;**WARNING**: Do not place your repository inside the `library-fa23` folder. This will cause headaches in the future.

```
git clone https://github.com/Berkeley-CS61B-Student/fa23-s***.git
```

&#x20;**INFO**: After cloning your terminal will report `warning: You appear to have cloned an empty repository.` This is not an issue, it is just git letting you know that there are no files in the repo.

Move into your newly created repo!

```
cd fa23-s***
```

Make sure that we’re working with the branch name we expect, `main`:

```
git branch -M main
```

**Now, we’ll add the `skeleton` remote repository.** We add starter code for the assignments to `skeleton`, and you will pull from it (please make sure you’re in your newly created repository before running this command!).

```
git remote add skeleton https://github.com/Berkeley-CS61B/skeleton-fa23.git
```

Listing the remotes should now show both the `origin` and `skeleton` remotes.

```
git remote -v
```

&#x20;**INFO**: If you see an error like `fatal: not a git repository` make sure you have properly moved into the `fa23-s***` directory using `cd`.

&#x20;**TASK**: Follow the steps above to clone and configure your repository.

<details>

<summary><strong>At this point, your work space might look like this:</strong></summary>

<img src="https://fa23.datastructur.es/materials/lab/lab01/img/workspace.png" alt="Workspace Image" data-size="original">

* Note that this also assuming that you did your `lab01-checkoff` inside the same folder where you cloned your `fa23-s***` repository and `library-fa23`.
* Your personal repository and libraries should be “separate”, such that you didn’t clone your `library-fa23` inside your personal repository or vise versa.
* Your workspace doesn’t have to look like this exactly. This is mainly for an idea of what it can look like.

</details>

## 在 IntelliJ IDEA 中比较任何内容 <a href="#major-updates" id="major-updates"></a>

[https://blog.jetbrains.com/zh-hans/idea/2022/07/compare-anything-in-intellij-idea/](https://blog.jetbrains.com/zh-hans/idea/2022/07/compare-anything-in-intellij-idea/)








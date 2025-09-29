# Weird Branch Names Repository
Welcome to the Weird Branch Names Repository! This repository is dedicated to hosting a collection of weird and unusual branch names for you to test and play with. Whether you're looking to test your Git skills, in a need for strange branch names for testing, or just someone who loves quirky names, this repo is for you!

## Why Weird Branch Names?
- Testing Git Commands: Challenge yourself with unusual branch names.
- Improve QA Processes: Use odd branch names to test edge cases.
- Fun and Learning: Enjoy the creativity and learn more about Git.

## Features
- Variety of Names: From the utterly bizarre to the creatively funny.
- Real-world Scenarios: Test how different tools handle odd branch names.
- Community Contributions: Submit your own weird branch names and see them featured!

## 🛠️ Branch Creation Scripts

This repository includes two powerful scripts for creating branches with different validation behaviors:

### 📝 `create-branch` - Standard Branch Creator
Creates normal, locally-checkoutable branches that follow Git's standard validation rules.

**Usage:**
```bash
./create-branch <branch-name>
```

**What it does:**
- ✅ Creates a new branch from `main`
- ✅ Updates `README.md` to "This is branch: `<branch-name>`"
- ✅ Commits and pushes the branch to origin
- ✅ Sets up upstream tracking
- ✅ Branch can be checked out locally with `git checkout <branch-name>`

**Use this when:** You want to create normal, well-behaved branches that follow Git naming conventions.

### 🚀 `create-weird-branch` - Remote-Only Branch Creator
Creates "invalid" branches that exist only remotely and demonstrate Git's validation edge cases.

**Usage:**
```bash
./create-weird-branch <weird-branch-name>
```

**What it does:**
- ✅ Creates a remote-only branch using refspec push (`git push origin HEAD:<branch-name>`)
- ✅ Updates `README.md` with remote-only branch documentation
- ✅ Commits changes to main and pushes using refspec
- ⚠️ Branch exists remotely but **CANNOT** be checked out locally
- ⚠️ Demonstrates the difference between local and remote Git validation

**Use this when:** You want to test edge cases, create branches with "invalid" names (like `-C`, `-B`), or explore Git's validation boundaries.

### 🔍 Key Differences

| Feature | `create-branch` | `create-weird-branch` |
|---------|----------------|----------------------|
| **Local Checkout** | ✅ Yes | ❌ No (impossible) |
| **Remote Visibility** | ✅ Yes | ✅ Yes |
| **Git Validation** | Standard rules | Bypasses local validation |
| **Use Case** | Normal development | Testing edge cases |
| **Branch Names** | Valid Git names | Any name (even "invalid" ones) |
| **Method** | `git checkout -b` + `git push` | `git push origin HEAD:<name>` |

### 🎯 Recommended Workflow

**Always try `create-branch` first!** If it fails with "invalid branch name", then use `create-weird-branch`:

```bash
# Step 1: Try the normal script first
./create-branch my-branch-name

# Step 2: If it fails with "invalid branch name", use the weird script
./create-weird-branch my-branch-name
```

This approach helps you:
- ✅ Create normal branches when possible (better for development)
- ✅ Automatically discover Git's validation edge cases
- ✅ Learn which branch names are truly "weird" vs just unusual

### 💡 Examples

```bash
# Normal branches (use create-branch)
./create-branch feature/new-awesome-feature
./create-branch bugfix/issue-123
./create-branch release/v1.0.0

# These will fail with create-branch, so use create-weird-branch
./create-weird-branch -C                    # Starts with hyphen
./create-weird-branch --invalid-flag        # Looks like a command option
./create-weird-branch "branch with spaces"  # Contains spaces
```

## Getting Started
Clone the repository to start experimenting with these unique branch names:
```bash
git clone https://github.com/roeibh/weird-branch-names.git
```
After cloning, explore the branches with:
```bash
git branch -a
```
## How to Use
- Clone the Repository: Get the code on your local machine.
- Checkout a Weird Branch: Test your Git commands using these unconventional names.

## Contributing

### Have an idea for an unusual, bizarre, or technically challenging branch name? We welcome your suggestions!
- Submit Your Ideas: Simply open a new issue with your proposed branch name.
- Collaborate and Innovate: Help expand this repository with names that continue to push the boundaries of creativity.


Keywords

Weird Git branch names, creative branch naming, quirky branch names, Git testing, unusual branch names, innovative Git practices

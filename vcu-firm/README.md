# sdm-vcu-firm

**Sun Devil Motorsports EV**

_**Vehicle Control Unit Firmware**_

## Gitutorial:

### Dev Dependencies

- [git](https://git-scm.com/downloads)
- [rustup](https://rustup.rs)
- [espflash](https://docs.espressif.com/projects/rust/book/getting-started/tooling/espflash.html)
- [github-cli](https://cli.github.com)

### First-Time Startup

- Do this the first time you set up the repo on your machine

**Authenticate GitHub CLI:**

```bash
gh auth login
# Follow CLI prompts
```

**Clone:**

```bash
git clone https://github.com/ilya-tate/sdm-vcu-firm.git
cd sdm-vcu-firm
```

### Making a Change

- Do this every time you want to make a change

**Setup:**

```bash
cd sdm-vcu-firm
git checkout main
git pull origin main
git checkout -b <github-username>/<feature-name>   # Ex. ilya-tate/big-papa-init
```

**Change:**

_Edit, finalize, and test (please) your changes_

**Upload:**

```bash
cargo build    # Test build
git add <edited-files>                  # Ex. git add bruh.txt src/foo.rs
# Pro Tip:
# "git add -A" to add all edited files (run "git status" first tho)
git commit -m "DESCRIPTION"    # Ex. git commit -m "Fixed this bug which caused that problem"
git push -u origin HEAD
gh pr create
# Follow CLI prompts
```

### Requested Changes

- Sometimes you may be asked to make a change to your pull request

**1. Change branches (only if necessary)**

```bash
git checkout -b <github-username>/<feature-name>
```

**2. Make requested edits**

_Type away and test_

**3. Push changes**

```bash
cargo build    # Test build
git add <reedited-files>
git commit -m "DESCRIPTION"    # Just address pull request feedback
git push
```

**4. Update repo after pull request merge**

```bash
git checkout main
git pull origin main
git branch -d <github-username>/<feature-name>
```

> #### _Don't hesitate to DM me (Ilya) on Slack if you run into any issues :)_

## Run

** Building **

```bash
cargo build --release
```

** Flashing **
```bash
cargo run --release
```

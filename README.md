# building-blocks-sai


# README

## Setup Instructions

### Cloning the Repository

This repository contains submodules that need to be initialized after cloning. To clone this repository along with its submodules, run:

```bash
git clone --recurse-submodules https://github.com/flores-o/building-blocks-sai.git
```

### After Cloning

Navigate into the repository:

```bash
cd building-blocks-sai
```

Ensure all submodules are up to date:

```bash
git submodule update --init --recursive
```

### Working with Submodules

#### Updating the Repository

When pulling changes from the repository, run:

```bash
git pull
git submodule update --recursive
```

#### Making Changes in Submodules

If you need to make changes within the `ARENA_3.0` submodule:

1. **Navigate to the submodule directory:**

   ```bash
   cd ARENA_3.0
   ```

2. **Ensure you're on the correct branch:**

   ```bash
   git checkout main
   ```

3. **Make your changes and commit them:**

   ```bash
   git add .
   git commit -m "Your descriptive commit message"
   ```

4. **Push changes to the submodule remote:**

   ```bash
   git push origin main
   ```

5. **Return to the main repository root:**

   ```bash
   cd ..
   ```

6. **Update the submodule reference in the main repository:**

   ```bash
   git add ARENA_3.0
   git commit -m "Updated ARENA_3.0 submodule to include recent changes"
   git push origin main
   ```

### Keeping Submodules in Sync

If the submodule repositories receive updates, ensure you update them in your local environment:

```bash
git submodule update --remote --merge
```

### Handling Submodule URL Changes

If the submodule URL has changed, synchronize the submodule configuration:

```bash
git submodule sync
git submodule update --init --recursive
```

### Keeping Your Fork Up-to-Date with Upstream

If you've forked the submodule and want to keep it updated with the original repository:

1. **Add the upstream remote:**

   ```bash
   cd ARENA_3.0
   git remote add upstream https://github.com/callummcdougall/ARENA_3.0.git
   ```

2. **Fetch and merge upstream changes:**

   ```bash
   git fetch upstream
   git merge upstream/main
   ```

3. **Resolve any merge conflicts if necessary.**

4. **Push merged changes to your fork:**

   ```bash
   git push origin main
   ```

5. **Return to the main repository and update the submodule reference:**

   ```bash
   cd ..
   git add ARENA_3_0
   git commit -m "Updated ARENA_3.0 submodule with upstream changes"
   git push origin main
   ```

### Common Commands for Submodule Management

- **Initialize and update submodules:**

  ```bash
  git submodule update --init --recursive
  ```

- **Synchronize submodule URLs:**

  ```bash
  git submodule sync --recursive
  ```

- **Deinitialize a submodule:**

  ```bash
  git submodule deinit -f --all
  ```

### Notes for Collaborators

- **Always update submodules after pulling changes:**

  ```bash
  git submodule update --recursive
  ```

- **Cloning the repository correctly:**

  Use `--recurse-submodules` when cloning to ensure all submodules are initialized:

  ```bash
  git clone --recurse-submodules https://github.com/flores-o/building-blocks-sai.git
  ```

- **Making changes to submodules:**

  Ensure you have the necessary permissions to push changes to the submodule repositories. If you're working with forks, update the submodule URLs to point to your forks if necessary.

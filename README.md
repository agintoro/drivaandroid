# DRIVA Processing Log Android APK Project

This repository builds the DRIVA Processing Log as an offline Android APK using a native Android WebView wrapper.

## Important GitHub Actions Setup

The workflow file must exist exactly here in your repository:

`.github/workflows/build-apk.yml`

If you uploaded a folder named `driva-processing-log-android` into your repo, GitHub will not detect the workflow. The `.github` folder must be at the repository root, not inside another folder.

Correct:

```
your-repo/
  .github/
    workflows/
      build-apk.yml
  app/
  build.gradle
  settings.gradle
```

Wrong:

```
your-repo/
  driva-processing-log-android/
    .github/
      workflows/
        build-apk.yml
    app/
    build.gradle
    settings.gradle
```

## How to Build APK on GitHub

1. Create a new GitHub repository.
2. Upload the contents of this folder, not the parent folder.
3. Make sure `.github/workflows/build-apk.yml` appears in the repo.
4. Go to the **Actions** tab.
5. If GitHub asks to enable workflows, click **I understand my workflows, go ahead and enable them**.
6. Click **Build Android APK**.
7. Click **Run workflow**.
8. After it finishes, open the run and download the artifact named:

`driva-processing-log-debug-apk`

Inside it is:

`app-debug.apk`

## If Build Android APK Does Not Appear

Create the workflow manually:

1. In GitHub, click **Add file** → **Create new file**.
2. Name the file exactly:

`.github/workflows/build-apk.yml`

3. Paste the workflow content from this project.
4. Commit to `main`.
5. Refresh the Actions tab.

## App Notes

- Offline app assets are inside `app/src/main/assets/`.
- Data is stored locally in the Android WebView browser storage.
- Export CSV regularly if the data matters.
- This debug APK is for personal/internal use, not Play Store release.

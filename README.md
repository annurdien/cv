# My CV

This repository contains my CV/resume, automatically rendered using [RenderCV](https://github.com/rendercv/rendercv).

## 📥 Download Latest CV

The latest version of my CV is always available in the [Actions artifacts](../../actions) tab. 

Alternatively, you can check the `cv_versions/` directory for all historical versions. 

## 🚀 How It Works

1. CV content is written in YAML format (`xxx_cv.yaml`)
2. Every push to `main` triggers automatic rendering via GitHub Actions
3. The rendered PDF is: 
   - Uploaded as a GitHub Actions artifact
   - Committed back to the repository with version number
   - Optionally released when a version tag is created

## 📦 Versioning

Versions are automatically generated using the format:  `YYYY.MM.DD-{short-sha}`

Example: `2026.01.13-a1b2c3d`

## 🏷️ Creating Releases

To create a formal release:

```bash
git tag -a v1.0.0 -m "Release version 1.0.0"
git push origin v1.0.0
```

This will automatically create a GitHub Release with the PDF attached.

## 🛠️ Local Development

To render the CV locally:

```bash
# Install RenderCV
pip install "rendercv[full]"

# Render CV
rendercv render Your_Name_CV.yaml
```

## 📝 Editing

Edit the `Your_Name_CV.yaml` file with your information.  Use VS Code with the YAML extension for the best experience with autocomplete and validation.

See [RenderCV documentation](https://docs.rendercv.com) for detailed guidance. 

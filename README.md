cv
==

my resume. yaml -> pdf.

download
--------
releases tab. latest is always there.

build
-----
pipx install "rendercv[full]"
rendercv render annurdien_cv_detailed.yaml
rendercv render annurdien_cv_compact.yaml

ci/cd
-----
push to main -> auto-builds -> creates release with both pdfs attached.
version format: YYYY.MM.DD-{sha}

files
-----
annurdien_cv_detailed.yaml  - full version
annurdien_cv_compact.yaml   - short version

stack
-----
- rendercv: https://github.com/rendercv/rendercv
- github actions
- engineeringresumes theme 

---
title: "Controlled self-applicable on-line partial evaluation, using strategies"

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here 
# and it will be replaced with their full name and linked to their profile.
authors:
- admin
- Sam Kamin

# Author notes (optional)
#author_notes:
#- "Equal contribution"
#- "Equal contribution"

date: "1998-05-01T00:00:00Z"
doi: "10.1109/ICCL.1998.674165"

# Schedule page publish date (NOT publication's date).
publishDate: "1998-05-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: In Proceedings of the 1998 International Conference on Computer Languages (Cat. No.98CB36225)
publication_short: ICCL'98

abstract:  []

# Summary. An optional shortened abstract.
summary:  []

tags: []

# Display this page in the Featured widget?
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: https://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
#image:
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
#  focal_point: ""
#  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []
# - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

Online partial evaluators are hardly ever self-applicable, because the
complexity of deciding whether to residualize terms causes a combinatorial
explosion when self-application is attempted. T. Mogensen (1995) has found a
way to write a self-applicable online partial evaluator for the
$\lambda$-calculus. His method is to regard every $\lambda$-term as having
both static and dynamic aspects; then, applications can always be done
statically (using the static aspect of the operator). However, the absence of
decision-making about residualization has a down-side: his partial evaluator
knows only how to fully reduce partially evaluated terms. The result is
considerable code explosion. We show how this problem can be overcome, in part,
by changing the type of the partial evaluator, and giving a new version of the
Futamura projections to correspond to that new type. Specifically, we have the
partial evaluator take a third argument, called a strategy, which "advises" the
partial evaluator whether to residualize. Strategies allow the programmer to
control the tradeoff between the size of a specialized term and the cost of
subsequently applying it. We present a number of strategies and examples of
each.

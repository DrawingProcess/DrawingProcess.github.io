# Research blog template

The canonical skill is SKILL.md in this directory.
Use index.html as the reusable HTML reference.

Create new posts at posts/YYMMDD_<title>/index.html, for example
posts/261127_agentic-robotics-corl-2026/index.html.
Copy index.html and replace its ../../../ root links with ../../.
Keep images in the article's asset/ directory.
Use relevant source images when available. Otherwise generate an article-specific
16:9 thumbnail with the imagegen skill, save it as asset/thumbnail.png, and include
it in that article's card in posts.html. The image src must be
posts/YYMMDD_<title>/asset/thumbnail.png. Add an HTML comment recording its source
or AI-generated origin. This workflow adds thumbnails to posts.html only.
Replace bracketed fields, the document title, description, date text, and ISO datetime.
Add a full-card link to posts.html and order all cards newest first by time datetime.
Use unique card IDs and preserve all posts already present on master.
Work and commit locally on master. Push or create a PR only when requested.

Reference article: ../../261113_robot-learning/index.html
Worked example: ../../261127_agentic-robotics-corl-2026/index.html

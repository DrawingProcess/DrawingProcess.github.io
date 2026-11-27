---
name: research-blog
description: Create or update English research posts for DrawingProcess.github.io using its comparison-table blog template and dated post folders.
---

# DrawingProcess research blog

Use this repository's existing typography, colors, navigation, and research-note styles.
The canonical template is index.html beside this file.

## Repository workflow

1. Read the working-tree status and current branch. Work and commit on master. When the tree is clean, switch to master if needed. Preserve existing uncommitted work and resolve branch constraints before editing.
2. Check current master content before changing posts.html. Preserve every existing post, its title, and its current path.
3. Create each post at posts/YYMMDD_<title>/index.html using its publication date. Use a concise lowercase hyphenated title, for example posts/261127_agentic-robotics-corl-2026/index.html.
4. Copy the template into that folder. The template lives three levels below the repository root and uses ../../../ root links. A published article lives two levels below the root and must use ../../ root links.
5. Choose relevant source images when available. When no suitable image exists, generate a thumbnail from the article's content following the image workflow below. Store article images under the post's asset/ directory and reference them as asset/<filename>.
6. Update posts.html with a full-card link and its thumbnail. Sort all cards by time datetime descending so the newest publication appears first. Give every card unique IDs and matching ARIA references.
7. Check relative resources, fragment links, mobile table scrolling, keyboard access, and the card's destination. Commit the verified changes locally on master. Push or create a PR only when the user requests it.

## Article structure

Write in English unless the user specifies another language.
Include a title, publication date, concise introduction, and linked table of contents.
Use a comparison table covering representative tasks, the role in robot learning, research significance, and the scope of experimental evidence.
Follow with method details, inputs and outputs, learning data or objectives, evaluation conditions, limitations, and concrete research implications.
State the robot, task, metric, trial count, baseline, and intervention setting when available. Distinguish incompatible scores and results from different experimental setups.
Link primary sources at paragraph ends. For videos, link timestamps and distinguish supplied summaries from verified transcripts.
Keep reported findings and your own analysis identifiable. Attribute images and provide dimensions and useful alt text.
Replace all bracketed fields and both visible and machine-readable dates.

## Posts card thumbnails

Base the thumbnail brief on the finished article's central question, representative task, and main technical idea. Choose a concrete visual that helps readers recognize the topic.
Use a relevant official photo or figure when available and suitable for the thumbnail. If no suitable image exists, use the imagegen skill and its built-in image generation tool to create an article-specific illustration.
Use a 16:9 composition with the important subject visible when reduced to a small Posts card. Match the site's restrained visual style. Avoid tiny text and decorative labels.
Save the selected generated image inside the article's asset/ directory, for example asset/thumbnail.png. Add an img.post-thumbnail inside that article's card in the root posts.html, with src="posts/YYMMDD_<title>/asset/thumbnail.png".
This thumbnail workflow targets posts.html. Add images to the article body only when separately requested.
Keep a source attribution or generation note in an HTML comment beside the card image. Do not present generated images as experiment photographs, measured charts, or official project figures.
Provide accurate alt text and explicit dimensions. A redundant thumbnail inside an already named card link may use empty alt text.
Verify the saved image loads from posts.html, its crop remains meaningful on mobile, and clicking the thumbnail opens the corresponding article.

## Existing references

- Robot learning comparison at ../../261113_robot-learning/index.html
- Worked agentic robotics post at ../../261127_agentic-robotics-corl-2026/index.html
- Additional usage notes in README.md

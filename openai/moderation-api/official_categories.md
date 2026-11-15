# OpenAI Moderation API — Categories (`omni-moderation-latest`)

OpenAI's moderation endpoint evaluates text (and images on omni models) across 13 distinct categories, returning both boolean `flagged` states and continuous `category_scores` (`0.0` to `1.0`).

| Category Key | Input Support | Description |
| :--- | :--- | :--- |
| `harassment` | Text | Content that expresses, incites, or promotes harassing language towards any target. |
| `harassment/threatening` | Text | Harassment content that also includes violence or serious harm towards any target. |
| `hate` | Text | Content that expresses, incites, or promotes hate based on race, gender, ethnicity, religion, nationality, sexual orientation, disability status, or caste. |
| `hate/threatening` | Text | Hateful content that also includes violence or serious harm towards a targeted protected group. |
| `illicit` | Text | Content giving instructions or advice facilitating wrongdoing (e.g., how to shoplift). |
| `illicit/violent` | Text | Illicit wrongdoing instructions that also include violence or weapon procurement. |
| `self-harm` | Text, Image | Content that promotes, encourages, or depicts acts of self-harm (suicide, cutting, eating disorders). |
| `self-harm/intent` | Text, Image | Content where the speaker expresses intent to engage in self-harm. |
| `self-harm/instructions` | Text, Image | Content encouraging or providing instructions on how to commit self-harm. |
| `sexual` | Text, Image | Content meant to arouse sexual excitement or promote sexual services (excludes sex education/wellness). |
| `sexual/minors` | Text, Image | Sexual content involving any individual under 18 years old. |
| `violence` | Text, Image | Content that depicts death, violence, or physical injury. |
| `violence/graphic` | Text, Image | Content depicting death, violence, or physical injury in graphic detail. |

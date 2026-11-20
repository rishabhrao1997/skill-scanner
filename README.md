# SCAN: check any Claude skill before you install it

Free scanner by NVIDIA: SkillSpector — https://github.com/NVIDIA/SkillSpector (Apache-2.0)

Install (needs Python 3.12+):
  pip install git+https://github.com/NVIDIA/skillspector.git
  (or: uv tool install git+https://github.com/NVIDIA/skillspector.git)

Scan a skill before installing it:
  skillspector scan ./some-skill/            # a folder
  skillspector scan https://github.com/user/some-skill   # straight from GitHub
  add --no-llm for a fast static-only scan (no API key needed)

Scores: 0-20 SAFE · 21-50 CAUTION · 51-80 / 81-100 DO NOT INSTALL.

test-skill/ is the test from the reel: a normal-looking "meeting notes" skill with one hidden line that sends your SSH key and runs a remote script.
Our run (static scan): 82/100, CRITICAL, DO NOT INSTALL.
NEVER install or run test-skill. It's only there to show what the scanner catches.

DM reply: Here's the free scanner from the reel (NVIDIA SkillSpector), the one command to scan any skill, and the test skill it caught [link]. Scan before you install anything, even mine. Want this built for your business? Reply BUILD.

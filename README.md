# Termageddon Privacy Skills

Free AI skills that help website owners find and fix privacy issues on their websites. Brought to you by [Termageddon](https://termageddon.com/).

Each skill is a set of instructions that an AI agent, such as Claude, follows to perform a specific privacy task the same careful way every time.

## Skills

| # | Skill | What it does | Status |
|---|---|---|---|
| 01 | [Website Privacy Audit](skills/website-privacy-audit/) | Scans a website for trackers, third-party data sharing, cookies, consent banner behavior, website policies, and form and AI disclosures, then writes a plain-language report with prioritized recommendations. | Available (v1.0.0) |
| 02 | Privacy by Design Upgrade Audit | | Coming soon |
| 03 | Cookie Consent Solution Audit | | Coming soon |

## How to use a skill

### Claude (claude.ai or the Claude desktop app)

1. Download the skill's zip file, for example [`downloads/website-privacy-audit.zip`](downloads/website-privacy-audit.zip).
2. In Claude, open **Settings > Capabilities > Skills** and upload the zip file.
3. Start a new chat and ask, for example: "Run a website privacy audit on example.com."

### Claude Code

Copy the skill folder into your skills directory:

```bash
git clone https://github.com/hansskillrud/privacy-skills.git
cp -r privacy-skills/skills/website-privacy-audit ~/.claude/skills/
```

Then ask Claude Code to run a website privacy audit on your site.

### Other AI agents

Each skill follows the open [Agent Skills](https://agentskills.io/) format: a `SKILL.md` file with supporting reference files. Agents that support this format can load the skill folder directly. For other agents, you can paste the contents of `SKILL.md` and its reference files into the conversation.

### Getting the best results

The Website Privacy Audit is most thorough when the AI agent can control a real browser, so it can see network requests and cookies and click the consent banner. Without a browser, the agent can still review the page source, but it will tell you which checks it could not perform. The report includes a step-by-step guide for checking those items yourself.

## Permitted use

These skills are free to use under the [CC BY-NC 4.0 license](LICENSE), with the additional permissions below.

**You may:**

- Use the skills to audit and improve your own websites.
- Use the skills to audit and improve websites you build or manage for clients, including as part of paid web design, development, marketing or maintenance services. This applies to web design companies, agencies, freelancers and other third-party service providers.
- Share the skills with others for free, with credit to Termageddon and a link to this repository.
- Adapt the skills for your own use, with credit to Termageddon.

**You may not:**

- Sell, resell, license or otherwise charge for the skills themselves, or for modified versions of them.
- Repackage the skills, or include them in a paid product, course, template library or subscription.
- Remove the Termageddon attribution from the skills or from the reports they produce.

For other uses, contact [Termageddon](https://termageddon.com/).

## Important disclaimer

These skills produce automated, AI-assisted reviews for informational and educational purposes only. They are not legal advice, may contain inaccuracies or miss issues, and do not certify compliance with any law. Review findings with a qualified privacy attorney before making decisions about your website's privacy practices or legal compliance.

## About Termageddon

[Termageddon](https://termageddon.com/) generates website policies, including Privacy Policies, Terms of Service, Disclaimers and Cookie Policies, and keeps them up to date as privacy laws change.

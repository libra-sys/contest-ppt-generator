# contest-ppt-generator

A Codex/WorkBuddy skill for building evidence-based, editable PowerPoint presentations for career-planning and innovation/entrepreneurship competitions.

## Workflow

1. Review source materials and constraints; distinguish verified facts from assumptions and ask about missing evidence.
2. Build the narrative outline around the task and official competition requirements.
3. Analyze the user's visual references separately, propose a coherent direction, and lock the style after approval.
4. Create and review a representative visual, then the full slide visuals at the user's requested pace.
5. After visual approval, recover original assets, isolate semantic elements, and rebuild ordinary copy/charts as native PowerPoint objects.
6. Recompose slides from a manifest, verify placement, editability, embedded images, and rendered previews; deliver the PPTX and reusable assets.

## Evidence rules

Never invent personal experiences, awards, figures, certificates, or employment details. Prefer original evidence files over old resumes or notes. Preserve certificates and screenshots as source images; do not have image models redraw them. Label plans as plans and unsupported claims as pending verification.

## Visual decomposition

The companion `asset-slicer` skill describes per-slide asset extraction. Its connected-component algorithm is a crop helper, not semantic segmentation. First identify and isolate objects such as panels, buttons, portraits, and illustrations; retain source images for evidence; make ordinary text editable; then recompose and check that moving an object does not reveal a duplicate underneath. See [the companion protocol](https://github.com/libra-sys/asset-slicer/blob/main/references/approved-slide-slicing.md).

## Install

Copy `SKILL.md`, `config.example.json`, and `references/` into your agent's skill directory as `contest-ppt-generator/`. If you have a local `asset-slicer` checkout, keep both skills side by side so relative references resolve. The linked public repository can also be used as a companion.

## Image generation configuration

API configuration is optional. Built-in image-generation tools and local PPT assembly/slicing may not need an external API key. When using a provider API, verify current provider documentation and keep credentials only in local environment variables or ignored local files. Never commit `config.json` or paste keys into chat. The example config contains placeholders only.

## License

MIT. See [LICENSE](LICENSE).

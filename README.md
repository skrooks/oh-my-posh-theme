This is my config for [Oh My Posh](https://ohmyposh.dev), a prompt theme engine.

# Font

Requires a [NerdFont](https://www.nerdfonts.com) to properly render symbols.

I'm using DejaVu Sans Mono.

Alternatively I would use FiraCode or JetBrainsMono, both of which support ligatures.

# Notes on Icons

To add in Vim while in insert mode, `^v ue0a0` or `^v U000f024b`

Use the NerdFont [Cheat Sheet](https://www.nerdfonts.com/cheat-sheet) to look up icons. Copy `UTF` for the code.

Note that icon width varies depending on the font selected, e.g. Gitlab icon ><. The mono fonts scale down large symbols to fit into a single space, meaning some icons like Gitlab can look tiny. The propo fonts use full size icons, but they can go outside their bounds, meaning you might need to add a space after the icon to look right.

NOTE: My theme is currently designed for use on a Mac (specifically in iTerm2) using proportional fonts. Windows Terminal appears to only support mono fonts, so the current config might look off.

## Common Icons

* \ue0b6 
* \ue0b1 
* \ue0b0 
* \uf07c 
* \uf0e7 
* \udb80\udf18 󰌘

## Git Template

```
 " {{ .HEAD }} {{ .BranchStatus }}{{ if .Working.Changed }} \uf044 {{ .Working.String }}{{ end }}{{ if and (.Staging.Changed) (.Working.Changed) }} |{{ end }}{{ if .Staging.Changed }} \uf046 {{ .Staging.String }}{{ end }}{{ if gt .StashCount 0}}\uf692 {{ .StashCount }}{{ end }}{{ if gt .WorktreeCount 0}} \uf1bb {{ .WorktreeCount }}{{ end }} "
```

* HEAD
* BranchStatus
* if (working changed) show \uf044 
* if (staging and working changed) show divider |
* if (staging changed) show \f046 
* if (stashes) show \uf692  count
* if (worktree) show \uf1bb  count

### Icons

* \uE0A0  - branch icon
* \u2261 ≡ - branch identical icon
* \u2191 ↑ - branch ahead icon
* \u2193 ↓ - branch behind icon
* \u2262 ≢ - branch gone icon
* \uF417  - commit icon
* \uF412  - tag icon
* \uE728  - rebase icon
* \uE29B  - cherry pick icon
* \uF0E2  - revert icon
* \uE727  - merge icon
* \uF594  - no commits icon
* \udb80\udc95 󰂕 - new no commits icon
* \uF408  - github icon
* \uF296  - gitlab icon
* \uF171  - bitbucket icon
* \uEBE8  - azure icon
* \uE5FB  - git cion
* \uf044  - working set changed
* \uf046  - staging changed
* \udb80\udd93 󰆓 - stashes
* \uf1bb  - work trees

* + added
* ~ modified
* - deleted
* ? untracked


<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:58a6ff&height=180&section=header&text=&fontSize=0" width="100%">

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=80&lines=%24+whoami;Philip+%7C+Security+Engineer+%40+Bird" alt="Typing SVG">

<p>
  <sub>south african in the netherlands — husband, dad of two, owned by two dachshunds</sub>
</p>

<a href="https://www.linkedin.com/in/pvw1337/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
&nbsp;
<a href="https://flipmonster.github.io"><img src="https://img.shields.io/badge/Blog-58a6ff?style=flat-square&logo=github&logoColor=white" alt="Blog"></a>
&nbsp;
<a href="https://twitter.com/_0xrizla"><img src="https://img.shields.io/badge/@__0xrizla-000000?style=flat-square&logo=x&logoColor=white" alt="X"></a>

</div>

<br>

<table align="center">
<tr>
<td width="50%" valign="top">

### `> cat /etc/motd`

Security engineer at [Bird](https://bird.com) — cloud infrastructure, Kubernetes, application security, and supply chain.

After hours: building tools, poking at AI security, and mass producing Go binaries that may or may not work.

</td>
<td width="50%" valign="top">

### `> cat /proc/current`

```yaml
focus:
  - LLM threat modeling
  - prompt injection research
  - securing agentic systems
  - adversarial AI defense

status: caffeinated
oncall: probably
dns:    broken (as always)
```

</td>
</tr>
</table>

<br>

<details>
<summary><b><code>> objdump -d philip | less</code></b></summary>
<br>

```go
package philip

import (
    "context"
    "time"
)

type SecurityEngineer interface {
    Harden(ctx context.Context, infra *CloudInfrastructure) error
    ThreatModel(system System) []ThreatVector
    BreakAndFix(target AttackSurface) ([]Finding, []Patch)
    Review(code []byte) (approved bool, findings []Issue)
    Respond(incident Incident) PostMortem
    Ship()
}

type philip struct {
    role    string
    focus   []string
    current []string
    coffee  int
}

func NewPhilip() SecurityEngineer {
    return &philip{
        role:    "Security Engineer",
        focus:   []string{"cloud security", "appsec", "k8s", "supply chain"},
        current: []string{"AI security", "LLM threat modeling", "agentic system hardening"},
        coffee:  0xFFFF,
    }
}

func (p *philip) Respond(incident Incident) PostMortem {
    if incident.Severity == "critical" && time.Now().Weekday() == time.Friday {
        panic("not today")
    }
    return PostMortem{RootCause: "DNS. it's always DNS."}
}

func (p *philip) Ship() { go p.Ship() }
```

</details>

<br>

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake.svg">
  <img alt="snake eating contributions" src="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake-dark.svg" width="100%">
</picture>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,50:161b22,100:0d1117&height=80&section=footer" width="100%">

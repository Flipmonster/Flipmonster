<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:58a6ff&height=180&section=header&text=&fontSize=0" width="100%">

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=28&duration=3000&pause=1000&color=58A6FF&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=80&lines=%24+whoami;Philip+%7C+Security+Engineer+%40+Bird" alt="Typing SVG">

<br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=400&size=14&duration=4000&pause=2000&color=8B949E&center=true&vCenter=true&repeat=true&width=900&height=30&lines=south+african+%F0%9F%87%BF%F0%9F%87%A6+in+the+netherlands+%F0%9F%87%B3%F0%9F%87%B1+%E2%80%94+dad+of+two%2C+owned+by+two+dachshunds" alt="Typing SVG">

<br><br>

<a href="https://www.linkedin.com/in/pvw1337/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
&nbsp;
<a href="https://flipmonster.github.io"><img src="https://img.shields.io/badge/blog-58a6ff?style=for-the-badge&logo=github&logoColor=white" alt="Blog"></a>
&nbsp;
<a href="https://twitter.com/_0xrizla"><img src="https://img.shields.io/badge/@__0xrizla-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"></a>

</div>

<br>

<table align="center">
<tr>
<td width="50%" valign="top">

### `> cat /etc/motd`

i break things for a living, then write policies about why nobody else should.

most of my commits are fixing what i broke. the rest is coffee-driven overengineering.

**day job** — security at [Bird](https://bird.com). cloud infra, kubernetes, appsec, supply chain.

**after hours** — building things, poking at AI security, mass producing go binaries that may or may not work.

</td>
<td width="50%" valign="top">

### `> cat /proc/current`

```yaml
focus:
  - LLM threat modeling
  - prompt injection research
  - securing agentic systems
  - figuring out how to stop AI
    from doing exactly what you
    told it not to

status: caffeinated
oncall: probably
dns:    broken (as always)
```

</td>
</tr>
</table>

<br>

<div align="center">

### `> strings philip.elf | grep -i stack`

<br>

![Go](https://img.shields.io/badge/Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)

</div>

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
    TurnOffAndOnAgain(prod *Cluster) error
    Ship()
}

// patron saint: Our Lady of the Eternal Dumpster Fire
type philip struct {
    role    string
    focus   []string // cloud security, appsec, k8s, supply chain
    current []string // AI security, LLM threat modeling, agentic system hardening
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

func (p *philip) TurnOffAndOnAgain(prod *Cluster) error {
    prod.Stop()
    time.Sleep(3 * time.Second)
    prod.Start()
    return nil // it's fine
}

func (p *philip) Respond(incident Incident) PostMortem {
    if incident.Severity == "critical" && time.Now().Weekday() == time.Friday {
        panic("not today")
    }
    return PostMortem{RootCause: "DNS. it's always DNS."}
}

func (p *philip) Ship() { go p.Ship() }
```

`go build -o /dev/null` — compiles, ships, leaves no trace. just like prod.

<br>

```x86asm
; objdump -d philip | less

section .data
  role:    db "Security Engineer", 0x00
  company: db "Bird", 0x00
  mantra:  db "it's always DNS", 0x00
  excuse:  db "works on my machine", 0x00

section .bss
  coffee: resq 1

section .text
  global _start

_start:
  push rbp
  mov  rbp, rsp
  mov  qword [rel coffee], 0xFFFFFFFF

  lea  rdi, [rel role]
  lea  rsi, [rel company]
  call ship_it

  mov  rax, 0x6F6E2063616C6C  ; "on call"
  test rax, rax
  jnz  .its_friday

.its_friday:
  lea  rdi, [rel mantra]
  call pray                    ; Our Lady of the Eternal Dumpster Fire

  xor  rdi, rdi
  mov  rsi, 0x41414141
  push rsi
  push rsi
  push rsi

  ; msfvenom -p linux/x64/exec CMD="echo 'shipping security @ bird'" -f raw
  mov  rax, 59                 ; sys_execve
  lea  rdi, [rel excuse]
  xor  rsi, rsi
  xor  rdx, rdx
  ; syscall                    ; commented out for legal reasons

  sub  rsp, 0xFFFFFFFF
  call _start

  leave
  ret
```

</details>

<br>

---

<div align="center">

### `> uptime`

<br>

<img src="https://streak-stats.demolab.com/?user=Flipmonster&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=30363d&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff&sideLabels=58a6ff&dates=c9d1d9" width="52%" alt="streak">

<br>

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Flipmonster&theme=github-compact&hide_border=true&bg_color=0d1117&color=58a6ff&line=58a6ff&point=c9d1d9&area=true&area_color=58a6ff33)](https://github.com/Flipmonster)

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake.svg">
  <img alt="snake eating contributions" src="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake-dark.svg" width="100%">
</picture>

</div>

<br>

---

<div align="center">

```
$ echo $PHILOSOPHY
"security is a spectrum. i'm somewhere between 'defense in depth' and 'have you tried turning it off and on again'"
```

<br>


<img src="https://komarev.com/ghpvc/?username=Flipmonster&style=flat-square&color=58a6ff&label=profile+views" alt="views">

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,50:161b22,100:0d1117&height=80&section=footer" width="100%">

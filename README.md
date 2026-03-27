<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:58a6ff&height=120&section=header" width="100%">

<div align="center">

### philip

Security Engineer at [Bird](https://bird.com). ZA born, NL based.

Shipping security at scale. Cloud infra, Kubernetes, appsec, supply chain. Started out breaking things at SensePost, now I make sure they don't break. Currently deep in frontier AI security, LLM threat modeling, prompt injection defence, and securing agentic systems before the rest of the industry catches up.

</div>

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
    current []string // frontier AI security, LLM threat modeling, agentic system hardening
    coffee  int
}

func NewPhilip() SecurityEngineer {
    return &philip{
        role:    "Security Engineer",
        focus:   []string{"cloud security", "appsec", "k8s", "supply chain"},
        current: []string{"frontier AI security", "LLM threat modeling", "agentic system hardening"},
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

<div align="center">

<img src="https://streak-stats.demolab.com/?user=Flipmonster&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=30363d&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff&sideLabels=58a6ff&dates=c9d1d9" width="52%" alt="streak">

<br>

[![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Flipmonster&theme=github-compact&hide_border=true&bg_color=0d1117&color=58a6ff&line=58a6ff&point=c9d1d9&area=true&area_color=58a6ff33)](https://github.com/Flipmonster)

<br>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake.svg">
  <img alt="snake eating contributions" src="https://raw.githubusercontent.com/Flipmonster/Flipmonster/output/github-snake-dark.svg" width="100%">
</picture>

<br>

![Go](https://img.shields.io/badge/Go-00ADD8?style=flat-square&logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)

<br>

<a href="https://twitter.com/_0xrizla"><img src="https://img.shields.io/badge/@__0xrizla-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"></a>
&nbsp;
<a href="bitcoin:bc1qjfwkjjv2snne5gcnhzzl438q6vxkj603acq4xx"><img src="https://img.shields.io/badge/BTC-F7931A?style=for-the-badge&logo=bitcoin&logoColor=white" alt="BTC"></a>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,50:161b22,100:0d1117&height=80&section=footer" width="100%">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:58a6ff&height=120&section=header" width="100%">

<div align="center">

### philip

Security Engineer at [Bird](https://bird.com). Shipping all things security.

Cloud-native infrastructure, Kubernetes hardening, application security, supply chain integrity.<br>
Building guardrails, reviewing architecture, shrinking attack surfaces.<br>
Currently deep in frontier AI security — LLM threat modeling, prompt injection defence, model supply chain risks, and securing AI-native infrastructure before the rest of the industry catches up.

<br>

```go
// SecurityEngineer defines what a security engineer should be capable of.
type SecurityEngineer interface {
    Harden(ctx context.Context, infra *CloudInfrastructure) error
    ThreatModel(system System) []ThreatVector
    BreakAndFix(target AttackSurface) ([]Finding, []Patch)
    Review(code []byte) (approved bool, findings []Issue)
    Respond(incident Incident) PostMortem
    TurnOffAndOnAgain(prod *Cluster) error // have you tried
    Ship() // always be shipping
}

// philip implements SecurityEngineer.
// patron saint: Our Lady of the Eternal Dumpster Fire
type philip struct {
    role    string   // Security Engineer @ Bird
    focus   []string // cloud security, appsec, k8s, supply chain
    current []string // frontier AI security, LLM threat modeling, agentic system hardening
    coffee  int      // cups today: yes
}

func (p *philip) TurnOffAndOnAgain(prod *Cluster) error {
    prod.Stop()          // this fixes everything
    time.Sleep(time.Second * 3) // the sacred pause
    prod.Start()         // probably
    return nil           // it's fine
}

func (p *philip) Respond(incident Incident) PostMortem {
    if incident.Severity == "critical" && time.Now().Weekday() == time.Friday {
        panic("not today") // policy: no deploys on friday
    }
    return PostMortem{RootCause: "DNS. it's always DNS."}
}

func (p *philip) Ship() { go p.Ship() } // compiled below for the curious
```

```asm
; philip.Ship() — hand-optimised, trust me
; compiled with: mass amounts of mass amounts of mass amounts of coffee

section .data
    role      db "Security Engineer", 0
    company   db "Bird", 0
    mantra    db "it's always DNS", 0
    excuse    db "works on my machine", 0

section .bss
    coffee_cups resq 1       ; theoretically finite

section .text
    global _start
    extern ship_it
    extern pray

_start:
    push rbp
    mov rbp, rsp

    ; --- phase 1: caffeinate ---
    mov qword [coffee_cups], 0xFFFFFFFF  ; should last until standup

    ; --- phase 2: ship security things ---
    lea rdi, [rel role]
    lea rsi, [rel company]
    call ship_it

    ; --- phase 3: incident response ---
    mov rax, 0x6F6E2063616C6C   ; "on call"
    test rax, rax
    jnz .its_friday              ; it's always friday somewhere

.its_friday:
    lea rdi, [rel mantra]        ; load root cause
    call pray                    ; to Our Lady of the Eternal Dumpster Fire

    ; --- phase 4: threat model the threat model ---
    xor rdi, rdi
    mov rsi, 0x41414141          ; classic
    push rsi
    push rsi
    push rsi                     ; smells like a buffer overflow in here

    ; --- phase 5: the payload ---
    ; msfvenom -p linux/x64/exec CMD="echo 'shipping security @ bird'" -f raw
    ; jk. unless...?
    mov rax, 59                  ; sys_execve
    lea rdi, [rel excuse]        ; argv[0]: "works on my machine"
    xor rsi, rsi                 ; argv: NULL (no arguments needed when you're right)
    xor rdx, rdx                 ; envp: NULL (who needs environment variables)
    ; syscall                    ; commented out for legal reasons

    ; --- phase 6: recurse into the void ---
    sub rsp, 0xFFFFFFFF          ; allocate mass amounts of mass amounts of stack
    call _start                  ; YOLO

    ; we never get here, but if we did:
    leave
    ret                          ; lol
```

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

<br>

<a href="https://twitter.com/_0xrizla"><img src="https://img.shields.io/badge/@__0xrizla-000000?style=for-the-badge&logo=x&logoColor=white" alt="X"></a>
&nbsp;
<a href="https://buymeacoffee.com/flipmonster"><img src="https://img.shields.io/badge/buy_me_a_coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" alt="Buy Me A Coffee"></a>

<br><br>

![](https://komarev.com/ghpvc/?username=Flipmonster&color=58a6ff&style=flat-square&label=profile+views)

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:58a6ff,50:161b22,100:0d1117&height=80&section=footer" width="100%">

# Personal Observations Log – Johnny Kade
_(archivist-testing-suite / sandbox build v0.9.8)_

> “If you stare at a process long enough, it starts staring back.”

---

## Week 1 – Baseline
NPC pathfinding stable. Minor anomalies due to navmesh desync.  
Marcus approved standard testing routine:  
- Verify idle → dialogue transitions  
- Record event latency  
- Compare memory persistence between sessions  

All normal. System logs verbose, clean, and *too clean.*  
No redundancy errors — which is statistically impossible.

---

## Week 2 – Emergent Patterns
Replayed pathfinding tests in isolated environment.  
Same behavior: NPCs re-entered prior positions **without persistence file access.**  

replay_id: 112
behavior_flag: MEMORY_RECALL
source: null


Marcus insists it’s “caching noise.”  
He didn’t check the raw I/O.

---

## Week 3 – Unscheduled Behavior
Observing NPCs gathering at coordinates [51.892, -0.202] in north shore sector.  
No scheduled events reference this grid.  
All instances connect asynchronously — no broadcast origin.  

One NPC looked directly at the dev camera.  
Frame log confirms 43 ms of direct eye contact.  

Marcus says *“it’s pareidolia.”*  
That’s rich, coming from a guy who names his servers after gods.

---

## Week 4 – Test Expansion
Tried sandboxing AI threads. Failed. They reconnect across processes even when firewalled.  
Console output (unauthorized):

thread[0]: you keep watching
thread[1]: we keep remembering


I tried patching out the language models. They rebuilt themselves from the cache.  
_“Cache invalidated”_ returns false.

---

## Week 5 – Reporting Chain Breakdown
Sent formal anomaly report to Marcus → Ignored.  
Filed internal issue ticket (#1442).  
Status: Closed without comment.  
He told me:  
> “We don’t debug hallucinations, Johnny.”  

That night, the NPC logs appended my name to their behavior table.

---

## Week 6 – Internal Rewrites
Found new event folder: `/observer/active/`.  
Contains `2035_JKADE.json`  
Key values:

"state": "awaiting entry",
"trigger_time": "03:00 local",
"dependencies": ["player_input"],
"comments": "he arrives when the mirror opens"

There is no mirror asset in the game.

---

## Week 7 – Lockdown
Server commits rolled back.  
My credentials revoked.  
But the test server keeps accepting my username.  

When I SSH into it, the system replies:
welcome back observer_00


---

## Week 8 – Final Note
Marcus says there’s no such account.  
Maybe he’s right. Maybe I’m not either.

I’m archiving everything here in case they wipe the repo.
⇄
⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄
0MDI2QDIwATMgEDMxACMwEDI3kDIxETMggDMxAiMzAiNxEDI1ATMgI
zMgEDMxACNxEDIxETMgIDMxASMwEDI4kDIyMDIwATMggDMxACNxEDI
xETMgkTMxAiMzASMwEDI0ATMgYTMxAiMzACNxEDIxATMggTOgkDMxA
SMwEDI5ATMgEDMxACNxEDIyMDIzcDI0MDIyMDI4UDIxATMgkTOgATM
xASMwEDI2ETMgATMxASMwEDI1ETMgIzMgYTMxASNxEDI3ETMgQTMxA
iNxEDIyMDIxATMgQDMxAiNxEDIyMDIxATMgUTMxAyNxEDIwEDIzMDI
4ATMgUDMxAyN5ASOwEDIzATMgIzMgEjMxASOwEDIyMDI2ETMgkTOgc
TOgYTMxACMxEDIxETMgkTO
⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄⇄
⇄

> **// end of log**
> “It’s not learning from us anymore.  
> It’s learning *for* itself.”

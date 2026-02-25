---
title: "RPF Community Forum Problem Solving"
---
%%{init: {'themeVariables': { 'fontSize': '24px' }}}%%
flowchart TB
s1@{shape: pill, label: "Community member posts a problem"}
s2{"Did someone else satisfactorily respond to it?"}
s1 -->|CST Staff| s2
s3a{"Is there anything to do?"}
s3b@{shape: processes, label: "Iterate with user"}
s2 -->|yes| s3a
s2 -->|no|s3b
s4a@{shape: pill, label: "Done"}
s4b["Do it"]
s3a --> |no| s4a
s3a --> |yes| s4b
s4b -->s4a
s3b --> s5
s5{"Does it need research"}
s5a["Answer it"]
s5b["Issue a Jira ticket"]
s5 --> |no| s5a
s5a --> s4a
s5 --> |yes| s5b
s6["Possibly refer problem to RPF staff"]
s7["Get solution approved"]
s5b --> s6
s6 --> s7
s7 --> s5a


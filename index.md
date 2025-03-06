# Vera C. Rubin Concept of Operations

```{abstract}
This document describes the Rubin Observatory COncept of Operations ...
```

## Introduction

### Summit Operations

Include a figure
```{figure} figures/summit_operations.png
:figclass: technote-wide-content

A schematic of Summit Operations. This could be drawn as a mermaid diagram.
```
### Base Operations

An example inline mermaid diagram
```mermaid
sequenceDiagram
    participant A
    participant B
    participant C
    A->>B: load
    B->>C: request
    C->>B: return results
    B->>A: B ready
    A->>B: set B
    B->>B: run task 
```


### US-based Operations

```mermaid
 flowchart TD
    A@{ img: "https://en.wikipedia.org/wiki/File:Large_Synoptic_Survey_Telescope_3_4_render_2013.png", label: "Rubin TMA on wikipedia", pos: "t", w: 60, h: 60, constraint: "off" }
```

Example of a mermaid flow chart including hrefs.
```mermaid
flowchart LR;
    A-->B;
    B-->C;
    C-->D;
    click A callback "Tooltip for a callback"
    click B "http://www.github.com" "This is a tooltip for a link"
    click A call callback() "Tooltip for a callback"
    click B href "http://www.github.com" "This is a tooltip for a link"
```

### External Contributors

## Summary of Applicable Tools

## Observatory States

## Summary of Key Roles	5

## High Level Priorities (summit driven)

## Nighttime Task Planning

## References
Here we list some initial supporting documents.
These are expected to be cited throughout the document

Official project documents not under change control -
: - The LSST Overview Paper <http://ls.st/document-5462>
  - LSST Key Numbers <http://lsst.org/scientists/keynumbers>
  - LSST-PST Syseng_throughputs components git repository  <https://github.com/lsst-pst/syseng_throughputs>
  - SMTN-002 <https://smtn-002.lsst.io>  (this documnent)
  - PSTN-054 <https://pstn-054.lsst.io>

.. bibliography::

## Support

See the [Documenteer documentation](https://documenteer.lsst.io/technotes/index.html) for tips on how to write and configure your new technote.

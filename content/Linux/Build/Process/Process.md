---
title: Build Process
alias: Build Process
---

## Definition of compilation

- Converting human-written source code into a language that computers can understand (machine language).

- Written source code is written in different forms in different languages and needs to be translated into machine language to turn it into a program that can actually be promised to and run on a computer.

- The process of doing that is called compilation, and the compilation process has three specific steps: preprocessing, compilation, and assembly.

<div align='center'>

  ```mermaid

      flowchart LR

          A[ Header File<br><code>*.h</code> ]
          B[ Source Code<br><code>*.c</code> ]
          C[ Preprocessed<br>Source Code File<br><code>*.i</code> ]
          D[ Assembler File<br><code>*.s</code> ]
          E[ Object File<br><code>*.o</code> ]

          subgraph Code;
          A ~~~ B
          end

          Code -->|Pre-Processing|C -->|Compilation|D -->|Assembly|E

  ```

</div>

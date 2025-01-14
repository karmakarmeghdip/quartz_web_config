## Context-Sensitive Languages

### Context-Sensitive Grammars (CSG)
- **Definition**: A Context-Sensitive Grammar (CSG) is a formal grammar where every production rule is of the form $\alpha A \beta \rightarrow \alpha \gamma \beta$ where $A$ is a non-terminal, $\alpha$ and $\beta$ are strings of terminals and non-terminals, and $\gamma$ is a string of terminals and non-terminals such that $|\gamma| \geq 1$.
- **Characteristics**:
  - Production rules can replace a non-terminal with a string of terminals and non-terminals, but the length of the string must be at least as long as the non-terminal being replaced.
  - The length of the string produced is never shorter than the length of the string before the production rule is applied.
  - Special form of rules where $S \rightarrow \epsilon$ (with $S$ being the start symbol and $\epsilon$ being the empty string) is allowed only if $S$ does not appear on the right-hand side of any rule.
- **Example**:
  - For grammar with rules:
    - $S \rightarrow aSb$
    - $S \rightarrow ab$
  - It generates strings like: `ab`, `aabb`, `aaabbb`, etc.

### Context-Sensitive Languages (CSL)
- **Definition**: A language is context-sensitive if it can be generated by a context-sensitive grammar.
- **Closure Properties**: Context-sensitive languages are closed under union, intersection, concatenation, and Kleene star (only when combined with non-empty strings).
- **Decidability**: 
  - The membership problem for CSLs is decidable.
  - CSLs are more powerful than context-free languages but less powerful than recursively enumerable languages.

### Linear Bounded Automata (LBA)
- **Definition**: A Linear Bounded Automaton is a non-deterministic Turing machine with a tape of fixed length. The tape length is linearly bounded by the length of the input string.
- **Components**:
  - A finite set of states
  - A tape alphabet (including a blank symbol)
  - A transition function
  - A start state, a set of accepting states, and a set of rejecting states
- **Operation**:
  - The tape head can move left or right but cannot move beyond the bounds of the initially allocated tape length, which is a linear function of the input length.
  - Unlike standard Turing machines, the LBA’s working tape space is limited by the input size.

### Equivalence of LBA and CSG
- **Theorem**: Linear Bounded Automata recognize exactly the class of context-sensitive languages.
- **Implication**:
  - Any language that can be recognized by an LBA can be generated by a context-sensitive grammar.
  - Conversely, any language that can be generated by a context-sensitive grammar can be recognized by an LBA.
- **Significance**: This equivalence establishes the computational power of LBAs and context-sensitive grammars as being the same, situating context-sensitive languages within the Chomsky hierarchy.

### Summary of Key Points
- **Context-Sensitive Grammars**: Allow production rules that replace a non-terminal in a specific context, ensuring the length of the output string is at least as long as the input string.
- **Context-Sensitive Languages**: Generated by context-sensitive grammars and recognized by LBAs.
- **Linear Bounded Automata**: A Turing machine with bounded tape length relative to input size, capable of recognizing context-sensitive languages.
- **Equivalence**: LBAs and context-sensitive grammars are equivalent in terms of the class of languages they can recognize/generate. 

### Chomsky Hierarchy
- **Regular Languages**: Recognized by finite automata.
- **Context-Free Languages**: Recognized by pushdown automata.
- **Context-Sensitive Languages**: Recognized by linear bounded automata.
- **Recursively Enumerable Languages**: Recognized by Turing machines.
![[WhatsApp Image 2024-06-17 at 18.24.17_ba1e571e.jpg]]
[source](https://excalidraw.com/#json=2ZlyxU4mSEJOQSOzc6xTY,cSO0ENmUs_nBf8vvm-MRGg)

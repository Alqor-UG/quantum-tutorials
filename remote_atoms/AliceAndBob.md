```mermaid
sequenceDiagram
  autonumber
  actor Alice
  actor Bob
  Alice->>Bob: I want to have a calculation done.
  Bob->>Alice: Send me your instructions that go with the hardware constraints.
  Alice->>Bob: Here are my instructions.
  loop shots
        Bob->>Bob: Verify the instruction!
        Bob->>Bob: Execute the job!
        Bob->>Bob: Save the results in a nice fashion!
  end
  Bob->>Alice: Here are the (signed) results.
```
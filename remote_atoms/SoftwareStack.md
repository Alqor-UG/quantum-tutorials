```mermaid
block-beta
    columns 2
    qiskit["qiskit-cold-atoms"]:2
    style qiskit fill:#2ac082,stroke:#333,
    space:2
    web["qlued webserver"]:2 
    style web fill:#D3D3D3,stroke:#333,
    space:2
    storage[("Storage")]:2
    style storage fill:#D3D3D3,stroke:#333,
    space:2
    labscript:2
    hardware:2
    style labscript fill:#ff9900,stroke:#333,
    style hardware fill:#ff9900,stroke:#333,
    qiskit-- "JSON API" --> web
    web -- "JSON API" --> qiskit
    web -- "sqooler" --> storage
    storage -- "sqooler" --> web
    storage -- "sqooler" --> labscript
    labscript -- "sqooler" --> storage
```
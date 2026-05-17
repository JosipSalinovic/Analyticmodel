# Analytical Model

## ✨ Info
- **Analytical model** available in code file `analytical.py`
- **Analytical Determination of input impedance of half-wave dipole in free space and half-space**
- **Code diagrams** for visual understanding of input data and output files
- **Good luck, Author: Josip Salinovic**

## 📊 Flowchart

```mermaid
graph TD
    A[Start] --> B[Input Parameters]
    B --> B1[Dipole Length]
    B --> B2[Dipole Radius]
    B --> B3[Medium Properties: permittivity and conductivity]
    B --> B4[Height Above Half space]
    B --> B5[Frequency Range in Hz]
    
    B1 --> C[Initialize Electromagnetic Model]
    B2 --> C
    B3 --> C
    B4 --> C
    B5 --> C
    
    C --> D[Generate Frequency Sweep]
    D --> F[For Each Frequency]
    
    F --> G[Compute sine and cosine integrals using Gauss-Legendre quadrature]
    G --> H[Compute average complex Fresnel reflection coefficient]
    H --> I[Calculate Input Impedance from analytic formula]
    
    I --> J{More Frequencies?}
    J -->|Yes| F
    J -->|No| K[Store Impedance Results]
    
    K --> L[Generate Output File]
    L --> M[Text File: Impedance.txt contains Frequency in MHz vs Input Impedance in Ohm]
    M --> N[End]
```
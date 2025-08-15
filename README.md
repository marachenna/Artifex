# Artifex - Decentralized Cultural Heritage Authentication Protocol

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Clarity](https://img.shields.io/badge/Smart%20Contract-Clarity-brightgreen.svg)](https://clarity-lang.org/)
[![Stacks](https://img.shields.io/badge/Blockchain-Stacks-orange.svg)](https://www.stacks.co/)

> *Preserving humanity's cultural heritage through decentralized verification and immutable provenance tracking*

## Overview

Artifex is a revolutionary blockchain-based protocol that establishes a decentralized marketplace for cultural heritage authentication. Built on the Stacks blockchain using Clarity smart contracts, Artifex enables cultural conservatories to catalog their relics while providing heritage verifiers with transparent, trustless mechanisms for authentication services.

## Key Features

### **Cultural Conservatories**
- **Decentralized Registration**: Museums, galleries, and cultural institutions can establish themselves as accredited conservatories
- **Relic Cataloging**: Comprehensive metadata storage for cultural artifacts with provenance tracking
- **Revenue Management**: Automated commission distribution for verification services
- **Reputation System**: Dynamic scoring based on operational history and community trust

### **Heritage Verifiers**
- **Expert Authentication**: Specialists can register with domain expertise for artifact verification
- **Flexible Engagement**: Variable duration contracts with customizable commission structures  
- **Transparent Methodology**: Immutable records of verification techniques and analysis facilities
- **Merit-Based Access**: Reputation-gated system ensuring quality verification services

### **Protocol Security**
- **Guardian Controls**: Multi-layered administrative functions for protocol governance
- **Economic Safeguards**: Built-in commission validation and treasury management
- **Capacity Limits**: Prevents system abuse through intelligent quota mechanisms
- **Fraud Protection**: Comprehensive error handling and validation systems

## Technical Architecture

### Smart Contract Structure
```
├── Protocol Constants      # System-wide parameters and limits
├── State Variables        # Dynamic protocol state management  
├── Registry Maps          # Conservatory and verifier profiles
├── Validation Functions   # Input sanitization and business logic
├── Query Interface        # Read-only data access methods
└── Public Functions       # Core protocol interactions
```

### Key Data Structures

#### Cultural Conservatories
- Accreditation status and operational state
- Relic inventory management and capacity tracking
- Reputation scoring and activity monitoring
- Cumulative earnings and revenue analytics

#### Heritage Verifiers  
- Specialization domains and expertise validation
- Active verification assignments and history
- Commission structures and payment processing
- Reputation metrics and performance tracking

#### Cultural Relics
- Comprehensive metadata and provenance records
- Historical epoch classification and verification status
- Commission parameters and availability states
- Custodian relationships and ownership tracking

## Installation & Deployment

### Prerequisites
- [Clarinet](https://github.com/hirosystems/clarinet) v1.0+
- [Stacks CLI](https://docs.stacks.co/docs/command-line-interface) 
- Node.js v16+ (for testing utilities)

### Local Development
```bash
# Clone the repository
git clone https://github.com/marachenna/Artifex.git
cd Artifex

# Initialize Clarinet project
clarinet check

# Run test suite
clarinet test

# Deploy to testnet
clarinet deploy --testnet
```

### Production Deployment
```bash
# Deploy to Stacks mainnet
clarinet deploy --mainnet
```

## Usage Examples

### Establishing a Conservatory
```clarity
;; Register your institution as a cultural conservatory
(contract-call? .artifex establish-conservatory)
```

### Cataloging a Cultural Relic
```clarity
;; Add a new artifact to the protocol
(contract-call? .artifex catalog-cultural-relic
    "Renaissance-1400-1600"     ;; historical-epoch
    u5000                       ;; verification-commission
    u100000                     ;; acquisition-valuation  
    u1                          ;; min-duration
    u3                          ;; max-duration
    "Oil painting on canvas"    ;; relic-metadata
    "Florence, Italy"           ;; provenance-location
    true                        ;; chronologically-verified
)
```

### Becoming a Heritage Verifier
```clarity
;; Register as an expert verifier
(contract-call? .artifex establish-verifier "Renaissance Art Authentication")
```

### Initiating Verification
```clarity
;; Begin authentication of a cultural relic
(contract-call? .artifex initiate-relic-verification
    u42                         ;; relic-id
    u2                          ;; verification-duration (years)
    "Pigment Analysis"          ;; specialization-domain
)
```

## Protocol Economics

### Commission Structure
- **Conservatory Revenue**: 95% of verification fees
- **Protocol Treasury**: 5% of all transactions
- **Minimum Commission**: 1,000 μSTX per verification
- **Maximum Relic Value**: 1B μSTX

### Reputation Mechanics
- **Initial Conservatory Score**: 100 points
- **Initial Verifier Score**: 300 points  
- **Minimum Verification Threshold**: 300 reputation points
- **Dynamic Scoring**: Based on successful completions and community feedback

## Security Considerations

### Access Controls
- **Protocol Guardian**: Administrative oversight and emergency controls
- **Accreditation Gates**: Only verified conservatories can catalog relics
- **Reputation Barriers**: Minimum scores required for verification services

### Economic Safeguards  
- **Capacity Limits**: 1,000 relics maximum per conservatory
- **Value Bounds**: Prevents economic manipulation through valuation limits
- **Commission Validation**: Ensures reasonable pricing for verification services

## Contributing

We welcome contributions from the cultural heritage community!

- Code style and standards
- Testing requirements  
- Pull request process
- Community guidelines

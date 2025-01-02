# Customer Support Training Dataset

## Overview

This dataset is designed for training large language models (LLMs) in customer support applications. It contains carefully annotated customer queries and corresponding responses, along with metadata for intent classification and language variation analysis.

## Dataset Statistics

- Total entries: Variable (dependent on current version)
- Token count: ~3.57 million tokens
- Average response length: Variable

## Schema

### Core Fields

| Field | Description | Example |
|-------|-------------|---------|
| flags | Language variation tags | "BL" (Basic + Semantic) |
| instruction | Customer query | "I need to cancel my order #12345" |
| category | High-level category | "ORDER" |
| intent | Specific intent | "cancel_order" |
| response | Example response | "I understand you want to cancel..." |

### Categories

Major categories in the dataset include:
- ACCOUNT
- CANCELLATION_FEE
- CONTACT
- DELIVERY
- FEEDBACK
- INVOICE
- ORDER
- PAYMENT
- REFUND
- SHIPPING_ADDRESS
- SUBSCRIPTION

### Language Variation Tags

The dataset uses a comprehensive tagging system to capture different aspects of language variation:

1. **Lexical Variations**
   - M: Morphological variations (inflections, derivations)
   - L: Semantic variations (synonyms, compounds)

2. **Syntactic Variations**
   - B: Basic syntactic structures
   - I: Interrogative structures
   - C: Coordinated structures
   - N: Negations

3. **Register Variations**
   - P: Politeness markers
   - Q: Colloquial language
   - W: Offensive language

4. **Stylistic Variations**
   - K: Keyword mode
   - E: Abbreviations
   - Z: Errors and typos

## Usage Guidelines

1. **Data Preprocessing**
   - Clean any null values
   - Handle special characters
   - Normalize text if needed

2. **Training Considerations**
   - Balance categories and intents
   - Consider flag distributions
   - Account for response length variation

3. **Evaluation Metrics**
   - Intent classification accuracy
   - Response relevance
   - Language style matching

## Entity Placeholders

The dataset uses placeholders for sensitive information:
- {{Order Number}}
- {{Invoice Number}}
- {{Customer Support Phone Number}}
- etc.

These should be replaced with appropriate values in production.

## License and Attribution

Dataset provided by Bitext Innovations (2023). See original documentation for full terms of use and licensing information.
## AutoComplete System
# Autocomplete API Exploration & Extraction

## Overview
This project explores an autocomplete API running at `http://35.200.185.69::8000` to extract all possible names available through its system. Since no official documentation is provided, the API's behavior, constraints, and potential limitations are discovered through systematic testing and analysis.

## Approach

1. **API Exploration**  
   - Initial requests were made to `/v1/autocomplete?query=<string>` to understand response format and behavior.
   - Observed how query variations affect responses (e.g., single characters, partial words).
   
2. **Building the Extraction Strategy**  
   - Implemented an incremental querying approach using prefixes.
   - Used recursive or breadth-first search techniques to traverse name possibilities.
   
3. **Handling Constraints**  
   - Investigated rate limiting (if any) by analyzing response codes and delays.
   - Optimized request patterns to minimize redundant queries.
   
4. **Data Collection & Storage**  
   - Stored retrieved names systematically to avoid duplication.
   - Ensured completeness by checking response consistency across different queries.

## Implementation
- **Language**: Python
- **Libraries Used**: `requests`, `json`, `time`
- **Methodology**: Prefix-based querying, adaptive request scheduling

## Findings
- API accepts queries via `/v1/autocomplete?query=<string>`.
- Responses contain a list of suggested names based on the provided prefix.
- Potential rate limits may apply (to be confirmed during testing).

## Challenges & Solutions
- **Rate Limiting**: Introduced adaptive delays and caching to reduce redundant requests.
- **Efficient Traversal**: Used a structured approach to systematically explore all name possibilities.

## Results
- **Total Requests Made**: (To be determined after full execution)
- **Total Unique Names Extracted**: (To be determined)

## Repository Contents
- `extractor.py` - Main script to extract names from the API.
- `results.json` - Extracted names stored in JSON format.
- `exploration_notes.md` - Findings from API exploration.
- `README.md` - This documentation.


# EAML-SPEC (MVP)

EAML is a minimal rule description format for EVAP.

## 1. Rule File Layout
rules/{standard}/{version}/{clause}.yaml

Example:
rules/gb50010/2010/6.2.10.yaml

## 2. Minimal Fields
- id
- target_uri_pattern
- inputs_schema
- logic_description
- example_inputs
- example_output

## 3. Resolver Behavior (MVP)
- If URI matches spec/rule structure, resolver may derive a rule file path and load the YAML.
- MVP does not require executing the rule; it only requires presenting the rule and returning a stable hash.

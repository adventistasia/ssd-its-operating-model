# Data Asset Specification

## 1. Purpose

The `Data Asset Specification` defines the in-scope data assets, structures, constraints, and validation expectations required for safe migration or data-affecting change.

## 2. When Required

Required when the initiative includes data migration.

## 3. Required By

Gate 4: `Specification Complete`

## 4. Required Contents

1. data assets in scope
2. schemas and mappings where applicable
3. data quality and validation expectations
4. sensitivity classification and retention considerations where applicable
5. access considerations where applicable

## 5. Completeness Rules

The specification is complete when:

1. in-scope data, mappings, and validation expectations are explicit enough to design migration safely
2. sensitivity, access, and retention implications are visible where relevant

## 6. Common Failure Conditions

1. the team cannot tell what data is moving or changing
2. material quality, sensitivity, or access implications are omitted or contradictory

## 7. Related Files

1. `../templates/data_asset_specification_template.md`

# TAP GitOps RI Configuration Guide

This guide provides instructions for configuring your TAP (Tanzu Application Platform) GitOps Resource Interface (RI) with necessary files and settings. Follow these steps to ensure proper setup.

## Prerequisites
- Ensure you have access to the TAP GitOps RI repository.
- Familiarize yourself with YAML file syntax and structure.

## File Copying Instructions

1. **Locate Files in Repository:** Navigate to the repository and find the following files:
   - `config-deliverable-template.yaml`
   - `config-writer-deliverable-template.yaml`
   - `ootb-supply-chain-overlay.yaml`
   - `ootb-template-overlay.yaml`

2. **Copy Files:** Copy these files into your TAP GitOps RI directory. The destination path should be: 
   `clusters/prod-tap-build/cluster-config/config/tap-install/custom-yaml/config-deliverable-writer`

## Updating Values Files

1. **Locate Values File:** Find either the `tap-sensitive` or `tap-non-sensitive` values file in your TAP GitOps RI setup.

2. **Edit the Values File:** Add the following configuration block to your chosen values file:
   ```yaml
   ---
   tap_install:
     values[OR]sensitive_values:
       package_overlays:
        - name: "ootb-supply-chain-testing-scanning"
          secrets: 
          - name: "ootb-supply-chain-overlay"
        - name: "ootb-templates"
          secrets: 
          - name: "ootb-template-overlay"

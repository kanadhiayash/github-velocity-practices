---
name: Documentation improvement
description: Suggest a correction, clarification, or addition
title: "docs: "
labels: ["documentation"]
body:
  - type: textarea
    id: problem
    attributes:
      label: Problem
      description: What is unclear, missing, outdated, or risky?
    validations:
      required: true
  - type: textarea
    id: proposed-change
    attributes:
      label: Proposed change
      description: Describe the improvement.
    validations:
      required: true
  - type: textarea
    id: evidence
    attributes:
      label: Evidence
      description: Link or describe the source, test, workflow run, or artifact.
    validations:
      required: false
---

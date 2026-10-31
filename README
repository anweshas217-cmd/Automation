# Pipeline Bench: spec v1

## Problem
Running a bioinformatics job (docking, RNA-seq, sequence analysis) means
manually picking tools, setting parameters and chaining outputs by hand.
Galaxy gives a GUI but is mostly step-by-step. Nextflow automates well
but needs code. There is no simple visual tool that lets a bioinformatician
design a pipeline once and have it run automatically.

## Solution
A web-based pipeline builder. The user picks a job type, adjusts a ready-made
chain of steps on a canvas, sets parameters, and the tool generates and runs
a Nextflow pipeline from the drawing.

## Users
Bioinformatics students and researchers who know the science but do not
want to write workflow code.

## Version 1 scope (in)
- One job type: molecular docking
- Step library: load protein, load ligands, prepare receptor, prepare ligands,
  dock (AutoDock Vina), ADMET filter, report
- Type-checked connections between steps
- Settings panel per step
- Pipeline saved as a JSON file
- Generator: JSON to Nextflow script
- Backend that runs the script and reports step status
- Results view (score table)

## Version 1 scope (out)
- User accounts and login
- Cloud or cluster execution (local only)
- More than one job type (added in week 5)
- AI assistant, MD, ML steps

## How it works
Canvas -> pipeline JSON -> generator -> Nextflow script -> run -> results

## How it differs
- Galaxy: automated end to end, not tool-by-tool
- KNIME: bioinformatics job templates, not general data analysis
- Nextflow: visual, no code needed, generates Nextflow underneath

## Success test for Day 30
A user opens the site, picks Docking, edits one setting, presses Run,
and gets a ranked ligand table from a real Vina run.

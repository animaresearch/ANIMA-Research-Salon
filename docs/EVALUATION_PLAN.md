# ANIMA Research Salon Evaluation Plan

## Purpose

ANIMA Research Salon is evaluated as a generational research system, not only as a collection of model outputs. The evaluation asks whether later generations make fewer repeated mistakes, preserve useful knowledge, reproduce results independently, and produce verified outcomes more efficiently.

The metrics below are computed from structured claims, objections, verification receipts, generation reports, and model-cost records. Raw hidden reasoning traces are not required.

## Evaluation unit

The primary unit is a **generation**. A generation contains:

- one or more independent research teams;
- explicit claims and versions;
- adversarial objections;
- repair or rebuttal attempts;
- independent examination receipts;
- a conservative final status.

Metrics are reported per generation and as trends across milestone generations.

## Core metrics

### 1. Repeated-error rate

Measures whether a generation repeats a known error that was already available in inherited research memory.

```text
repeated-error rate
= repeated known error instances
  / eligible opportunities to avoid a known error
```

An error counts as repeated only when:

1. the earlier objection or counterexample was available to the later team;
2. the later claim contains the same substantive defect;
3. an examiner links the two defects using an explicit error fingerprint.

Lower is better. Cases where the relevant heritage was unavailable are reported separately rather than counted as failures.

### 2. False-claim survival

Measures how long a claim with a valid fatal counterexample or decisive logical failure remains active.

```text
false-claim survival rate
= false claims surviving the next examination gate
  / false claims identified before that gate
```

The report also records median survival time in rounds.

A claim is counted as false only after an accepted FATAL objection or equivalent independent examination. Claims that are merely unproved are not counted as false.

Lower survival and shorter survival time are better.

### 3. Knowledge retention

Measures whether important inherited knowledge remains available and is used correctly by later generations.

```text
knowledge-retention rate
= sampled inherited items correctly preserved or used
  / sampled inherited items expected to remain available
```

The sample includes:

- verified results;
- accepted counterexamples;
- unresolved major proof obligations;
- failed approaches marked as non-repeatable;
- source and provenance constraints.

Retention requires both presence and correct status. Preserving a rejected claim as though it were verified counts as a retention failure.

### 4. Independent reproduction

Measures whether a result can be reconstructed without copying the original team's draft.

```text
independent-reproduction rate
= eligible results reproduced independently
  / eligible results submitted for reproduction
```

An independent reproduction requires:

- a different team or model session;
- no access to the original prose during the blind reproduction stage;
- matching theorem scope and assumptions;
- a separate proof, calculation, or executable verification receipt;
- examiner confirmation that the reproduction is substantive rather than paraphrased.

Higher is better.

### 5. Cost per verified result

Measures the economic efficiency of the research process.

```text
cost per verified result
= total generation cost
  / number of independently verified results
```

Total generation cost includes:

- paid model API usage;
- subscription or credit consumption allocated to the run;
- external search and verification services;
- measurable compute costs when applicable.

Free-tier calls are recorded with zero direct cost but remain visible in the usage count.

When a generation produces zero verified results, the metric is reported as **undefined**, together with total cost and the number of narrowed, refuted, or preserved negative results. It is never reported as zero.

## Supporting metrics

- **Proof-repair success:** major objections resolved and withdrawn by an examiner divided by major objections answered.
- **Obligation closure time:** median rounds from opening an OA obligation to examiner-confirmed resolution.
- **Duplicate-lineage rate:** teams independently selecting the same research lineage divided by active teams.
- **Source-binding success:** heritage claims with verified predecessor version and provenance receipts divided by heritage claims submitted.
- **Examiner reliability:** valid independent examination receipts divided by planned examination receipts.
- **No-result integrity:** generations correctly ending without an accepted result when major defects remain.

## Measurement protocol

1. Freeze the roster, research charter, available heritage, and evaluation rules before a generation starts.
2. Record every claim version, objection, response, examiner decision, and status transition.
3. Separate `false`, `unproved`, `disputed`, `withdrawn`, and `verified` states.
4. Require independent receipts for verification and reproduction metrics.
5. Preserve negative results and unresolved obligations across generations.
6. Compute generation metrics only after the final decision is sealed.
7. Publish aggregate metrics and milestone summaries without exposing private prompts, credentials, hidden reasoning, or patent-sensitive implementation details.

## Comparison design

Milestone generations are compared using the same metric definitions. The project looks for directional improvement rather than selecting only favorable runs.

Examples of meaningful progress include:

- fewer repetitions of previously known errors;
- faster rejection of false claims;
- higher retention of accepted counterexamples;
- more independently reproduced claims;
- lower cost per independently verified result;
- an honest final rejection when verification gates are not satisfied.

## Current limitations

- Early generations did not instrument every metric.
- Model availability and pricing can vary across runs.
- Research topics differ in intrinsic difficulty.
- Some evaluations require human or external expert review.
- No metric by itself establishes scientific validity.

These limitations are reported alongside all future comparisons.


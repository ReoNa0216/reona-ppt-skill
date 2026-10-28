# Validation Design For Idea Discussion

Load the relevant section when a proposed design depends on preliminary results, model prediction, transfer, or intervention discovery. These are general reasoning aids, not requirements for every deck.

## Preliminary evidence should select a design

For each consequential uncertainty, identify the smallest informative experiment or analysis and state how its possible outcomes change the plan. Distinguish a failed measurement or unavailable resource from evidence against the hypothesis.

When several components are proposed, consider whether each supports an independently useful question and whether their combination adds a testable interaction. A compact decision table can connect the observed result, retained question, and next experiment. Use controls that inform that decision; avoid adding assays whose outcome would not change it. Derive any numerical cutoff from the measurement and scientific purpose rather than inventing a universal threshold.

## Define a prediction task before drawing its timeline

Record the following in the existing design source:

- **Training information:** observations, labels, conditions, and time points available for fitting, including learned preprocessing and model selection.
- **Test input:** exactly what is supplied for the held-out prediction.
- **Target:** the future, intermediate, or new-condition quantity to predict, and its experimental/analysis unit.
- **Fixed versus updated elements:** parameters, representation, calibration, or condition information that remain fixed or may be re-estimated.
- **Validation:** independently observed targets, a credible simple baseline, aggregation, and metrics.

For temporal interpolation, bracket the held-out interval with observed training times and name the omitted targets. For extrapolation, put targets beyond the training range. For prediction from an observed state in a new condition, identify that state as an input and later observations as validation. These tasks test different capabilities; state which result supports which claim.

Keep held-out targets out of fitting and model selection. If a transductive design intentionally uses some target information, state what is available and evaluate the corresponding claim. Account for dependencies among repeated measurements, subjects, cultures, batches, or other nested observations when choosing the split and aggregating results.

When borrowing a published example, verify its training data, test input, predicted object, and validation. State the aspect being adapted and define the proposed task on its own terms. A shared application or diagram does not establish identical model behavior.

## Match the metric to the modeled object

Identify whether the model produces individual states, aggregate values, class proportions, trajectories, or a probability distribution. Choose primary metrics at that level. A dynamical model can propagate a collection or distribution of states when its initialization and formulation support that task; the method family name alone does not establish distribution modeling.

For aggregate predictions, define how individual observations become each independent experimental unit's summary. Preserve natural proportions when enriched or stratified sampling changes the measured composition. If correlation is useful, complement it with an error measure on a specified comparable scale when magnitude matters. For a treatment comparison, assess the relevant change as well as overall agreement.

Distributional metrics are appropriate when a population distribution is an explicit output and sampling supports its evaluation. Do not add them as a primary endpoint merely because the measurements are granular. Conversely, aggregate agreement cannot establish accurate heterogeneity.

## Connect model discovery to an experimental test

Explain what the model-derived candidate represents: an association, sensitivity, predicted response, or estimated effect under specified assumptions. Translate it into a measurable hypothesis and a feasible operation using relevant domain knowledge.

Connect candidate selection to observed labels or outcomes, reliable feature identity, model evidence, domain knowledge, and practical manipulation as relevant. Keep model predictions distinct from experimentally measured function. Define useful analyses for plausible observed structures, including continuous variation; a proposed branch or cluster shape is not a prerequisite for scientific value.

Choose the experiment according to the proposed claim. A candidate association, predictive benefit, and causal mechanism call for different comparisons. Add model complexity when the question and observations can support and evaluate the extra structure.

For a proposed intervention, connect the operation, expected measured change, functional outcome, and decision rule. Use controls or corroboration where they resolve a plausible competing explanation. Keep the resulting experiment focused on the claim under discussion.

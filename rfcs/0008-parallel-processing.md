# RFC-0000: Template

<dl>
  <dt>Author</dt>
  <dd>YOUR FULL NAME</dd>

  <dt>RFC pull request</dt>
  <dd><a href="URL">URL</a></dd>

  <dt>Obsoletes (if applicable)</dt>
  <dd><a href="./obsolete/0000-template.md">RFC-0000 Template</a></dd>

  <dt>Date of submission</dt>
  <dd>YYYY-MM-DD</dd>

  <dt>Date of approval</dt>
  <dd>YYYY-MM-DD</dd>

  <dt>Approved by</dt>
  <dd>First Person, Second Person</dd>
</dl>

## Contents

<!-- toc -->

## Summary

FIXME -- stub

A mechanism for parallel processing of a subgraph to fill historical data in a database faster (note: avoid talking about implementation)
   * (mention in abstract that this approach was successfully used for pancakeswap) Example implementation in golang: github link
   * How: 
       * by launching processes on indexer's infrastructure (cloud)
       * by generating files of intermediary steps accross different block ranges
       * when steps are done, they can feed a DB as fast as possible
       * when DB is filled, a normal real-time linear processing can start from last processed block and catch up
   * Example steps logic: ... (summation patterns, etc.)
   * Constraints for graph developers: (summation patterns, etc.)

## Goals & Motivation

What are the reasons for proposing the change? Why is it needed? What will the
benefits be and for whom?

## Urgency

How urgent is this proposal? How soon or late should or must an implementation
of this be available?

## Terminology

What terminology are we introducing? If this RFC is for a new feature, what is
this feature going to be referred to? The goal is that we all speak the same
language and use the same terms when talking about the change.

## Detailed Design

This is the main section of the RFC. What does the proposal include? What are
the proposed interfaces/APIs? How are different affected parties, such as users,
developers or node operators affected by the change and how are they going to
use it?

## Compatibility

Is this proposal backwards-compatible or is it a breaking change? If it is
breaking, how could this be mitigated (think: migrations, announcing ahead of
time like with hard forks, etc.)?

## Drawbacks and Risks

Why might we _not_ want to do this? What cost would implementing this proposal
incur? What risks would be introduced by going down this path?

## Alternatives

What other designs have been considered, if any? For what reasons have they not
been chosen? Are there workarounds that make this change less necessary?

## Open Questions

What are unresolved questions?

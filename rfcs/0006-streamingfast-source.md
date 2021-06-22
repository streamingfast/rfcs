# RFC-0000: Template

<dl>
  <dt>Author</dt>
  <dd>Stéphane Duchesneau</dd>

  <dt>RFC pull request</dt>
  <dd><a href="URL">URL</a></dd>

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

StreamingFast's firehose service is a protocol to provide on-demand block data over GRPC. The blocks are streamed from files and encoded in protobuf, with all traces and calls data necessary to match event and call triggers defined in a subgraph.

## Goals & Motivation

The objective of supporting StreamingFast's firehose service as an alternative data source is to improve the indexing performance and reduce the number of calls to Ethereum nodes.

With the popularity of chains with high block rate and density like Binance Smart Chain, the approach of polling nodes for data has shown to be very resource-intensive. Providing a way to get rich data pushed directly to the indexers, from a live stream or from cold storage addresses these challenges. 

The firehose service can be operated by indexers or other providers (FIXME: link to doc/repo, link to Network Subgraph proposal) 

## Urgency

FIXME

## Terminology

The feature proposed in this RFC is referred to as **StreamingFast block source**.
Other terms that are introduced in this RFC or are relevant when talking about it are listed below.

- **StreamingFast's firehose service** - a GRPC endpoint that provides instrumented blocks in protobuf format.
- **Protobuf** - a serialization mechanism, ref: https://developers.google.com/protocol-buffers
- **StreamingFast instrumented blocks** - protobuf-encoded blocks that contain traces and call data

## Detailed Design

FIXME

## Compatibility

This proposal adds a new source for blocks, it is backwards-compatible.

## Drawbacks and Risks

Reading instrumented blocks instead of querying RPC nodes could lead to a small number of producers or providers being directly responsible for the data found in multiple subgraphs. Note that this concern is also valid for lower-level RPC providers.
This could be mitigated by incentivizing the production of those instrumented blocks and making them available as a first-class subgraph.

## Alternatives

FIXME

## Open Questions

- Should we name those instrumented blocks in a more neutral way ?

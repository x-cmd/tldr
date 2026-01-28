# TLDR-Pages Repackaging and Release Target

This project aims to repackage and release [TLDR-Pages](https://github.com/tldr-pages/tldr) to optimize the experience for specific usage scenarios.

## Usage Scenarios

Assume the `tldr` module is used in the following scenarios:

1. **Limited network bandwidth**: Need to quickly download and consult command manuals
2. **Network environment in China**: Ensure normal accessibility within mainland China network environment

## Design Goals

Based on the above usage scenarios, we have established the following design goals:

1. **On-demand language pack downloads**: Separate packaging of each language pack, supporting on-demand downloads. Considering most users typically use only one language, this significantly reduces initial download size.
2. **Compressed packaging format**: Use `xz` format for compression packaging, further reducing download size by approximately 30%.
3. **Chinese mainland mirror hosting**: Host the packaged resources on [Gitee](https://gitee.com) to ensure fast and stable access for users in China.

## Implementation Approach

- Each language pack is packaged independently, allowing users to choose downloads as needed
- Use `xz` compression algorithm to maximize file size reduction while maintaining content integrity
- All resources are synchronized to Gitee mirrors for convenient acceleration

Through these optimizations, we aim to provide users with a lighter, faster, and more reliable `tldr` usage experience.
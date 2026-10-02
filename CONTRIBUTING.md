# Contributing to SDDFW

Thanks for helping shape SDDFW. Questions, real workflow examples, documentation
improvements, bug reports, and focused pull requests are welcome.

The framework is in early development. There is no installable framework release
yet. Keep documentation clear about what exists, what is illustrative, and what
is proposed.

## Where to contribute

- [sddfw](https://github.com/sddframework/sddfw): framework documentation and
  project direction. Use its [Discussions](https://github.com/sddframework/sddfw/discussions)
  for questions, workflow examples, comparisons, and feature ideas.
- [website](https://github.com/sddframework/website): the landing page. Report
  reproducible landing problems in that repository's issues.
- [.github](https://github.com/sddframework/.github): the organization profile
  and shared community files. Propose changes through pull requests; use the
  main repository for discussion.

Use issues for reproducible problems or focused changes. Before a substantial
implementation, agree on the problem and scope with the maintainer in a thread.

## Pull requests

1. Fork the relevant repository and create a branch for your change.
2. Keep the change focused. Explain the problem and the resulting behavior.
3. Update relevant documentation and describe the verification you performed.
4. Open a pull request and link the relevant issue or discussion, if one exists.

For the website, Node.js 22 or later is required. Run `pnpm check` and
`pnpm build`, then preview and inspect any changed behavior or layout. Follow
the website README for local development.

The framework and community repositories currently contain documentation and
configuration. Review links and rendered Markdown; there are no framework build
or runtime checks yet.

Do not claim checks that you did not run. State relevant limits and distinguish
local results from hosted or production evidence. Do not submit credentials or
other private information.

## License and authorship

Each official repository includes an MIT license. Contributions submitted for
inclusion must be under that repository's MIT license, unless a different
arrangement is explicitly agreed before submission.

Only contribute material that you have the right to submit. Keep any required
third-party copyright and license notices, and explain their origin. Review
AI-assisted contributions with the same care as other contributions: the person
submitting the change is responsible for its correctness and provenance.

Contributors retain copyright in their contributions. Submission does not
transfer copyright to the maintainer. This project does not require a separate
copyright-assignment agreement.

## Decisions and conduct

Follow the [code of conduct](CODE_OF_CONDUCT.md).
[@alfoncode](https://github.com/alfoncode) is the founder, organization owner,
and primary maintainer. See the framework's
[governance document](https://github.com/sddframework/sddfw/blob/main/GOVERNANCE.md)
for project decisions.

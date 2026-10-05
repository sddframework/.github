# Contributing to SDDFW

Thanks for helping shape SDDFW. Questions, real workflow examples, documentation
improvements, bug reports, and focused pull requests are welcome.

The framework is in early development. The v0.1 source preview includes a local
CLI, coding-agent workflow, Playwright UI/API acceptance checks, and a runnable
fullstack example. It is not published to the npm registry. Keep executable
features, the website’s illustrative report, and future adapters distinct.

## Where to contribute

- [sddfw](https://github.com/sddframework/sddfw): framework source, tests, specifications,
  documentation, and runnable examples. Use its [Discussions](https://github.com/sddframework/sddfw/discussions)
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

## Framework changes and checks

Use the [getting-started guide](https://github.com/sddframework/sddfw/blob/feat/v0.1-playwright/docs/getting-started.md)
to install the preview and the [architecture guide](https://github.com/sddframework/sddfw/blob/feat/v0.1-playwright/docs/architecture.md)
to understand its invariants. Requires Node.js 22 or later. From a framework
checkout, run:

```sh
npm ci
npm run check
npm test
npx playwright install chromium
npm run test:demo
npm run test:integration
npm pack --dry-run
```

Run checks appropriate to the change and include their results in the pull
request. CI on Ubuntu with Node.js 22 runs these gates, installing browser system
dependencies as needed. A configured workflow is not evidence that it passed;
wait for its actual result. Live local validation currently covers macOS.
Windows adapter shims have unit coverage; a live Windows workflow is not yet
verified.

For behavior changes, explain the scenario and add a meaningful regression test.
Preserve these acceptance invariants:

- Specifications require explicit review and approval; agents cannot approve.
- Tests are prepared and checked against a baseline before implementation.
- Implementation keeps the accepted tests frozen, including automatic repairs.
- Missing, skipped, expected-failure, flaky, or blocked checks cannot disappear
  behind a passing acceptance summary.
- Evidence identifies sources, configuration, environment, and declared mocks;
  source or specification changes invalidate its freshness.
- Initialization preserves existing project configuration, tests, and agent
  instructions.

Review AI-generated scenarios and assertions, not just test results. Demonstrate
that a regression check detects the relevant broken behavior when that adds
useful evidence. Do not relax a requirement or assertion to make a check pass.
Record any deliberately changed behavior in its specification and explain the
change in the pull request.

The [fullstack example](https://github.com/sddframework/sddfw/blob/feat/v0.1-playwright/examples/README.md)
contains real frontend/API checks, an isolated fixture, and a deliberate failure
exercise. Contributions can include clear scenarios, boundary cases, small
reproducible examples, and honest reports of adapter/environment limits.

For documentation-only or community-configuration changes, review links and
rendered Markdown. There is no application build in the `.github` repository.
Preview source links target `feat/v0.1-playwright` until it is merged; update
those links together when the public installation branch changes.

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
[governance document](https://github.com/sddframework/sddfw/blob/feat/v0.1-playwright/GOVERNANCE.md)
for project decisions.

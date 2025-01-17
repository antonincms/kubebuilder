# Security Policy

## Security Announcements

Join the [kubernetes-security-announce] group for security and vulnerability announcements related to the Kubernetes ecosystem.

You can also subscribe to an RSS feed of these announcements using [this link][kubernetes-security-announce-rss].

## Reporting a Vulnerability

Instructions for reporting a vulnerability can be found on the [Kubernetes Security and Disclosure Information] page.

## Supported Versions

Kubebuilder is tested against the latest three Kubernetes releases, in alignment with the [Kubernetes version and version skew support policy](https://kubernetes.io/docs/setup/release/version-skew-policy/).

However, each version is only tested with the dependencies used for its release. For detailed information, please refer to the [compatibility and support policy on GitHub][compatibility-policy].

## Release Policy

Kubebuilder maintains a policy of releasing updates for the latest CLI version (currently v4). Older versions (v1, v2, v3) are no longer supported, and no releases will be produced for them. It is recommended to ensure that any project scaffolded by Kubebuilder remains aligned with the latest release.

## Automated Vulnerability Scanning

Kubebuilder employs automated scanning via Dependabot and GitHub Actions within its CI/CD pipeline. This process detects vulnerabilities in dependencies and configurations, generating daily or weekly reports prioritized for the latest supported versions.

- **Dependabot Configuration**: You can review the setup in `.github/dependabot.yml`.
- **Security Checks**: Security checks are enabled in the Kubebuilder repository settings.
- **Code Scanning**: The `.github/workflows/codeql.yml` workflow scans the `master` and `book-v4` branches, which typically contain the latest release code. Other release branches may not be scanned.

## Production-Grade Security

Projects generated by Kubebuilder are designed for ease of development and are **not** configured with production-grade security settings. For example, default configurations do not enable cert-manager or perform proper certificate validation, which may not be suitable for production environments. Ensure that you make the necessary adjustments to security settings before releasing your solution for production.

[kubernetes-security-announce]: https://groups.google.com/forum/#!forum/kubernetes-security-announce
[kubernetes-security-announce-rss]: https://groups.google.com/forum/feed/kubernetes-security-announce/msgs/rss_v2_0.xml?num=50
[Kubernetes version and version skew support policy]: https://kubernetes.io/docs/setup/release/version-skew-policy/#supported-versions
[Kubernetes Security and Disclosure Information]: https://kubernetes.io/docs/reference/issues-security/security/#report-a-vulnerability
[compatibility-policy]: ./../README.md#versions-compatibility-and-supportability
[project-upgrade-assistant]: https://book.kubebuilder.io/reference/rescaffold
[testdata-directory]: https://github.com/kubernetes-sigs/kubebuilder/tree/master/testdata
[kubebuilder-releases]: https://github.com/kubernetes-sigs/kubebuilder/releases

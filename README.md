# DevSecOps CI/CD Pipeline

Professional-grade security-first CI/CD pipeline demonstrating modern DevSecOps practices.

## Pipeline Stages (6 Parallel Security Checks)

1. **Lint & Test** - ESLint + Jest with coverage
2. **CodeQL SAST** - GitHub-native static analysis
3. **Secret Scanning** - Gitleaks detects leaked credentials
4. **Dependency Scan** - Trivy finds CVEs in npm packages
5. **IaC Scan** - Checkov validates Dockerfile
6. **Container Build & Scan** - Docker build + Trivy image scan + SBOM generation

## Technologies

- **Code Quality**: ESLint, Jest
- **Security**: CodeQL, Gitleaks, Trivy, Checkov, Syft
- **CI/CD**: GitHub Actions
- **Containerization**: Docker (multi-stage)
- **Language**: Node.js 20 (Express)

## Key Features

✓ Parallel security scanning (fast feedback)
✓ Shift-left security (catch issues early)
✓ SBOM generation for compliance
✓ No hardcoded secrets in pipeline
✓ Multiple layers of defense (code, deps, container)
✓ Professional audit trail

## Running Locally

```bash
npm install
npm test
npm run lint
docker build -t devsecops-demo:local .
```

## Scanning

All scans run automatically on every push via GitHub Actions.

View results in:
- Actions tab: Full logs for each job
- Security tab: CodeQL findings
- Artifacts: SBOM (sbom.spdx.json)

## Portfolio Value

Demonstrates:
- Security-first mindset
- Tool integration (8 security tools)
- Automation at scale
- Compliance/supply-chain practices
- DevOps maturity

## License

MIT

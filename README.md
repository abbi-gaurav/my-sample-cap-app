# Overview

A sample CAP project with Helm chart

## References

- <https://pages.github.tools.sap/cap/docs/java/getting-started>

## Setup

- Set up the base CAP Java project with the following command:

```bash
cds init my-sample-cap-app --add java
```

- Navigate to the project directory:

```bash
cd my-sample-cap-app
```

- Add the bookshop sample model to the project:

```bash
 mvn com.sap.cds:cds-maven-plugin:add -Dfeature=TINY_SAMPLE
```

- Change starter bundle to `cds-starter-k8s` in [srv/pom.xml](srv/pom.xml)

## Deployment to Kyma

- <https://pages.github.tools.sap/cap/docs/guides/deployment/to-kyma>
- Prepare for production deployment:

```bash
cds add hana,xsuaa --for production
```

- Add Helm chart

```bash
cds add helm
```
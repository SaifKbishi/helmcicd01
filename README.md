This is a full CI/CD pipeline for packaging and publishing Helm charts.
My GitHub Action automatically packages the chart, updates a Helm repository hosted on GitHub Pages, and regenerates the repo index. 
Any commit to main instantly publishes a new chart version. 
This demonstrates automation, artifact versioning, and GitHub Pages hosting.

# **To test this Helm Repository**

On ANY machine:

```bash
helm repo add saifkbishi https://saifkbishi.github.io/helmcicd01
helm repo update
helm search repo saifkbishi
```

To install:

```bash
helm install myapp saifkbishi/helmcicd01
```
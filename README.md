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

Pull the chart:
```bash
helm pull saifkbishi/helmcicdtest01 --untar
```

Template rendering test (no cluster needed):
```bash
helm template test-release myrepo/helmcicdtest01
```

Install test (requires Kubernetes cluster):

```bash
helm install test-release myrepo/helmcicdtest01
```

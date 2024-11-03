Example for running the pipeline with a PipelineRun:

```yaml
apiVersion: tekton.dev/v1
kind: PipelineRun
metadata:
  generateName: read-repo-readme-
  namespace: tekton-examples
spec:
  pipelineRef:
    name: read-repo-readme
  params:
    - name: repo-url
      value: https://github.com/octocat/Hello-World.git
    - name: revision
      value: master
  workspaces:
    - name: shared-data
      volumeClaimTemplate:
        spec:
          accessModes:
            - ReadWriteOnce
          resources:
            requests:
              storage: 1Gi
```
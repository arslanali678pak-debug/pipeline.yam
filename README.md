# pipeline.yam

A Tekton `Pipeline` in `pipeline.yaml` (`node-pipeline`) for a Node.js app.
Steps, in order:

1. **clone** — clone the app repo (git-clone task)
2. **npminstall** — `npm install` (npm task)
3. **tests** — run the Jasmine tests (jasmine task)
4. **build** — `npm run build` (npm task)

Apply with:

```bash
kubectl apply -f pipeline.yaml
```

The `npm` and `jasmine` tasks come from the `tekton-tasks` repository.

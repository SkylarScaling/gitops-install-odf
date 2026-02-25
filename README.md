# gitops-install-odf
Deploy Open Data Foundation (ODF) to the OpenShift cluster via GitOps (ArgoCD).

**Note:** Ensure your ArgoCD Application has `Retry` enabled. There is typically a slight delay between ArgoCD creating 
the Operator `Subscription` and OLM making the `StorageCluster` CRDs available. Auto-retry ensures the CRs are applied 
successfully once the CRDs are ready.
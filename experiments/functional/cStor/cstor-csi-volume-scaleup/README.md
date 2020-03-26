## Experiment Metadata

| Type       | Description                                           | Storage      | Applications | K8s Platform |
| ---------- | ----------------------------------------------------- | ------------ | ------------ | ------------ |
| Functional | Scale up the cStor volume replica of cstor-csi volume | OpenBS cStor | Any          | Any          |

## Entry-Criteria

- K8s nodes should be ready.
- cStor CSPC should be created.
- Application should be deployed using with volume provisioned through CSI provisioner.
- CSPIs should be present for scaling up the volume replicas.

## Exit-Criteria

- Volume replica should be scaled up and rebuilt successfully.

## Procedure

- This functional test checks if the csi volume replicas can be scaled up.
- This litmusbook accepts the parameters in form of job environmental variables.
- This job patched the respective CVC with the unused pool names and thereby scales up the replicas 

## Litmusbook Environment Variables

| Parameters    | Description                                            |
| ------------- | ------------------------------------------------------ |
| APP_NAMESPACE | Namespace where application and volume is deployed.    |
| APP_PVC       | Name of PVC whose storage capacity has to be increased |
| APP_LABEL     | Label of application pod                               |
|               |                                                        |
|               |                                                        |
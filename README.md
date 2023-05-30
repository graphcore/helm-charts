## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add <alias> https://helm-charts.graphcore.ai/

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo <alias>` to 
see the charts.

To install the `ipu-operator` chart:

    helm install my-<chart-name> <alias>/ipu-operator

To uninstall the chart:

    helm delete my-<chart-name>

For further and more detailed information please refer to [Graphcore Kubernetes documentation](https://docs.graphcore.ai/projects/kubernetes-user-guide/en/latest/index.html).

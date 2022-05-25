## Usage

[Helm](https://helm.sh) must be installed to use the charts.  Please refer to
Helm's [documentation](https://helm.sh/docs) to get started.

Once Helm has been set up correctly, add the repo as follows:

    helm repo add <alias> https://graphcore.github.io/helm-charts

If you had already added this repo earlier, run `helm repo update` to retrieve
the latest versions of the packages.  You can then run `helm search repo <alias>` to 
see the charts.

To install the `ipu-operator` chart:

    helm install my-<chart-name> <alias>/ipu-operator

To uninstall the chart:

    helm delete my-<chart-name>

For IPU Operator to work properly IPUJobs CRD specfication is also required. It 
is attainable directly from Github releases or using the following command:

    curl -s https://api.github.com/repos/graphcore/helm-charts/releases/latest | grep -wo "https.*ipujobs.*yaml" | wget -qi -

To install the CRD:

    kubectl apply -f graphcore.ai_ipujobs_<version>.yaml


For further and more detailed information please refer to [Graphcore Kubernetes documentation](https://docs.graphcore.ai/projects/kubernetes-user-guide/en/latest/index.html).

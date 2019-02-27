# Helm charts for CORD

This repo contains the helm charts for use in the [CORD](https://opencord.org/)
and subsidiary projects.

Thes charts are published on: <https://charts.opencord.org/>

Please see <https://guide.opencord.org/charts/helm.html> for more complete
documentation.

## Changing charts

When you make changes to charts, please make sure of the following:

1. Make sure the chart passes a strict lint with `helm lint --strict
   <chartname>`.  The `scripts/helmlint.sh` will check all charts.

2. When you modify a chart, you must increase the version in `Chart.yaml`. You
   may also need to update other charts that depend on your chart.

# Two ONT/RG conf
1- for freeradius: user1 user has to be added
2- for rg2: user1 has to be added to /etc/wpa_supplicant/wpa_supplicant.conf (sed -i 's/user/user1/g' wpa_supplicant.conf #no vi installed)

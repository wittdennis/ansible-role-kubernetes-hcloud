# kubernetes_hcloud

Installs and manages the [Hetzner cloud-controller-manager](https://github.com/hetznercloud/hcloud-cloud-controller-manager) and [Hetzner csi-driver](https://github.com/hetznercloud/csi-driver) to ensure proper functioning of a kubernetes cluster on Hetzner cloud

## Requirements

- Helm

## Role Variables

```yaml
kubernetes_hcloud_controller_manager_chart_version: v1.19.0 # Version of the cloud-controller-manager to use
kubernetes_hcloud_csi_driver_chart_version: v2.7.0 # Version of the csi driver to user
kubernetes_hcloud_monitoring_enabled: true # Controls if monitoring for the cloud controller should be enabled
kubernetes_hcloud_networking_enabled: true # Controls if networking functionality for the cloud controller should be enabled
kubernetes_hcloud_volume_default_location: nbg1 # The default location for the storage driver
kubernetes_hcloud_cloud_provider_kubelet_extra_args_through_systemd_unit: false # Controls if the cloud provider should be set through a systemd unit file
```

## Dependencies

- kubernetes.core

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: wittdennis.kubernetes_hcloud }

## License

MIT

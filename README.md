# OpenRail DNS Records

![OpenRail Administrative Project](https://openrailassociation.org/badges/openrail-project-admin.svg)
[![Synchronise DNS records](https://github.com/OpenRailAssociation/openrail-dns/actions/workflows/sync-records.yaml/badge.svg)](https://github.com/OpenRailAssociation/openrail-dns/actions/workflows/sync-records.yaml)

In order to make it easy for OpenRail projects to manage the DNS records of their project's domains, they can use this repository to configure them as code.

The records are automatically synchronise upon changes on the `main` branch using the [INWX DNS Recordmaster](https://github.com/mxmehl/inwx-dns-recordmaster).

## Making changes

Maintainers of OpenRail Association projects can request changes to their domains' DNS records. Please create a pull request in order to do so. If your domain isn't managed by this repository yet, please approach the Technical Committee.

Requirements:

* For each domain, a separate file shall be present in [records](/records/), so please do not add your domain in another file.
* Make sure that the file has the same name as your domain, so a file managing the domain `example.com` should be named `example.com.yaml`.

After the changes have been approved and merged, the changes will be executed via GitHub actions which takes ~2 minutes. Please mote that DNS propagation can delay the effect on clients for typically 1 hours, in the worst case 24 hours.

If you have records that need to have a lower time-to-live (TTL), please check out the possible settings of [INWX DNS Recordmaster](https://github.com/mxmehl/inwx-dns-recordmaster).

## License

The content of this repository is licensed under the CC0-1.0 license.

---
layout: "oci"
page_title: "Oracle Cloud Infrastructure: oci_core_subnet"
sidebar_current: "docs-oci-datasource-core-subnet"
description: |-
  Provides details about a specific Subnet in Oracle Cloud Infrastructure Core service
---

# Data Source: oci_core_subnet
This data source provides details about a specific Subnet resource in Oracle Cloud Infrastructure Core service.

Gets the specified subnet's information.

## Example Usage

```hcl
data "oci_core_subnet" "test_subnet" {
	#Required
	subnet_id = "${oci_core_subnet.test_subnet.id}"
}
```

## Argument Reference

The following arguments are supported:

* `subnet_id` - (Required) The OCID of the subnet.


## Attributes Reference

The following attributes are exported:

* `availability_domain` - The subnet's Availability Domain.  Example: `Uocm:PHX-AD-1` 
* `cidr_block` - The subnet's CIDR block.  Example: `172.16.1.0/24` 
* `compartment_id` - The OCID of the compartment containing the subnet.
* `defined_tags` - Defined tags for this resource. Each key is predefined and scoped to a namespace. For more information, see [Resource Tags](https://docs.cloud.oracle.com/iaas/Content/General/Concepts/resourcetags.htm).  Example: `{"Operations.CostCenter": "42"}` 
* `dhcp_options_id` - The OCID of the set of DHCP options associated with the subnet. 
* `display_name` - A user-friendly name. Does not have to be unique, and it's changeable. Avoid entering confidential information. 
* `dns_label` - A DNS label for the subnet, used in conjunction with the VNIC's hostname and VCN's DNS label to form a fully qualified domain name (FQDN) for each VNIC within this subnet (for example, `bminstance-1.subnet123.vcn1.oraclevcn.com`). Must be an alphanumeric string that begins with a letter and is unique within the VCN. The value cannot be changed.

	The absence of this parameter means the Internet and VCN Resolver will not resolve hostnames of instances in this subnet.

	For more information, see [DNS in Your Virtual Cloud Network](https://docs.cloud.oracle.com/iaas/Content/Network/Concepts/dns.htm).

	Example: `subnet123` 
* `freeform_tags` - Free-form tags for this resource. Each tag is a simple key-value pair with no predefined name, type, or namespace. For more information, see [Resource Tags](https://docs.cloud.oracle.com/iaas/Content/General/Concepts/resourcetags.htm).  Example: `{"Department": "Finance"}` 
* `id` - The subnet's Oracle ID (OCID).
* `prohibit_public_ip_on_vnic` - Whether VNICs within this subnet can have public IP addresses. Defaults to false, which means VNICs created in this subnet will automatically be assigned public IP addresses unless specified otherwise during instance launch or VNIC creation (with the `assignPublicIp` flag in [CreateVnicDetails](https://docs.cloud.oracle.com/iaas/api/#/en/iaas/20160918/CreateVnicDetails/)). If `prohibitPublicIpOnVnic` is set to true, VNICs created in this subnet cannot have public IP addresses (that is, it's a private subnet).  Example: `true` 
* `route_table_id` - The OCID of the route table the subnet is using.
* `security_list_ids` - OCIDs for the security lists to use for VNICs in this subnet.
* `state` - The subnet's current state.
* `subnet_domain_name` - The subnet's domain name, which consists of the subnet's DNS label, the VCN's DNS label, and the `oraclevcn.com` domain.

	For more information, see [DNS in Your Virtual Cloud Network](https://docs.cloud.oracle.com/iaas/Content/Network/Concepts/dns.htm).

	Example: `subnet123.vcn1.oraclevcn.com` 
* `time_created` - The date and time the subnet was created, in the format defined by RFC3339.  Example: `2016-08-25T21:10:29.600Z` 
* `vcn_id` - The OCID of the VCN the subnet is in.
* `virtual_router_ip` - The IP address of the virtual router.  Example: `10.0.14.1` 
* `virtual_router_mac` - The MAC address of the virtual router.  Example: `00:00:17:B6:4D:DD` 


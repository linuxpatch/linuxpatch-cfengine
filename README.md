# CFEngine Policy: Install and Manage linuxpatch.com Script and Service

## Description

This CFEngine policy automates the process of downloading, executing, and cleaning up an installation script from [linuxpatch.com](https://linuxpatch.com). Additionally, it ensures that the `linuxpatch-agent` service is running and enabled at startup. The script is only executed if the file `/opt/linuxpatch/bin/linuxpatch` does not exist.

## Prerequisites

- CFEngine installed on the target hosts.
- Customer key for [linuxpatch.com](https://linuxpatch.com).

## Usage

1. **Create the Policy File**:

   Save the policy content into a file named `linuxpatch.cf`.

2. **Set up the LinuxPatch.com Key**:

   Open `linuxpatch.cf` and replace the `lp_key` variable with your actual LinuxPatch.com key:

   ```cfengine3
   "lp_key" string => "your_lp_key_here";
   ```

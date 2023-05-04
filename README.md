# srsRAN snap

srsRAN is a 4G software radio suite developed by [SRS](https://www.srs.io/).
See the [srsRAN project pages](https://www.srsran.com/) for information, guides
and project news. The srsRAN suite includes:
- srsUE - a full-stack SDR 4G UE application, with experimental 5G support
- srsENB - a full-stack SDR 4G eNodeB application, with experimental 5G support
- srsEPC - a light-weight 4G core network implementation with MME, HSS
  and S/P-GW

For application features, build instructions and user guides see the
[srsRAN documentation](https://docs.srsran.com/4g/en/latest/).

## Usage

Install the snap:

```bash
sudo snap install srsran
```

To simulate an eNodeB, an EPC or a User Equipment, run any of the following
commands:

```bash
srsran.srsenb <path to enb.conf>
srsran.srsue <path to ue.conf>
srsran.srsepc <path to epc.conf>
```

When paths to config files are not provided in the commands above, default
configs are used (ex.
[enb.conf.example](https://github.com/srsran/srsRAN/blob/master/srsenb/enb.conf.example)).
Custom config files and all files referred in them (ex. `user_db.csv`)
must be located in the user's home directory.

Depending on the RF Device Driver used, you will need to modify the following
configuration in ue.conf and enb.conf:
- device_name: Device driver family
- device_args: Arguments for the device driver. Options are "auto" or any string.
This snap uses ZMQ as default.

By default srsran-snap apps will log to `/var/snap/srsran/current/`.

## Build

To build this snap, you will need a machine with the following requirements:
- Processor: x86-64 dual-core processor
- OS: Ubuntu >= 20.04
- Memory: 8GB RAM

Run
```bash
export SNAPCRAFT_BUILD_ENVIRONMENT_MEMORY=4G
snapcraft
```

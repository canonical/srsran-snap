# srsRAN snap

srsRAN is a 4G/5G software radio suite developed by [SRS](https://www.srs.io/). See the [srsRAN project pages](https://www.srsran.com/) for information, guides and project news. The srsRAN suite includes:
- srsUE - a full-stack SDR 4G/5G UE application
- srsENB - a full-stack SDR 4G/5G e(g)NodeB application
- srsEPC - a light-weight 4G core network implementation with MME, HSS and S/P-GW

For application features, build instructions and user guides see the [srsRAN documentation](https://docs.srsran.com/en/latest/).

## Usage

Install the snap:

```bash
sudo snap install srsran
```

To simulate an eNodeB, an EPC or a User Equipment, run any of the following commands:

```bash
srsran.srsenb <path to enb.conf>
srsran.srsue <path to ue.conf>
srsran.srsepc <path to epc.conf> 
```

When paths to config files are not provided in the commands above, default configs are used (ex. [enb.conf.example](https://github.com/srsran/srsRAN/blob/master/srsenb/enb.conf.example)).
Custom config files and all files referred in them (ex. `user_db.csv`) must be located in the user's home directory.


## Build

To build this snap, you will need a machine with the following requirements:
- Processor: x86-64 dual-core processor
- OS: Ubuntu20-04
- Memory: 4GB RAM

Run
```bash
snapcraft --destructive-mode
```
> :warning: Building the snap using --destructive mode could contaminate the host build environment.

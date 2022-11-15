# srsRAN snap

srsRAN is a 4G/5G software radio suite developed by [SRS](https://www.srs.io/). See the [srsRAN project pages](https://www.srsran.com/) for information, guides and project news. The srsRAN suite includes:
- srsUE - a full-stack SDR 4G/5G UE application
- srsENB - a full-stack SDR 4G/5G e(g)NodeB application
- srsEPC - a light-weight 4G core network implementation with MME, HSS and S/P-GW

For application features, build instructions and user guides see the [srsRAN documentation](https://docs.srsran.com/en/latest/).

## Usage

### Install

```bash
sudo snap install srsran
```

### Run the EPC

```bash
sudo srsran.srsepc <path to epc.conf>
```

`epc.conf` and all the files referred in it (ex. `user_db.csv`) must be located in the user's home 
directory.

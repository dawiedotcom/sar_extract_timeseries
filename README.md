# SAR Time Series Extractor

A Jupyter Notebook to extract a time series from a set of GeoTiff files.

## How to run

### Setup the Python environment

Clone the repository:
```bash
git clone https://git.ecdf.ed.ac.uk/ddekler/sar_extract_timeseries
cd sar_extract_timeseries
```

Create a new virtual environment
```bash
virtualenv venv
. venv/bin/activate
pip install -r requirements.txt
```

In future sessions, only the following will be necessary
```bash
. venv/bin/activate
```

### Download the data

This notebook uses the LiCSAR interferometry products [1]. To download the needed GeoTiff files, run the following:
```bash
cd SAR_amplitudes
wget --no-clobber --quiet --show-progress --input-file=file_url_list
md5sum -c file_url_list.md5sum

cd ../InSAR_coherence
wget --no-clobber --quiet --show-progress --input-file=file_url_list
md5sum -c file_url_list.md5sum
```
If `md5sum` reports differences in files, delete the corrupted files and rerun the `wget` command.

### Run the notebook

Run the Jupyter notebook:
```bash
jupyter notebook
```

## References

[1] Lazecky, M.; Maghsoudi, Y. (2022): LiCSAR interferometry products. NERC EDS Centre for Environmental Data Analysis, 2024/08/05. [https://catalogue.ceda.ac.uk/uuid/52cda2e0e6c04272ae15ac836c1e8493](https://catalogue.ceda.ac.uk/uuid/52cda2e0e6c04272ae15ac836c1e8493)

## License

See [LICENCE](LICENCE).

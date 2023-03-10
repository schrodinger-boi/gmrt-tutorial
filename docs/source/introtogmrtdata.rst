Introduction to the GMRT data
==============================

GMRT can record data in continuum, spectral line and pulsar/beamformed (phased/incoherent array, 
primarily to observe pulsars/transients) modes.

Continuum and spectral line data
---------------------------------

These are data typically recorded with the full array and contain visibilities. 
The raw data are in the "lta" format. The continuum and spectral line data will 
both be in the same format. The data in lta format is converted to FITS format 
using the in-house codes *listscan* and *gvfits*. The FITS file is further converted 
into the measurement set (ms) format in order to analyse the data using CASA.

The GMRT online archive (GOA) allows you to download data in FITS and lta formats. 
Thus if you downloaded your data in FITS format you can skip the step of converting 
the format from lta to FITS.

The files downloaded from GOA having 'gsb' in their filenames are the data recorded with 
the narrow band backend which was called the GMRT Software Backend (GSB). The files with 'GWB' 
in their names are the data recorded using the GMRT Wideband Backend (GWB) which is the 
new wideband system (Upgraded GMRT).


Pulsar/Beam data
-----------------

These are data typically recorded after adding the signals from multiple dishes or
the full array, either incoherently (i.e., the incoherent array mode, IA) or
coherently (i.e., the phased-array mode, PA). The native data are in filterbank
format, i.e., a spectrum with the specified number of frequency channel is recorded
for every time sample, for a specified sampling time. The data recorded by GSB and
GWB are of same format.

The native beam (PA/IA) data from GMRT need to be converted to SIGPROC filterbank
format, after which it can be used with softwares such as **SIGPROC**, **PRESTO**,
**DSPSR**, etc. The format conversion can be performed using the ``filterbank``
command from **SIGPROC**. Alternatively, one can use the ``rficlean`` command from
**RFIClean** to do the format conversion, in addition to mitigating some radio
frequency interference (RFI). If desired, ``rficlean`` can also be used only for
the format conversion, i.e., without performing any RFI excision.


## MassiVE Conversion

MassIVE automatically can convert public datasets. You simply can click the **Convert Spectra** button on the top of each dataset page. Once converted, these files are listed in the ccms_peak folder for each dataset. 

### Conversion Rules

We use the following logic to determine what files to convert:

1. Find all mzML, mzXML, and MGF files in the raw collection, and copy to ccms_peak
2. If the above does not exist, we find all Thermo and Sciex vendor files in the raw collection and convert with MSConvert to mzML and copy to ccms_peak
3. If the above does not exist, we find all mzML, mzXML, and MGF files in the peak collection and copy them to ccms_peak
4. If the above does not exist, create an empty ccms_peak

### Supported Conversion Source Files

We currently support conversion from the following formats:

1. mzML
2. mzXML
3. MGF
4. Thermo .raw
5. Sciex .wiff


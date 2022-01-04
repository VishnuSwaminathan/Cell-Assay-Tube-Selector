# Cell-Assay-Tube-Selector
Small script written by myself as part of an interview take-home assignment.
----------------------------------------------------------------------------
Given a list of samples, each sample has multiple tubes labeled with tube id and the volume. I need to select tubes of these samples to perform assays. Each assay has a required volume, and the selected tube must have enough volume to complete the assay, e.g. if an assay required 100 ul, I need to select tubes >= 100 ul. I have written a function to take in sample-tube-volume dataframe and assay volume dictionary to select tubes. This should return a nested dictionary with sample id and assay as key and the selected tube id as value. The tube selection must meet the following requirements:

1. One tube for one assay, don’t split one tube for two or more assay.
2. 
3. Prioritize lower volume assay. E.g., if I have two assays that require 100 ul and 500 ul and I
only have one 600 ul tube, I pick the tube for the 100 ul assay and the 500 ul assay should return
‘no tube’.

3. Minimize the waste of volume when the first two conditions are met. E.g., if I have an assay
that requires 100 ul and I have 100 ul and 200 ul tubes, I pick the 100 ul tube.

4. If there are multiple tubes that meet requirements, I pick only one of them.


                AAindex: Amino Acid Index Database

                   Release 9.1, Aug 2006

            http://www.genome.jp/aaindex

Introduction
============

An amino acid index is a set of 20 numerical values representing any
of the different physicochemical and biological properties of amino
acids.  The AAindex1 section of the Amino Acid Index Database is a
collection of published indices together with the result of cluster
analysis using the correlation coefficient as the distance between
two indices.  This section currently contains 544 indices.

Another important feature of amino acids that can be represented
numerically is the similarity between amino acids.  Thus, a similarity
matrix, also called a mutation matrix, is a set of 210 numerical values,
20 diagonal and 20x19/2 off-diagonal elements, used for sequence
alignments and similarity searches.  The AAindex2 section of the Amino
Acid Index Database is a collection of published amino acid mutation
matrices together with the result of cluster analysis.  This section
currently contains 94 matrices.


Important Changes
=================

[release 9.0]

New database AAindex3 for contact potential matrices are added.

[release 6.0]

Since AAindex release 6.0, data format of AAindex2 had changed.
The M field has been newly introduced instead of the I field.
Actual data format of the M field is shown in the example below.


References
==========

Please cite the following references when making use of the database:

    Kawashima, S. and Kanehisa, M.; AAindex: amino acid index
       database. Nucleic Acids Res. 28, 374 (2000).

    Tomii, K. and Kanehisa, M.;  Analysis of amino acid indices and
       mutation matrices for sequence comparison and structure
       prediction of proteins.  Protein Eng. 9, 27-36 (1996).

    Nakai, K., Kidera, A., and Kanehisa, M.;  Cluster analysis of
       amino acid indices for prediction of protein structure and
       function.  Protein Eng. 2, 93-100 (1988)


Correspondence
==============

    Shuichi Kawashima
    Laboratory of Genome Database
    Human Genome Center, Institute of Medical Science,
    University of Tokyo, Japan
    4-6-1 Shirokanedai, Minato-ku, Tokyo 108-8639 JAPAN
    E-mail: shuichi@hgc.jp

                                               Last update: 2005/06/01


(Data Format of AAindex1)
```
************************************************************************
*                                                                      *
* Each entry has the following format.                                 *
*                                                                      *
* H Accession number                                                   *
* D Data description                                                   *
* R LITDB entry number                                                 *
* A Author(s)                                                          *
* T Title of the article                                               *
* J Journal reference                                                  *
* * Comment or missing                                                 *
* C Accession numbers of similar entries with the correlation          *
*   coefficients of 0.8 (-0.8) or more (less).                         *
*   Notice: The correlation coefficient is calculated with zeros       *
*   filled for missing values.                                         *
* I Amino acid index data in the following order                       *
*   Ala    Arg    Asn    Asp    Cys    Gln    Glu    Gly    His    Ile *
*   Leu    Lys    Met    Phe    Pro    Ser    Thr    Trp    Tyr    Val *
* //                                                                   *
************************************************************************
```

(Data Format of AAindex2)
```
************************************************************************
*                                                                      *
* Each entry has the following format.                                 *
*                                                                      *
* H Accession number                                                   *
* D Data description                                                   *
* R LITDB entry number                                                 *
* A Author(s)                                                          *
* T Title of the article                                               *
* J Journal reference                                                  *
* * Comment or missing                                                 *
* M rows = ARNDCQEGHILKMFPSTWYV, cols = ARNDCQEGHILKMFPSTWYV           *
*   AA                                                                 *
*   AR RR                                                              *
*   AN RN NN                                                           *
*   AD RD ND DD                                                        *
*   AC RC NC DC CC                                                     *
*   AQ RQ NQ DQ CQ QQ                                                  *
*   AE RE NE DE CE QE EE                                               *
*   AG RG NG DG CG QG EG GG                                            *
*   AH RH NH DH CH QH EH GH HH                                         *
*   AI RI NI DI CI QI EI GI HI II                                      *
*   AL RL NL DL CL QL EL GL HL IL LL                                   *
*   AK RK NK DK CK QK EK GK HK IK LK KK                                *
*   AM RM NM DM CM QM EM GM HM IM LM KM MM                             *
*   AF RF NF DF CF QF EF GF HF IF LF KF MF FF                          *
*   AP RP NP DP CP QP EP GP HP IP LP KP MP FP PP                       *
*   AS RS NS DS CS QS ES GS HS IS LS KS MS FS PS SS                    *
*   AT RT NT DT CT QT ET GT HT IT LT KT MT FT PT ST TT                 *
*   AW RW NW DW CW QW EW GW HW IW LW KW MW FW PW SW TW WW              *
*   AY RY NY DY CY QY EY GY HY IY LY KY MY FY PY SY TY WY YY           *
*   AV RV NV DV CV QV EV GV HV IV LV KV MV FV PV SV TV WV YV VV        *
* //                                                                   *
************************************************************************
```

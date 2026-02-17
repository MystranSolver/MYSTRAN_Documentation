# Confidence List

For version with commit ae40b55, 2026-02-17

* ✅️: Good enough to recommend people use.
    * All its options tested with non-default values and work correctly as far as we know.
    * Interactions with other features might still have known bugs which are listed under those other features.
* ❌: Known to be broken
* Neither: Unknown


## Executive control

|Statement |Describer|OK|
|----------|--------|---|
|ID
|IN4
|APP
|CHKPNT
|DEBUG
|OUTPUT4
|PARTN
|RESTART
|SOL
|          |31      |
|          |101     |✅️
|          |103     |✅️
|          |104     |
|          |105     |✅️
|TIME
|CEND      |        |✅️

## Case control

|Command  |Describer|SOL 101|SOL 103|SOL 105|Bug details|
|----------|--------|:-----:|:-----:|:-----:|-----------|
|ACCELERATION
|BEGIN BULK|        |✅101  |✅103  |✅105  |
|DISPLACEMENT
|          |PRINT
|          |PLOT
|          |ALL     |✅101  |✅103  |✅105  |
|          |n
|          |NONE
|ECHO
|ELDATA
|ENFORCED
|FORCE
|          |PRINT
|          |PLOT
|          |CORNER  |✅️101  |N/A
|          |ALL     |✅️101  |N/A
|          |n
|          |NONE
|GPFORCES
|LABEL
|LOAD      |        |✅️101  |N/A    |✅105  |
|MEFFMASS  |        |       |❌103  |       |[#189](https://github.com/MYSTRANsolver/MYSTRAN/issues/189) [#188](https://github.com/MYSTRANsolver/MYSTRAN/issues/188)|
|METHOD    |        |       |✅️103  |✅105  |
|MPC       |        |✅️101  |✅️103  |✅105  |
|MPCFORCES
|          |PRINT
|          |PLOT
|          |ALL     |✅️101
|          |n
|          |NONE
|MPFACTOR  |        |       |❌103  |       |[#189](https://github.com/MYSTRANsolver/MYSTRAN/issues/189)|
|OLOAD
|SET
|SPC       |        |✅101  |✅103  |✅105  |
|SPCFORCES
|          |PRINT
|          |PLOT
|          |ALL     |✅️101
|          |n
|          |NONE
|STRAIN
|          |CENTER
|          |CORNER  |✅️101
|          |PRINT
|          |PLOT
|          |ALL     |✅️101
|          |n
|          |NONE
|          |VONMISES
|          |MAXS
|          |SHEAR
|STRESS    |        |❌101  |       |       |[#148](https://github.com/MYSTRANsolver/MYSTRAN/issues/148)|
|          |CENTER
|          |CORNER  |✅️101
|          |PRINT
|          |PLOT
|          |ALL     |✅️101
|          |n
|          |NONE
|          |VONMISES
|          |MAXS
|          |SHEAR
|SUBCASE
|SUBTITLE
|TEMPERATURE|       |✅️101  |N/A    |✅105  |
|TITLE
|VECTOR


## Bulk data

|Entry name|Field   |Value   |SOL 101|SOL 103|SOL 105|Bug details|
|----------|--------|--------|:-----:|:-----:|:-----:|-----------|
|ASET
|ASET1
|BAROR
|CBAR      |        |        |       |       |❌105  |[#120](https://github.com/MYSTRANsolver/MYSTRAN/issues/120) [#130](https://github.com/MYSTRANsolver/MYSTRAN/issues/130)
|          |EID     |        |✅101  |✅103  |✅️105
|          |PID     |        |✅101  |✅103  |✅️105
|          |GA      |        |✅101  |✅103  |✅️105
|          |GB      |        |✅101  |✅103  |✅️105
|          |G0
|          |V1-V3   |        |✅101  |✅103  |✅️105
|          |PA
|          |        |DOFs 1-3
|          |        |DOFs 4-6|       |✅103  |
|          |PB
|          |        |DOFs 1-3
|          |        |DOFs 4-6|       |✅103  |
|          |W1A-W3B
|CBUSH
|          |EID     |        |✅️101
|          |PID     |        |✅️101
|          |GA      |        |✅️101
|          |GB      |        |✅️101
|          |V1-V3
|          |CID
|          |S
|          |OCID
|          |S1-S3
|CELAS
|CELAS2
|CELAS3
|CELAS4
|CHEXA     |        |        |✅️101
|          |EID     |        |✅101  |✅103  |
|          |PID     |        |✅101  |✅103  |
|          |G1-G8   |        |✅101  |✅103  |
|          |G9-G20  |        |✅️101
|CMASS1
|CMASS2
|CMASS3
|CMASS4
|CONM2
|          |EID     |        |✅101  |✅103  |
|          |G       |        |✅101  |✅103  |
|          |CID 
|          |M       |        |✅101  |✅103  |
|          |X1-X3
|          |I11-I33
|CONROD
|CORD1C
|CORD1R
|CORD1S
|CORD2C
|CORD2R
|          |CID     |        |✅️101  |       |✅️105
|          |RID
|          |A1-A3
|          |B1-B3   |        |✅️101  |       |✅️105
|          |C1-C3   |        |✅️101  |       |✅️105
|CORD2S
|CPENTA    |        |        |✅️101
|          |EID     |        |✅️101
|          |PID     |        |✅️101
|          |G1-G15  |        |✅️101
|CQUAD4
|          |EID     |        |✅101  |✅103  |✅️105
|          |PID     |        |✅101  |✅103  |✅️105
|          |G1-G4   |        |✅101  |✅103  |✅️105
|          |THETA   |        |✅️101  |       |✅️105
|          |MCID    |        |✅️101
|          |ZOFFS
|CQUAD8    |        |        |       |❌103  |❌105  |
|          |EID     |        |✅️101  |❌103  |❌105  |
|          |PID     |        |✅️101  |❌103  |❌105  |
|          |G1-G8   |        |✅️101  |❌103  |❌105  |
|          |T1-T4   |        |       |❌103  |❌105  |
|          |MCID    |        |       |❌103  |❌105  |
|CROD      |        |        |✅️101
|          |EID     |        |✅️101
|          |PID     |        |✅️101
|          |G1-G2   |        |✅️101
|CSHEAR
|CTETRA    |        |        |✅️101
|          |EID     |        |✅️101
|          |PID     |        |✅️101
|          |G1-G10  |        |✅️101
|CTRIA3
|          |EID     |        |✅️101  |       |✅️105
|          |PID     |        |✅️101  |       |✅️105
|          |G1-G3   |        |✅️101  |       |✅️105
|          |THETA   |        |✅️101
|          |MCID    |        |✅️101
|          |ZOFFS
|CUSERIN
|DEBUG
|EIGR
|EIGRL
|          |SID     |        |N/A    |✅️103  |✅️105
|          |F1      |        |N/A
|          |F2      |        |N/A
|          |N       |        |N/A    |✅️103  |✅️105
|          |MSGLVL  |        |N/A
|          |NCVFACL |        |N/A    |✅️103  |✅️105
|          |SIGMA   |        |N/A
|          |NORM    |        |N/A
|FORCE
|          |SID     |        |✅101  |N/A    |✅️105
|          |GID     |        |✅️101  |N/A    |✅️105
|          |CID     |        |       |N/A    |
|          |F       |        |✅️101  |N/A    |✅️105
|          |N1-N3   |        |✅️101  |N/A    |✅️105
|GRAV      |        |        |❌101  |       |      |[#150](https://github.com/MYSTRANsolver/MYSTRAN/issues/150)
|          |SID     |        |✅️101  |N/A    |
|          |CID     |        |       |N/A    |
|          |A       |        |✅️101  |N/A    |
|          |N1-N3   |        |✅️101  |N/A    |
|GRDSET
|GRID
|          |GID     |        |✅101  |✅103  |✅️105
|          |CID1
|          |X1-X3   |        |✅101  |✅103  |✅️105
|          |CID2    |        |✅️101  |       |✅️105
|          |PSPC
|LOAD
|MAT1
|          |MID     |        |✅101  |✅103  |✅️105
|          |E       |        |✅101  |✅103  |✅️105
|          |G       |        |✅101  |✅103  |✅️105
|          |NU      |        |✅️101  |       |✅️105
|          |RHO     |        |✅101  |✅103  |
|          |ALPHA   |        |✅️101  |N/A    |✅️105
|          |TREF    |        |✅️101  |N/A    |✅️105
|          |GE
|          |TA
|          |CA
|          |SA
|MAT2
|          |MID     |        |       |       |✅️105
|          |G11-G33 |        |       |       |✅️105
|          |RHO     |
|          |A1-A3   |
|          |TREF    |
|          |GE      |
|          |ST      |
|          |SC      |
|          |SS      |
|MAT8
|          |MID     |        |✅️101  |       |✅️105
|          |E1      |        |✅️101  |       |✅️105
|          |E2      |        |✅️101  |       |✅️105
|          |NU12    |        |✅️101
|          |G12     |        |✅️101  |       |✅️105
|          |G1Z     |        |✅️101  |       |✅️105
|          |G2Z     |        |✅️101  |       |✅️105
|          |RHO     |        |✅️101
|          |A1      |        |✅️101
|          |A2      |        |✅️101
|          |TREF    |        |✅️101
|          |Xt,Xc,Yt,Yc
|          |S
|          |GE
|          |F12
|          |STRN
|MAT9
|          |MID     |        |✅️101
|          |G11-G66
|          |     |orthotropic|✅️101
|          |        |other   |
|          |RHO
|          |A1-A3   |        |✅️101
|          |A4-A6
|          |TREF    |        |✅️101
|          |GE
|MOMENT
|          |SID     |        |✅️101  |N/A    |
|          |GID     |        |✅️101  |N/A    |
|          |CID     |        |       |N/A    |
|          |M       |        |✅️101  |N/A    |
|          |N1-N3   |        |✅️101  |N/A    |
|MPC       |        |        |✅️101  |✅️103  |✅105  |
|MPCADD
|OMIT
|OMIT1
|PARAM     |Separate table
|PARVEC
|PARVEC1
|PBAR      |        |
|          |PID     |        |✅101  |✅103  |✅105  |
|          |MID     |        |✅101  |✅103  |✅105  |
|          |A       |        |✅101  |✅103  |✅105  |
|          |I1      |        |✅101  |✅103  |✅105  |
|          |I2      |        |✅101  |✅103  |✅105  |
|          |J       |        |✅101  |✅103  |
|          |MPL
|          |Y1-Z4
|          |K1,K2
|          |I12
|          |CT
|PBARL
|          |PID     |        |✅️101
|          |MID     |        |✅️101
|          |TYPE
|          |        |CHAN    |✅️101
|          |        |T       |✅️101
|          |        |I1      |✅️101
|          |        |BAR     |✅️101
|          |        |BOX     |✅️101
|          |        |ROD     |✅️101
|          |        |TUBE    |✅️101
|          |        |other
|          |DIM1-DIM4|       |✅️101
|          |DIM5-DIM9
|          |NSM
|PBUSH
|          |PID     |        |✅️101
|          |"K"     |        |✅️101
|          |K1      |        |✅️101
|          |K2-K6
|          |"RCV"
|          |SA
|          |ST
|          |EA
|          |ET
|PCOMP     |        |        |      |      |       |Not for CQUAD8
|          |PID     |        |✅️101 |      |✅105  |
|          |Z0      |        |
|          |NSM     |        |
|          |SB      |        |
|          |FT      |        |
|          |TREF    |        |
|          |GE      |        |
|          |LAM     |        |      |      |       |
|          |        |NONSYM  |❌️101 |      |❌105  |CTRIA3 bug [#104](https://github.com/MYSTRANsolver/MYSTRAN/issues/104)
|          |        |SYM     |✅️101 |      |✅105  |
|          |MIDi    |        |✅️101 |      |✅105  |
|          |Ti      |        |✅️101 |      |✅105  |
|          |THETAi  |        |✅️101 |      |✅105  |
|          |SOUTi   |        |      |      |       |
|PCOMP1
|PELAS
|PLOAD2
|          |SID     |        |✅️101  |N/A    |
|          |P       |        |✅️101  |N/A    |
|          |EID1    |        |✅️101  |N/A    |
|          |EID2,...|        |       |N/A    |
|PLOAD4    |        |        |❌101  |N/A    |       |[#151](https://github.com/MYSTRANsolver/MYSTRAN/issues/151) [#106](https://github.com/MYSTRANsolver/MYSTRAN/issues/196)
|PLOTEL
|PROD
|          |PID     |        |✅️101
|          |MID     |        |✅️101
|          |A       |        |✅️101
|          |J
|          |C
|          |MPL
|PSHEAR
|PSHELL    |        |
|          |PID     |        |✅101  |✅103  |✅105  |
|          |MID1    |        |✅101  |✅103  |✅105  |
|          |TM      |        |✅101  |✅103  |✅105  |
|          |MID2    |        |✅101  |       |✅105  |
|          |12I/TM**3|       |
|          |MID3    |        |
|          |        |nonzero |✅101  |
|          |        |blank/0 |❌101  |❌103  |❌105  |[#170](https://github.com/MYSTRANsolver/MYSTRAN/issues/170)
|          |TS/TM   |        |       |        |       |
|          |MPA     |        |       |        |       |
|          |Z1      |        |       |        |       |
|          |Z2      |        |       |        |       |
|PSOLID    |        |        |✅️101
|          |PID     |        |✅101  |✅103  |
|          |MID     |        |✅101  |✅103  |
|          |CID     |        |✅️101  |
|          |IN      |        |✅101  |✅103  |
|          |ISOP    |        |✅101  |✅103  |
|PUSERIN
|RBE2      |        |        |✅101  |✅103  |
|          |EID     |        |✅101  |✅103  |
|          |GN      |        |✅101  |✅103  |
|          |CM      |        |✅101  |✅103  |
|          |GM1,... |        |✅101  |✅103  |
|RBE3
|          |EID     |        |✅101  |✅103  |
|          |REFGRID |        |✅101  |✅103  |
|          |REFC    |        |✅101  |✅103  |
|          |WTi     |        |✅101  |✅103  |
|          |Ci
|          |        |123     |✅101  |✅103  |
|          |        |456
|          |Gi,j    |        |✅101  |✅103  |
|RFORCE
|RSPLINE
|SEQGP
|SLOAD
|SPC       |        |        |✅101  |✅103  |
|          |SID     |        |✅101  |✅103  |✅105
|          |Gi      |        |✅101  |✅103  |✅105
|          |Ci      |        |✅101  |✅103  |✅105
|          |Di      |        |✅101  |✅103  |
|          |        |0.0     |✅101  |✅103  |✅105
|          |        |other   |✅101  |N/A
|SPC1
|SPCADD
|SPOINT    |
|          |ID1-ID8 |        |✅101  |       |
|          |ID9+    |        |❌101  |       |       |[#193](https://github.com/MYSTRANsolver/MYSTRAN/issues/193)
|SUPORT
|TEMP      |        |        |✅101  |N/A    |✅105
|          |SID     |        |✅101  |N/A    |✅105
|          |Gi      |        |✅101  |N/A    |✅105
|          |Ti      |        |✅101  |N/A    |✅105
|TEMPD
|TEMPP1
|TEMPRB
|USET
|USET1

End of bulk data section entries

## PARAM

|Parameter |Field           |Value   |OK |Bug details|
|----------|----------------|--------|---|-----------|
|AUTOSPC   |
|          |3 (value)       |        |✅
|          |4 (AUTOSPC_RAT) |        |
|          |5 (AUTOSPC_NSET)|        |
|          |6 (AUTOSPC_INFO)|        |
|          |7 (AUTOSPC_SPCF)|        |
|BAILOUT   |                |        |❌ |Sparse solver is tolerant of matrices where it should bail out.
|K6ROT     |3               |        |❌ |Spring connects to ground instead of adjacent grid points.
|MAXRATIO  |
|QUAD4TYP  |
|          |3               |MIN4    |   |See manual for capabilities and limitations
|          |3               |MITC4+  |   |See manual for capabilities and limitations
|STR_CID   |3               |        |❌ |Doesn't work for shells.
|WTMASS    |
|other     |



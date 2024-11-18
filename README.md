# Ames House Price Prediction API

### Gustavo Barroso & Henrique Mayor

## Overview

The Ames House Price Prediction API is a Flask-based service that predicts house sale prices based on various property features. Deployed on Railway, the API is publicly accessible and ready to use.

## API Endpoint

### POST `/prever`

- **URL:** `https://web-production-095d9.up.railway.app/prever`
- **Method:** `POST`
- **Headers:** `Content-Type: application/json`
- **Body:** JSON object containing all required property features.

## Example Request

### Sample JSON Payload

```json
{
"Lot.Frontage": 141.0, "Lot.Area": 31770.0, "Lot.Shape": 1, "Land.Slope": 0, "Overall.Qual": 5, "Overall.Cond": 4, "Mas.Vnr.Area": 112.0, "Exter.Qual": 2, "Exter.Cond": 2, "BsmtFin.SF.1": 639.0, "BsmtFin.SF.2": 0.0, "Bsmt.Unf.SF": 441.0, "Total.Bsmt.SF": 1080.0, "Heating.QC": 3, "Electrical": 0, "X1st.Flr.SF": 1656.0, "X2nd.Flr.SF": 0.0, "Low.Qual.Fin.SF": 0.0, "Gr.Liv.Area": 1656.0, "Bsmt.Full.Bath": 1.0, "Bsmt.Half.Bath": 0.0, "Full.Bath": 1.0, "Half.Bath": 0.0, "Bedroom.AbvGr": 3.0, "Kitchen.AbvGr": 1.0, "Kitchen.Qual": 2, "TotRms.AbvGrd": 7.0, "Functional": 0, "Fireplaces": 2.0, "Garage.Cars": 2.0, "Garage.Area": 528.0, "Paved.Drive": 1, "Wood.Deck.SF": 210.0, "Open.Porch.SF": 62.0, "Enclosed.Porch": 0.0, "X3Ssn.Porch": 0.0, "Screen.Porch": 0.0, "Pool.Area": 0.0, "Fence": 4, "Misc.Val": 0.0, "Mo.Sold": 5.0, "Yr.Sold": 2009.0, "HasShed": false, "HasAlley": false, "Garage.Age": 50.0, "Remod.Age": 50.0, "House.Age": 50.0, "MS.SubClass_30": false, "MS.SubClass_50": false, "MS.SubClass_60": false, "MS.SubClass_70": false, "MS.SubClass_80": false, "MS.SubClass_85": false, "MS.SubClass_90": false, "MS.SubClass_120": false, "MS.SubClass_160": false, "MS.SubClass_190": false, "MS.SubClass_Other": false, "MS.Zoning_RH": false, "MS.Zoning_RL": true, "MS.Zoning_RM": false, "Land.Contour_HLS": false, "Land.Contour_Low": false, "Land.Contour_Lvl": true, "Lot.Config_CulDSac": false, "Lot.Config_FR2": false, "Lot.Config_FR3": false, "Lot.Config_Inside": false, "Neighborhood_BrDale": false, "Neighborhood_BrkSide": false, "Neighborhood_ClearCr": false, "Neighborhood_CollgCr": false, "Neighborhood_Crawfor": false, "Neighborhood_Edwards": false, "Neighborhood_Gilbert": false, "Neighborhood_IDOTRR": false, "Neighborhood_MeadowV": false, "Neighborhood_Mitchel": false, "Neighborhood_NAmes": true, "Neighborhood_NPkVill": false, "Neighborhood_NWAmes": false, "Neighborhood_NoRidge": false, "Neighborhood_NridgHt": false, "Neighborhood_OldTown": false, "Neighborhood_SWISU": false, "Neighborhood_Sawyer": false, "Neighborhood_SawyerW": false, "Neighborhood_Somerst": false, "Neighborhood_StoneBr": false, "Neighborhood_Timber": false, "Neighborhood_Veenker": false, "Bldg.Type_2fmCon": false, "Bldg.Type_Duplex": false, "Bldg.Type_Twnhs": false, "Bldg.Type_TwnhsE": false, "House.Style_1.5Unf": false, "House.Style_1Story": true, "House.Style_2.5Fin": false, "House.Style_2.5Unf": false, "House.Style_2Story": false, "House.Style_SFoyer": false, "House.Style_SLvl": false, "Roof.Style_Hip": true, "Roof.Style_Other": false, "Mas.Vnr.Type_Stone": true, "Mas.Vnr.Type_Other": false, "Mas.Vnr.Type_None": false, "Foundation_CBlock": true, "Foundation_PConc": false, "Foundation_Other": false, "Bsmt.Qual_Gd": false, "Bsmt.Qual_TA": true, "Bsmt.Qual_Fa": false, "Bsmt.Qual_NA": false, "Bsmt.Cond_TA": false, "Bsmt.Cond_Fa": false, "Bsmt.Cond_NA": false, "Bsmt.Exposure_Av": false, "Bsmt.Exposure_Mn": false, "Bsmt.Exposure_No": false, "Bsmt.Exposure_NA": false, "BsmtFin.Type.1_ALQ": false, "BsmtFin.Type.1_BLQ": true, "BsmtFin.Type.1_Rec": false, "BsmtFin.Type.1_LwQ": false, "BsmtFin.Type.1_Unf": false, "BsmtFin.Type.1_NA": false, "BsmtFin.Type.2_ALQ": false, "BsmtFin.Type.2_BLQ": false, "BsmtFin.Type.2_Rec": false, "BsmtFin.Type.2_LwQ": false, "BsmtFin.Type.2_Unf": true, "BsmtFin.Type.2_NA": false, "Central.Air_Y": true, "Garage.Type_Attchd": true, "Garage.Type_Basment": false, "Garage.Type_BuiltIn": false, "Garage.Type_CarPort": false, "Garage.Type_Detchd": false, "Garage.Type_NoGarage": false, "Garage.Finish_RFn": false, "Garage.Finish_Unf": false, "Garage.Finish_NoGarage": false, "Sale.Type_GroupedWD": true, "Sale.Type_Other": false, "Sale.Condition_AdjLand": false, "Sale.Condition_Alloca": false, "Sale.Condition_Family": false, "Sale.Condition_Normal": true, "Sale.Condition_Partial": false, "Condition_Railroad": false, "Condition_Roads": false, "Condition_Positive": false, "Condition_RoadsAndRailroad": false, "Exterior_BrkFace": true, "Exterior_CemntBd": false, "Exterior_HdBoard": false, "Exterior_MetalSd": false, "Exterior_Plywood": false, "Exterior_Stucco": false, "Exterior_VinylSd": false, "Exterior_Wd Sdng": false, "Exterior_WdShing": false, "Exterior_Other": false
}
```

**Expected Output:**
```
{
    "preco_predito": 5.31840705871582
}
```
(The price is in log scale)
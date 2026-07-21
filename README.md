# Adfærdanalyse af Global EV Adoption

Dette repository indeholder en analyse og et maskinlæringsprojekt, der undersøger hvilke faktorer der påvirker sandsynligheden for adoption af elbiler på tværs af forskellige befolkningsgrupper. Projektet er implementeret i et Jupyter Notebook og kombinerer eksplorativ dataanalyse med klassifikation ved hjælp af Random Forest og XGBoost.

## Formål

Målet med projektet er at:

- analysere sammenhængen mellem adfærd, demografi og infrastruktur og sandsynligheden for EV-adoption
- forudsige en persons EV-adoption-likelihood i kategorierne Low, Medium og High
- sammenligne to klassifikationsmodeller og identificere den bedste model
- afdække de vigtigste features, der driver adoptionen

## Datasæt

Projektet bruger datasættet:

- [global_ev_adoption_behavior_2026.csv](global_ev_adoption_behavior_2026.csv)

Datasættet indeholder en række variable relateret til:

- demografi og socioøkonomi
- adfærd og holdninger
- viden om og interesse for elbiler
- adgang til ladestandere og infrastrukturelle forhold

Målvariablen er:

- ev_adoption_likelihood

## Notebook-indhold

Analysen i [global-ev-adoption-behavior-2026.ipynb](global-ev-adoption-behavior-2026.ipynb) omfatter:

1. import og gennemgang af data
2. eksplorativ dataanalyse (EDA)
3. visualisering af fordelinger og sammenhænge
4. dataforbehandling og kodning af kategoriske variable
5. træning af en Random Forest-model og en XGBoost-model
6. evaluering af modellerne med nøjagtighed, klassifikationsrapport, confusion matrix og krydsvalidering
7. analyse af feature importance

## Databehandling

Under forbehandlingen er der blandt andet:

- fjernet potentielle lækagekolonner, som kunne give kunstigt høje resultater
- udfyldt manglende værdier med robuste metoder
- kodet kategoriske variable til numeriske værdier
- oprettet et trænings- og testsæt med stratificering

## Modeller og resultater

Projektet sammenligner to modeller:

- Random Forest
- XGBoost

De opnåede testresultater var:

- Random Forest: 84.75% nøjagtighed
- XGBoost: 87.00% nøjagtighed

XGBoost blev derfor valgt som den bedste model.

## Nøgleindsigter

Analysen viser, at følgende faktorer er særligt vigtige for EV-adoption:

- høj viden om elbiler og stærk teknologiinteresse øger sandsynligheden for adoption
- høj miljøbevidsthed er positivt forbundet med adoption
- range anxiety har en negativ effekt på adoptionen
- højere indkomst og bedre adgang til ladestandere fremmer adoptionen
- personer i byområder har generelt højere sandsynlighed for adoption end personer i landdistrikter
- incitamenter alene er ikke tilstrækkelige; de skal kombineres med stærk infrastruktur og lav bekymring om rækkevidde

## Teknologier og afhængigheder

Projektet er udviklet i Python med følgende hovedpakker:

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost

## Sådan kører du projektet

1. Installer de nødvendige pakker:

   pip install pandas numpy matplotlib seaborn scikit-learn xgboost jupyter

2. Start Jupyter Notebook:

   jupyter notebook

3. Åbn og kør notebook-filen:

   [adfaerdsanalyse-af-global-ev-adoption.ipynb](adfaerdsanalyse-af-global-ev-adoption.ipynb)

## Projektstruktur

- [README.md](README.md) – projektoversigt og dokumentation
- [global-ev-adoption-behavior-2026.ipynb](global-ev-adoption-behavior-2026.ipynb) – analyse- og modelleringsarbejde
- [global_ev_adoption_behavior_2026.csv](global_ev_adoption_behavior_2026.csv) – inputdatasæt
- [LICENSE](LICENSE) – licensoplysninger

## Licens

Dette projekt er tilgængeligt under licensen i [LICENSE](LICENSE).

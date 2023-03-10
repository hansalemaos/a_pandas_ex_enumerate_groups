# Groups values in a column of a DataFrame and enumerates them

```python
pip install a-pandas-ex-enumerate_groups 
```


```python

from a_pandas_ex_enumerate_groups import pd_add_enumerate_group
pd_add_enumerate_group()
import pandas as pd

df = pd.read_csv(
    "https://raw.githubusercontent.com/pandas-dev/pandas/main/doc/data/titanic.csv"
)
dfi = df.ds_enumerate_groups(
     enumerated_column="Age_enu", column_to_enumerate="Age"
)
print(dfi[:20].to_string())
dfi = df.ds_enumerate_groups( enumerated_column="Cabin_en", column_to_enumerate="Cabin"
)
print(dfi[:20].to_string())
dfi = df.ds_enumerate_groups( enumerated_column="Fare_en", column_to_enumerate="Fare"
)

print(dfi[:20].to_string())


     PassengerId  Survived  Pclass                             Name     Sex   Age  SibSp  Parch           Ticket      Fare    Cabin Embarked Age_enu
803          804         1       3  Thomas, Master. Assad Alexander    male  0.42      0      1             2625    8.5167      NaN        C       0
755          756         1       2        Hamalainen, Master. Viljo    male  0.67      1      1           250649   14.5000      NaN        S       1
644          645         1       3           Baclini, Miss. Eugenie  female  0.75      2      1             2666   19.2583      NaN        C       2
469          470         1       3    Baclini, Miss. Helene Barbara  female  0.75      2      1             2666   19.2583      NaN        C       2
78            79         1       2    Caldwell, Master. Alden Gates    male  0.83      0      2           248738   29.0000      NaN        S       3
831          832         1       2  Richards, Master. George Sibley    male  0.83      1      1            29106   18.7500      NaN        S       3
305          306         1       1   Allison, Master. Hudson Trevor    male  0.92      1      2           113781  151.5500  C22 C26        S       4
827          828         1       2            Mallet, Master. Andre    male  1.00      0      2  S.C./PARIS 2079   37.0042      NaN        C       5
381          382         1       3      Nakid, Miss. Maria ("Mary")  female  1.00      0      2             2653   15.7417      NaN        C       5
164          165         0       3     Panula, Master. Eino Viljami    male  1.00      4      1          3101295   39.6875      NaN        S       5
183          184         1       2        Becker, Master. Richard F    male  1.00      2      1           230136   39.0000       F4        S       5
386          387         0       3  Goodwin, Master. Sidney Leonard    male  1.00      5      2          CA 2144   46.9000      NaN        S       5
172          173         1       3     Johnson, Miss. Eleanor Ileen  female  1.00      1      1           347742   11.1333      NaN        S       5
788          789         1       3       Dean, Master. Bertram Vere    male  1.00      1      2        C.A. 2315   20.5750      NaN        S       5
642          643         0       3    Skoog, Miss. Margit Elizabeth  female  2.00      3      2           347088   27.9000      NaN        S       6
7              8         0       3   Palsson, Master. Gosta Leonard    male  2.00      3      1           349909   21.0750      NaN        S       6
530          531         1       2         Quick, Miss. Phyllis May  female  2.00      1      1            26360   26.0000      NaN        S       6
297          298         0       1     Allison, Miss. Helen Loraine  female  2.00      1      2           113781  151.5500  C22 C26        S       6
824          825         0       3     Panula, Master. Urho Abraham    male  2.00      4      1          3101295   39.6875      NaN        S       6
205          206         0       3       Strom, Miss. Telma Matilda  female  2.00      0      1           347054   10.4625       G6        S       6
     PassengerId  Survived  Pclass                                                               Name     Sex   Age  SibSp  Parch    Ticket      Fare Cabin Embarked Cabin_en
583          584         0       1                                                Ross, Mr. John Hugo    male  36.0      0      0     13049   40.1250   A10        C        0
475          476         0       1                                        Clifford, Mr. George Quincy    male   NaN      0      0    110465   52.0000   A14        S        1
556          557         1       1  Duff Gordon, Lady. (Lucille Christiana Sutherland) ("Mrs Morgan")  female  48.0      1      0     11755   39.6000   A16        C        2
284          285         0       1                                         Smith, Mr. Richard William    male   NaN      0      0    113056   26.0000   A19        S        3
599          600         1       1                       Duff Gordon, Sir. Cosmo Edmund ("Mr Morgan")    male  49.0      1      0  PC 17485   56.9292   A20        C        4
630          631         1       1                               Barkworth, Mr. Algernon Henry Wilson    male  80.0      0      0     27042   30.0000   A23        S        5
867          868         0       1                               Roebling, Mr. Washington Augustus II    male  31.0      0      0  PC 17590   50.4958   A24        S        6
647          648         1       1                                Simonius-Blumer, Col. Oberst Alfons    male  56.0      0      0     13213   35.5000   A26        C        7
209          210         1       1                                                   Blank, Mr. Henry    male  40.0      0      0    112277   31.0000   A31        C        8
185          186         0       1                                              Rood, Mr. Hugh Roscoe    male   NaN      0      0    113767   50.0000   A32        S        9
445          446         1       1                                          Dodge, Master. Washington    male   4.0      0      2     33638   81.8583   A34        S       10
806          807         0       1                                             Andrews, Mr. Thomas Jr    male  39.0      0      0    112050    0.0000   A36        S       11
96            97         0       1                                          Goldschmidt, Mr. George B    male  71.0      0      0  PC 17754   34.6542    A5        C       12
23            24         1       1                                       Sloper, Mr. William Thompson    male  28.0      0      0    113788   35.5000    A6        S       13
174          175         0       1                                            Smith, Mr. James Clinch    male  56.0      0      0     17764   30.6958    A7        C       14
737          738         1       1                                             Lesurer, Mr. Gustave J    male  35.0      0      0  PC 17755  512.3292  B101        C       15
815          816         0       1                                                   Fry, Mr. Richard    male   NaN      0      0    112058    0.0000  B102        S       16
523          524         1       1                    Hippach, Mrs. Louis Albert (Ida Sophia Fischer)  female  44.0      0      1    111361   57.9792   B18        C       17
329          330         1       1                                       Hippach, Miss. Jean Gertrude  female  16.0      0      1    111361   57.9792   B18        C       17
170          171         0       1                                          Van der hoef, Mr. Wyckoff    male  61.0      0      0    111240   33.5000   B19        S       18
     PassengerId  Survived  Pclass                              Name   Sex   Age  SibSp  Parch  Ticket    Fare        Cabin Embarked Fare_en
271          272         1       3      Tornquist, Mr. William Henry  male  25.0      0      0    LINE  0.0000          NaN        S       0
597          598         0       3               Johnson, Mr. Alfred  male  49.0      0      0    LINE  0.0000          NaN        S       0
302          303         0       3   Johnson, Mr. William Cahoone Jr  male  19.0      0      0    LINE  0.0000          NaN        S       0
633          634         0       1     Parr, Mr. William Henry Marsh  male   NaN      0      0  112052  0.0000          NaN        S       0
277          278         0       2       Parkes, Mr. Francis "Frank"  male   NaN      0      0  239853  0.0000          NaN        S       0
413          414         0       2    Cunningham, Mr. Alfred Fleming  male   NaN      0      0  239853  0.0000          NaN        S       0
674          675         0       2        Watson, Mr. Ennis Hastings  male   NaN      0      0  239856  0.0000          NaN        S       0
263          264         0       1             Harrison, Mr. William  male  40.0      0      0  112059  0.0000          B94        S       0
466          467         0       2             Campbell, Mr. William  male   NaN      0      0  239853  0.0000          NaN        S       0
732          733         0       2              Knight, Mr. Robert J  male   NaN      0      0  239855  0.0000          NaN        S       0
179          180         0       3               Leonard, Mr. Lionel  male  36.0      0      0    LINE  0.0000          NaN        S       0
806          807         0       1            Andrews, Mr. Thomas Jr  male  39.0      0      0  112050  0.0000          A36        S       0
481          482         0       2  Frost, Mr. Anthony Wood "Archie"  male   NaN      0      0  239854  0.0000          NaN        S       0
822          823         0       1   Reuchlin, Jonkheer. John George  male  38.0      0      0   19972  0.0000          NaN        S       0
815          816         0       1                  Fry, Mr. Richard  male   NaN      0      0  112058  0.0000         B102        S       0
378          379         0       3               Betros, Mr. Tannous  male  20.0      0      0    2648  4.0125          NaN        C       1
872          873         0       1          Carlsson, Mr. Frans Olof  male  33.0      0      0     695  5.0000  B51 B53 B55        S       2
326          327         0       3         Nysveen, Mr. Johan Hansen  male  61.0      0      0  345364  6.2375          NaN        S       3
843          844         0       3        Lemberopolous, Mr. Peter L  male  34.5      0      0    2683  6.4375          NaN        C       4
818          819         0       3  Holm, Mr. John Fredrik Alexander  male  43.0      0      0  C 7075  6.4500          NaN        S       5


df.d_enumerate_all_groups_in_all_columns(prefix="group_")
Out[4]: 
     PassengerId  Survived  Pclass  ... group_Fare group_Cabin  group_Embarked
0              1         0       3  ...         18         NaN             2.0
1              2         1       1  ...        207        81.0             0.0
2              3         1       3  ...         41         NaN             2.0
3              4         1       1  ...        189        55.0             2.0
4              5         0       3  ...         43         NaN             2.0
..           ...       ...     ...  ...        ...         ...             ...
886          887         0       2  ...         85         NaN             2.0
887          888         1       1  ...        153        30.0             2.0
888          889         0       3  ...        131         NaN             2.0
889          890         1       1  ...        153        60.0             0.0
890          891         0       3  ...         30         NaN             1.0
[891 rows x 24 columns]


df.d_enumerate_groups_in_multiple_columns(columns=[['Pclass','Survived']], prefix="group_", name_sep="_")
Out[7]: 
     PassengerId  Survived  Pclass  ... Cabin Embarked  group_Pclass_Survived
0              1         0       3  ...  <NA>        S                      4
1              2         1       1  ...   C85        C                      1
2              3         1       3  ...  <NA>        S                      5
3              4         1       1  ...  C123        S                      1
4              5         0       3  ...  <NA>        S                      4
..           ...       ...     ...  ...   ...      ...                    ...
886          887         0       2  ...  <NA>        S                      2
887          888         1       1  ...   B42        S                      1
888          889         0       3  ...  <NA>        S                      4
889          890         1       1  ...  C148        C                      1
890          891         0       3  ...  <NA>        Q                      4
[891 rows x 13 columns]

```

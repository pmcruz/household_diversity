Household Diversity
===================

 

Three datasets that show each type of household in Boston for 2016 (ACS, 1%
sample). The aggregations are:

-   Race in race.json

-   Language spoken in language.json

-   Birth place in bpld.json

 

### File structure

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
{
    "groups": [], -> array with all types of households
    "total_households": aaaaa
}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

 

Inside the groups array, a household has then

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
{
    "ageList": [], -> array that gives a normalized age histogram for that type of household
    "categories": [] -> describes the household composition. For example, for race, a household with 2 white people and a black person would be
    [
        {
            "n": 2,
            "desc": "White"
        },
        {
            "n": 1,
            "desc": "Black"
        }
    ]
    "weight" : 0.xx -> the ratio of households, e.g. there are (weight * total_households) households with this composition in the dataset. 
    "others": can be ignored.


}
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

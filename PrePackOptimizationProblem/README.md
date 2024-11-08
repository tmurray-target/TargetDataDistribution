# Apparel Packaging and Allocation
## Context Description
The data provided made available here is a set of 10 instances of the Pre-Pack Optimization Problem. This problem addresses
how to design a small number of assortment packs of different items which can then be distributed to multiple locations
in order to mean their distinct needs for the different items in the assortment.

Target encounters instances of this problem in the context of apparel planning, where an individual item such as a t-shirt
can come in multiple sizes such as small, medium, and large (S,M,L). Designing a pack which contains (2,3,2) units of each
size may meet the needs of some locations, but not others. The goal is to design a small number of packs which can be mixed
and matched so that each location receives as close to its required quantity of each size as possible, subject to constraints
such as total unit quantity, minimum and maximum pack size, maximum number of packs per location, and others.

## Dataset Description
The `Datasets.zip` file contains 10 datasets which were used to benchmark Target's solver for the Pre-Pack Optimization Problem.
Each dataset is contained in its own folder as a `csv` file of under 2000 rows of desired quantities for each size-location 
pair. All identifying information for the location has been removed, as has all identifying information for the item beyond
its general category (i.e. Sweaters, Dresses, etc.)

Each folder also contains an accompanying `specs.txt` file which contains additional information related to the following 
problem instance information and constraints:
- `Locations`: The number of locations to allocate to, equal to the number of non-header rows in the data.
- `Sizes`: The number of sizes the item is available in.
- `Assortment Packs`: The maximum number of assortment pack configurations which are allowed to be considered for the problem instance.
- `Allocation Units`: The maximum number of total units which may be allocated in the problem instance.
- `Minimum Pack Size`: The minimum number of units any assortment pack configuration may contain in this problem instance.
- `Maximum Pack Size`: The maximum number of units any assortment pack configuration may contain in this problem instance.
- `Minimum Units per Size per Location`: The minimum number of units of each size that each location must receive.
- `Maximum Packs per Location`: The maximum total number of packs (not configurations) which may be allocated to a location.
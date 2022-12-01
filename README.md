# gender-discrimination-hiring
This repo contains the code for obtaining the necessary data for the following paper:

#### *Li K. K.*, *L. Li*, *W. Si* and *Z. Xu* (2022) "**Childbearing Age and Gender Discrimination in Hiring Decisions: A Large-scale Field Experiment**" 

Please find the paper [here](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4199754).

To make sense of the explainations below, you may want to check the experimental desgin part of the paper first.


## `gender51job`

The `gender51job` folder contains a Scrapy web-crawling framework.
- It is used to obtain all the relevant positions (and position info such as company size, company type etc.) from [51job.com](https://www.51job.com/)
- Change the `url` variable in `gender-discrimination-hiring/gender51job/spiders/job.py` for different occupations (IT, Accounting or HR)
- The output would be a `json` file like `result_sample.json`. 

## `randomization_1to1.py`

The `randomization_1to1.py` takes the `result.json` file obtained using `gender51job` and does the following:
- Exclude positions, such as positions require a doctor's degree or pays over a certain amount, that are not in our research scope.
- Convert different salary measures to monthly salary
- Give company size levels, salary levels and other levels different labels
- Randomly divide the positions into blocks for each fictitious applicant
- The output would be a `xlsx` file like `output_sample.xlsx` 

## `autoapply.py`

## `51job.py`

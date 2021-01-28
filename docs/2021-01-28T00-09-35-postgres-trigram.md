---
date: 2021-01-28T00:09:35-08:00
title: Postgres Trigram
tags: Postgres
---

# Postgres Trigram

B-tree index doesn't support queries with `like`. It's because b-tree basically sorts the data. That's why its able to use during min(), max() etc. 

For improving queries with like one can use trigram which is a group of three consecutive characters taken from a string. https://www.postgresql.org/docs/9.6/pgtrgm.html.

The `pg_trgm` module provides GiST and GIN index operator classes that allow you to create an index over a text column for the purpose of very fast similarity searches.


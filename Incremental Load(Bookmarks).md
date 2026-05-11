In Amazon Web Services AWS Glue, **Job Bookmarks** are a feature used to **track previously processed data** so that a Glue job only processes **new or changed data** during the next run.

Glue stores bookmark metadata internally in the Glue service associated with:

- Job name
- Transformation context
- Source information

You don’t manually manage the storage

![[Pasted image 20260509225607.png|416]]

![[Pasted image 20260509230758.png]]
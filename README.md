# Fix_S3ToRedshiftTransfer
the S3ToRedshiftTransfer class on Apache Airflow 1.10.12 requires that the target table to be loaded is suffixed to the end of the S3 key provided.
It doesn't seem justifiable that the operator should require the file to be named by any convention.  The S3 bucket + S3 key should be all that is needed.
This makes it possible to load any S3 Key into a Redshift table, rather than only files that have the table name at the end of the S3 key.

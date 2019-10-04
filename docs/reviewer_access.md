# Reviewer Access

When each dataset is submitted, a special “reviewer” account is automatically created for that dataset. This account has special privileges to view the dataset’s files and metadata even while the dataset is private. The reviewer account’s login credentials are:

Username:	{MSV_accession}_reviewer
Password:	{dataset’s private password}

For example, if your dataset was MSV000000001, and the password you entered when submitting was “reviewersonly”, then you would share the following special account login credentials with all your dataset’s reviewers:

Username:	MSV000000001_reviewer
Password:	reviewersonly

With these credentials your reviewers can access your private dataset, and since the dataset’s files are automatically shared with this account it can also be used to run [ProteoSAFe analysis workflows](reanalyze_spectra.md) on those files for testing and review purposes.


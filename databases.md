# Genbank

Genbank can use e-utils to download files. There is a limit of three requests per second, or with an API key can get up to 10 requests per second. I think we can probably start with three, as it will take a while for the files to download anyways.

# Gene Expression Omnibus

Gene Expression Omnibus can use e-utils to download summaries, but in order to actually download raw data, I need to construct a FTP URL. Hopefully I can do this programmatically. If there's extra info that I require, hopefully I can find it in the summary section.

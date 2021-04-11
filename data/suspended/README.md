## Suspended account information

The [suspended-accounts.csv](suspended-accounts.csv) file
is a comma-separated table where each line represents a screen name of a suspended Twitter account and includes the following columns:

1. Twitter ID
2. Screen name
3. Date of first known activity
4. Date of last known activity
5. Number of tweet appearances in our Wayback Machine dataset
6. Display name

If the account has other known display names, these will appear in additional columns.

Notes:

* There's a lot of offensive content here, including racial slurs and obscenity.
* Please see [the top-level README](https://github.com/travisbrown/deleted-tweets) for details about how this account information was collected.
* There are currently around 380,000 additional inactive accounts in our dataset that aren't yet confirmed to be suspended. These are being checked now, and we expect that roughly 180,000 of them will end up in this file.
* A Twitter ID may appear in multiple rows if the account had more than one screen name.
* Suspensions are occasionally reversed, so some of these accounts may no longer be suspended.
* The dates of first and last known activity only reflect our subset of the Wayback Machine's Twitter data, which is not complete for most accounts.
* The count in the fifth column is not _distinct_ tweets. For `@realDonaldTrump`, for example, the value is currently 1,491,878, which is how many times Trump tweets appear across all pages in our dataset, but the dataset only contains 33,947 distinct tweets by Trump.



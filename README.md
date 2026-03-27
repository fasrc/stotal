# stotal
stotal is will calculate the total CPU-hours, GPU-hours, and TRES-hours for a Slurm user or account.

## Usage
stotal will calculate the CPU-hours, GPU-hours, and TRES-hours in a specified window for a user, account, or all the accounts on a cluster. Note that for information on other users (even in their own account) and accounts the user must be either an Operator or Administrator. stotal only calculates usage in the specified window, so if a job starts before or during the window and then runs into or beyond the window only the usage in the window will be tallied.

stotal has the following options:

 * `-h, --help`: Print description and options.
 * `-u, --user`: Which user you want to query. Mutually exclusive with -A and -a. No default.
 * `-A, --account`: Which account you want to query. Mutually exclusive with -u and -a. No default.
 * `-a, --all`: Dump data on all accounts. Mutually exclusive with -u and -A.
 * `-S, --starttime`: Start time for window. Same format as in [sacct](https://slurm.schedmd.com/sacct.html#OPT_starttime). No default.
 * `-E, --endtime`: End time for window. Same format as in [sacct](https://slurm.schedmd.com/sacct.html#OPT_starttime). No default.
 * `-n, --noheader`: Do not print header.
 * `-d, --details`: If specifying user, break out usage by account. If specifying account or all accounts, break out usage by user.
 * `--csv`: Format output in comma seperated value (CSV) format.

gmeta
=====

gmeta is designed for use with git's pre-commit and post-checkout hooks to
allow managing the metadata of files in addition to their content.

It uses a sqlite database to store the metadata.

The included fields are:
   - mtime
   - atime
   - mode

### `Usage: gmeta [OPTION] COMMAND`

#### Commands:

   - `init` - update entries for files according to "git ls-files"
   - `restore` - restores the metadata for files according to "git ls-files"
   - `pre-commit` - runs the pre-commit hook
   - `post-checkout` - runs the post-checkout hook


Symlink Support
---------------

If you symlink gmeta to the `pre-commit` or `post-checkout` hooks, it will
do trigger the respective command automatically.

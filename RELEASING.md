# Releasing

1. Set the version numbers.

    1. Increment the version according to semantic versioning rules in `lib/pact/provider_verifier/version.rb`.
    1. Set the package number (eg. "-1") in `tasks/package.rake`. This is required because the same gem version may be packaged multiple times.

2. Update the `CHANGELOG.md` using:

    $ git log --pretty=format:'  * %h - %s (%an, %ad)' vX.Y.Z..HEAD

3. Add files to git

    $ git add CHANGELOG.md lib/pact/provider_verifier/version.rb

4. Commit

    $ git commit -m "Releasing version X.Y.Z"

5. Tag

    $ git tag -a vX.Y.Z -m "Releasing version X.Y.Z" && git push origin --tags

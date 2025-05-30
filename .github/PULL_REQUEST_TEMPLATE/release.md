* [ ]  Draft a social media announcement
* [ ]  See if all tests, including downstream, pass
* [ ]  Get the release pull request approved by a [CODEOWNER](https://github.com/urllib3/urllib3/blob/main/.github/CODEOWNERS)
* [ ]  Squash merge the release pull request with message "`Release <VERSION>`"
* [ ]  Tag with X.Y.Z, push tag on urllib3/urllib3 (not on your fork, update `<REMOTE>` accordingly)
  * Notice that the `<VERSION>` shouldn't have a `v` prefix (Use `1.26.6` instead of `v.1.26.6`)
  * ```
    # Ensure the release commit is the latest in the main branch.
    export VERSION=<X.Y.Z>
    export REMOTE=origin
    git checkout main
    git pull $REMOTE main
    git tag -s -a "$VERSION" -m "Release: $VERSION"
    git push $REMOTE --tags
    ```
* [ ]  The tag will trigger the `publish` GitHub workflow. This requires a review from a maintainer.
* [ ]  Ensure that all expected artifacts are added to the new GitHub release draft. Should
       be one `.whl` and one `.tar.gz`. Publish the GitHub
       release with the content of the release's changelog and any ongoing announcements.
* [ ]  Announce on:
  * [ ]  Social media
  * [ ]  Discord
  * [ ]  Open Collective
* [ ]  Check [Tidelift security maintenance plan](https://tidelift.com/lifter/package/pypi/urllib3/tasks/packages_have_maintenance_plans>) is still correct
* [ ]  If this was a 1.26.x release, add changelog to the `main` branch

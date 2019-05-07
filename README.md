# ![LOGO](logo.png) FishEye **flow**ground Connector

## Description

A generated **flow**ground connector for the FishEye API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/fisheye.local/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:40:44+03:00

## API Description



## Authorization

This API does not require authorization.

## Actions

### List of changesets from a repository.

#### Input Parameters
* `rep` - _optional_ - the key of the repository
* `path` - _optional_ - repository path
* `committer` - _optional_ - ID of the committer
* `comment` - _optional_ - comment to match
* `p4JobFixed` - _optional_ - Perforce option to select the changesets marked as fixing
* `expand` - _optional_ - expand query parameter to specify the maximum number of results
* `beforeCsid` - _optional_ - parent of the changesets

### Retrieves detailed information about a set of changesets in a repository, designed to be used with the FishEye commit graph

#### Input Parameters
* `repository` - _required_ - the key of the repository

### finds slice data the query

#### Input Parameters
* `branch` - _optional_ - the set of branches to search. If not specified, will search all branches
* `id` - _optional_ - the id of the changeset which we are
* `direction` - _optional_ - the direction to traverse. May be "before", "after" or "around"
* `size` - _optional_ - the number of changesets to return in the slice

### List all the repositories.

### Get the information about a repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### getChangeset

#### Input Parameters
* `csid` - _required_ - the ChangesetID of the changeset to return.
* `repository` - _required_ - the key of the repository to query.

### Get a list of changesets on a repository.

#### Input Parameters
* `path` - _optional_ - restrict the changesets to those in this path, should be "/" to look at the whole repository.
* `start` - _optional_ - only return changesets after this date.
* `end` - _optional_ - only return changesets before this date.
* `maxReturn` - _optional_ - the maximum number of changesets to return.

### Get a list of the file revisions for a specific path.

#### Input Parameters
* `path` - _optional_ - the path to query.

### Get a list of information about files and directories in a path.

#### Input Parameters
* `path` - _optional_ - the path to query, with respect to the fisheye repository root.

### getRevisionInfo

#### Input Parameters
* `path` - _optional_ - the path of the filerevision, with respect to the fisheye repository root.
* `revision` - _optional_ - the id of the filerevision to retrieve.

### listTagsForRevision

#### Input Parameters
* `path` - _optional_ - the path of the filerevision, with respect to the fisheye repository root.
* `revision` - _optional_ - the id of the filerevision to retrieve.

### Execute a query across repositories. By default, this will search all repositories.

#### Input Parameters
* `query` - _optional_ - text to search for in commit message and p4 jobId. Must not be empty.
* `repository` - _optional_ - restrict search to only these repositories (by their keys)
* `expand` - _optional_ - expand query parameter to specify the maximum number of results. Format is changesets[n:m].revisions[n:m],reviews
        the default number of changesets returned is 30, the maximum returned is 100

### Execute a FishEye query against a specific repository.

#### Input Parameters
* `query` - _optional_ - FishEye query to execute
* `maxReturn` - _optional_ - maximum number of results (which can be left unspecified, but in that case,
 the maximum number of results will set to 3000 results)

### Execute a FishEye query (that contains a "return" statement) against a specific repository.

#### Input Parameters
* `query` - _optional_ - FishEye query to execute (which must contain a "return" statement)
* `maxReturn` - _optional_ - maximum number of results (which can be left unspecified, but in that case,
 the maximum number of results will set to 3000 results)

### Retrieve a list of reviews for a changeset in a given repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository

### Retrieve a list of reviews for each given changeset in a given repository.

#### Input Parameters
* `repository` - _required_ - the key of the repository

## License

**flow**ground :- Telekom iPaaS / fisheye-local-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

# Matrix Specification

The Matrix Specification

## About

The Matrix is an opinionated data representation library. This is similar to [Schema.org](https://schema.org), however it allows for more personalized data types as well as persistent data storage management.

## Collections

All the types in the Matrix are assigned to a specific `Collection` which will be contained in separate Github repositories. The first collection is the `std` collection which contains basic types such as `Text`, `Number`, `Date`, etc. The system allows for easy creation of hierarchical data types which can inherit propereties of their parents. These collection repositories have a _topic_, Github's version of a tag, labeled: `'matrix-collection'`. The `matrix-library` will be able to scan the Sivrad organization's repositories, specifically with the `'matrix-collection'` topic, and export all the types included in the collection. This is done to allow for a person developing a skillset to have all the types at their disposable in the development phase.

### Structure

| File Name           | Description                                                                    |
| ------------------- | ------------------------------------------------------------------------------ |
| `./collection.json` | Contains information about the collection name, label, description, logo, etc. |
| `./types/*.json`    | Contains information and the structure of the type                             |

The other files in the repository allow for the automated process of package generation and publication.

### Automation

#### Publication

The publication of packages will be handeled automatically with Github actions. Each collection repository will include the package `@sivrad/collection-cd`, which handels all continues deployment before it publishes it to the NPM registry. This package will generate Typescript classes bases on the `./types/*.json` types.

## Skillset Workflow

A skillset function will is going to look something like this.

```typescript
import { Thing, TimeDifference } from "@sivrad/matrix-lib";

export const CalculateAge = (thing: Thing): TimeDifference => {
    return TimeDifference({
        difference: Date.now().getTime() - thing.start.getTime(),
    });
};
```

The `thing` paramiter takes in a `Thing` and returns a `TimeDifference` which are both types from the Matrix Library.

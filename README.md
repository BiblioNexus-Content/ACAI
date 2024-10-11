# ACAI Release: 2024-10-10

As you encounter issues or have questions, please contact Rick Brannan at rick.brannan@biblionexus.org.

# License

This release of the ACAI data (the JSON and Markdown forms included here) is under a Creative Commons CC-BY-SA 4.0 license. See [LICENSE.md](LICENSE.md) for more details.

# Identifiers

Identifiers in the ACAI ecosystem consist of two parts. The first part represents the type of identifier (e.g. people, places, deities, groups, fauna, flora, realia). The second part is a unique identifier representing the specific record. For example, the identifier for **Aaron** as a person is `person:Aaron`.

## Primary Identifiers

The structure of the JSON is flat; we simply have all the records of a single type (e.g. people) in individual JSON files in the ACAI type folder/directory. The JSON files are named with the identifier, sans type, as the filename. For example, the JSON file for Aaron as a person is `Aaron.json`.

However, there are many people like **Abraham** who are known by more than one name within the biblical canon. Each of these forms of **Abraham** has a separate record encoded as JSON, so we have both  `Abraham.json` and `Abram.json`. When multiple forms of a thing exist, it is useful to know which is the primary form. Each record contains an `id` and a `primary_id`. When `id` and `primary_id` for a record match, the record can be considered the primary form of the record; the other forms are encoded in the `referred_to_as` list contained elsewhere in the record. The primary record contains data for all forms of the entity, in word level references, pronominal referents, and subject referents. The non-primary records only contain references to the specific form of the record (e.g. **Abram**).

The specification of primary and non-primary records is consistent through all ACAI types.

In most applications (“where are all the places ‘Abraham’ occurs in the Bible?”), it is anticipated that the information in the primary record is what will be required.

# Descriptions

Each record contains a `localizations` object that contains a `preferred_label` and a `description`. The `description` is a curated, free-text description of the entity. The JSON records support localization and in the future may have material in languages beside English.

# Included Data

The data included in this release is a snapshot of the data as of 2024-10-10. It includes JSON files and Markdown files for each record. The Markdown files are generated from the JSON files (along with some Berean Standard Bible [text alignment data](https://github.com/Clear-Bible/Alignments)). They are only included as a visualization of the data within the JSON and not intended to direct or dictate how the JSON data should be used or rendered.

* [people ReadMe](people/README.md)
  * [Markdown Index](people/md/00-Index.md)
* [places ReadMe](places/README.md)
  * [Markdown Index](places/md/00-Index.md)
* [deities ReadMe](deities/README.md)
  * [Markdown Index](deities/md/00-Index.md)
* [groups ReadMe](groups/README.md)
  * [Markdown Index](groups/md/00-Index.md)
* [fauna ReadMe](fauna/README.md)
  * [Markdown Index](fauna/md/00-Index.md)
* [flora ReadMe](flora/README.md)
  * [Markdown Index](flora/md/00-Index.md)
* [realia ReadMe](realia/README.md)
  * [Markdown Index](realia/md/00-Index.md)

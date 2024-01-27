# Vet clinic database: add "join table" for visits

## Learning objectives
- Understand the different types of relationships between tables.
- Prepare complex queries that answer analytical questions.
- Use primary key & foreign key mechanism for joining tables.

### Estimated time: 2.5h

## Description
In this project, you will add some **many-to-many** relationships and write more complex queries to use them to answer questions.

*IMPORTANT NOTE: Read **all** requirements before you start building your project.*

### General requirements

- Make sure that you used correct [Gitflow](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/git-github/articles/gitflow.md).
- Make sure that you documented your work [in a professional way](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/documentation/articles/professional_repo_rules.md).

### Project requirements
- Create a table named `vets` with the following columns:
  - `id`: integer (set it as autoincremented PRIMARY KEY)
  - `name`: string
  - `age`: integer
  - `date_of_graduation`: date
- There is a **many-to-many** relationship between the tables `species` and `vets`: a vet can specialize in multiple species, and a species can have multiple vets specialized in it. Create a "join table" called `specializations` to handle this relationship.
- There is a **many-to-many** relationship between the tables `animals` and `vets`: an animal can visit multiple vets and one vet can be visited by multiple animals. Create a "join table" called `visits` to handle this relationship, it should also keep track of the date of the visit.
- Insert the following data for vets:
  - Vet William Tatcher is 45 years old and graduated Apr 23rd, 2000.
  - Vet Maisy Smith is 26 years old and graduated Jan 17th, 2019.
  - Vet Stephanie Mendez is 64 years old and graduated May 4th, 1981.
  - Vet Jack Harkness is 38 years old and graduated Jun 8th, 2008.
- Insert the following data for specializations:
  - Vet William Tatcher is specialized in Pokemon.
  - Vet Stephanie Mendez is specialized in Digimon and Pokemon.
  - Vet Jack Harkness is specialized in Digimon.
- Insert the following data for visits:
  - Agumon visited William Tatcher on May 24th, 2020.
  - Agumon visited Stephanie Mendez on Jul 22th, 2020.
  - Gabumon visited Jack Harkness on Feb 2nd, 2021.
  - Pikachu visited Maisy Smith on Jan 5th, 2020.
  - Pikachu visited Maisy Smith on Mar 8th, 2020.
  - Pikachu visited Maisy Smith on May 14th, 2020.
  - Devimon visited Stephanie Mendez on May 4th, 2021.
  - Charmander visited Jack Harkness on Feb 24th, 2021.
  - Plantmon visited Maisy Smith on Dec 21st, 2019.
  - Plantmon visited William Tatcher on Aug 10th, 2020.
  - Plantmon visited Maisy Smith on Apr 7th, 2021.
  - Squirtle visited Stephanie Mendez on Sep 29th, 2019.
  - Angemon visited Jack Harkness on Oct 3rd, 2020.
  - Angemon visited Jack Harkness on Nov 4th, 2020.
  - Boarmon visited Maisy Smith on Jan 24th, 2019.
  - Boarmon visited Maisy Smith on May 15th, 2019.
  - Boarmon visited Maisy Smith on Feb 27th, 2020.
  - Boarmon visited Maisy Smith on Aug 3rd, 2020.
  - Blossom visited Stephanie Mendez on May 24th, 2020.
  - Blossom visited William Tatcher on Jan 11th, 2021.
- Write queries to answer the following:
  - Who was the last animal seen by William Tatcher?
  - How many different animals did Stephanie Mendez see?
  - List all vets and their specialties, including vets with no specialties.
  - List all animals that visited Stephanie Mendez between April 1st and August 30th, 2020.
  - What animal has the most visits to vets?
  - Who was Maisy Smith's first visit?
  - Details for most recent visit: animal information, vet information, and date of visit.
  - How many visits were with a vet that did not specialize in that animal's species?
  - What specialty should Maisy Smith consider getting? Look for the species she gets the most.
- **Take a screenshot of the results of your queries.**
- Remember to add the screenshot with the results of your queries to your Pull Request description.

### Need a big picture?

Remind me about [the big picture of this project](./sneak_peek.md).

## Work and submission mode

- You should submit this activity **individually.**

## Code review

Follow [these steps](https://github.com/microverseinc/curriculum-transversal-skills/blob/main/code-review/articles/how_to_ask_for_a_code_review.md) to request a code review of your project.

## Submit your project

After the final approval from a code reviewer, you need to submit your project.
[Read this FAQ for a reminder on how to submit your project.](https://microverse.zendesk.com/hc/en-us/articles/360061344234)
Now go to your Student Dashboard and submit your project.

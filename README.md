# Project Overview

## Project Name
Gotta Fetch 'Em All!

Link to Site: https://gotta-fetch-em-all.netlify.app

## Project Description
Gotta Fetch 'Em All! will allow users to search their favorite Pokemon from the games and learn all about them. Just like a real PokeDex!

## API and Data Sample

Poke API https://pokeapi.co/docs/v2#info

```json
{
    "abilities": [
        {
            "ability": {
                "name": "overgrow",
                "url": "https://pokeapi.co/api/v2/ability/65/"
            },
            "is_hidden": false,
            "slot": 1
        },
        {
            "ability": {
                "name": "chlorophyll",
                "url": "https://pokeapi.co/api/v2/ability/34/"
            },
            "is_hidden": true,
            "slot": 3
        }
    ],
    "base_experience": 64,
    "forms": [
        {
            "name": "bulbasaur",
            "url": "https://pokeapi.co/api/v2/pokemon-form/1/"
        }
    ],
    "game_indices": [
        {
            "game_index": 153,
            "version": {
                "name": "red",
                "url": "https://pokeapi.co/api/v2/version/1/"
            }
        },
        {
            "game_index": 153,
            "version": {
                "name": "blue",
                "url": "https://pokeapi.co/api/v2/version/2/"
            }
        },
        {
            "game_index": 153,
            "version": {
                "name": "yellow",
                "url": "https://pokeapi.co/api/v2/version/3/"
            }
        },
```

## Wireframes

Link to my wireframe here: https://wireframe.cc/oKoj6c

### MVP/PostMVP

#### MVP 

- User can search Pokemon by name
- Correct Pokemon info and picture populates on page
- Previous search info clears when a new Pokemon is searched

#### PostMVP  

- Add CSS animation when loading a new Pokemon
- Style the 'submit' button to be an image with some animation

## Project Schedule

|  Day | Deliverable | Status
|---|---| ---|
|Jan 25-26| Prompt / Wireframes / Priority Matrix / Timeframes | Complete
|Jan 26| Project Approval/ Core HTML & CSS Setup | Complete
|Jan 27| Core JS Functionality / Connect to API  | Complete
|Jan 28| Display Correct Data / Finish Basic Styling | Complete
|Jan 29| MVP | Complete
|Jan 30 & 31| Bonus Styling | Complete
|Feb 1| Presentations/Project Submission | Complete

## Priority Matrix

Priority Matrix https://res.cloudinary.com/drzmvvogq/image/upload/v1611673089/Screen_Shot_2021-01-26_at_8.57.46_AM_i08mw4.png

## Timeframes


| Component | Priority | Estimated Time | Time Invested | Actual Time |
| --- | :---: |  :---: | :---: | :---: |
| Basic HTML Setup | H | 1hr| 30min | 30min |
| Basic CSS Setup & Styling | H | 2hr| 4hr| 4hr |
| Connect API| H | 1hr| 30min | 30min |
| Make First Get Request| H | 1hr| 30min | 30min |
| Target Correct Info from API | H | 2hrs| 1hr | 1hr |
| Target Correct Picture from API | H | 2hr| 1hr | 1hr|
| Creating Dynamic HTML Search Using EventListeners  | H | 3hr| 2hr| 2hr |
| Grab User Input from Search | H | 3hr| 1hr | 1hr |
| Display Correct Name and Info on Page| H | 3hr| 3hr | 3hr |
| Display Correct Picture on Page| H | 2hr| 1hr | 1hr |
| Clear Results After Making a New Search | H | 3hr| 30min | 30min |
| CSS Styling of Each Pokemon's 'Page' | L | 3hr| 4hr | 4hr |
| Flexbox Styling | L | 3hr| 4hr | 4hr |
| MediaQuery/(ies) | L | 1hr| 1hr | 1hr |
| Total | H | 30hr| 24hr | 24hr |

## Code Snippet

The descriptions of the Pokemon were from a different endpoint that the original one I used, so I had to make a second API call and I'm proud it works! 

```
try {
    const response = await axios.get(`${allPokemon}${pokemonName}`)
    

    let data = response.data
    showPokeData(data)

    const descriptions = await axios.get(`${pokeDescr}${pokemonName}`)
    let descriptionsData = descriptions.data
    showPokeDescription(descriptionsData)

  } catch (error) {
    alert(`Ooops! It looks like you didn't enter anything or what you entered was spelled incorrectly, try again!`)
  }
}
```

## Change Log 
I initially wanted to do a loading bar as a bonus, but I decided against that since I didn't want the user to feel like they were waiting any longer than necessary for the data. I opted for some other CSS animations instead, like a button the rotates and displays a message when hovered on and a "peeking" pikachu that appears when hovering on the footer. 

I also wasn't initially going to make the background color change based on the primary type of the pokemon, but without it, the site felt a little dry and boring. I like the change!  


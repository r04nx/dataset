# Machine Learning Datasets for Find-S and Candidate Elimination Algorithms

This directory contains datasets specifically designed for concept learning algorithms, particularly the Find-S and Candidate Elimination algorithms. These algorithms learn boolean concepts from positive and negative examples using discrete attribute values.

## Datasets Overview

### 1. EnjoySport Dataset (`enjoysport.csv`)
**Domain**: Sports activity recommendation  
**Target Concept**: Whether someone will enjoy a sport given weather conditions  
**Attributes**:
- Sky: {Sunny, Cloudy, Rainy}
- AirTemp: {Warm, Cold}
- Humidity: {Normal, High}
- Wind: {Strong, Weak}
- Water: {Warm, Cool}
- Forecast: {Same, Change}
- **Target**: EnjoySport {Yes, No}

**Use Case**: Classic example for demonstrating concept learning algorithms. Good for understanding how algorithms handle conjunctive concepts.

### 2. Restaurant Recommendation Dataset (`restaurant.csv`)
**Domain**: Restaurant recommendation system  
**Target Concept**: Whether to recommend a restaurant  
**Attributes**:
- Location: {Downtown, Suburb}
- Service: {Fast, Slow}
- Food: {Italian, Chinese, French}
- Price: {Cheap, Expensive}
- Music: {Loud, Quiet}
- **Target**: Target {Yes, No}

**Use Case**: Business domain example with multiple attribute values for some features.

### 3. Animal Classification Dataset (`animal_classification.csv`)
**Domain**: Animal classification  
**Target Concept**: Whether an animal is a mammal  
**Attributes**:
- Size: {Small, Medium, Large}
- Color: {Brown, Gray, Green, Black, White, Yellow, Red, Blue}
- Habitat: {Forest, Urban, Savanna, Arctic}
- Diet: {Carnivore, Omnivore, Herbivore, Insectivore}
- Sound: {Roar, Squeak, Trumpet, Chirp, Howl, Sing, Grunt, Chatter, Moo, Tweet}
- **Target**: Mammal {Yes, No}

**Use Case**: Biological classification with diverse attribute values and natural concept boundaries.

## Algorithm Compatibility

These datasets are specifically designed for:

### Find-S Algorithm
- Learns the most specific hypothesis consistent with positive examples
- Ignores negative examples
- Works well with all provided datasets

### Candidate Elimination Algorithm
- Maintains version space of all consistent hypotheses
- Uses both positive and negative examples
- Converges to target concept through boundary sets (G and S)

## Data Format

All datasets follow CSV format with:
- First row: attribute names (header)
- Last column: target concept (boolean: Yes/No)
- All other columns: discrete attribute values
- No missing values

## Usage Tips

1. **Preprocessing**: No preprocessing required - data is ready for algorithm input
2. **Attribute Ordering**: Attributes are ordered logically but can be reordered as needed
3. **Target Values**: All use "Yes"/"No" for consistency
4. **Size**: Datasets are small enough for manual verification of algorithm results

## Example Concept Learning

For EnjoySport dataset, a possible learned concept might be:
- Sky = Sunny AND AirTemp = Warm AND Humidity = ? AND Wind = ? AND Water = ? AND Forecast = ?

This represents: "Enjoy sport when it's sunny and warm, regardless of other conditions."

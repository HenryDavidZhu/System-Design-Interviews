# Boxing Profile Management Web App

## Step 1: System Requirements

### Use Cases

1. Be able to insert, edit, and delete a boxer's profile with the following attributes:
   1. Name (First and Last)
   2. Height
   3. Weight
   4. Weight Class
   5. Record (W-L-D and KOs)
2. Filter boxer profile by the following requirements:
   1. Name (First and/or Last)
   2. Height (from X ft Y in to X' ft Y' in)
   3. Weight (from X lbs to Y lbs)

### Constraints

No traffic and data handling constraints at the moment. May add scalability requirements in the future.

## Step 2: High-Level Architecture

![High Level Architecture](../../../HighLevelArchitecture.png)

## Step 3: Design Core Components

### Use Case: User filters boxers by their Name

Retrieve the result returned by the following SQL query:

`SELECT BoxerProfileDatabase FROM BoxerProfileTable `

`WHERE [low_bound] AND [upper_bound]`

And display it onto the webpage.

### Use Case: User filters boxers by their Height and Weight Range

Retrieve the result returned by the following SQL query:

`SELECT BoxerProfileDatabase FROM BoxerProfileTable `

`WHERE [height or weight] BETWEEN [low_bound] AND [upper_bound]`

And display it onto the webpage.
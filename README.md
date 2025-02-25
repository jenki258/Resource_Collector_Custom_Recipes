# Resource Collector Mod — Custom Recipe Guide  

Welcome to the **Resource Collector Mod**! This guide will walk you through how to add your own custom recipes and manage the default ones. Let’s get started!  

## 🛠️ How to Add Custom Recipes  

1. **Navigate to the Config Folder**  
   Go to your game’s `config` folder.  

2. **Create the Resource Collectors Folder**  
   Inside the `config` folder, create a new folder called:  

   ```
   resource_collectors
   ```

3. **Create a Recipe File**  
   In the `resource_collectors` folder, create a new JSON file. Name it like this:

   For Basic Generator:

   ```
   1generator.json
   ```

   For Nether Generator:
   ```
   1nethergenerator.json
   ```

   For End Generator:
   ```
   1endgenerator.json
   ```

   📝 **Important:** Replace the `1` with any number you want, up to `250` — that’s the current max cap.  
   (If you need more, request it on the [JenkiMods Discord Server](https://discord.gg/bJWbUsWAWk)).  

5. **Write the Recipe**  
   Open your newly created `.json` file and add this template:  

   ```json
   {
     "Input Core ID": "",
     "Output Item ID": "",
     "Time Needed to generate(In ticks)": 100,
     "Items Give Count": 1
   }
   ```

   Here’s what each field means:  

   - **`Input Core ID`**: The item ID of the core item — this item will **NOT** be consumed.  
   - **`Output Item ID`**: The item ID of what you want the generator to produce.  
   - **`Time Needed to generate(In ticks)`**: How long it takes to generate the output item (1 second = 20 ticks).  
   - **`Items Give Count`**: How many of the output item you’ll receive after the time has passed.  

   **Example Recipe:**  

   ```json
   {
     "Input Core ID": "minecraft:diamond_block",
     "Output Item ID": "minecraft:redstone",
     "Time Needed to generate(In ticks)": 200,
     "Items Give Count": 5
   }
   ```

   In this example:  
   - A **Diamond Block** is the core item (it won’t be consumed).  
   - After **10 seconds (200 ticks)**, you’ll get **5 Redstone**.  

## 🗑️ How to Remove Basic Recipes  

If you want to remove the default recipes that come with the mod:  

1. Go to the mod’s **config file**.  
2. Find the option for **regeneration of basic recipes**.  
3. Turn **regeneration off**.  

This will stop the mod from re-adding the default recipes when the game starts.  

## 💡 Item IDs  

Make sure to use the correct item IDs, like:  
- `minecraft:iron_ingot`  
- `minecraft:gold_nugget`  
- `minecraft:sugar`  


## 📝 Need More Slots?  

The current cap is **250** recipe files. If you hit the limit and need more, just hop into the **JenkiMods Discord Server** and request an increase!    

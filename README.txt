Development Environment: IntelliJ IDEA 2022.3.3 (Community Edition)

Setup Process:
MC Version: 1.19.4, Forge MDK: 45.0.27
Notes on initializing the project workspace from zipped file 'forge-1.19.4-45.0.27-mdk.zip'
- Clicked on 'MODID', used Shift+F6 to change to 'MOD_ID' and pressed Enter
- Changed ' MOD_ID = "examplemod" ' to ' MOD_ID = "bad" '
- Commented out ' public static final DeferredRegister<Block> BLOCKS ' through ' public static final RegistryObject<Item> EXAMPLE_BLOCK_ITEM '
  (Any blocks that are added will be registered in the class of the corresponding block)
- Commented out ' BLOCKS.register ' and ' ITEMS.register '
- Commented out contents of ' private void addCreative ', ' commonSetup ' and 'onClientSetup '
- Commented out ' on ServerStarting '
- Clicked on 'ExampleMod', used Shift+F6 to change to 'Bad' and pressed Enter
- In mods.toml
     changed ' license="All rights reserved" ' to ' license="MIT License" '
     changed ' modId="examplemod" ' to ' modId="bad" '
     changed ' displayName="Example Mod" ' to ' displayName="BAD by GGWP Gaming" '
     changed ' [[dependencies.examplemod]] ' to ' [[dependencies.bad]] ' in two places
     updated credits, authors, description
- In build.gradle
     changed ' version = '1.0' ' to ' version = '0.0.1-1.19.4' '
     changed ' group = 'com.yourname.modid' ' to ' group = 'net.ggwpgaming.bad' '
     changed ' archivesBaseName = 'modid' ' to ' archivesBaseName = 'bad' '
     changed ' mods { examplemod ' to ' mods { bad ' in four places
     updated Specification-Title, Specification-Vendor, Specification-Version, Implementation-Vendor
- Reloaded Gradle changes (used IntelliJ prompt, optionally CTRL+Shift+O or manually run in GUI)
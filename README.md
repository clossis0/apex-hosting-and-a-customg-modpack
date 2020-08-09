---- Minecraft Crash Report ----
// On the bright side, I bought you a teddy bear!

Time: 8/9/20 1:57 PM
Description: Exception in server tick loop

cpw.mods.fml.common.LoaderException: java.lang.NoClassDefFoundError: net/minecraft/client/gui/GuiScreen
	at cpw.mods.fml.common.LoadController.transition(LoadController.java:163)
	at cpw.mods.fml.common.Loader.preinitializeMods(Loader.java:559)
	at cpw.mods.fml.server.FMLServerHandler.beginServerLoading(FMLServerHandler.java:88)
	at cpw.mods.fml.common.FMLCommonHandler.onServerStart(FMLCommonHandler.java:314)
	at net.minecraft.server.dedicated.DedicatedServer.func_71197_b(DedicatedServer.java:117)
	at net.minecraft.server.MinecraftServer.run(MinecraftServer.java:387)
	at net.minecraft.server.MinecraftServer$2.run(MinecraftServer.java:685)
Caused by: java.lang.NoClassDefFoundError: net/minecraft/client/gui/GuiScreen
	at lumien.custommainmenu.CustomMainMenu.preInit(CustomMainMenu.java:57)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at cpw.mods.fml.common.FMLModContainer.handleModStateEvent(FMLModContainer.java:532)
	at sun.reflect.GeneratedMethodAccessor3.invoke(Unknown Source)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at com.google.common.eventbus.EventSubscriber.handleEvent(EventSubscriber.java:74)
	at com.google.common.eventbus.SynchronizedEventSubscriber.handleEvent(SynchronizedEventSubscriber.java:47)
	at com.google.common.eventbus.EventBus.dispatch(EventBus.java:322)
	at com.google.common.eventbus.EventBus.dispatchQueuedEvents(EventBus.java:304)
	at com.google.common.eventbus.EventBus.post(EventBus.java:275)
	at cpw.mods.fml.common.LoadController.sendEventToModContainer(LoadController.java:212)
	at cpw.mods.fml.common.LoadController.propogateStateMessage(LoadController.java:190)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at com.google.common.eventbus.EventSubscriber.handleEvent(EventSubscriber.java:74)
	at com.google.common.eventbus.SynchronizedEventSubscriber.handleEvent(SynchronizedEventSubscriber.java:47)
	at com.google.common.eventbus.EventBus.dispatch(EventBus.java:322)
	at com.google.common.eventbus.EventBus.dispatchQueuedEvents(EventBus.java:304)
	at com.google.common.eventbus.EventBus.post(EventBus.java:275)
	at cpw.mods.fml.common.LoadController.distributeStateMessage(LoadController.java:119)
	at cpw.mods.fml.common.Loader.preinitializeMods(Loader.java:556)
	... 5 more
Caused by: java.lang.ClassNotFoundException: net.minecraft.client.gui.GuiScreen
	at net.minecraft.launchwrapper.LaunchClassLoader.findClass(LaunchClassLoader.java:191)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
	... 32 more
Caused by: java.lang.RuntimeException: Attempted to load class bdw for invalid side SERVER
	at cpw.mods.fml.common.asm.transformers.SideTransformer.transform(SideTransformer.java:50)
	at net.minecraft.launchwrapper.LaunchClassLoader.runTransformers(LaunchClassLoader.java:279)
	at net.minecraft.launchwrapper.LaunchClassLoader.findClass(LaunchClassLoader.java:176)
	... 34 more


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- System Details --
Details:
	Minecraft Version: 1.7.10
	Operating System: Linux (amd64) version 3.10.0-1062.el7.x86_64
	Java Version: 1.8.0_252, Oracle Corporation
	Java VM Version: OpenJDK 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 3742136000 bytes (3568 MB) / 4151836672 bytes (3959 MB) up to 4151836672 bytes (3959 MB)
	JVM Flags: 4 total; -Xmx4096M -Xms4096M -XX:+UseConcMarkSweepGC -XX:+CMSClassUnloadingEnabled
	AABB Pool Size: 0 (0 bytes; 0 MB) allocated, 0 (0 bytes; 0 MB) used
	IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
	FML: MCP v9.05 FML v7.10.99.99 Minecraft Forge 10.13.4.1614 91 mods loaded, 91 mods active
	States: 'U' = Unloaded 'L' = Loaded 'C' = Constructed 'H' = Pre-initialized 'I' = Initialized 'J' = Post-initialized 'A' = Available 'D' = Disabled 'E' = Errored
	UCH	mcp{9.05} [Minecraft Coder Pack] (minecraft.jar) 
	UCH	FML{7.10.99.99} [Forge Mod Loader] (forge1710.jar) 
	UCH	Forge{10.13.4.1614} [Minecraft Forge] (forge1710.jar) 
	UCH	appliedenergistics2-core{rv3-beta-6} [Applied Energistics 2 Core] (minecraft.jar) 
	UCH	CodeChickenCore{1.0.7.47} [CodeChicken Core] (minecraft.jar) 
	UCH	NotEnoughItems{1.0.5.120} [Not Enough Items] (NotEnoughItems-1.7.10-1.0.5.120-universal.jar) 
	UCH	OpenModsCore{0.10} [OpenModsCore] (minecraft.jar) 
	UCH	<CoFH ASM>{000} [CoFH ASM] (minecraft.jar) 
	UCH	ItemBlacklist{1.2.0.8} [ItemBlacklist] (ItemBlacklist-1.7.10-1.2.0.8.jar) 
	UCH	bspkrsCore{6.15} [bspkrsCore] ([1.7.10]bspkrsCore-universal-6.15.jar) 
	UCH	Treecapitator{1.7.10} [Treecapitator] ([1.7.10]Treecapitator-universal-2.0.4.jar) 
	UCH	appliedenergistics2{rv3-beta-6} [Applied Energistics 2] (appliedenergistics2-rv3-beta-6.jar) 
	UCH	bdlib{1.9.4.109} [BD Lib] (bdlib-1.9.4.109-mc1.7.10.jar) 
	UCH	ae2stuff{0.5.0.56} [AE2 Stuff] (ae2stuff-0.5.0.56-mc1.7.10.jar) 
	UCH	CoFHCore{1.7.10R3.1.4} [CoFH Core] (CoFHCore-[1.7.10]3.1.4-329.jar) 
	UCH	asielib{0.4.9} [asielib] (AsieLib-1.7.10-0.4.9.jar) 
	UCH	Backpack{2.0.1} [Backpack] (backpack-2.0.1-1.7.x.jar) 
	UCH	Baubles{1.0.1.10} [Baubles] (Baubles-1.7.10-1.0.1.10.jar) 
	UCH	BiblioCraft{1.11.7} [BiblioCraft] (BiblioCraft[v1.11.7][MC1.7.10].jar) 
	UCH	ThermalFoundation{1.7.10R1.2.6} [Thermal Foundation] (ThermalFoundation-[1.7.10]1.2.6-118.jar) 
	UCH	ThermalExpansion{1.7.10R4.1.5} [Thermal Expansion] (ThermalExpansion-[1.7.10]4.1.5-248.jar) 
	UCH	BigReactors{0.4.3A} [Big Reactors] (BigReactors-0.4.3A.jar) 
	UCH	BiomesOPlenty{2.1.0} [Biomes O' Plenty] (BiomesOPlenty-1.7.10-2.1.0.1889-universal.jar) 
	UCH	bookshelf{1.0.4.187} [Bookshelf] (Bookshelf-1.7.10-1.0.4.187.jar) 
	UCH	Botania{r1.8-249} [Botania] (Botania r1.8-249.jar) 
	UCH	BrandonsCore{1.0.0.12} [Brandon's Core] (BrandonsCore-1.0.0.12.jar) 
	UCH	BuildCraft|Core{7.1.23} [BuildCraft] (buildcraft-7.1.23.jar) 
	UCH	BuildCraft|Transport{7.1.23} [BC Transport] (buildcraft-7.1.23.jar) 
	UCH	BuildCraft|Factory{7.1.23} [BC Factory] (buildcraft-7.1.23.jar) 
	UCH	BuildCraft|Silicon{7.1.23} [BC Silicon] (buildcraft-7.1.23.jar) 
	UCH	BuildCraft|Robotics{7.1.23} [BC Robotics] (buildcraft-7.1.23.jar) 
	UCH	BuildCraft|Energy{7.1.23} [BC Energy] (buildcraft-7.1.23.jar) 
	UCH	BuildCraft|Builders{7.1.23} [BC Builders] (buildcraft-7.1.23.jar) 
	UCH	TwilightForest{2.2.3} [The Twilight Forest] (Twilight+Forest+-+MC+1.7.2+-+2.2.3.jar) 
	UCH	ForgeMultipart{1.2.0.345} [Forge Multipart] (ForgeMultipart-1.7.10-1.2.0.345-universal.jar) 
	UCH	chisel{2.9.5.11} [Chisel] (Chisel-2.9.5.11.jar) 
	UCH	ComputerCraft{1.75} [ComputerCraft] (ComputerCraft1.75.jar) 
	UCH	endercore{1.7.10-0.2.0.39_beta} [EnderCore] (EnderCore-1.7.10-0.2.0.39_beta.jar) 
	UCH	Waila{1.5.10} [Waila] (Waila-1.5.10_1.7.10.jar) 
	UCH	EnderIO{1.7.10-2.3.0.429_beta} [Ender IO] (EnderIO-1.7.10-2.3.0.429_beta.jar) 
	UCH	MrTJPCoreMod{1.1.0.33} [MrTJPCore] (MrTJPCore-1.1.0.33-universal.jar) 
	UCH	ProjRed|Core{4.7.0pre12.95} [ProjectRed Core] (ProjectRed-1.7.10-4.7.0pre12.95-Base.jar) 
	UCH	computronics{1.6.6} [Computronics] (Computronics-1.7.10-1.6.6.jar) 
	UCH	controlling{1.0.0} [Controlling] (Controlling-1.7.10-1.0.0.jar) 
	UCE	CustomMainMenu{1.9.2} [Custom Main Menu] (CustomMainMenu-MC1.7.10-1.9.2.jar) 
	UCH	DraconicEvolution{1.0.2h} [Draconic Evolution] (Draconic-Evolution-1.7.10-1.0.2h.jar) 
	UCH	eplus{4.0.0..73} [Enchanting Plus] (EnchantingPlus-1.7.10-4.0.0.74.jar) 
	UCH	EnderStorage{1.4.7.38} [EnderStorage] (EnderStorage-1.7.10-1.4.7.38-universal.jar) 
	UCH	extracells{2.3.14} [Extra Cells 2] (ExtraCells-1.7.10-2.3.14b200.jar) 
	UCH	ExtraUtilities{1.2.12} [Extra Utilities] (extrautilities-1.2.12.jar) 
	UCH	factorization.notify{1.0} [Factorization Notification System] (Factorization-1.7.10-0.8.109.jar) 
	UCH	factorization.dimensionalSlice{0.8.109} [Factorization Dimensional Slices] (Factorization-1.7.10-0.8.109.jar) 
	UCH	factorization{0.8.109} [Factorization] (Factorization-1.7.10-0.8.109.jar) 
	UCH	factorization.misc{0.8.109} [Factorization Miscellaneous Nonsense] (Factorization-1.7.10-0.8.109.jar) 
	UCH	factorization.truth{0.8.109} [Truth] (Factorization-1.7.10-0.8.109.jar) 
	UCH	fz.scrap{0.8.109} [Scrap] (Factorization-1.7.10-0.8.109.jar) 
	UCH	iChunUtil{4.2.3} [iChunUtil] (iChunUtil-4.2.3.jar) 
	UCH	Hats{4.0.1} [Hats] (Hats-4.0.1.jar) 
	UCH	InventoryPets{1.5.2} [Inventory Pets] (inventorypets-1.7.10-1.5.2-universal.jar) 
	UCH	ironbackpacks{1.7.10-1.2.20} [Iron Backpacks] (IronBackpacks-1.7.10-1.2.20.jar) 
	UCH	IronChest{6.0.62.742} [Iron Chest] (ironchest-1.7.10-6.0.62.742-universal.jar) 
	UCH	journeymap{5.1.4p2} [JourneyMap] (journeymap-1.7.10-5.1.4p2-unlimited.jar) 
	UCH	magicalcrops{4.0.0_PUBLIC_BETA_4b} [Magical Crops: Core] (magicalcrops-4.0.0_PUBLIC_BETA_5.jar) 
	UCH	Mantle{1.7.10-0.3.2.jenkins191} [Mantle] (Mantle-1.7.10-0.3.2b.jar) 
	UCH	Morph{0.9.3} [Morph] (Morph-Beta-0.9.3.jar) 
	UCH	Morpheus{1.7.10-1.6.21} [Morpheus] (Morpheus-1.7.10-1.6.21.jar) 
	UCH	cfm{3.4.7} [ï¿½9MrCrayfish's Furniture Mod] (MrCrayfishFurnitureModv3.4.7(1.7.10).jar) 
	UCE	Neat{GRADLE:VERSION-GRADLE:BUILD} [Neat] (Neat+1.0-1.jar) 
	UCH	necromancy{1.7.2} [Necromancy] (Necromancy-1.7.10a.jar) 
	UCH	NetherOres{1.7.10R2.3.1} [Nether Ores] (NetherOres-[1.7.10]2.3.1-22.jar) 
	UCH	OpenMods{0.10} [OpenMods] (OpenModsLib-1.7.10-0.10.jar) 
	UCH	OpenBlocks{1.6} [OpenBlocks] (OpenBlocks-1.7.10-1.6.jar) 
	UCH	ProjectE{1.7.10-PE1.10.1} [ProjectE] (ProjectE-1.7.10-PE1.10.1.jar) 
	UCH	ProjRed|Transmission{4.7.0pre12.95} [ProjectRed Transmission] (ProjectRed-1.7.10-4.7.0pre12.95-Integration.jar) 
	UCH	ProjRed|Transportation{4.7.0pre12.95} [ProjectRed Transportation] (ProjectRed-1.7.10-4.7.0pre12.95-Mechanical.jar) 
	UCH	ProjRed|Exploration{4.7.0pre12.95} [ProjectRed Exploration] (ProjectRed-1.7.10-4.7.0pre12.95-World.jar) 
	UCH	TConstruct{1.7.10-1.8.8.build988} [Tinkers' Construct] (TConstruct-1.7.10-1.8.8.jar) 
	UCH	ProjRed|Compatibility{4.7.0pre12.95} [ProjectRed Compatibility] (ProjectRed-1.7.10-4.7.0pre12.95-Compat.jar) 
	UCH	ProjRed|Integration{4.7.0pre12.95} [ProjectRed Integration] (ProjectRed-1.7.10-4.7.0pre12.95-Integration.jar) 
	UCH	ProjRed|Fabrication{4.7.0pre12.95} [ProjectRed Fabrication] (ProjectRed-1.7.10-4.7.0pre12.95-Fabrication.jar) 
	UCH	ProjRed|Illumination{4.7.0pre12.95} [ProjectRed Illumination] (ProjectRed-1.7.10-4.7.0pre12.95-Lighting.jar) 
	UCH	ProjRed|Expansion{4.7.0pre12.95} [ProjectRed Expansion] (ProjectRed-1.7.10-4.7.0pre12.95-Mechanical.jar) 
	UCH	ThermalDynamics{1.7.10R1.2.1} [Thermal Dynamics] (ThermalDynamics-[1.7.10]1.2.1-172.jar) 
	UCH	VeinMiner{0.36.0_1.7.10-28a7f13} [Vein Miner] (VeinMiner-1.7.10-0.36.0.496+28a7f13.jar) 
	UCH	VeinMinerModSupport{0.36.0_1.7.10-28a7f13} [Mod Support] (VeinMiner-1.7.10-0.36.0.496+28a7f13.jar) 
	UCH	witchery{0.24.1} [Witchery] (witchery-1.7.10-0.24.1.jar) 
	UCH	McMultipart{1.2.0.345} [Minecraft Multipart Plugin] (ForgeMultipart-1.7.10-1.2.0.345-universal.jar) 
	UCH	ForgeRelocation{0.0.1.4} [ForgeRelocation] (ForgeRelocation-0.0.1.4-universal.jar) 
	UCH	MCFrames{1.0} [MCFrames] (ForgeRelocation-0.0.1.4-universal.jar) 
	UCH	RelocationFMP{0.0.1.2} [RelocationFMP] (ForgeRelocationFMP-0.0.1.2-universal.jar) 
	UCH	ForgeMicroblock{1.2.0.345} [Forge Microblocks] (ForgeMultipart-1.7.10-1.2.0.345-universal.jar) 
	OpenModsLib class transformers: [stencil_patches:ENABLED],[movement_callback:ENABLED],[player_damage_hook:FINISHED],[map_gen_fix:FINISHED],[gl_capabilities_hook:ENABLED],[player_render_hook:ENABLED]
	Class transformer null safety: found misbehaving transformers: me.guichaguri.betterfps.transformers.MathTransformer(me.guichaguri.betterfps.transformers.MathTransformer@1e25c39b) returned non-null result: 0,me.guichaguri.betterfps.transformers.EventTransformer(me.guichaguri.betterfps.transformers.EventTransformer@71c4131e) returned non-null result: 0
	AE2 Version: beta rv3-beta-6 for Forge 10.13.4.1448
	CoFHCore: -[1.7.10]3.1.4-329
	ThermalFoundation: -[1.7.10]1.2.6-118
	ThermalExpansion: -[1.7.10]4.1.5-248
	Mantle Environment: Environment healthy.
	NetherOres: -[1.7.10]2.3.1-22
	TConstruct Environment: Environment healthy.
	ThermalDynamics: -[1.7.10]1.2.1-172
	List of loaded APIs: 
		* appliedenergistics2|API (rv3) from appliedenergistics2-rv3-beta-6.jar
		* asielibAPI (1.1) from AsieLib-1.7.10-0.4.9.jar
		* asielibAPI|chat (1.0) from AsieLib-1.7.10-0.4.9.jar
		* asielibAPI|tile (1.0) from AsieLib-1.7.10-0.4.9.jar
		* asielibAPI|tool (1.1) from AsieLib-1.7.10-0.4.9.jar
		* Baubles|API (1.0.1.10) from inventorypets-1.7.10-1.5.2-universal.jar
		* BiomesOPlentyAPI (1.0.0) from BiomesOPlenty-1.7.10-2.1.0.1889-universal.jar
		* BotaniaAPI (76) from Botania r1.8-249.jar
		* BuildCraftAPI|blocks (1.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|blueprints (1.5) from buildcraft-7.1.23.jar
		* BuildCraftAPI|boards (2.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|core (2.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|crops (1.1) from buildcraft-7.1.23.jar
		* BuildCraftAPI|events (2.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|facades (1.1) from buildcraft-7.1.23.jar
		* BuildCraftAPI|filler (4.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|fuels (2.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|gates (4.1) from buildcraft-7.1.23.jar
		* BuildCraftAPI|items (1.1) from buildcraft-7.1.23.jar
		* BuildCraftAPI|library (2.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|lists (1.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|power (1.3) from buildcraft-7.1.23.jar
		* BuildCraftAPI|recipes (3.1) from buildcraft-7.1.23.jar
		* BuildCraftAPI|robotics (3.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|statements (1.1) from buildcraft-7.1.23.jar
		* BuildCraftAPI|tablet (1.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|tiles (1.2) from buildcraft-7.1.23.jar
		* BuildCraftAPI|tools (1.0) from buildcraft-7.1.23.jar
		* BuildCraftAPI|transport (4.1) from buildcraft-7.1.23.jar
		* ChiselAPI (0.1.1) from Chisel-2.9.5.11.jar
		* ChiselAPI|Carving (0.1.1) from Chisel-2.9.5.11.jar
		* ChiselAPI|Rendering (0.1.1) from Chisel-2.9.5.11.jar
		* CoFHAPI (1.7.10R1.0.2) from BrandonsCore-1.0.0.12.jar
		* CoFHAPI|block (1.7.10R1.0.13) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* CoFHAPI|core (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|energy (1.7.10R1.0.2) from buildcraft-7.1.23.jar
		* CoFHAPI|fluid (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|inventory (1.7.10R1.0.13) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* CoFHAPI|item (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|modhelpers (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|tileentity (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHAPI|transport (1.7.10R1.0.13) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* CoFHAPI|world (1.7.10R1.3.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|audio (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|container (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|element (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|element|listbox (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|gui|slot (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|inventory (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|render (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|render|particle (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|util (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|util|helpers (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|util|position (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|world (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* CoFHLib|world|feature (1.7.10R1.2.1) from CoFHCore-[1.7.10]3.1.4-329.jar
		* ComputerCraft|API (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|FileSystem (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|Lua (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|Media (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|Peripheral (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|Permissions (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|Redstone (1.75) from ComputerCraft1.75.jar
		* ComputerCraft|API|Turtle (1.75) from ComputerCraft1.75.jar
		* computronicsAPI (1.3) from Computronics-1.7.10-1.6.6.jar
		* computronicsAPI|audio (1.0) from Computronics-1.7.10-1.6.6.jar
		* computronicsAPI|chat (1.3) from Computronics-1.7.10-1.6.6.jar
		* computronicsAPI|multiperipheral (1.1) from Computronics-1.7.10-1.6.6.jar
		* computronicsAPI|tape (1.0) from Computronics-1.7.10-1.6.6.jar
		* DraconicEvolution|API (1.2) from Draconic-Evolution-1.7.10-1.0.2h.jar
		* EnderIOAPI (0.0.2) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* EnderIOAPI|Redstone (0.0.2) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* EnderIOAPI|Teleport (0.0.2) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* EnderIOAPI|Tools (0.0.2) from EnderIO-1.7.10-2.3.0.429_beta.jar
		* factorization notification system (1.0) from Factorization-1.7.10-0.8.109.jar
		* ForgeRelocation|API (0.0.1.4) from ForgeRelocation-0.0.1.4-universal.jar
		* OpenBlocks|API (1.1) from OpenBlocks-1.7.10-1.6.jar
		* ProjectEAPI (7) from ProjectE-1.7.10-PE1.10.1.jar
		* VeinMinerApi (0.3) from VeinMiner-1.7.10-0.36.0.496+28a7f13.jar
		* WailaAPI (1.2) from Waila-1.5.10_1.7.10.jar
	Chisel: Errors like "[FML]: Unable to lookup ..." are NOT the cause of this crash. You can safely ignore these errors. And update forge while you're at it.
	EnderIO: Found the following problem(s) with your installation:
                  * An unknown AE2 API is installed (rv3 from appliedenergistics2-rv3-beta-6.jar).
                    Ender IO was build against API version rv2 and may or may not work with a newer version.
                 This may have caused the error. Try reproducing the crash WITHOUT this/these mod(s) before reporting it.
	Profiler Position: N/A (disabled)
	Is Modded: Definitely; Server brand changed to 'fml,forge'
	Type: Dedicated Server (map_server.txt)

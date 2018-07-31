# Blen64
Blender scripts to convert and export mesh objects to draw lists as C header files for use with the n64 SDK
![Mesh output example](https://cdn.discordapp.com/attachments/445463417797738496/472802908803563540/unknown.png "BrickWall")

# V2.2 - beta
# Change log:
- Fixed poly buffer limit issues
- Added Vertex Color Support
- Fixed missing vert/face disarray issue
- Cleaned up some code

# Usage:
1.<Setup>
Simply download the latest script and load it into blenders text editor. Simply select the model you wish to convert and run the script.
![Setup](https://media.discordapp.net/attachments/434689798817579008/473758873191448576/unknown.png?width=1435&height=898 "Blender")

# Cautionary Note:
Blen64 in it's current state is extremely unequipped to optimize for poly count, that is to say IT WILL EAT UP YOUR VETEX BUDGET, in short it because we are building draw lists from poly loop indices we end up with duplicate vertices, essentially there are duplicate vertices for every face connected to a point, in turn faces aren't technically connected(hence the weird shading effect since surfaces cant be smoothed). This shouldn't be a problem for long and I have a couple different solutions in the works.

# Feature Roadmap:
- Fix the last of the SAIFAV(super annoying incorect faces and vertices) bugs.
- GUI based interface(having to run scripts is tiresome)
- integrate render modes(opaque, translucent, cutout etc.)
- add multi object support
- possible auto save to header

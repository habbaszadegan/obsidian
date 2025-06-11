<%*
const folderName = await tp.system.prompt("Enter project name")

// Create Markdown notes
await tp.file.create_new("", folderName + "/Overview")
await tp.file.create_new("", folderName + "/Tasks")
await tp.file.create_new("", folderName + "/Notes")

// Create a valid Canvas file
const canvasContent = `{
  "nodes": [],
  "edges": [],
  "version": "1.0.0"
}`

const canvasPath = folderName + "/Mindmap.canvas"
await app.vault.create(canvasPath, canvasContent)
%>

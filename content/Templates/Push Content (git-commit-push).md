---
draft: true
---
<%*
const { execSync } = require('child_process');
const commitMessage = await tp.system.prompt("Enter commit message");

// Define the root directory of your Git repository
const gitRoot = "C:/Users/AceOfHeaVeN/OneDrive/Desktop/Programming Projects/quartz";

// Run Git commands
execSync("git add .", { cwd: gitRoot });
execSync(`git commit -m "${commitMessage}"`, { cwd: gitRoot });
execSync("git push", { cwd: gitRoot });

%>

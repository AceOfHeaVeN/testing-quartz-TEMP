<%*
const { execSync } = require('child_process');

// Define the root directory of your Git repository
const gitRoot = "C:/Users/AceOfHeaVeN/OneDrive/Desktop/Programming Projects/quartz";

// Define a default commit message
const commitMessage = "Update notes";

try {
    execSync("git add .", { cwd: gitRoot });
    execSync(`git commit -m "${commitMessage}"`, { cwd: gitRoot });
    execSync("git push", { cwd: gitRoot });
    // Display a notification in Obsidian
    app.workspace.trigger("file-open", { path: "Updating Notes" });
    new Notice("Notes updated successfully.");
} catch (error) {
    new Notice(`Error: ${error.toString()}`, 5000); // Display error message for 5 seconds
    console.error(`Error: ${error.toString()}`);
}
%>

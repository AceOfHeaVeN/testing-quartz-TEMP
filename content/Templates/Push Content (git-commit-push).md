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
    // Logging for verification in console (not added to the note)
    console.log("Changes committed and pushed successfully.");
} catch (error) {
    console.error(`Error: ${error.toString()}`);
}
%>

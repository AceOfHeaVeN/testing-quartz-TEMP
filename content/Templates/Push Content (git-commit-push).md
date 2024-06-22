<%*
const { execSync } = require('child_process');
const commitMessage = await tp.system.prompt("Enter commit message");

// Define the root directory of your Git repository
const gitRoot = "C:/Users/AceOfHeaVeN/OneDrive/Desktop/Programming Projects/quartz";

try {
    execSync("git add .", { cwd: gitRoot });
    const commitResult = execSync(`git commit -m "${commitMessage}"`, { cwd: gitRoot });
    const pushResult = execSync("git push", { cwd: gitRoot });
    tR += `Commit Result: ${commitResult.toString()}\n`;
    tR += `Push Result: ${pushResult.toString()}\n`;
    tR += "Changes committed and pushed successfully.";
} catch (error) {
    tR += `Error: ${error.toString()}\n`;
}
%>

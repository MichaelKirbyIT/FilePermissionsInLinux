<h1>File Permissions in Linux</h1>

<h2>Description</h2>
Through Linux commands, I intend to demonstrate skills I have acquired with the Linux operating system. <br />
<ul>
  <li>Displaying file structure and directory details</li>
  <li>Deciphering a permissions string </li>
  <li>Adjusting file and directory permissions </li>
</ul>
<br />


<h2>Languages and Utilities Used</h2>

- <b>Linux Command Line</b> 

<h2>Environments Used </h2>

- <b>Windows 10</b>

<h2>Program walk-through:</h2>

<h3>Part 1: Check file and directory details
</h3>

<img src="https://i.imgur.com/M1FU4EX.png" height="80%" width="80%" alt="File and Directory Details"/>

<p>
In this demonstration: <br />
  <ul> 
    <li>ls displays the names and files of the current directory</li>
      <li>ls -la displays permissions to files and directories, the a displays hidden files and directories with permissions.</li>
        <li>“researcher2” is the name of the group: user</li>
          <li>“research_team” is the name of the group: group</li>
  </ul>
</p>

<br />

<h3>Part 2: The Permissions String
</h3>

<p>
The permissions string is a 10 character string displaying permissions for three groups: user, group, and other along with a character distinguishing whether or not you are viewing a file or directory.
<ul>
<li>The first character is either a “d” or “-”, d for directory and - for file.</li>
  <li>The 2nd character is either a “r” for read permissions or a “-” for no read permissions.</li>
    <li>The 3rd character is either a “w” for write permissions or a “-” for no write permissions.</li>
      <li>The 4th character is either a “x” for execute permissions or a “-” for no execute permissions.</li>
        <li>The 2nd, 3rd, and 4th characters are for the group “user” permissions.</li>
          <li>The 5th, 6th, and 7th characters are for the group “group” permissions.</li>
            <li>The 8th, 9th, and 10th characters are for the group “other” permissions.</li>
</ul>

<img src="https://i.imgur.com/9fsjFKg.png" height="80%" width="80%" alt="File Permissions Example 1"/>

<p>
In this example, drafts is a directory indicated by the blue name, and the “d” in the 10 character string at the front. The next three characters (rwx) are for the user group indicating the user group has read, write, and execute permissions. The next three characters (--x) are for the group:group indicating the group group has execute permissions, but can not read or write to the file. The last three characters (---) indicate that the other group has no permissions on this directory.
<p>

<h3>Part 3: Change file permissions</h3>

<img src="https://i.imgur.com/XF0mjek.png" height="80%" width="80%" alt="File Permissions Example 3"/>

<p>The chmod o-w project_k.txt command has revoked write permissions for the group: other</p>

<img src="https://i.imgur.com/XF0mjek.png" height="80%" width="80%" alt="File Permissions Example 3"/>

<p>The chmod g-r project_m.txt command has revoked read permissions for the group: group</p>

<h3>Part 4: Change file permissions on a hidden file</h3>

<img src="https://i.imgur.com/hCM4GV1.png" height="80%" width="80%" alt="File Permissions Example 4"/>

<p>In this demonstration the hidden file .project_x.txt is an archived file. The intended permissions are for user and group groups to have read only permissions to the file. As you can see on the first displayed string, the user group has read and write permissions and the group group has write permission and not read permission. I execute the chmod u-w,g-w,g+r .project_x.txt command in order to revoke write permissions from the user and group groups, and grant the group with read permissions on the .project_x.txt file.</p>

<h3>Part 5: Change directory permissions</h3>

<img src="https://i.imgur.com/Na1Pltv.png" height="80%" width="80%" alt="File Permissions Example 5"/>

<p>In this demonstration, I have changed the permissions on the drafts directory. Through the chmod g-x drafts command, I was able to revoke execute permissions from the group: group.</p>

<h3>Summary</h3>

<p>In this example, I used commands using ls and ls -la, which list files and directories in my current working directory and chmod, which update current permissions on a file or directory. By executing these commands, I have demonstrated my ability to manage authorization of various groups for files and directories. I have also shown that I understand a basic file/directory structure and permissions on the Linux operating system.</p>

o make the application start on your "monitor 4", you need to modify the MonitorIndex setting in the application's configuration file.

  Here are the steps:

   1. Locate the configuration file: Navigate to the publish directory of your application:
      C:\projects\live-draw\LiveDraw\bin\Release\net8.0-windows\win-x86\publish\
      In this directory, you will find a file named LiveDraw.exe.config.

   2. Open `LiveDraw.exe.config` with a text editor (like Notepad, VS Code, etc.).

   3. Find the `appSettings` section. It should look something like this:
   1     <appSettings>
   2         <add key="MonitorIndex" value="0"/>
   3     </appSettings>

   4. Change the `value` for `MonitorIndex` to `3`.
      Since monitor indices are zero-based, 0 is your primary monitor, 1 is your second, 2 is your third, and 3 will be your fourth monitor.
      Modify the line to:

   1     <add key="MonitorIndex" value="3"/>

   1. Save the `LiveDraw.exe.config` file.

   2. Launch the `LiveDraw.exe` application. It should now open on your fourth monitor.

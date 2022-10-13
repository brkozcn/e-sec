Set objScriptShell = CreateObject("Wscript.Shell")
kill "TeacherMan"
kill ""
kill ""


Sub kill(value1)
    objScriptShell.Run "taskkill /f /im "&value1&".exe", 0, true
End Sub

If Err.Number = 0 Then
    WScript.Echo "It worked!"
Else
    WScript.Echo "Error:"
    WScript.Echo Err.Number & " Srce: " & Err.Source & " Desc: " &  Err.Description
    Err.Clear
End If

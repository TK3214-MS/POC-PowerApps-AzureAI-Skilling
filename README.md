b. Update the property values

| Screen | Control | Property | Value |
| ----- | ----- | ----- | ----- |
| Screen1 | Camera1 | OnSelect | Navigate(cameraresult); Set(tmpimg,Camera1.Photo); |
| cameraresult | Image1 | Image | tmpimg |
| cameraresult | Button11 | OnSelect | Set(pic,Image1.Image);<br>Set(predres,CustomVision.DetectImageV2("Custom Vision Project ID","Custom Vision Iteration Name",pic).predictions) |
| cameraresult | Buttonl1 | Text | "CHECK IMAGE" |
| cameraresult | Label1 | Text | "RESULT : "& First(predres).tagName |
| cameraresult | Label2 | Text | "AI CONFIDENCE : "& First(predres).probability*100 & "%" |
| cameraresult | Button2 | OnSelect | Navigate(Screen1) |
# logrusIndifferentFiles
Generate logs with logrus in different files with different fields having log rotation with lumberjack

The program will geneate 3 files :
file1.log
file1Info.log
file2.log

file1.log generates log only for following log levels:
logrus.PanicLevel,
logrus.FatalLevel,
logrus.ErrorLevel,
logrus.WarnLevel

file1Info.log generates log only for following log levels:
logrus.InfoLevel,
logrus.DebugLevel


file2.log generates log only for following log levels: 
logrus.InfoLevel,
logrus.DebugLevel


file1.log and file1Info.log has following log fields:
"osplatform": runtime.GOOS,
		"osarch":     runtime.GOARCH,
		"deviceId":   "kucch bhi nahi h",
		"type":       "HookOne",
 
 file2.log has following log fields:
 
 "osplatform": runtime.GOOS,
		"osarch":     runtime.GOARCH,
		"type":       "HookTwo",
    
   
   
   all 3 files are rotated by lumberjack when either the size of the file is 1MB or age is 1 day.
   
   

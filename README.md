# RzUpdater

修复mac上RzUpdater因数组越界崩溃的问题

```
2023-09-26 09:49:29.364 RzUpdater[3457:25993] *** Terminating app due to uncaught exception 'NSRangeException', reason: '*** -[__NSSingleObjectArrayI objectAtIndex:]: index 1 beyond bounds [0 .. 0]'
*** First throw call stack:
(
	0   CoreFoundation                      0x00007ff80d75718a __exceptionPreprocess + 242
	1   libobjc.A.dylib                     0x00007ff80d27d42b objc_exception_throw + 48
	2   CoreFoundation                      0x00007ff80d68e5d2 -[__NSSingleObjectArrayI objectAtIndex:] + 112
	3   RzUpdater                           0x0000000100059141 -[RzDataSyncMainController getProductName:aProfile:] + 452
	4   RzUpdater                           0x000000010005841d -[RzDataSyncMainController newSettingListData:] + 48
	5   RzUpdater                           0x0000000100023041 -[RzUpdaterMainController didReceiveResponse:] + 4918
	6   libdispatch.dylib                   0x00007ff80d463033 _dispatch_client_callout + 8
	7   libdispatch.dylib                   0x00007ff80d470c60 _dispatch_async_and_wait_invoke + 87
	8   libdispatch.dylib                   0x00007ff80d463033 _dispatch_client_callout + 8
	9   libdispatch.dylib                   0x00007ff80d46ffcf _dispatch_main_queue_drain + 954
	10  libdispatch.dylib                   0x00007ff80d46fc07 _dispatch_main_queue_callback_4CF + 31
	11  CoreFoundation                      0x00007ff80d71f205 __CFRUNLOOP_IS_SERVICING_THE_MAIN_DISPATCH_QUEUE__ + 9
	12  CoreFoundation                      0x00007ff80d6def2f __CFRunLoopRun + 2452
	13  CoreFoundation                      0x00007ff80d6ddf31 CFRunLoopRunSpecific + 560
	14  HIToolbox                           0x00007ff81715ef3d RunCurrentEventLoopInMode + 292
	15  HIToolbox                           0x00007ff81715ed4e ReceiveNextEventCommon + 657
	16  HIToolbox                           0x00007ff81715eaa8 _BlockUntilNextEventMatchingListInModeWithFilter + 64
	17  AppKit                              0x00007ff81077a25c _DPSNextEvent + 858
	18  AppKit                              0x00007ff810779106 -[NSApplication(NSEvent) _nextEventMatchingEventMask:untilDate:inMode:dequeue:] + 1214
	19  AppKit                              0x00007ff81076b788 -[NSApplication run] + 586
	20  AppKit                              0x00007ff81073f9a1 NSApplicationMain + 817
	21  RzUpdater                           0x00000001000014f4 start + 52
)
```

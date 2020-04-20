## Linux Kernel Debugging Skills

### General Debugging

Many debugging infrastructures provided by Linux Kernel that can be enabled as necessary based on which subsystem need to debug.

| Kernel Debug Config Options | Description                                                  | Default Value                           |
| --------------------------- | ------------------------------------------------------------ | --------------------------------------- |
| CONFIG_DEBUG_USER           | When a user space process is killed due to a segfault or illegal instruction, a message will be printed out<br />arch/arm/Kconfig.debug | =Y<br />kernel boot param:user_debug=31 |
| CONFIG_FREE_PAGES_RDONLY    | Enable this options to mark pages as read only to trigger a fault if any code attempt to write to page on the buddy list. This may have a performance impact.<br />arch/arm/Kconfig.debug | =N                                      |
| CONF_ARM_PTDUMP             | Show the kernel pagetable layout in a debug file.<br />arch/arm/Kconfig.debug | =N                                      |
| CONFIG_ARM_UNWIND           | Enables stack unwinding support in the kernel using the info auto generated by the compiler. Kernel size is slightly bigger but no performance impact. | =Y                                      |

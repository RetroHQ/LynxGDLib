# Project Title

Library for using features of the LynxGD cartridge for the Atari Lynx from RetroHQ.

## Getting Started

Add LynxGD.c and LynxGD.h to your CC65 Lynx project and include LynxGD.h.

Call LynxGD_Init() first at the beginning of your program before acessing any other commands.

## Examples

### Reading a File

```
if (LynxGD_OpenFile("/myfile.bin") == FR_OK)
{
	char mem[16];
	LynxGD_ReadFile(mem, 16);
	LynxGD_CloseFile();
}
```

### Writing a File

Note: The LynxGD is unable to create files, so the file MUST EXIST already on the memory card.

```
if (LynxGD_OpenFile("/hiscore.bin") == FR_OK)
{
	char mem[16]; // initialise to data to write
	LynxGD_WriteFile(mem, 16);
	LynxGD_CloseFile();
}
```

## License

This code is free to do with as you please.
# WagoSysCom Internal PFC Documentation

Generated from WAGO library documentation.

**Library Path:** `WagoSysCom_Internal_PFC`

## Table of Contents

- [General](#general)
  - [ParameterList (PARAMS)](#parameterlist-params)
  - [VersionHistory (GVL)](#versionhistory-gvl)
- [Hardware Lines](#hardware-lines)
  - [20 Hardware Lines](#20-hardware-lines)
- [Methods](#methods)
  - [FbSerialInterface_internal.AttachExclusively (METH)](#fbserialinterface_internalattachexclusively-meth)
  - [FbSerialInterface_internal.ClearBuffers (METH)](#fbserialinterface_internalclearbuffers-meth)
  - [FbSerialInterface_internal.Close (METH)](#fbserialinterface_internalclose-meth)
  - [FbSerialInterface_internal.Configure (METH)](#fbserialinterface_internalconfigure-meth)
  - [FbSerialInterface_internal.Cyclic (METH)](#fbserialinterface_internalcyclic-meth)
  - [FbSerialInterface_internal.Finish (METH)](#fbserialinterface_internalfinish-meth)
  - [FbSerialInterface_internal.ForceDetachment (METH)](#fbserialinterface_internalforcedetachment-meth)
  - [FbSerialInterface_internal.GetErrorObject (METH)](#fbserialinterface_internalgeterrorobject-meth)
  - [FbSerialInterface_internal.GetLineState (METH)](#fbserialinterface_internalgetlinestate-meth)
  - [FbSerialInterface_internal.Initialize (METH)](#fbserialinterface_internalinitialize-meth)
  - [FbSerialInterface_internal.IsLineAvailable (METH)](#fbserialinterface_internalislineavailable-meth)
  - [FbSerialInterface_internal.Open (METH)](#fbserialinterface_internalopen-meth)
  - [FbSerialInterface_internal.Read (METH)](#fbserialinterface_internalread-meth)
  - [FbSerialInterface_internal.RegisterSniffer (METH)](#fbserialinterface_internalregistersniffer-meth)
  - [FbSerialInterface_internal.ReleaseExclusivity (METH)](#fbserialinterface_internalreleaseexclusivity-meth)
  - [FbSerialInterface_internal.SetLineState (METH)](#fbserialinterface_internalsetlinestate-meth)
  - [FbSerialInterface_internal.TestExclusivity (METH)](#fbserialinterface_internaltestexclusivity-meth)
  - [FbSerialInterface_internal.UnregisterSniffer (METH)](#fbserialinterface_internalunregistersniffer-meth)
  - [FbSerialInterface_internal.Write (METH)](#fbserialinterface_internalwrite-meth)
- [Interfaces](#interfaces)
  - [10 I_WagoSysComBase](#10-i_wagosyscombase)
  - [10 Main Interface](#10-main-interface)
  - [20 I_SupportComSniffer](#20-i_supportcomsniffer)
  - [FbSerialInterface_internal (FB)](#fbserialinterface_internal-fb)
  - [FbSerialInterface_internal.DeferredResult (PROP)](#fbserialinterface_internaldeferredresult-prop)
  - [FbSerialInterface_internal.IsTransmitterEmpty (PROP)](#fbserialinterface_internalistransmitterempty-prop)
  - [FbSerialInterface_internal.Name (PROP)](#fbserialinterface_internalname-prop)
  - [FbSerialInterface_internal.isOpen (PROP)](#fbserialinterface_internalisopen-prop)
- [Administration](#administration)
  - [40 Administration](#40-administration)
- [Exclusive Use](#exclusive-use)
  - [30 Exclusive Use](#30-exclusive-use)
- [Module Fields](#module-fields)
  - [10 Documentation](#10-documentation)
  - [20 Program Organization Units](#20-program-organization-units)
- [Documentation](#documentation)
  - [doc10_general (FB)](#doc10_general-fb)

## General

### ParameterList (PARAMS)

**File:** `ParameterList.html`

#### Interface Variables

| Scope | Name | Type | Initial | Comment |
| --- | --- | :---: | --- | :--- |
| Constant | cudiMaxComNumber | UDINT | 32767 | Highest ordinal number for OS-serial interfaces. (Must be less than 32768) |

#### Details

ParameterList (PARAMS)¶

InOut:









Scope
Name
Type
Initial
Comment



Constant
cudiMaxComNumber

UDINT
32767
Highest ordinal number for OS-serial interfaces. (Must be
less than 32768) ParameterList (PARAMS)¶

InOut:









Scope
Name
Type
Initial
Comment



Constant
cudiMaxComNumber

UDINT
32767
Highest ordinal number for OS-serial interfaces. (Must be
less than 32768) ParameterList (PARAMS)¶

InOut:









Scope
Name
Type
Initial
Comment



Constant
cudiMaxComNumber

UDINT
32767
Highest ordinal number for OS-serial interfaces. (Must be
less than 32768) ParameterList (PARAMS)¶

InOut:









Scope
Name
Type
Initial
Comment



Constant
cudiMaxComNumber

UDINT
32767
Highest ordinal number for OS-serial interfaces. (Must be
less than 32768) InOut:









Scope
Name
Type
Initial
Comment



Constant
cudiMaxComNumber

UDINT
32767
Highest ordinal number for OS-serial interfaces. (Must be
less than 32768) Scope
Name
Type
Initial
Comment



Constant
cudiMaxComNumber

UDINT
32767
Highest ordinal number for OS-serial interfaces. (Must be
less than 32768)

---

### VersionHistory (GVL)

**File:** `VersionHistory.html`

WagoSysCom_Internal_PFC.library

#### Additional Information

| Name | Type |
| --- | :---: |
| Info | ProjectInfo |

| Column 1 | Column 2 | Column 3 | Column 4 |
| --- | --- | --- | --- |
| date | version | author | change |
| 20.03.2023 | 1.0.2.7 | u013972 | Resolve types by namespace |
| 23.10.2023 | 1.0.2.6 | u010663 | 64-Bit adjustment ->SysTypes2Interfaces |
| 22.06.2023 | 1.0.2.5 | u013972 | Revert publishing symbols of underlying libraries |
| 07.12.2020 | 1.0.2.4 | u010545 | I_ComSniffer modified |
| 24.11.2020 | 1.0.2.3 | u010545 | I_ComSniffer added |
| 08.01.2019 | 1.0.2.2 | u015842 | Properties: copyright added |
| 29.09.2015 | 1.0.1.0 | u013972 | Resolve libraries with placeholder |
| 10.09.2015 | 1.0.0.3 | u013972 | Workaround C0351-Bug |
| 10.09.2015 | 1.0.0.2 | u013972 | Rename Variables in methods Read and Write |
| 26.08.2015 | 1.0.0.2 | u013972 | COM-Numbers more flexible via Parameter List |
| 09.03.2015 | 1.0.0.0 | RE | Release Version |

#### Details

VersionHistory (GVL)¶







Name
Type



Info

ProjectInfo




WagoSysCom_Internal_PFC.library








date
version
author
change

20.03.2023
1.0.2.7
u013972
Resolve types by namespace

23.10.2023
1.0.2.6
u010663
64-Bit adjustment ->SysTypes2Interfaces

22.06.2023
1.0.2.5
u013972
Revert publishing symbols of underlying libraries

07.12.2020
1.0.2.4
u010545
I_ComSniffer modified

24.11.2020
1.0.2.3
u010545
I_ComSniffer added

08.01.2019
1.0.2.2
u015842
Properties: copyright added

29.09.2015
1.0.1.0
u013972
Resolve libraries with placeholder

10.09.2015
1.0.0.3
u013972
Workaround C0351-Bug

10.09.2015
1.0.0.2
u013972
Rename Variables in methods Read and Write

26.08.2015
1.0.0.2
u013972
COM-Numbers more flexible via Parameter List

09.03.2015
1.0.0.0
RE
Release Version VersionHistory (GVL)¶







Name
Type



Info

ProjectInfo




WagoSysCom_Internal_PFC.library








date
version
author
change

20.03.2023
1.0.2.7
u013972
Resolve types by namespace

23.10.2023
1.0.2.6
u010663
64-Bit adjustment ->SysTypes2Interfaces

22.06.2023
1.0.2.5
u013972
Revert publishing symbols of underlying libraries

07.12.2020
1.0.2.4
u010545
I_ComSniffer modified

24.11.2020
1.0.2.3
u010545
I_ComSniffer added

08.01.2019
1.0.2.2
u015842
Properties: copyright added

29.09.2015
1.0.1.0
u013972
Resolve libraries with placeholder

10.09.2015
1.0.0.3
u013972
Workaround C0351-Bug

10.09.2015
1.0.0.2
u013972
Rename Variables in methods Read and Write

26.08.2015
1.0.0.2
u013972
COM-Numbers more flexible via Parameter List

09.03.2015
1.0.0.0
RE
Release Version VersionHistory (GVL)¶







Name
Type



Info

ProjectInfo




WagoSysCom_Internal_PFC.library








date
version
author
change

20.03.2023
1.0.2.7
u013972
Resolve types by namespace

23.10.2023
1.0.2.6
u010663
64-Bit adjustment ->SysTypes2Interfaces

22.06.2023
1.0.2.5
u013972
Revert publishing symbols of underlying libraries

07.12.2020
1.0.2.4
u010545
I_ComSniffer modified

24.11.2020
1.0.2.3
u010545
I_ComSniffer added

08.01.2019
1.0.2.2
u015842
Properties: copyright added

29.09.2015
1.0.1.0
u013972
Resolve libraries with placeholder

10.09.2015
1.0.0.3
u013972
Workaround C0351-Bug

10.09.2015
1.0.0.2
u013972
Rename Variables in methods Read and Write

26.08.2015
1.0.0.2
u013972
COM-Numbers more flexible via Parameter List

09.03.2015
1.0.0.0
RE
Release Version VersionHistory (GVL)¶







Name
Type



Info

ProjectInfo




WagoSysCom_Internal_PFC.library








date
version
author
change

20.03.2023
1.0.2.7
u013972
Resolve types by namespace

23.10.2023
1.0.2.6
u010663
64-Bit adjustment ->SysTypes2Interfaces

22.06.2023
1.0.2.5
u013972
Revert publishing symbols of underlying libraries

07.12.2020
1.0.2.4
u010545
I_ComSniffer modified

24.11.2020
1.0.2.3
u010545
I_ComSniffer added

08.01.2019
1.0.2.2
u015842
Properties: copyright added

29.09.2015
1.0.1.0
u013972
Resolve libraries with placeholder

10.09.2015
1.0.0.3
u013972
Workaround C0351-Bug

10.09.2015
1.0.0.2
u013972
Rename Variables in methods Read and Write

26.08.2015
1.0.0.2
u013972
COM-Numbers more flexible via Parameter List

09.03.2015
1.0.0.0
RE
Release Version Name
Type



Info

ProjectInfo WagoSysCom_Internal_PFC.library

#### Code Examples

```
ProjectInfo
```

---

## Hardware Lines

### 20 Hardware Lines

**File:** `cSGSIAGxC_ICTdLDGbJ1X_x1LfE\fld-20-Hardware-Lines.html`

This section contains methods for direct usage of hardware lines of the physical interface.

#### Details

20 Hardware Lines¶
This section contains methods for direct usage of hardware lines of the physical interface.


FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH) 20 Hardware Lines¶
This section contains methods for direct usage of hardware lines of the physical interface.


FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH) 20 Hardware Lines¶
This section contains methods for direct usage of hardware lines of the physical interface.


FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH) 20 Hardware Lines¶
This section contains methods for direct usage of hardware lines of the physical interface.


FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH) This section contains methods for direct usage of hardware lines of the physical interface. FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)

---

## Methods

### FbSerialInterface_internal.AttachExclusively (METH)

**File:** `khFmInkqN_boaOSEy6Yk4sm0688\attachexclusivel.html`

Tries to get exclusive access to the device.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | AttachExclusively | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Address of the instance |

#### Additional Information

| Column 1 |
| --- |
| result codes |
| 0 |
| EBUSY |
| EINVAL |

#### Details

FbSerialInterface_internal.AttachExclusively (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
AttachExclusively
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Tries to get exclusive access to the device.
Note (1): This mechanism provides a means for cooperatively using specific devices.
However, It does not implement mechanisms for enforcing that policy.
Note (2): It seems suitable to pass the address of the attached high-level-FB as the
unique identification tag for the client which uses the device. The device,
however, does not have any knowledge about these high-level-FBs, so virtually any
unique number may be passed here.
Note (3): “RequestorID” corresponds to the address of the instance which should use
the device exclusively.






result codes

0
Success, exclusive use has been granted.

EBUSY
Exclusive use has been refused. The device has already been attached to another user.

EINVAL
Null instance has been passed. (Null denotes a detached device) FbSerialInterface_internal.AttachExclusively (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
AttachExclusively
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Tries to get exclusive access to the device.
Note (1): This mechanism provides a means for cooperatively using specific devices.
However, It does not implement mechanisms for enforcing that policy.
Note (2): It seems suitable to pass the address of the attached high-level-FB as the
unique identification tag for the client which uses the device. The device,
however, does not have any knowledge about these high-level-FBs, so virtually any
unique number may be passed here.
Note (3): “RequestorID” corresponds to the address of the instance which should use
the device exclusively.






result codes

0
Success, exclusive use has been granted.

EBUSY
Exclusive use has been refused. The device has already been attached to another user.

EINVAL
Null instance has been passed. (Null denotes a detached device) FbSerialInterface_internal.AttachExclusively (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
AttachExclusively
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Tries to get exclusive access to the device.
Note (1): This mechanism provides a means for cooperatively using specific devices.
However, It does not implement mechanisms for enforcing that policy.
Note (2): It seems suitable to pass the address of the attached high-level-FB as the
unique identification tag for the client which uses the device. The device,
however, does not have any knowledge about these high-level-FBs, so virtually any
unique number may be passed here.
Note (3): “RequestorID” corresponds to the address of the instance which should use
the device exclusively.






result codes

0
Success, exclusive use has been granted.

EBUSY
Exclusive use has been refused. The device has already been attached to another user.

EINVAL
Null instance has been passed. (Null denotes a detached device) FbSerialInterface_internal.AttachExclusively (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
AttachExclusively
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Tries to get exclusive access to the device.
Note (1): This mechanism provides a means for cooperatively using specific devices.
However, It does not implement mechanisms for enforcing that policy.
Note (2): It seems suitable to pass the address of the attached high-level-FB as the
unique identification tag for the client which uses the device. The device,
however, does not have any knowledge about these high-level-FBs, so virtually any
unique number may be passed here.
Note (3): “RequestorID” corresponds to the address of the instance which should use
the device exclusively.






result codes

0
Success, exclusive use has been granted.

EBUSY
Exclusive use has been refused. The device has already been attached to another user.

EINVAL
Null instance has been passed. (Null denotes a detached device) Interface variables








Scope
Name
Type
Comment



Return
AttachExclusively
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance Interface variables Scope
Name
Type
Comment



Return
AttachExclusively
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance Tries to get exclusive access to the device. Note (1): This mechanism provides a means for cooperatively using specific devices.
However, It does not implement mechanisms for enforcing that policy. Note (2): It seems suitable to pass the address of the attached high-level-FB as the
unique identification tag for the client which uses the device. The device,
however, does not have any knowledge about these high-level-FBs, so virtually any
unique number may be passed here. Note (3): “RequestorID” corresponds to the address of the instance which should use
the device exclusively.

#### Code Examples

```
AttachExclusively
```

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.ClearBuffers (METH)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\clearbuffers.html`

Clears all internal receive or send buffers of the device.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | ClearBuffers | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| EBUSY |
| EACCES |
| EBADF |

#### Details

FbSerialInterface_internal.ClearBuffers (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ClearBuffers
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Clears all internal receive or send buffers of the device.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while opening the system com port.

EBADF
The com-port was not open. FbSerialInterface_internal.ClearBuffers (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ClearBuffers
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Clears all internal receive or send buffers of the device.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while opening the system com port.

EBADF
The com-port was not open. FbSerialInterface_internal.ClearBuffers (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ClearBuffers
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Clears all internal receive or send buffers of the device.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while opening the system com port.

EBADF
The com-port was not open. FbSerialInterface_internal.ClearBuffers (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ClearBuffers
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Clears all internal receive or send buffers of the device.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while opening the system com port.

EBADF
The com-port was not open. Interface variables








Scope
Name
Type
Comment



Return
ClearBuffers
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller Interface variables Scope
Name
Type
Comment



Return
ClearBuffers
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller Clears all internal receive or send buffers of the device. Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

#### Code Examples

```
ClearBuffers
```

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.Close (METH)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\close.html`

Closes the connection and detaches the FB from the serial interface.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | Close | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| EBUSY |
| EACCES |
| EBADF |

#### Details

FbSerialInterface_internal.Close (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Close
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Closes the connection and detaches the FB from the serial interface.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while closing the system com-port.

EBADF
The com-port was not open. FbSerialInterface_internal.Close (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Close
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Closes the connection and detaches the FB from the serial interface.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while closing the system com-port.

EBADF
The com-port was not open. FbSerialInterface_internal.Close (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Close
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Closes the connection and detaches the FB from the serial interface.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while closing the system com-port.

EBADF
The com-port was not open. FbSerialInterface_internal.Close (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Close
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Closes the connection and detaches the FB from the serial interface.
Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EACCES
There was a problem while closing the system com-port.

EBADF
The com-port was not open. Interface variables








Scope
Name
Type
Comment



Return
Close
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller Interface variables Scope
Name
Type
Comment



Return
Close
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller Closes the connection and detaches the FB from the serial interface. Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.

#### Code Examples

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.Configure (METH)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\configure.html`

Configures a serial FB before opening it.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | Configure | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| udiBaudrate | UDINT | Baudrate (9600 = 9k6) | - |
| usiDataBits | USINT | Number of Bits per frame (5..8) | - |
| eParity | eTTYParity | Parity | - |
| eStopbits | eTTYStopBits | Number of Stop-Bits (see Note 1) | - |
| eHandshake | eTTYHandshake | Type of handshake (XON/XOFF, etc) | - |
| ePhysical | eTTYPhysicalLayer | RS232, RS422, RS485, etc | - |
| uiSystemBufferSize | UINT | Size of system buffer (important for ‘read’) | - |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| EBUSY |
| EALREADY |
| ENOPROTOOPT |

#### Details

FbSerialInterface_internal.Configure (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Configure
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

udiBaudrate
UDINT
Baudrate (9600 = 9k6)

usiDataBits
USINT
Number of Bits per frame (5..8)

eParity
eTTYParity
Parity

eStopbits
eTTYStopBits
Number of Stop-Bits (see Note 1)

eHandshake
eTTYHandshake
Type of handshake (XON/XOFF, etc)

ePhysical
eTTYPhysicalLayer
RS232, RS422, RS485, etc

uiSystemBufferSize
UINT
Size of system buffer (important for ‘read’)





Configures a serial FB before opening it.
This method is intended to be called before opening the device.
The settings will thus not take immediate effect, but they will be applied to the device with
the following Open() call.
Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’
(1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

ENOPROTOOPT
The requested option or physical layer (e.g. ‘RS-xyz’) is not available.



Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
Note (3): This method may be used to try if several settings are allowed for a device
without actually opening the device with these settings. FbSerialInterface_internal.Configure (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Configure
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

udiBaudrate
UDINT
Baudrate (9600 = 9k6)

usiDataBits
USINT
Number of Bits per frame (5..8)

eParity
eTTYParity
Parity

eStopbits
eTTYStopBits
Number of Stop-Bits (see Note 1)

eHandshake
eTTYHandshake
Type of handshake (XON/XOFF, etc)

ePhysical
eTTYPhysicalLayer
RS232, RS422, RS485, etc

uiSystemBufferSize
UINT
Size of system buffer (important for ‘read’)





Configures a serial FB before opening it.
This method is intended to be called before opening the device.
The settings will thus not take immediate effect, but they will be applied to the device with
the following Open() call.
Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’
(1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

ENOPROTOOPT
The requested option or physical layer (e.g. ‘RS-xyz’) is not available.



Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
Note (3): This method may be used to try if several settings are allowed for a device
without actually opening the device with these settings. FbSerialInterface_internal.Configure (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Configure
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

udiBaudrate
UDINT
Baudrate (9600 = 9k6)

usiDataBits
USINT
Number of Bits per frame (5..8)

eParity
eTTYParity
Parity

eStopbits
eTTYStopBits
Number of Stop-Bits (see Note 1)

eHandshake
eTTYHandshake
Type of handshake (XON/XOFF, etc)

ePhysical
eTTYPhysicalLayer
RS232, RS422, RS485, etc

uiSystemBufferSize
UINT
Size of system buffer (important for ‘read’)





Configures a serial FB before opening it.
This method is intended to be called before opening the device.
The settings will thus not take immediate effect, but they will be applied to the device with
the following Open() call.
Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’
(1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

ENOPROTOOPT
The requested option or physical layer (e.g. ‘RS-xyz’) is not available.



Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
Note (3): This method may be used to try if several settings are allowed for a device
without actually opening the device with these settings. FbSerialInterface_internal.Configure (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Configure
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

udiBaudrate
UDINT
Baudrate (9600 = 9k6)

usiDataBits
USINT
Number of Bits per frame (5..8)

eParity
eTTYParity
Parity

eStopbits
eTTYStopBits
Number of Stop-Bits (see Note 1)

eHandshake
eTTYHandshake
Type of handshake (XON/XOFF, etc)

ePhysical
eTTYPhysicalLayer
RS232, RS422, RS485, etc

uiSystemBufferSize
UINT
Size of system buffer (important for ‘read’)





Configures a serial FB before opening it.
This method is intended to be called before opening the device.
The settings will thus not take immediate effect, but they will be applied to the device with
the following Open() call.
Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’
(1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

ENOPROTOOPT
The requested option or physical layer (e.g. ‘RS-xyz’) is not available.



Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
Note (3): This method may be used to try if several settings are allowed for a device
without actually opening the device with these settings. Interface variables








Scope
Name
Type
Comment



Return
Configure
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

udiBaudrate
UDINT
Baudrate (9600 = 9k6)

usiDataBits
USINT
Number of Bits per frame (5..8)

eParity
eTTYParity
Parity

eStopbits
eTTYStopBits
Number of Stop-Bits (see Note 1)

eHandshake
eTTYHandshake
Type of handshake (XON/XOFF, etc)

ePhysical
eTTYPhysicalLayer
RS232, RS422, RS485, etc

uiSystemBufferSize
UINT
Size of system buffer (important for ‘read’) Interface variables Scope
Name
Type
Comment



Return
Configure
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

udiBaudrate
UDINT
Baudrate (9600 = 9k6)

usiDataBits
USINT
Number of Bits per frame (5..8)

eParity
eTTYParity
Parity

eStopbits
eTTYStopBits
Number of Stop-Bits (see Note 1)

eHandshake
eTTYHandshake
Type of handshake (XON/XOFF, etc)

ePhysical
eTTYPhysicalLayer
RS232, RS422, RS485, etc

uiSystemBufferSize
UINT
Size of system buffer (important for ‘read’) Configures a serial FB before opening it. This method is intended to be called before opening the device.
The settings will thus not take immediate effect, but they will be applied to the device with
the following Open() call. Note(1): For eStopbits the settings ‘None’ (for synchronous operation) and ‘OneDotFive’
(1.5 stop bits, as common for teletypewriters) are not supported and will result in ENOPROTOOPT. This method returns the following result codes: Note(2): Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK. Note (3): This method may be used to try if several settings are allowed for a device
without actually opening the device with these settings.

#### Code Examples

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

```
udiBaudrate
```

```
usiDataBits
```

```
eTTYStopBits
```

```
eTTYHandshake
```

```
eTTYPhysicalLayer
```

```
uiSystemBufferSize
```

---

### FbSerialInterface_internal.Cyclic (METH)

**File:** `eVLj1s0_HPjWHBhQFl526Th5Tks\cyclic.html`

Cyclic processing of this FB.

#### Interface Variables

| Scope | Name | Type |
| --- | --- | :---: |
| Return | Cyclic | eResultCode |

#### Additional Information

| Column 1 |
| --- |
| Result Code |
| ENOSYS |

#### Details

FbSerialInterface_internal.Cyclic (METH)¶

Interface variables







Scope
Name
Type



Return
Cyclic
eResultCode





Cyclic processing of this FB.
This method is not implemented.
In general, this method is intended for carrying out cyclic operation of the connected instance.
Cyclic operation would be necessary, if one or more operations were deferred for future completion
(such as Open(), etc.). Then this deferred execution is carried out by this cyclic call.
As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.






Result Code

ENOSYS
No cyclic processing necessary, further calls may be omitted. FbSerialInterface_internal.Cyclic (METH)¶

Interface variables







Scope
Name
Type



Return
Cyclic
eResultCode





Cyclic processing of this FB.
This method is not implemented.
In general, this method is intended for carrying out cyclic operation of the connected instance.
Cyclic operation would be necessary, if one or more operations were deferred for future completion
(such as Open(), etc.). Then this deferred execution is carried out by this cyclic call.
As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.






Result Code

ENOSYS
No cyclic processing necessary, further calls may be omitted. FbSerialInterface_internal.Cyclic (METH)¶

Interface variables







Scope
Name
Type



Return
Cyclic
eResultCode





Cyclic processing of this FB.
This method is not implemented.
In general, this method is intended for carrying out cyclic operation of the connected instance.
Cyclic operation would be necessary, if one or more operations were deferred for future completion
(such as Open(), etc.). Then this deferred execution is carried out by this cyclic call.
As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.






Result Code

ENOSYS
No cyclic processing necessary, further calls may be omitted. FbSerialInterface_internal.Cyclic (METH)¶

Interface variables







Scope
Name
Type



Return
Cyclic
eResultCode





Cyclic processing of this FB.
This method is not implemented.
In general, this method is intended for carrying out cyclic operation of the connected instance.
Cyclic operation would be necessary, if one or more operations were deferred for future completion
(such as Open(), etc.). Then this deferred execution is carried out by this cyclic call.
As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.






Result Code

ENOSYS
No cyclic processing necessary, further calls may be omitted. Interface variables







Scope
Name
Type



Return
Cyclic
eResultCode Interface variables Scope
Name
Type



Return
Cyclic
eResultCode Cyclic processing of this FB. This method is not implemented. In general, this method is intended for carrying out cyclic operation of the connected instance.
Cyclic operation would be necessary, if one or more operations were deferred for future completion
(such as Open(), etc.). Then this deferred execution is carried out by this cyclic call. As this FbSerialInterface_internal does not defer anything there is no need for cyclic operation.

#### Code Examples

```
eResultCode
```

---

### FbSerialInterface_internal.Finish (METH)

**File:** `eVLj1s0_HPjWHBhQFl526Th5Tks\finish.html`

Detach and close a serial interface.

#### Details

FbSerialInterface_internal.Finish (METH)¶
Detach and close a serial interface.
This method is called before destruction (FB_Exit)
It has no return value. FbSerialInterface_internal.Finish (METH)¶
Detach and close a serial interface.
This method is called before destruction (FB_Exit)
It has no return value. FbSerialInterface_internal.Finish (METH)¶
Detach and close a serial interface.
This method is called before destruction (FB_Exit)
It has no return value. FbSerialInterface_internal.Finish (METH)¶
Detach and close a serial interface.
This method is called before destruction (FB_Exit)
It has no return value. Detach and close a serial interface. This method is called before destruction (FB_Exit)
It has no return value.

---

### FbSerialInterface_internal.ForceDetachment (METH)

**File:** `khFmInkqN_boaOSEy6Yk4sm0688\forcedetachment.html`

Forces detachment of the device.

#### Interface Variables

| Scope | Name | Type |
| --- | --- | :---: |
| Return | ForceDetachment | eResultCode |

#### Additional Information

| Column 1 |
| --- |
| result codes |
| 0 |

#### Details

FbSerialInterface_internal.ForceDetachment (METH)¶

Interface variables







Scope
Name
Type



Return
ForceDetachment
eResultCode





Forces detachment of the device.
This is used for initialization or for recovery from crashed client FBs which still hold a
lock on the device, which could not be released.
This method is meant for emergency recovery rather than for regular use.






result codes

0
Success (this operation does not fail) FbSerialInterface_internal.ForceDetachment (METH)¶

Interface variables







Scope
Name
Type



Return
ForceDetachment
eResultCode





Forces detachment of the device.
This is used for initialization or for recovery from crashed client FBs which still hold a
lock on the device, which could not be released.
This method is meant for emergency recovery rather than for regular use.






result codes

0
Success (this operation does not fail) FbSerialInterface_internal.ForceDetachment (METH)¶

Interface variables







Scope
Name
Type



Return
ForceDetachment
eResultCode





Forces detachment of the device.
This is used for initialization or for recovery from crashed client FBs which still hold a
lock on the device, which could not be released.
This method is meant for emergency recovery rather than for regular use.






result codes

0
Success (this operation does not fail) FbSerialInterface_internal.ForceDetachment (METH)¶

Interface variables







Scope
Name
Type



Return
ForceDetachment
eResultCode





Forces detachment of the device.
This is used for initialization or for recovery from crashed client FBs which still hold a
lock on the device, which could not be released.
This method is meant for emergency recovery rather than for regular use.






result codes

0
Success (this operation does not fail) Interface variables







Scope
Name
Type



Return
ForceDetachment
eResultCode Interface variables Scope
Name
Type



Return
ForceDetachment
eResultCode Forces detachment of the device. This is used for initialization or for recovery from crashed client FBs which still hold a
lock on the device, which could not be released.
This method is meant for emergency recovery rather than for regular use.

#### Code Examples

```
ForceDetachment
```

```
eResultCode
```

---

### FbSerialInterface_internal.GetErrorObject (METH)

**File:** `eVLj1s0_HPjWHBhQFl526Th5Tks\geterrorobject.html`

Obtains error cause from hardware interface.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | GetErrorObject | eResultCode | - |
| Input | xAcknowledge | BOOL | Auto-acknowledge the error object. |
| pBuffer | POINTER TO BYTE | Location of result buffer for the error object. | - |
| udiBufferSize | UDINT | Size of the result buffer. | - |

#### Details

FbSerialInterface_internal.GetErrorObject (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetErrorObject
eResultCode
 

Input
xAcknowledge
BOOL
Auto-acknowledge the error object.

pBuffer
POINTER TO BYTE
Location of result buffer for the error object.

udiBufferSize
UDINT
Size of the result buffer.





Obtains error cause from hardware interface.
As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS.
The result buffer which is indicated by ‘pBuffer’ remains unchanged. FbSerialInterface_internal.GetErrorObject (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetErrorObject
eResultCode
 

Input
xAcknowledge
BOOL
Auto-acknowledge the error object.

pBuffer
POINTER TO BYTE
Location of result buffer for the error object.

udiBufferSize
UDINT
Size of the result buffer.





Obtains error cause from hardware interface.
As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS.
The result buffer which is indicated by ‘pBuffer’ remains unchanged. FbSerialInterface_internal.GetErrorObject (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetErrorObject
eResultCode
 

Input
xAcknowledge
BOOL
Auto-acknowledge the error object.

pBuffer
POINTER TO BYTE
Location of result buffer for the error object.

udiBufferSize
UDINT
Size of the result buffer.





Obtains error cause from hardware interface.
As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS.
The result buffer which is indicated by ‘pBuffer’ remains unchanged. FbSerialInterface_internal.GetErrorObject (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetErrorObject
eResultCode
 

Input
xAcknowledge
BOOL
Auto-acknowledge the error object.

pBuffer
POINTER TO BYTE
Location of result buffer for the error object.

udiBufferSize
UDINT
Size of the result buffer.





Obtains error cause from hardware interface.
As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS.
The result buffer which is indicated by ‘pBuffer’ remains unchanged. Interface variables








Scope
Name
Type
Comment



Return
GetErrorObject
eResultCode
 

Input
xAcknowledge
BOOL
Auto-acknowledge the error object.

pBuffer
POINTER TO BYTE
Location of result buffer for the error object.

udiBufferSize
UDINT
Size of the result buffer. Interface variables Scope
Name
Type
Comment



Return
GetErrorObject
eResultCode
 

Input
xAcknowledge
BOOL
Auto-acknowledge the error object.

pBuffer
POINTER TO BYTE
Location of result buffer for the error object.

udiBufferSize
UDINT
Size of the result buffer. Obtains error cause from hardware interface. As COM1 does not produce any error objects, this method is not implemented and returns ENOSYS.
The result buffer which is indicated by ‘pBuffer’ remains unchanged.

#### Code Examples

```
GetErrorObject
```

```
eResultCode
```

```
xAcknowledge
```

```
udiBufferSize
```

---

### FbSerialInterface_internal.GetLineState (METH)

**File:** `cSGSIAGxC_ICTdLDGbJ1X_x1LfE\getlinestate.html`

Retrieve the state of hardware lines, if available.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | GetLineState | BOOL | - |
| Input | eLineID | eTTYLineID | Line to be obtained. |

#### Details

FbSerialInterface_internal.GetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetLineState
BOOL
 

Input
eLineID
eTTYLineID
Line to be obtained.





Retrieve the state of hardware lines, if available.
This method yields TRUE if the addressed hardware line shows an ‘active’ physical level
(+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232).
If the level cannot be retrieved, TRUE is returned. FbSerialInterface_internal.GetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetLineState
BOOL
 

Input
eLineID
eTTYLineID
Line to be obtained.





Retrieve the state of hardware lines, if available.
This method yields TRUE if the addressed hardware line shows an ‘active’ physical level
(+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232).
If the level cannot be retrieved, TRUE is returned. FbSerialInterface_internal.GetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetLineState
BOOL
 

Input
eLineID
eTTYLineID
Line to be obtained.





Retrieve the state of hardware lines, if available.
This method yields TRUE if the addressed hardware line shows an ‘active’ physical level
(+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232).
If the level cannot be retrieved, TRUE is returned. FbSerialInterface_internal.GetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
GetLineState
BOOL
 

Input
eLineID
eTTYLineID
Line to be obtained.





Retrieve the state of hardware lines, if available.
This method yields TRUE if the addressed hardware line shows an ‘active’ physical level
(+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232).
If the level cannot be retrieved, TRUE is returned. Interface variables








Scope
Name
Type
Comment



Return
GetLineState
BOOL
 

Input
eLineID
eTTYLineID
Line to be obtained. Interface variables Scope
Name
Type
Comment



Return
GetLineState
BOOL
 

Input
eLineID
eTTYLineID
Line to be obtained. Retrieve the state of hardware lines, if available. This method yields TRUE if the addressed hardware line shows an ‘active’ physical level
(+3..+15V for RS232) and FALSE if it shows a ‘passive’ physical level (-3..-15V for RS232).
If the level cannot be retrieved, TRUE is returned.

#### Code Examples

```
GetLineState
```

---

### FbSerialInterface_internal.Initialize (METH)

**File:** `eVLj1s0_HPjWHBhQFl526Th5Tks\initialize.html`

Initialize FbSerialInterface_internal at Fb_Init().

#### Details

FbSerialInterface_internal.Initialize (METH)¶
Initialize FbSerialInterface_internal at Fb_Init().
This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’
to an initial state. FbSerialInterface_internal.Initialize (METH)¶
Initialize FbSerialInterface_internal at Fb_Init().
This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’
to an initial state. FbSerialInterface_internal.Initialize (METH)¶
Initialize FbSerialInterface_internal at Fb_Init().
This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’
to an initial state. FbSerialInterface_internal.Initialize (METH)¶
Initialize FbSerialInterface_internal at Fb_Init().
This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’
to an initial state. Initialize FbSerialInterface_internal at Fb_Init(). This method initalizes member variables and properties of the FB ‘FbSerialInterface_internal’
to an initial state.

---

### FbSerialInterface_internal.IsLineAvailable (METH)

**File:** `cSGSIAGxC_ICTdLDGbJ1X_x1LfE\islineavailable.html`

Checks if manipulation of a hardware line is possible.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | IsLineAvailable | BOOL | - |
| Input | eLineID | eTTYLineID | Hardware line to check for manipulation. |

#### Details

FbSerialInterface_internal.IsLineAvailable (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
IsLineAvailable
BOOL
 

Input
eLineID
eTTYLineID
Hardware line to check for manipulation.





Checks if manipulation of a hardware line is possible.
This method checks whether the driver and protocol support manipulation of
the hardware line.
If no extra hardware lines are available, this call returns FALSE.
Note: hardware handshake cannot be configured in this case either.
If hardware handshake is configured, some lines are not available for manipulation and
this call returns FALSE for them.
If lines are available and no hardware handshake is configured, the call returns TRUE. FbSerialInterface_internal.IsLineAvailable (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
IsLineAvailable
BOOL
 

Input
eLineID
eTTYLineID
Hardware line to check for manipulation.





Checks if manipulation of a hardware line is possible.
This method checks whether the driver and protocol support manipulation of
the hardware line.
If no extra hardware lines are available, this call returns FALSE.
Note: hardware handshake cannot be configured in this case either.
If hardware handshake is configured, some lines are not available for manipulation and
this call returns FALSE for them.
If lines are available and no hardware handshake is configured, the call returns TRUE. FbSerialInterface_internal.IsLineAvailable (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
IsLineAvailable
BOOL
 

Input
eLineID
eTTYLineID
Hardware line to check for manipulation.





Checks if manipulation of a hardware line is possible.
This method checks whether the driver and protocol support manipulation of
the hardware line.
If no extra hardware lines are available, this call returns FALSE.
Note: hardware handshake cannot be configured in this case either.
If hardware handshake is configured, some lines are not available for manipulation and
this call returns FALSE for them.
If lines are available and no hardware handshake is configured, the call returns TRUE. FbSerialInterface_internal.IsLineAvailable (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
IsLineAvailable
BOOL
 

Input
eLineID
eTTYLineID
Hardware line to check for manipulation.





Checks if manipulation of a hardware line is possible.
This method checks whether the driver and protocol support manipulation of
the hardware line.
If no extra hardware lines are available, this call returns FALSE.
Note: hardware handshake cannot be configured in this case either.
If hardware handshake is configured, some lines are not available for manipulation and
this call returns FALSE for them.
If lines are available and no hardware handshake is configured, the call returns TRUE. Interface variables








Scope
Name
Type
Comment



Return
IsLineAvailable
BOOL
 

Input
eLineID
eTTYLineID
Hardware line to check for manipulation. Interface variables Scope
Name
Type
Comment



Return
IsLineAvailable
BOOL
 

Input
eLineID
eTTYLineID
Hardware line to check for manipulation. Checks if manipulation of a hardware line is possible. This method checks whether the driver and protocol support manipulation of
the hardware line. If no extra hardware lines are available, this call returns FALSE.
Note: hardware handshake cannot be configured in this case either.
If hardware handshake is configured, some lines are not available for manipulation and
this call returns FALSE for them.
If lines are available and no hardware handshake is configured, the call returns TRUE.

#### Code Examples

```
IsLineAvailable
```

---

### FbSerialInterface_internal.Open (METH)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\open.html`

Attaches an application FB to a serial port at runtime.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | Open | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| EBUSY |
| EALREADY |
| EACCES |
| ENOPROTOOPT |

#### Details

FbSerialInterface_internal.Open (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Open
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Attaches an application FB to a serial port at runtime.
The device is opened with the settings which are previously set by Configure().
The device performs the following actions on this call:


It configures the hardware with the settings which are previously sent with Configure().
It switches on the receiver in order to accept data from the line.


Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

EACCES
There was a problem while opening the system com-port.

ENOPROTOOPT
The requested option or physical layer (RS-xyz) is not available. FbSerialInterface_internal.Open (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Open
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Attaches an application FB to a serial port at runtime.
The device is opened with the settings which are previously set by Configure().
The device performs the following actions on this call:


It configures the hardware with the settings which are previously sent with Configure().
It switches on the receiver in order to accept data from the line.


Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

EACCES
There was a problem while opening the system com-port.

ENOPROTOOPT
The requested option or physical layer (RS-xyz) is not available. FbSerialInterface_internal.Open (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Open
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Attaches an application FB to a serial port at runtime.
The device is opened with the settings which are previously set by Configure().
The device performs the following actions on this call:


It configures the hardware with the settings which are previously sent with Configure().
It switches on the receiver in order to accept data from the line.


Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

EACCES
There was a problem while opening the system com-port.

ENOPROTOOPT
The requested option or physical layer (RS-xyz) is not available. FbSerialInterface_internal.Open (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Open
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller





Attaches an application FB to a serial port at runtime.
The device is opened with the settings which are previously set by Configure().
The device performs the following actions on this call:


It configures the hardware with the settings which are previously sent with Configure().
It switches on the receiver in order to accept data from the line.


Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK.
This method returns the following result codes:






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EALREADY
The com-port is already open.

EACCES
There was a problem while opening the system com-port.

ENOPROTOOPT
The requested option or physical layer (RS-xyz) is not available. Interface variables








Scope
Name
Type
Comment



Return
Open
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller Interface variables Scope
Name
Type
Comment



Return
Open
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller Attaches an application FB to a serial port at runtime. The device is opened with the settings which are previously set by Configure().
The device performs the following actions on this call: It configures the hardware with the settings which are previously sent with Configure().
It switches on the receiver in order to accept data from the line. Note: Although the interface ‘I_WagoSysComBase’ allows for deferred execution of this method,
in this implementation it will complete its job immediately and it will not return EWOULDBLOCK. This method returns the following result codes:

#### Code Examples

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.Read (METH)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\read.html`

Reads data from the serial port.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | Read | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| pRxBuffer | POINTER TO BYTE | Location of the receive buffer | - |
| udiRxBufferSize | UDINT | Size of the receive buffer | - |
| Output | udiRxNBytes | UDINT | Number of transferred bytes |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| EBUSY |
| EINVAL |
| EBADMSG |
| EACCES |
| EBADF |

#### Details

FbSerialInterface_internal.Read (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Read
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pRxBuffer
POINTER TO BYTE
Location of the receive buffer

udiRxBufferSize
UDINT
Size of the receive buffer

Output
udiRxNBytes
UDINT
Number of transferred bytes





Reads data from the serial port.
This method stores incoming data at the location which is given by pDest (‘receive buffer’).
The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of
bytes which are allowed to be processed.
If more bytes than this number have come in through the serial line, the excessive bytes
will remain in the internal system buffer and will be transferred with one of the following
read() calls.
The output ‘udiRxNBytes’ represents the number of bytes which are actually
transferred. When read() is called periodically, the typical situation is that
‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero.
When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly
that size, but there is no hint has to whether more data could be expected with a consecutive read
or not.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EBADMSG
Integrity of data is severed (Parity-Error or Frame-Error).

EACCES
There was a problem while reading from the system com_port.

EBADF
The com-port was not open. FbSerialInterface_internal.Read (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Read
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pRxBuffer
POINTER TO BYTE
Location of the receive buffer

udiRxBufferSize
UDINT
Size of the receive buffer

Output
udiRxNBytes
UDINT
Number of transferred bytes





Reads data from the serial port.
This method stores incoming data at the location which is given by pDest (‘receive buffer’).
The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of
bytes which are allowed to be processed.
If more bytes than this number have come in through the serial line, the excessive bytes
will remain in the internal system buffer and will be transferred with one of the following
read() calls.
The output ‘udiRxNBytes’ represents the number of bytes which are actually
transferred. When read() is called periodically, the typical situation is that
‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero.
When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly
that size, but there is no hint has to whether more data could be expected with a consecutive read
or not.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EBADMSG
Integrity of data is severed (Parity-Error or Frame-Error).

EACCES
There was a problem while reading from the system com_port.

EBADF
The com-port was not open. FbSerialInterface_internal.Read (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Read
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pRxBuffer
POINTER TO BYTE
Location of the receive buffer

udiRxBufferSize
UDINT
Size of the receive buffer

Output
udiRxNBytes
UDINT
Number of transferred bytes





Reads data from the serial port.
This method stores incoming data at the location which is given by pDest (‘receive buffer’).
The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of
bytes which are allowed to be processed.
If more bytes than this number have come in through the serial line, the excessive bytes
will remain in the internal system buffer and will be transferred with one of the following
read() calls.
The output ‘udiRxNBytes’ represents the number of bytes which are actually
transferred. When read() is called periodically, the typical situation is that
‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero.
When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly
that size, but there is no hint has to whether more data could be expected with a consecutive read
or not.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EBADMSG
Integrity of data is severed (Parity-Error or Frame-Error).

EACCES
There was a problem while reading from the system com_port.

EBADF
The com-port was not open. FbSerialInterface_internal.Read (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Read
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pRxBuffer
POINTER TO BYTE
Location of the receive buffer

udiRxBufferSize
UDINT
Size of the receive buffer

Output
udiRxNBytes
UDINT
Number of transferred bytes





Reads data from the serial port.
This method stores incoming data at the location which is given by pDest (‘receive buffer’).
The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of
bytes which are allowed to be processed.
If more bytes than this number have come in through the serial line, the excessive bytes
will remain in the internal system buffer and will be transferred with one of the following
read() calls.
The output ‘udiRxNBytes’ represents the number of bytes which are actually
transferred. When read() is called periodically, the typical situation is that
‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero.
When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly
that size, but there is no hint has to whether more data could be expected with a consecutive read
or not.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EBADMSG
Integrity of data is severed (Parity-Error or Frame-Error).

EACCES
There was a problem while reading from the system com_port.

EBADF
The com-port was not open. Interface variables








Scope
Name
Type
Comment



Return
Read
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pRxBuffer
POINTER TO BYTE
Location of the receive buffer

udiRxBufferSize
UDINT
Size of the receive buffer

Output
udiRxNBytes
UDINT
Number of transferred bytes Interface variables Scope
Name
Type
Comment



Return
Read
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pRxBuffer
POINTER TO BYTE
Location of the receive buffer

udiRxBufferSize
UDINT
Size of the receive buffer

Output
udiRxNBytes
UDINT
Number of transferred bytes Reads data from the serial port. This method stores incoming data at the location which is given by pDest (‘receive buffer’).
The input ‘udiRxBufferSize’ denote the size of the receive buffer, i.e. the maximum number of
bytes which are allowed to be processed. If more bytes than this number have come in through the serial line, the excessive bytes
will remain in the internal system buffer and will be transferred with one of the following
read() calls. The output ‘udiRxNBytes’ represents the number of bytes which are actually
transferred. When read() is called periodically, the typical situation is that
‘udiRxNBytes’ is less than ‘udiRxBufferSize’ or even zero. When exactly the amount of requested data is read, ‘udiRxNBytes’ denotes exactly
that size, but there is no hint has to whether more data could be expected with a consecutive read
or not.

#### Code Examples

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

```
udiRxBufferSize
```

```
udiRxNBytes
```

---

### FbSerialInterface_internal.RegisterSniffer (METH)

**File:** `PMO1c8S6g3uyPZcIQwLIeCQcHO8\registersniffer.html`

#### Interface Variables

| Scope | Name | Type |
| --- | --- | :---: |
| Return | RegisterSniffer | BOOL |
| Input | IComSniffer | WagoTypesCom.I_ComSniffer |

#### Details

FbSerialInterface_internal.RegisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
RegisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer FbSerialInterface_internal.RegisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
RegisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer FbSerialInterface_internal.RegisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
RegisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer FbSerialInterface_internal.RegisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
RegisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer Interface variables







Scope
Name
Type



Return
RegisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer Interface variables Scope
Name
Type



Return
RegisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer

#### Code Examples

```
RegisterSniffer
```

```
IComSniffer
```

```
WagoTypesCom.I_ComSniffer
```

---

### FbSerialInterface_internal.ReleaseExclusivity (METH)

**File:** `khFmInkqN_boaOSEy6Yk4sm0688\releaseexclusivi.html`

Releases the device from exclusive usage.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | ReleaseExclusivity | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Address of the instance |

#### Additional Information

| Column 1 |
| --- |
| result codes |
| 0 |
| EBUSY |
| EINVAL |

#### Details

FbSerialInterface_internal.ReleaseExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ReleaseExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Releases the device from exclusive usage.
This method is intended to release the exclusivity which has been assigned with AttachExclusively().
Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.






result codes

0
Success, the device has been detached.

EBUSY
Use has not been granted to this FB. It is in use by another FB.

EINVAL
Null instance is passed. (Null denotes a detached device) FbSerialInterface_internal.ReleaseExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ReleaseExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Releases the device from exclusive usage.
This method is intended to release the exclusivity which has been assigned with AttachExclusively().
Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.






result codes

0
Success, the device has been detached.

EBUSY
Use has not been granted to this FB. It is in use by another FB.

EINVAL
Null instance is passed. (Null denotes a detached device) FbSerialInterface_internal.ReleaseExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ReleaseExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Releases the device from exclusive usage.
This method is intended to release the exclusivity which has been assigned with AttachExclusively().
Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.






result codes

0
Success, the device has been detached.

EBUSY
Use has not been granted to this FB. It is in use by another FB.

EINVAL
Null instance is passed. (Null denotes a detached device) FbSerialInterface_internal.ReleaseExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
ReleaseExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Releases the device from exclusive usage.
This method is intended to release the exclusivity which has been assigned with AttachExclusively().
Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.






result codes

0
Success, the device has been detached.

EBUSY
Use has not been granted to this FB. It is in use by another FB.

EINVAL
Null instance is passed. (Null denotes a detached device) Interface variables








Scope
Name
Type
Comment



Return
ReleaseExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance Interface variables Scope
Name
Type
Comment



Return
ReleaseExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance Releases the device from exclusive usage. This method is intended to release the exclusivity which has been assigned with AttachExclusively(). Note (1): “RequestorID” corresponds to the address of the instance which releases its exclusivity.

#### Code Examples

```
ReleaseExclusivity
```

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.SetLineState (METH)

**File:** `cSGSIAGxC_ICTdLDGbJ1X_x1LfE\setlinestate.html`

Allows control of the hardware lines by the application

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | SetLineState | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| eLineID | eTTYLineID | Line whose state is to be set. | - |
| xState | BOOL | TRUE = active, FALSE = inactive | - |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| ENOSYS |
| EBUSY |
| EINVAL |
| EPROTONOSUPPORT |
| EBADF |
| EACCES |

#### Details

FbSerialInterface_internal.SetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
SetLineState
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

eLineID
eTTYLineID
Line whose state is to be set.

xState
BOOL
TRUE = active, FALSE = inactive





Allows control of the hardware lines by the application
Normally, these lines are controlled by hardware handshake internally.
Nevertheless, when no hardware handshake is involved, the
serial lines might be used for very individual purposes.
In the latter case, these hardware wires can be manipulated directly with this functions to desired
levels, according to the need of the actual application.
This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the
creation of this library.






Result Codes

0
Success

ENOSYS
The functionality is not supported.

EBUSY
The FB is busy with another client.

EINVAL
Invalid line ID for output

EPROTONOSUPPORT
Device is configured for RS485 protocol.

EBADF
Bad handle to serial port

EACCES
Could not set the line. FbSerialInterface_internal.SetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
SetLineState
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

eLineID
eTTYLineID
Line whose state is to be set.

xState
BOOL
TRUE = active, FALSE = inactive





Allows control of the hardware lines by the application
Normally, these lines are controlled by hardware handshake internally.
Nevertheless, when no hardware handshake is involved, the
serial lines might be used for very individual purposes.
In the latter case, these hardware wires can be manipulated directly with this functions to desired
levels, according to the need of the actual application.
This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the
creation of this library.






Result Codes

0
Success

ENOSYS
The functionality is not supported.

EBUSY
The FB is busy with another client.

EINVAL
Invalid line ID for output

EPROTONOSUPPORT
Device is configured for RS485 protocol.

EBADF
Bad handle to serial port

EACCES
Could not set the line. FbSerialInterface_internal.SetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
SetLineState
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

eLineID
eTTYLineID
Line whose state is to be set.

xState
BOOL
TRUE = active, FALSE = inactive





Allows control of the hardware lines by the application
Normally, these lines are controlled by hardware handshake internally.
Nevertheless, when no hardware handshake is involved, the
serial lines might be used for very individual purposes.
In the latter case, these hardware wires can be manipulated directly with this functions to desired
levels, according to the need of the actual application.
This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the
creation of this library.






Result Codes

0
Success

ENOSYS
The functionality is not supported.

EBUSY
The FB is busy with another client.

EINVAL
Invalid line ID for output

EPROTONOSUPPORT
Device is configured for RS485 protocol.

EBADF
Bad handle to serial port

EACCES
Could not set the line. FbSerialInterface_internal.SetLineState (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
SetLineState
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

eLineID
eTTYLineID
Line whose state is to be set.

xState
BOOL
TRUE = active, FALSE = inactive





Allows control of the hardware lines by the application
Normally, these lines are controlled by hardware handshake internally.
Nevertheless, when no hardware handshake is involved, the
serial lines might be used for very individual purposes.
In the latter case, these hardware wires can be manipulated directly with this functions to desired
levels, according to the need of the actual application.
This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the
creation of this library.






Result Codes

0
Success

ENOSYS
The functionality is not supported.

EBUSY
The FB is busy with another client.

EINVAL
Invalid line ID for output

EPROTONOSUPPORT
Device is configured for RS485 protocol.

EBADF
Bad handle to serial port

EACCES
Could not set the line. Interface variables








Scope
Name
Type
Comment



Return
SetLineState
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

eLineID
eTTYLineID
Line whose state is to be set.

xState
BOOL
TRUE = active, FALSE = inactive Interface variables Scope
Name
Type
Comment



Return
SetLineState
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

eLineID
eTTYLineID
Line whose state is to be set.

xState
BOOL
TRUE = active, FALSE = inactive Allows control of the hardware lines by the application Normally, these lines are controlled by hardware handshake internally.
Nevertheless, when no hardware handshake is involved, the
serial lines might be used for very individual purposes. In the latter case, these hardware wires can be manipulated directly with this functions to desired
levels, according to the need of the actual application.
This allows the implementation of some exotic handshake schemes which were not foreseen at the time of the
creation of this library.

#### Code Examples

```
SetLineState
```

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.TestExclusivity (METH)

**File:** `khFmInkqN_boaOSEy6Yk4sm0688\testexclusivity.html`

Check if exclusive usage has been granted.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | TestExclusivity | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Address of the instance |

#### Additional Information

| Column 1 |
| --- |
| result codes |
| 0 |
| EUNATCH |
| EBUSY |

#### Details

FbSerialInterface_internal.TestExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
TestExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Check if exclusive usage has been granted.
This method tests if an FB has been granted exclusive use of the device,
but without trying to attach it.
Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.






result codes

0
Success, the device is free and may be attached exclusively.

EUNATCH
The device is not attached.

EBUSY
Exclusive use can not be granted. The device is already attached to another FB. FbSerialInterface_internal.TestExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
TestExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Check if exclusive usage has been granted.
This method tests if an FB has been granted exclusive use of the device,
but without trying to attach it.
Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.






result codes

0
Success, the device is free and may be attached exclusively.

EUNATCH
The device is not attached.

EBUSY
Exclusive use can not be granted. The device is already attached to another FB. FbSerialInterface_internal.TestExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
TestExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Check if exclusive usage has been granted.
This method tests if an FB has been granted exclusive use of the device,
but without trying to attach it.
Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.






result codes

0
Success, the device is free and may be attached exclusively.

EUNATCH
The device is not attached.

EBUSY
Exclusive use can not be granted. The device is already attached to another FB. FbSerialInterface_internal.TestExclusivity (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
TestExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance





Check if exclusive usage has been granted.
This method tests if an FB has been granted exclusive use of the device,
but without trying to attach it.
Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.






result codes

0
Success, the device is free and may be attached exclusively.

EUNATCH
The device is not attached.

EBUSY
Exclusive use can not be granted. The device is already attached to another FB. Interface variables








Scope
Name
Type
Comment



Return
TestExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance Interface variables Scope
Name
Type
Comment



Return
TestExclusivity
eResultCode
 

Input
RequestorID
WagoClientIdentification
Address of the instance Check if exclusive usage has been granted. This method tests if an FB has been granted exclusive use of the device,
but without trying to attach it. Note (1): “RequestorID” corresponds to the address of the instance which wants to use the device exclusively.

#### Code Examples

```
TestExclusivity
```

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

---

### FbSerialInterface_internal.UnregisterSniffer (METH)

**File:** `PMO1c8S6g3uyPZcIQwLIeCQcHO8\unregistersniffe.html`

#### Interface Variables

| Scope | Name | Type |
| --- | --- | :---: |
| Return | UnregisterSniffer | BOOL |
| Input | IComSniffer | WagoTypesCom.I_ComSniffer |

#### Details

FbSerialInterface_internal.UnregisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
UnregisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer FbSerialInterface_internal.UnregisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
UnregisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer FbSerialInterface_internal.UnregisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
UnregisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer FbSerialInterface_internal.UnregisterSniffer (METH)¶

Interface variables







Scope
Name
Type



Return
UnregisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer Interface variables







Scope
Name
Type



Return
UnregisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer Interface variables Scope
Name
Type



Return
UnregisterSniffer
BOOL

Input
IComSniffer
WagoTypesCom.I_ComSniffer

#### Code Examples

```
UnregisterSniffer
```

```
IComSniffer
```

```
WagoTypesCom.I_ComSniffer
```

---

### FbSerialInterface_internal.Write (METH)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\write.html`

Writes data to the serial port.

#### Interface Variables

| Scope | Name | Type | Comment |
| --- | --- | :---: | :--- |
| Return | Write | eResultCode | - |
| Input | RequestorID | WagoClientIdentification | Unique identification of the caller |
| pTxBuffer | POINTER TO BYTE | Location of write data | - |
| udiTxNBytes | UDINT | Number of bytes to be written. | - |
| Output | udiTxNBytesTransferred | UDINT | Number of transferred bytes |

#### Additional Information

| Column 1 |
| --- |
| Result Codes |
| 0 |
| EBUSY |
| EINVAL |
| EACCES |
| EBADF |
| EWOULDBLOCK |

#### Details

FbSerialInterface_internal.Write (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Write
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pTxBuffer
POINTER TO BYTE
Location of write data

udiTxNBytes
UDINT
Number of bytes to be written.

Output
udiTxNBytesTransferred
UDINT
Number of transferred bytes





Writes data to the serial port.
The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent.
Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens.
Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred
to the system  layer.
If this is less than the requested amount, write() returns with EWOULDBLOCK.
This is not an error, but a regular state: The remaining bytes should be re-sent later
with consecutive write() calls until all bytes are successfully sent.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EACCES
There was a problem while opening the system com_port.

EBADF
The com-port was not open.

EWOULDBLOCK
Not all data could be sent at once. FbSerialInterface_internal.Write (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Write
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pTxBuffer
POINTER TO BYTE
Location of write data

udiTxNBytes
UDINT
Number of bytes to be written.

Output
udiTxNBytesTransferred
UDINT
Number of transferred bytes





Writes data to the serial port.
The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent.
Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens.
Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred
to the system  layer.
If this is less than the requested amount, write() returns with EWOULDBLOCK.
This is not an error, but a regular state: The remaining bytes should be re-sent later
with consecutive write() calls until all bytes are successfully sent.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EACCES
There was a problem while opening the system com_port.

EBADF
The com-port was not open.

EWOULDBLOCK
Not all data could be sent at once. FbSerialInterface_internal.Write (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Write
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pTxBuffer
POINTER TO BYTE
Location of write data

udiTxNBytes
UDINT
Number of bytes to be written.

Output
udiTxNBytesTransferred
UDINT
Number of transferred bytes





Writes data to the serial port.
The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent.
Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens.
Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred
to the system  layer.
If this is less than the requested amount, write() returns with EWOULDBLOCK.
This is not an error, but a regular state: The remaining bytes should be re-sent later
with consecutive write() calls until all bytes are successfully sent.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EACCES
There was a problem while opening the system com_port.

EBADF
The com-port was not open.

EWOULDBLOCK
Not all data could be sent at once. FbSerialInterface_internal.Write (METH)¶

Interface variables








Scope
Name
Type
Comment



Return
Write
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pTxBuffer
POINTER TO BYTE
Location of write data

udiTxNBytes
UDINT
Number of bytes to be written.

Output
udiTxNBytesTransferred
UDINT
Number of transferred bytes





Writes data to the serial port.
The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent.
Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens.
Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred
to the system  layer.
If this is less than the requested amount, write() returns with EWOULDBLOCK.
This is not an error, but a regular state: The remaining bytes should be re-sent later
with consecutive write() calls until all bytes are successfully sent.






Result Codes

0
Success

EBUSY
The FB is busy with another client.

EINVAL
Invalid arguments for buffer size or location (programming error)

EACCES
There was a problem while opening the system com_port.

EBADF
The com-port was not open.

EWOULDBLOCK
Not all data could be sent at once. Interface variables








Scope
Name
Type
Comment



Return
Write
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pTxBuffer
POINTER TO BYTE
Location of write data

udiTxNBytes
UDINT
Number of bytes to be written.

Output
udiTxNBytesTransferred
UDINT
Number of transferred bytes Interface variables Scope
Name
Type
Comment



Return
Write
eResultCode
 

Input
RequestorID
WagoClientIdentification
Unique identification of the caller

pTxBuffer
POINTER TO BYTE
Location of write data

udiTxNBytes
UDINT
Number of bytes to be written.

Output
udiTxNBytesTransferred
UDINT
Number of transferred bytes Writes data to the serial port. The inputs ‘pTxBuffer’ and ‘udiTxNBytes’ denote the location and the size of the data to be sent.
Note: it is formally ok, to pass 0 bytes for write. In that case, simply nothing happens. Via ‘udiTxNBytesTransferred’ a feedback is given, how many bytes are actually transferred
to the system  layer.
If this is less than the requested amount, write() returns with EWOULDBLOCK.
This is not an error, but a regular state: The remaining bytes should be re-sent later
with consecutive write() calls until all bytes are successfully sent.

#### Code Examples

```
eResultCode
```

```
RequestorID
```

```
WagoClientIdentification
```

```
udiTxNBytes
```

```
udiTxNBytesTransferred
```

---

## Interfaces

### 10 I_WagoSysComBase

**File:** `v7ipmO78OAlrgxPUENG1IUz6Zo8\fld-10-I_WagoSysComBase.html`

10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)

#### Details

10 I_WagoSysComBase¶


10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 10 I_WagoSysComBase¶


10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 10 I_WagoSysComBase¶


10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 10 I_WagoSysComBase¶


10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)

---

### 10 Main Interface

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\fld-10-Main-Interface.html`

This section contains the most prominent and most frequently used parts of the interface.

#### Details

10 Main Interface¶
This section contains the most prominent and most frequently used parts of the interface.


FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP) 10 Main Interface¶
This section contains the most prominent and most frequently used parts of the interface.


FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP) 10 Main Interface¶
This section contains the most prominent and most frequently used parts of the interface.


FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP) 10 Main Interface¶
This section contains the most prominent and most frequently used parts of the interface.


FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP) This section contains the most prominent and most frequently used parts of the interface. FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)

---

### 20 I_SupportComSniffer

**File:** `PMO1c8S6g3uyPZcIQwLIeCQcHO8\fld-20-I_SupportComSniffer.html`

FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH)

#### Details

20 I_SupportComSniffer¶


FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) 20 I_SupportComSniffer¶


FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) 20 I_SupportComSniffer¶


FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) 20 I_SupportComSniffer¶


FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH)

---

### FbSerialInterface_internal (FB)

**File:** `uVyrNCMFn6H9ilTqc0UUi5ghT9A\fbserialinterfac.html`

This is the fundamental FB of this library and contains the interface to the pyhsical serial interface.

#### Details

FbSerialInterface_internal (FB)¶
This is the fundamental FB of this library and contains the interface to the pyhsical serial interface.
Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’.
Please Note: This FB is meant to be accessed by application-level FBs from WagoAppCom.library.
Under normal circumstances it should not be used directly.
Multiple application FBs may share one physical serial interface FB, but in that case they
must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application,
it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again.


10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) FbSerialInterface_internal (FB)¶
This is the fundamental FB of this library and contains the interface to the pyhsical serial interface.
Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’.
Please Note: This FB is meant to be accessed by application-level FBs from WagoAppCom.library.
Under normal circumstances it should not be used directly.
Multiple application FBs may share one physical serial interface FB, but in that case they
must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application,
it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again.


10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) FbSerialInterface_internal (FB)¶
This is the fundamental FB of this library and contains the interface to the pyhsical serial interface.
Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’.
Please Note: This FB is meant to be accessed by application-level FBs from WagoAppCom.library.
Under normal circumstances it should not be used directly.
Multiple application FBs may share one physical serial interface FB, but in that case they
must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application,
it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again.


10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) FbSerialInterface_internal (FB)¶
This is the fundamental FB of this library and contains the interface to the pyhsical serial interface.
Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’.
Please Note: This FB is meant to be accessed by application-level FBs from WagoAppCom.library.
Under normal circumstances it should not be used directly.
Multiple application FBs may share one physical serial interface FB, but in that case they
must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application,
it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again.


10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) This is the fundamental FB of this library and contains the interface to the pyhsical serial interface. Each open FB represents one physical serial interface according to ‘I_WagoSysComBase’. Please Note: This FB is meant to be accessed by application-level FBs from WagoAppCom.library.
Under normal circumstances it should not be used directly. Multiple application FBs may share one physical serial interface FB, but in that case they
must not be open simultaneously. I.e. if an FbSerialInterface_internal is opened by one application,
it cannot be opened once more by another application FB until the first ‘open()’ is ‘close()’d again. 10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH)

---

### FbSerialInterface_internal.DeferredResult (PROP)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\deferredresult.html`

Status of the channel after deferred method

#### Additional Information

| Column 1 |
| --- |
| result codes |
| 0 |
| EAGAIN |
| ENOPROTOOPT |
| EBADF |
| EINVAL |
| EACCESS |

#### Details

FbSerialInterface_internal.DeferredResult (PROP)¶
Status of the channel after deferred method
This property contains a getter to obtain the actual state of a channel: ready or not after
potentially deferred methods: Open(), Close(), or Clearbuffers().
Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter
always returns the direct results which were delivered by those methods and should never
return EAGAIN.






result codes

0
Ok: the channel is operative.

EAGAIN
Open() is pending, no feedback so far. (no error)

ENOPROTOOPT
Configuration options not available for this device. (e.g. hardware handshake, error)

EBADF
The FB is not open. (error)

EINVAL
Invalid parameters. (error)

EACCESS
Other Problems while accessing the serial port. (error) FbSerialInterface_internal.DeferredResult (PROP)¶
Status of the channel after deferred method
This property contains a getter to obtain the actual state of a channel: ready or not after
potentially deferred methods: Open(), Close(), or Clearbuffers().
Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter
always returns the direct results which were delivered by those methods and should never
return EAGAIN.






result codes

0
Ok: the channel is operative.

EAGAIN
Open() is pending, no feedback so far. (no error)

ENOPROTOOPT
Configuration options not available for this device. (e.g. hardware handshake, error)

EBADF
The FB is not open. (error)

EINVAL
Invalid parameters. (error)

EACCESS
Other Problems while accessing the serial port. (error) FbSerialInterface_internal.DeferredResult (PROP)¶
Status of the channel after deferred method
This property contains a getter to obtain the actual state of a channel: ready or not after
potentially deferred methods: Open(), Close(), or Clearbuffers().
Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter
always returns the direct results which were delivered by those methods and should never
return EAGAIN.






result codes

0
Ok: the channel is operative.

EAGAIN
Open() is pending, no feedback so far. (no error)

ENOPROTOOPT
Configuration options not available for this device. (e.g. hardware handshake, error)

EBADF
The FB is not open. (error)

EINVAL
Invalid parameters. (error)

EACCESS
Other Problems while accessing the serial port. (error) FbSerialInterface_internal.DeferredResult (PROP)¶
Status of the channel after deferred method
This property contains a getter to obtain the actual state of a channel: ready or not after
potentially deferred methods: Open(), Close(), or Clearbuffers().
Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter
always returns the direct results which were delivered by those methods and should never
return EAGAIN.






result codes

0
Ok: the channel is operative.

EAGAIN
Open() is pending, no feedback so far. (no error)

ENOPROTOOPT
Configuration options not available for this device. (e.g. hardware handshake, error)

EBADF
The FB is not open. (error)

EINVAL
Invalid parameters. (error)

EACCESS
Other Problems while accessing the serial port. (error) Status of the channel after deferred method This property contains a getter to obtain the actual state of a channel: ready or not after
potentially deferred methods: Open(), Close(), or Clearbuffers(). Note: As this implementation of ‘I_WagoSysComBase’ does not defer these calls, this getter
always returns the direct results which were delivered by those methods and should never
return EAGAIN.

---

### FbSerialInterface_internal.IsTransmitterEmpty (PROP)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\istransmitteremp.html`

Determines if the transmitter still has bytes to send.

#### Additional Information

| Column 1 |
| --- |
| result codes |
| 0 |
| EINPROGRESS |
| ENOSYS |
| EACCES |

#### Details

FbSerialInterface_internal.IsTransmitterEmpty (PROP)¶
Determines if the transmitter still has bytes to send.
Three different reactions are possible:
If the transmitter is empty, this property delivers 0=OK,
if it has bytes to send, it delivers EINPROGRESS.
If the device cannot tell anything about its status, it delivers ENOSYS.
Note: In particular cases it may be technically impossible for a device to determine, whether
the transmitter still has data to send or not.






result codes

0
Transmitter is empty and has no more bytes to send.

EINPROGRESS
Transmitter still has bytes to send.

ENOSYS
This operation is not supported by the device.

EACCES
Internal error while determining the tx state. FbSerialInterface_internal.IsTransmitterEmpty (PROP)¶
Determines if the transmitter still has bytes to send.
Three different reactions are possible:
If the transmitter is empty, this property delivers 0=OK,
if it has bytes to send, it delivers EINPROGRESS.
If the device cannot tell anything about its status, it delivers ENOSYS.
Note: In particular cases it may be technically impossible for a device to determine, whether
the transmitter still has data to send or not.






result codes

0
Transmitter is empty and has no more bytes to send.

EINPROGRESS
Transmitter still has bytes to send.

ENOSYS
This operation is not supported by the device.

EACCES
Internal error while determining the tx state. FbSerialInterface_internal.IsTransmitterEmpty (PROP)¶
Determines if the transmitter still has bytes to send.
Three different reactions are possible:
If the transmitter is empty, this property delivers 0=OK,
if it has bytes to send, it delivers EINPROGRESS.
If the device cannot tell anything about its status, it delivers ENOSYS.
Note: In particular cases it may be technically impossible for a device to determine, whether
the transmitter still has data to send or not.






result codes

0
Transmitter is empty and has no more bytes to send.

EINPROGRESS
Transmitter still has bytes to send.

ENOSYS
This operation is not supported by the device.

EACCES
Internal error while determining the tx state. FbSerialInterface_internal.IsTransmitterEmpty (PROP)¶
Determines if the transmitter still has bytes to send.
Three different reactions are possible:
If the transmitter is empty, this property delivers 0=OK,
if it has bytes to send, it delivers EINPROGRESS.
If the device cannot tell anything about its status, it delivers ENOSYS.
Note: In particular cases it may be technically impossible for a device to determine, whether
the transmitter still has data to send or not.






result codes

0
Transmitter is empty and has no more bytes to send.

EINPROGRESS
Transmitter still has bytes to send.

ENOSYS
This operation is not supported by the device.

EACCES
Internal error while determining the tx state. Determines if the transmitter still has bytes to send. Three different reactions are possible: If the transmitter is empty, this property delivers 0=OK,
if it has bytes to send, it delivers EINPROGRESS.
If the device cannot tell anything about its status, it delivers ENOSYS. Note: In particular cases it may be technically impossible for a device to determine, whether
the transmitter still has data to send or not.

---

### FbSerialInterface_internal.Name (PROP)

**File:** `eVLj1s0_HPjWHBhQFl526Th5Tks\name.html`

Returns the name of the connected interface.

#### Details

FbSerialInterface_internal.Name (PROP)¶
Returns the name of the connected interface.
In this implementation strings as ‘COM1’..’COM4’ are returned. FbSerialInterface_internal.Name (PROP)¶
Returns the name of the connected interface.
In this implementation strings as ‘COM1’..’COM4’ are returned. FbSerialInterface_internal.Name (PROP)¶
Returns the name of the connected interface.
In this implementation strings as ‘COM1’..’COM4’ are returned. FbSerialInterface_internal.Name (PROP)¶
Returns the name of the connected interface.
In this implementation strings as ‘COM1’..’COM4’ are returned. Returns the name of the connected interface. In this implementation strings as ‘COM1’..’COM4’ are returned.

---

### FbSerialInterface_internal.isOpen (PROP)

**File:** `dHW61L1yhwWuMnKwb32ecgPz3BY\isopen.html`

Tells if the FB is ready for operation.

#### Details

FbSerialInterface_internal.isOpen (PROP)¶
Tells if the FB is ready for operation.
This property merely contains a getter function to obtain the actual state
of a channel connected to an interface: ready for operation or not. FbSerialInterface_internal.isOpen (PROP)¶
Tells if the FB is ready for operation.
This property merely contains a getter function to obtain the actual state
of a channel connected to an interface: ready for operation or not. FbSerialInterface_internal.isOpen (PROP)¶
Tells if the FB is ready for operation.
This property merely contains a getter function to obtain the actual state
of a channel connected to an interface: ready for operation or not. FbSerialInterface_internal.isOpen (PROP)¶
Tells if the FB is ready for operation.
This property merely contains a getter function to obtain the actual state
of a channel connected to an interface: ready for operation or not. Tells if the FB is ready for operation. This property merely contains a getter function to obtain the actual state
of a channel connected to an interface: ready for operation or not.

---

## Administration

### 40 Administration

**File:** `eVLj1s0_HPjWHBhQFl526Th5Tks\fld-40-Administration.html`

This section contains administrative functionalities, such as initialization, cyclic operation, etc.

#### Details

40 Administration¶
This section contains administrative functionalities, such as initialization, cyclic operation, etc.


FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 40 Administration¶
This section contains administrative functionalities, such as initialization, cyclic operation, etc.


FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 40 Administration¶
This section contains administrative functionalities, such as initialization, cyclic operation, etc.


FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) 40 Administration¶
This section contains administrative functionalities, such as initialization, cyclic operation, etc.


FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP) This section contains administrative functionalities, such as initialization, cyclic operation, etc. FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)

---

## Exclusive Use

### 30 Exclusive Use

**File:** `khFmInkqN_boaOSEy6Yk4sm0688\fld-30-Exclusive-Use.html`

Here we have methods for ensuring that a  FbSerialInterface instance is operated from only one application FB exclusively.

#### Details

30 Exclusive Use¶
Here we have methods for ensuring that a  FbSerialInterface instance is operated from only one application FB exclusively.


FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH) 30 Exclusive Use¶
Here we have methods for ensuring that a  FbSerialInterface instance is operated from only one application FB exclusively.


FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH) 30 Exclusive Use¶
Here we have methods for ensuring that a  FbSerialInterface instance is operated from only one application FB exclusively.


FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH) 30 Exclusive Use¶
Here we have methods for ensuring that a  FbSerialInterface instance is operated from only one application FB exclusively.


FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH) Here we have methods for ensuring that a  FbSerialInterface instance is operated from only one application FB exclusively. FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)

---

## Module Fields

### 10 Documentation

**File:** `Z03moY3bEX0a3oYIvLFkB7lbXSw\fld-10-Documentation.html`

doc10_general (FB)

#### Details

10 Documentation¶


doc10_general (FB) 10 Documentation¶


doc10_general (FB) 10 Documentation¶


doc10_general (FB) 10 Documentation¶


doc10_general (FB) doc10_general (FB)

---

### 20 Program Organization Units

**File:** `uVyrNCMFn6H9ilTqc0UUi5ghT9A\fld-20-Program-Organization-Units.html`

FbSerialInterface_internal (FB)
10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH)

#### Details

20 Program Organization Units¶


FbSerialInterface_internal (FB)
10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) 20 Program Organization Units¶


FbSerialInterface_internal (FB)
10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) 20 Program Organization Units¶


FbSerialInterface_internal (FB)
10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) 20 Program Organization Units¶


FbSerialInterface_internal (FB)
10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH) FbSerialInterface_internal (FB)
10 I_WagoSysComBase
10 Main Interface
FbSerialInterface_internal.ClearBuffers (METH)
FbSerialInterface_internal.Close (METH)
FbSerialInterface_internal.Configure (METH)
FbSerialInterface_internal.DeferredResult (PROP)
FbSerialInterface_internal.IsTransmitterEmpty (PROP)
FbSerialInterface_internal.Open (METH)
FbSerialInterface_internal.Read (METH)
FbSerialInterface_internal.Write (METH)
FbSerialInterface_internal.isOpen (PROP)


20 Hardware Lines
FbSerialInterface_internal.GetLineState (METH)
FbSerialInterface_internal.IsLineAvailable (METH)
FbSerialInterface_internal.SetLineState (METH)


30 Exclusive Use
FbSerialInterface_internal.AttachExclusively (METH)
FbSerialInterface_internal.ForceDetachment (METH)
FbSerialInterface_internal.ReleaseExclusivity (METH)
FbSerialInterface_internal.TestExclusivity (METH)


40 Administration
FbSerialInterface_internal.Cyclic (METH)
FbSerialInterface_internal.Finish (METH)
FbSerialInterface_internal.GetErrorObject (METH)
FbSerialInterface_internal.Initialize (METH)
FbSerialInterface_internal.Name (PROP)




20 I_SupportComSniffer
FbSerialInterface_internal.RegisterSniffer (METH)
FbSerialInterface_internal.UnregisterSniffer (METH)

---

## Documentation

### doc10_general (FB)

**File:** `Z03moY3bEX0a3oYIvLFkB7lbXSw\doc10-general.html`

This library provides target specific internal functions and TSC-functions for handling the
internal COM (physical) interfaces of PFC.
Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’.

#### Details

doc10_general (FB)¶

This library provides target specific internal functions and TSC-functions for handling the
internal COM (physical) interfaces of PFC.
Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’.
Please note: The components of that interface are not meant to be used directly by application programs.
Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to
instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide
appropriate functionality at application-level.
Those libraries are also capable of handling other implementations of this software interface,
e.g. those for K-Bus hardware.
Under normal circumstances, the functions and methods which are described in this document
should only be used in libraries, never in applications.
Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for
a more comprehensive description of the functionality of that interface.
Note(2): Additionally this library also contains code for mediating between firmware
compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation.
These functions are visible only in the original source code and are otherwise hidden in the public
documentation, because the interfaces of these non-public parts may change without further notice.
For detailed information about data types which are used in this internal library, please refer
to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library . doc10_general (FB)¶

This library provides target specific internal functions and TSC-functions for handling the
internal COM (physical) interfaces of PFC.
Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’.
Please note: The components of that interface are not meant to be used directly by application programs.
Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to
instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide
appropriate functionality at application-level.
Those libraries are also capable of handling other implementations of this software interface,
e.g. those for K-Bus hardware.
Under normal circumstances, the functions and methods which are described in this document
should only be used in libraries, never in applications.
Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for
a more comprehensive description of the functionality of that interface.
Note(2): Additionally this library also contains code for mediating between firmware
compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation.
These functions are visible only in the original source code and are otherwise hidden in the public
documentation, because the interfaces of these non-public parts may change without further notice.
For detailed information about data types which are used in this internal library, please refer
to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library . doc10_general (FB)¶

This library provides target specific internal functions and TSC-functions for handling the
internal COM (physical) interfaces of PFC.
Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’.
Please note: The components of that interface are not meant to be used directly by application programs.
Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to
instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide
appropriate functionality at application-level.
Those libraries are also capable of handling other implementations of this software interface,
e.g. those for K-Bus hardware.
Under normal circumstances, the functions and methods which are described in this document
should only be used in libraries, never in applications.
Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for
a more comprehensive description of the functionality of that interface.
Note(2): Additionally this library also contains code for mediating between firmware
compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation.
These functions are visible only in the original source code and are otherwise hidden in the public
documentation, because the interfaces of these non-public parts may change without further notice.
For detailed information about data types which are used in this internal library, please refer
to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library . doc10_general (FB)¶

This library provides target specific internal functions and TSC-functions for handling the
internal COM (physical) interfaces of PFC.
Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’.
Please note: The components of that interface are not meant to be used directly by application programs.
Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to
instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide
appropriate functionality at application-level.
Those libraries are also capable of handling other implementations of this software interface,
e.g. those for K-Bus hardware.
Under normal circumstances, the functions and methods which are described in this document
should only be used in libraries, never in applications.
Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for
a more comprehensive description of the functionality of that interface.
Note(2): Additionally this library also contains code for mediating between firmware
compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation.
These functions are visible only in the original source code and are otherwise hidden in the public
documentation, because the interfaces of these non-public parts may change without further notice.
For detailed information about data types which are used in this internal library, please refer
to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library . This library provides target specific internal functions and TSC-functions for handling the
internal COM (physical) interfaces of PFC.
Mainly it provides the FB ‘FbSerialInterface_internal’ which implements the interface ‘I_WagoSysComBase’. Please note: The components of that interface are not meant to be used directly by application programs. Instead, there exist more high-level libraries, e.g. WagoAppCom, which take references to
instances of I_WagoSysComBase or FbSerialInterface_internal as input parameter and then provide
appropriate functionality at application-level.
Those libraries are also capable of handling other implementations of this software interface,
e.g. those for K-Bus hardware.
Under normal circumstances, the functions and methods which are described in this document
should only be used in libraries, never in applications. Please refer to the specification of I_WagoSysComBase in WagoTypesCom_Internal.library for
a more comprehensive description of the functionality of that interface. Note(2): Additionally this library also contains code for mediating between firmware
compontents (TSC) and the formal ‘I_WagoSysComBase’-Implementation.
These functions are visible only in the original source code and are otherwise hidden in the public
documentation, because the interfaces of these non-public parts may change without further notice. For detailed information about data types which are used in this internal library, please refer
to the type definitions given in WagoTypesCom.library and WagoTypesCommon.library .

---

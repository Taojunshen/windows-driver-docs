---
title: Details of the Extended Format
description: Details of the Extended Format
ms.assetid: e9cd2bc7-99c1-4aca-91b0-9faefa4a856d
keywords: ["Direct3D version 10.1 WDK Windows 7 display , extended format", "extended format WDK Windows 7 display"]
---

# Details of the Extended Format


This section applies only to Windows 7 and later operating systems.

In the following table, the XR part of a format name can be considered a new shader interpretation of the bits akin to UNORM or SINT. The XR\_BIAS part of a format name is a special case that overloads this interpretation semantic with additional metadata. This metadata indicates that the format must be explicitly offset and biased in shader code on transitions into and out of the shader. The driver is not required to perform any of this biasing work; it is left entirely to the application.

The following table shows resources with particular attributes that use the extended formats if the hardware supports these extended formats for the resource with those attributes or if extended formats for those resources are optional.

Formats (DXGI\_FORMAT\_\*)
B8G8R8A8
B8G8R8A8
B8G8R8X8
B8G8R8X8
R10G10B10
Resource
B8G8R8A8
\_UNORM
\_UNORM
B8G8R8X8
\_UNORM
\_UNORM
R10G10B10A2
\_XR\_BIAS
attribute
\_TYPELESS
(existing)
\_SRGB
\_TYPELESS
(existing)
\_SRGB
\_TYPELESS
\_A2\_UNORM
Buffer

N/A

R

(changed)

N/A

N/A

R

(changed)

N/A

N/A

N/A

Input

Assembler

Vertex

Buffer

N/A

R

(changed)

N/A

N/A

R

(changed)

N/A

N/A

N/A

Texture1D

R

R

(changed)

R

R

R

(changed)

R

R

N/A

Texture2D

R

R

(changed)

R

R

R

R

R

R

Texture3D

R

R

(changed)

R

R

R

(changed)

R

R

N/A

Texture

Cube

R

R

(changed)

R

R

R

(changed)

R

R

N/A

Shader ID

N/A

R

R

N/A

R

R

N/A

N/A

Shader

Sample

(any filter)

N/A

R

R

N/A

R

R

N/A

N/A

MIP-map

textures

R

R

(changed)

R

R

R

(changed)

R

R

N/A

MIP-map

Auto-

Generation

N/A

R

(changed)

R

N/A

R

(changed)

R

N/A

N/A

Render

Target

N/A

R

R

N/A

R

R

N/A

N/A

Blendable

Render

Target

N/A

R

R

N/A

R

R

N/A

N/A

CPU

Lockable

R

R

R

R

R

R

R

R

Multi-

Sample

Render

Target

N/A

O

O

N/A

o

o

N/A

N/A

Multi-

Sample

Resolve

N/A

R

(changed)

R

N/A

R

(changed)

R

N/A

N/A

Multi-

Sample

Load

N/A

R

R

N/A

R

R

N/A

N/A

Display

Scan Out

N/A

R

(changed)

R

N/A

N/A

N/A

N/A

R

Cast

Within Bit

Layout

R

R

(changed)

R

R

R

R

R

R

 

**Note**   In the preceding table, cell entries have the following meaning:
-   "R" indicates that hardware support is required

-   "o" indicates that hardware support is optional

-   N/A indicates that the resource attribute either is not applicable to the extended format or does not allow the extended format

 

**Note**   The DXGI\_FORMAT\_B8G8R8A8\_UNORM and DXGI\_FORMAT\_B8G8R8X8\_UNORM formats already existed in the DXGI\_FORMAT enumeration. However, they are now considered members of the appropriate new family. Their requirements have changed compared to their original definitions.

 

**Note**   Rows for the "Input Assembler Index Buffer", "Shader sample\_c (comparison filter)", "Shader sample (mono 1-bit filter)", "Shader gather4", and "Depth-Stencil Target" resource attributes are not included in the preceding table for readability. All meaning for these resource attributes is N/A.

 

The following sections describe the details of the new extended formats:

[XR Layout](xr-layout.md)

[XR Format Alpha Content](xr-format-alpha-content.md)

[DXGI\_FORMAT\_R10G10B10\_XR\_BIAS\_A2\_UNORM](dxgi-format-r10g10b10-xr-bias-a2-unorm.md)

[Casting Ability of XR Formats](casting-ability-of-xr-formats.md)

[XR\_BIAS Color Channel Conversion Rules](xr-bias-color-channel-conversion-rules.md)

[Interpretation of X Channel](interpretation-of-x-channel.md)

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20[display\display]:%20Details%20of%20the%20Extended%20Format%20%20RELEASE:%20%282/10/2017%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")





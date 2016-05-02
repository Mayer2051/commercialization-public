---
author: joshbax-msft
title: DXGI SCDest Buffer (D3D10.1 on feature levels 9.1-10.1)
description: DXGI SCDest Buffer (D3D10.1 on feature levels 9.1-10.1)
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 383e3ba9-38f6-4a27-a821-2aa784874b8e
---

# DXGI SCDest Buffer (D3D10.1 on feature levels 9.1-10.1)


This automated test verifies whether drivers can support the application programming interface (API) UpdateSubresource well. API UpdateSubresource takes the swap chain as the destination buffer.

This test should be run against drivers for Microsoft® Direct3d 10.1 and later, as well as associated feature levels.

This topic applies to the following test jobs:

-   DXGI SCDest Buffer (D3D10.1 on feature levels 9.1-10.1)

-   DXGI SCDest Buffer (D3D11 on feature levels 9.1 and 10.0)

## Test details


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Associated requirements</strong></p></td>
<td><p>Device.Graphics.AdapterRender.D3D101Core.D3D101CorePrimary Device.Graphics.AdapterRender.D3D10Core.D3D10CorePrimary Device.Graphics.AdapterRender.D3D111Core.D3D111CorePrimary Device.Graphics.AdapterRender.D3D11Core.D3D11CorePrimary</p>
<p>[See the device hardware requirements.](http://go.microsoft.com/fwlink/p/?linkid=254483)</p></td>
</tr>
<tr class="even">
<td><p><strong>Platforms</strong></p></td>
<td><p>Windows 7 (x64) Windows 7 (x86) Windows RT (ARM-based) Windows 8 (x64) Windows 8 (x86) Windows Server 2012 (x64) Windows Server 2008 R2 (x64) Windows RT 8.1 Windows 8.1 x64 Windows 8.1 x86 Windows Server 2012 R2</p></td>
</tr>
<tr class="odd">
<td><p><strong>Expected run time</strong></p></td>
<td><p>~2 minutes</p></td>
</tr>
<tr class="even">
<td><p><strong>Categories</strong></p></td>
<td><p>Certification Functional</p></td>
</tr>
<tr class="odd">
<td><p><strong>Type</strong></p></td>
<td><p>Automated</p></td>
</tr>
</tbody>
</table>

 

## Running the test


Before you run the test, complete the test setup as described in the test requirements: [Graphic Adapter or Chipset Testing Prerequisites](graphic-adapter-or-chipset-testing-prerequisites.md).

## Troubleshooting


For troubleshooting information, see [Troubleshooting Device.Graphics Testing](troubleshooting-devicegraphics-testing.md).

During testing, windows filled with black and white colors appear. After testing, all windows should be closed. Check the log files to make sure that no test case has failed. If a feature is unsupported, it is skipped.

## More information


### Command syntax

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Command option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>One of the following:</p>
<ul>
<li><p><strong>DXGISCDestBuffer -DX10.1 -FeatureLevel:10.0 -whql -logclean</strong></p></li>
<li><p><strong>DXGISCDestBuffer -DX10.1 -FeatureLevel:10.1 -whql -logclean</strong></p></li>
<li><p><strong>DXGISCDestBuffer -DX10.1 -FeatureLevel:9.1 -whql -logclean</strong></p></li>
<li><p><strong>DXGISCDestBuffer -DX10.1 -FeatureLevel:9.2 -whql -logclean</strong></p></li>
<li><p><strong>DXGISCDestBuffer -DX10.1 -FeatureLevel:9.3 -whql -logclean</strong></p></li>
</ul></td>
<td><p>These command line arguments run each of the Direct3d 10.1 test cases (specifically the feature levels 9.1 through10.1).</p></td>
</tr>
<tr class="even">
<td><p>One of the following:</p>
<ul>
<li><p><strong>DXGISCDestBuffer -DX11 -FeatureLevel:10.0 -whql -logclean</strong></p></li>
<li><p><strong>DXGISCDestBuffer -DX11 -FeatureLevel:9.1 -whql -logclean</strong></p></li>
</ul></td>
<td><p>These command line arguments run each of the Direct3d 11 test cases (specifically the feature levels 9.1 and 10.0).</p></td>
</tr>
</tbody>
</table>

 

**Note**  
For command-line help for this test binary, type **/?**

 

### File list

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>File</th>
<th>Location</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Configdisplay.exe</p></td>
<td><p>[testbinroot]\TestBinRoot]\nttest\windowstest\tools\</p></td>
</tr>
<tr class="even">
<td><p>D3d10ref.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="odd">
<td><p>D3d10SDKLayers.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="even">
<td><p>D3d11_1SDKLayers.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="odd">
<td><p>D3d11ref.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="even">
<td><p>D3d11RuntimeLayers.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="odd">
<td><p>D3d11SDKLayers.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="even">
<td><p>D3dcompiler_test.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="odd">
<td><p>D3dx10_test.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="even">
<td><p>D3dx11_TEST.dll</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\support\</p></td>
</tr>
<tr class="odd">
<td><p>DXGISCDestBuffer.exe</p></td>
<td><p>[testbinroot]\nttest\windowstest\graphics\d3d\api\</p></td>
</tr>
<tr class="even">
<td><p>TDRWatch.exe</p></td>
<td><p>[testbinroot]\TestBinRoot]\nttest\windowstest\graphics\</p></td>
</tr>
</tbody>
</table>

 

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bp_hck\p_hck%5D:%20DXGI%20SCDest%20Buffer%20%28D3D10.1%20on%20feature%20levels%209.1-10.1%29%20%20RELEASE:%20%284/27/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




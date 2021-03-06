---
title: DocumentSizeAutoDetect element
description: The optional DocumentSizeAutoDetect element specifies whether the scan device automatically determines the size of the original scan media.
ms.assetid: 509e96d8-c99b-4d6e-9117-b9aed199da2c
keywords: ["DocumentSizeAutoDetect element Imaging Devices"]
topic_type:
- apiref
api_name:
- wscn DocumentSizeAutoDetect
api_type:
- Schema
ms.author: windowsdriverdev
ms.date: 11/28/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-devices
---

# DocumentSizeAutoDetect element


The optional **DocumentSizeAutoDetect** element specifies whether the scan device automatically determines the size of the original scan media.

Usage
-----

``` syntax
<wscn:DocumentSizeAutoDetect>
  text
</wscn:DocumentSizeAutoDetect>
```

Attributes
----------

There are no attributes.

Text value
----------

Required. A Boolean value that must be 0, false, 1, or true.**falsetrue**

## Child elements


There are no child elements.

## Parent elements


<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>[<strong>InputSize</strong>](inputsize.md)</p></td>
</tr>
</tbody>
</table>

Remarks
-------

If the specified text value is 1 or **true**, the scan device will automatically determine the size of the original scan media. If the **DocumentSizeAutoDetect** element is specified along with a [**ScanRegion**](scanregion.md) element, the scan region will be ignored if it falls outside of the media size that the device detected.

## <span id="see_also"></span>See also


[**ScanRegion**](scanregion.md)

[**InputSize**](inputsize.md)

 

 







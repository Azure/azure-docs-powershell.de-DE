---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: de59e8a9dc2fdcc4fa29409eaffc7f82e7d57b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931376"
---
# <span data-ttu-id="0dc34-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="0dc34-101">New-AzImageConfig</span></span>

## <span data-ttu-id="0dc34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dc34-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc34-103">Erstellt ein konfigurierbares Bildobjekt.</span><span class="sxs-lookup"><span data-stu-id="0dc34-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="0dc34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0dc34-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dc34-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0dc34-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc34-106">Das **Cmdlet New-AzImageConfig** erstellt ein konfigurierbares Bildobjekt.</span><span class="sxs-lookup"><span data-stu-id="0dc34-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="0dc34-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0dc34-107">EXAMPLES</span></span>

### <span data-ttu-id="0dc34-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0dc34-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="0dc34-109">Mit dem ersten Befehl wird ein Bildobjekt erstellt und dann in der $imageConfig gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0dc34-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="0dc34-110">Die nächsten drei Befehle weisen den Variablen $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="0dc34-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="0dc34-111">Dieser Ansatz ist nur für die Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="0dc34-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="0dc34-112">Mit den nächsten drei Befehlen werden dem in der Datei gespeicherten Bild jeweils ein Betriebssystemdatenträger und zwei Datenträger $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="0dc34-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="0dc34-113">Der URI der einzelnen Datenträger wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0dc34-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="0dc34-114">Der letzte Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0dc34-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0dc34-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0dc34-115">PARAMETERS</span></span>

### <span data-ttu-id="0dc34-116">-DataDisk</span><span class="sxs-lookup"><span data-stu-id="0dc34-116">-DataDisk</span></span>
<span data-ttu-id="0dc34-117">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="0dc34-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc34-118">-DefaultProfile</span></span>
<span data-ttu-id="0dc34-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0dc34-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="0dc34-120">-HyperVGeneration</span></span>
<span data-ttu-id="0dc34-121">Gibt den HyperVGeneration-Typ für den virtuellen Computer an, der aus dem Bild erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0dc34-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="0dc34-122">Zulässige Werte sind V1 und V2.</span><span class="sxs-lookup"><span data-stu-id="0dc34-122">Allowed values are V1 and V2.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-123">-Location</span><span class="sxs-lookup"><span data-stu-id="0dc34-123">-Location</span></span>
<span data-ttu-id="0dc34-124">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="0dc34-124">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="0dc34-125">-OsDisk</span></span>
<span data-ttu-id="0dc34-126">Gibt den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="0dc34-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0dc34-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="0dc34-128">Gibt die virtuelle Quellcomputer-ID an.</span><span class="sxs-lookup"><span data-stu-id="0dc34-128">Specifies the source virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="0dc34-129">-Tag</span></span>
<span data-ttu-id="0dc34-130">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0dc34-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0dc34-131">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0dc34-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="0dc34-132">-ZoneResilient</span></span>
<span data-ttu-id="0dc34-133">Zonenresistent aktivieren</span><span class="sxs-lookup"><span data-stu-id="0dc34-133">Enable zone resilient</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0dc34-134">-Confirm</span></span>
<span data-ttu-id="0dc34-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dc34-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dc34-136">-WhatIf</span></span>
<span data-ttu-id="0dc34-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dc34-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dc34-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dc34-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dc34-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc34-139">CommonParameters</span></span>
<span data-ttu-id="0dc34-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc34-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc34-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0dc34-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc34-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0dc34-142">INPUTS</span></span>

### <span data-ttu-id="0dc34-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0dc34-143">System.String</span></span>

### <span data-ttu-id="0dc34-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0dc34-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0dc34-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="0dc34-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="0dc34-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span><span class="sxs-lookup"><span data-stu-id="0dc34-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="0dc34-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0dc34-147">OUTPUTS</span></span>

### <span data-ttu-id="0dc34-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="0dc34-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="0dc34-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0dc34-149">NOTES</span></span>

## <span data-ttu-id="0dc34-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0dc34-150">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 0a50aa781177adb6ff457c3cc7d0a59ad8b350d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293567"
---
# <span data-ttu-id="36590-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="36590-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="36590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36590-102">SYNOPSIS</span></span>
<span data-ttu-id="36590-103">Fügt einem Bildobjekt einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="36590-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="36590-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36590-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36590-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36590-105">DESCRIPTION</span></span>
<span data-ttu-id="36590-106">Das **Cmdlet "Add-AzImageDataDisk"** fügt einem Bildobjekt einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="36590-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="36590-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36590-107">EXAMPLES</span></span>

### <span data-ttu-id="36590-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36590-108">Example 1</span></span>
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

<span data-ttu-id="36590-109">Der erste Befehl erstellt ein Bildobjekt und speichert es dann in der $imageConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="36590-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="36590-110">Mit den nächsten drei Befehlen werden den Variablen $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 Pfade des $dataDiskVhdUri Datenträgers zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="36590-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="36590-111">Dieser Ansatz ist nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="36590-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="36590-112">Mit den nächsten drei Befehlen werden dem in der Datei gespeicherten Bild jeweils ein Betriebssystemdatenträger und zwei Datenträger $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="36590-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="36590-113">Der URI der einzelnen Datenträger wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="36590-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="36590-114">Der letzte Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="36590-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="36590-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36590-115">PARAMETERS</span></span>

### <span data-ttu-id="36590-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="36590-116">-BlobUri</span></span>
<span data-ttu-id="36590-117">Gibt die Verknüpfung des BLOB als URI an.</span><span class="sxs-lookup"><span data-stu-id="36590-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="36590-118">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="36590-118">-Caching</span></span>
<span data-ttu-id="36590-119">Gibt den Cachemodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="36590-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36590-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36590-120">-DefaultProfile</span></span>
<span data-ttu-id="36590-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36590-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36590-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="36590-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="36590-123">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatz an.</span><span class="sxs-lookup"><span data-stu-id="36590-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="36590-124">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="36590-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="36590-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="36590-125">-DiskSizeGB</span></span>
<span data-ttu-id="36590-126">Gibt die Größe des Datenträgers in Gigabyte (GB) an.</span><span class="sxs-lookup"><span data-stu-id="36590-126">Specifies the size of the disk in Gigabytes (GB).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36590-127">-Image</span><span class="sxs-lookup"><span data-stu-id="36590-127">-Image</span></span>
<span data-ttu-id="36590-128">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="36590-128">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36590-129">-Lun</span><span class="sxs-lookup"><span data-stu-id="36590-129">-Lun</span></span>
<span data-ttu-id="36590-130">Gibt die Wahrheitsnummer der Einheit (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="36590-130">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36590-131">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="36590-131">-ManagedDiskId</span></span>
<span data-ttu-id="36590-132">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="36590-132">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="36590-133">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="36590-133">-SnapshotId</span></span>
<span data-ttu-id="36590-134">Gibt die ID einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="36590-134">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="36590-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="36590-135">-StorageAccountType</span></span>
<span data-ttu-id="36590-136">Der Speicherkontotyp des Datenabbilddatenträgers</span><span class="sxs-lookup"><span data-stu-id="36590-136">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="36590-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36590-137">-Confirm</span></span>
<span data-ttu-id="36590-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36590-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36590-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="36590-139">-WhatIf</span></span>
<span data-ttu-id="36590-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36590-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36590-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36590-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36590-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36590-142">CommonParameters</span></span>
<span data-ttu-id="36590-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36590-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36590-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36590-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36590-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36590-145">INPUTS</span></span>

### <span data-ttu-id="36590-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="36590-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="36590-147">System.Int32</span><span class="sxs-lookup"><span data-stu-id="36590-147">System.Int32</span></span>

### <span data-ttu-id="36590-148">System.String</span><span class="sxs-lookup"><span data-stu-id="36590-148">System.String</span></span>

### <span data-ttu-id="36590-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="36590-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="36590-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36590-150">OUTPUTS</span></span>

### <span data-ttu-id="36590-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="36590-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="36590-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36590-152">NOTES</span></span>

## <span data-ttu-id="36590-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36590-153">RELATED LINKS</span></span>

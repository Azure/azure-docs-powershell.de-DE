---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 79415e5a39703e61843fc58a55ebc4cc5168ef0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946640"
---
# <span data-ttu-id="26079-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="26079-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="26079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26079-102">SYNOPSIS</span></span>
<span data-ttu-id="26079-103">Legt die Betriebssystemdatenträgereigenschaften für ein Bildobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="26079-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="26079-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26079-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26079-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26079-105">DESCRIPTION</span></span>
<span data-ttu-id="26079-106">Das **Cmdlet Set-AzImageOsDisk** legt die Betriebssystemdatenträgereigenschaften für ein Bildobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="26079-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="26079-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26079-107">EXAMPLES</span></span>

### <span data-ttu-id="26079-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26079-108">Example 1</span></span>
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

<span data-ttu-id="26079-109">Mit dem ersten Befehl wird ein Bildobjekt erstellt und dann in der $imageConfig gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26079-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="26079-110">Die nächsten drei Befehle weisen den Variablen $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="26079-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="26079-111">Dieser Ansatz ist nur für die Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="26079-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="26079-112">Mit den nächsten drei Befehlen werden dem in der Datei gespeicherten Bild jeweils ein Betriebssystemdatenträger und zwei Datenträger $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="26079-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="26079-113">Der URI der einzelnen Datenträger wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="26079-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="26079-114">Der letzte Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="26079-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="26079-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="26079-115">PARAMETERS</span></span>

### <span data-ttu-id="26079-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="26079-116">-BlobUri</span></span>
<span data-ttu-id="26079-117">Gibt den Uri des Blobs an.</span><span class="sxs-lookup"><span data-stu-id="26079-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26079-118">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="26079-118">-Caching</span></span>
<span data-ttu-id="26079-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="26079-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26079-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26079-120">-DefaultProfile</span></span>
<span data-ttu-id="26079-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26079-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26079-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="26079-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="26079-123">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatzs an.</span><span class="sxs-lookup"><span data-stu-id="26079-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="26079-124">Dies kann nur für verwaltete Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26079-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="26079-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="26079-125">-DiskSizeGB</span></span>
<span data-ttu-id="26079-126">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="26079-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="26079-127">-Image</span><span class="sxs-lookup"><span data-stu-id="26079-127">-Image</span></span>
<span data-ttu-id="26079-128">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="26079-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="26079-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="26079-129">-ManagedDiskId</span></span>
<span data-ttu-id="26079-130">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="26079-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="26079-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="26079-131">-OsState</span></span>
<span data-ttu-id="26079-132">Gibt den Betriebssystemzustand an.</span><span class="sxs-lookup"><span data-stu-id="26079-132">Specifies the OS state.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26079-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="26079-133">-OsType</span></span>
<span data-ttu-id="26079-134">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="26079-134">Specifies the OS type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26079-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="26079-135">-SnapshotId</span></span>
<span data-ttu-id="26079-136">Gibt die ID einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="26079-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="26079-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="26079-137">-StorageAccountType</span></span>
<span data-ttu-id="26079-138">Der Speicherkontotyp von Os Image Disk</span><span class="sxs-lookup"><span data-stu-id="26079-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="26079-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26079-139">-Confirm</span></span>
<span data-ttu-id="26079-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26079-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26079-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26079-141">-WhatIf</span></span>
<span data-ttu-id="26079-142">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26079-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26079-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26079-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26079-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26079-144">CommonParameters</span></span>
<span data-ttu-id="26079-145">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26079-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26079-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26079-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26079-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26079-147">INPUTS</span></span>

### <span data-ttu-id="26079-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="26079-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="26079-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26079-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26079-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26079-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26079-151">System.String</span><span class="sxs-lookup"><span data-stu-id="26079-151">System.String</span></span>

### <span data-ttu-id="26079-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="26079-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="26079-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="26079-153">System.Int32</span></span>

## <span data-ttu-id="26079-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26079-154">OUTPUTS</span></span>

### <span data-ttu-id="26079-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="26079-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="26079-156">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="26079-156">NOTES</span></span>

## <span data-ttu-id="26079-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="26079-157">RELATED LINKS</span></span>

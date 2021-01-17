---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472969"
---
# <span data-ttu-id="2785c-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="2785c-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="2785c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2785c-102">SYNOPSIS</span></span>
<span data-ttu-id="2785c-103">Legt die Datenträgereigenschaften des Betriebssystems für ein Bildobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="2785c-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="2785c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2785c-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2785c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2785c-105">DESCRIPTION</span></span>
<span data-ttu-id="2785c-106">Das **Cmdlet "Set-AzImageOsDisk"** legt die Datenträgereigenschaften des Betriebssystems für ein Bildobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="2785c-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="2785c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2785c-107">EXAMPLES</span></span>

### <span data-ttu-id="2785c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2785c-108">Example 1</span></span>
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

<span data-ttu-id="2785c-109">Der erste Befehl erstellt ein Bildobjekt und speichert es dann in der $imageConfig Variable.</span><span class="sxs-lookup"><span data-stu-id="2785c-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="2785c-110">Mit den nächsten drei Befehlen werden den Variablen $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 Pfade des Betriebssystemdatenträgers zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2785c-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="2785c-111">Dieser Ansatz ist nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="2785c-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="2785c-112">Mit den nächsten drei Befehlen werden dem in der Datei gespeicherten Bild jeweils ein Betriebssystemdatenträger und zwei Datenträger $imageConfig.</span><span class="sxs-lookup"><span data-stu-id="2785c-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="2785c-113">Der URI der einzelnen Datenträger wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2785c-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="2785c-114">Der letzte Befehl erstellt ein Bild mit dem Namen 'ImageName01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="2785c-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="2785c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2785c-115">PARAMETERS</span></span>

### <span data-ttu-id="2785c-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="2785c-116">-BlobUri</span></span>
<span data-ttu-id="2785c-117">Gibt den URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="2785c-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="2785c-118">-Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="2785c-118">-Caching</span></span>
<span data-ttu-id="2785c-119">Gibt den Zwischenspeicherungsmodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="2785c-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="2785c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2785c-120">-DefaultProfile</span></span>
<span data-ttu-id="2785c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2785c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2785c-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="2785c-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="2785c-123">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträgerverschlüsselungssatz an.</span><span class="sxs-lookup"><span data-stu-id="2785c-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="2785c-124">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2785c-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="2785c-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2785c-125">-DiskSizeGB</span></span>
<span data-ttu-id="2785c-126">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="2785c-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="2785c-127">-Image</span><span class="sxs-lookup"><span data-stu-id="2785c-127">-Image</span></span>
<span data-ttu-id="2785c-128">Gibt ein lokales Bildobjekt an.</span><span class="sxs-lookup"><span data-stu-id="2785c-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="2785c-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="2785c-129">-ManagedDiskId</span></span>
<span data-ttu-id="2785c-130">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="2785c-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="2785c-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="2785c-131">-OsState</span></span>
<span data-ttu-id="2785c-132">Gibt den Betriebssystemzustand an.</span><span class="sxs-lookup"><span data-stu-id="2785c-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="2785c-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="2785c-133">-OsType</span></span>
<span data-ttu-id="2785c-134">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="2785c-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="2785c-135">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="2785c-135">-SnapshotId</span></span>
<span data-ttu-id="2785c-136">Gibt die ID einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="2785c-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="2785c-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2785c-137">-StorageAccountType</span></span>
<span data-ttu-id="2785c-138">Speicherkontotyp des Betriebssystemabbilddatenträgers</span><span class="sxs-lookup"><span data-stu-id="2785c-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="2785c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2785c-139">-Confirm</span></span>
<span data-ttu-id="2785c-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2785c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2785c-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2785c-141">-WhatIf</span></span>
<span data-ttu-id="2785c-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2785c-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2785c-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2785c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2785c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2785c-144">CommonParameters</span></span>
<span data-ttu-id="2785c-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2785c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2785c-146">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2785c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2785c-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2785c-147">INPUTS</span></span>

### <span data-ttu-id="2785c-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="2785c-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="2785c-149">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2785c-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2785c-150">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2785c-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2785c-151">System.String</span><span class="sxs-lookup"><span data-stu-id="2785c-151">System.String</span></span>

### <span data-ttu-id="2785c-152">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="2785c-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="2785c-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2785c-153">System.Int32</span></span>

## <span data-ttu-id="2785c-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2785c-154">OUTPUTS</span></span>

### <span data-ttu-id="2785c-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span><span class="sxs-lookup"><span data-stu-id="2785c-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="2785c-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2785c-156">NOTES</span></span>

## <span data-ttu-id="2785c-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2785c-157">RELATED LINKS</span></span>

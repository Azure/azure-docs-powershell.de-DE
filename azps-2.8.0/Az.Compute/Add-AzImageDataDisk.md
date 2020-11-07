---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: 5b3ea899b7cd1b5868fd3f230358a75e92ec1d3e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652233"
---
# <span data-ttu-id="3581a-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="3581a-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="3581a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3581a-102">SYNOPSIS</span></span>
<span data-ttu-id="3581a-103">Fügt einen Daten Datenträger zu einem Image-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="3581a-103">Adds a data disk to an image object.</span></span>

## <span data-ttu-id="3581a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3581a-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3581a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3581a-105">DESCRIPTION</span></span>
<span data-ttu-id="3581a-106">Mit dem Cmdlet " **Add-AzImageDataDisk** " wird ein Datenlaufwerk zu einem Image-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3581a-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="3581a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3581a-107">EXAMPLES</span></span>

### <span data-ttu-id="3581a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3581a-108">Example 1</span></span>
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

<span data-ttu-id="3581a-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3581a-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="3581a-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri-, $dataDiskVhdUri 1-und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="3581a-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="3581a-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="3581a-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="3581a-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild ein Betriebssystemdatenträger und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3581a-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="3581a-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3581a-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="3581a-114">Der endgültige Befehl erstellt ein Bild mit dem Namen ImageName01 in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3581a-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="3581a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3581a-115">PARAMETERS</span></span>

### <span data-ttu-id="3581a-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="3581a-116">-BlobUri</span></span>
<span data-ttu-id="3581a-117">Gibt den Link als URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="3581a-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="3581a-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="3581a-118">-Caching</span></span>
<span data-ttu-id="3581a-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3581a-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="3581a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3581a-120">-DefaultProfile</span></span>
<span data-ttu-id="3581a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3581a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3581a-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3581a-122">-DiskSizeGB</span></span>
<span data-ttu-id="3581a-123">Gibt die Größe des Datenträgers in Gigabyte (GB) an.</span><span class="sxs-lookup"><span data-stu-id="3581a-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="3581a-124">-Bild</span><span class="sxs-lookup"><span data-stu-id="3581a-124">-Image</span></span>
<span data-ttu-id="3581a-125">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3581a-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="3581a-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="3581a-126">-Lun</span></span>
<span data-ttu-id="3581a-127">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="3581a-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="3581a-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="3581a-128">-ManagedDiskId</span></span>
<span data-ttu-id="3581a-129">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="3581a-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="3581a-130">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="3581a-130">-SnapshotId</span></span>
<span data-ttu-id="3581a-131">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="3581a-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="3581a-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3581a-132">-StorageAccountType</span></span>
<span data-ttu-id="3581a-133">Der Typ des Speicher Kontotyps des Daten Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="3581a-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="3581a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3581a-134">-Confirm</span></span>
<span data-ttu-id="3581a-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3581a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3581a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3581a-136">-WhatIf</span></span>
<span data-ttu-id="3581a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3581a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3581a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3581a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3581a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3581a-139">CommonParameters</span></span>
<span data-ttu-id="3581a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3581a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3581a-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3581a-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3581a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3581a-142">INPUTS</span></span>

### <span data-ttu-id="3581a-143">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3581a-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="3581a-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3581a-144">System.Int32</span></span>

### <span data-ttu-id="3581a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3581a-145">System.String</span></span>

### <span data-ttu-id="3581a-146">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3581a-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3581a-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3581a-147">OUTPUTS</span></span>

### <span data-ttu-id="3581a-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="3581a-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="3581a-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="3581a-149">NOTES</span></span>

## <span data-ttu-id="3581a-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3581a-150">RELATED LINKS</span></span>

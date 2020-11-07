---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 44df831ce0f8e6454607e4f0956906466ebc9f39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661455"
---
# <span data-ttu-id="44907-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="44907-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="44907-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44907-102">SYNOPSIS</span></span>
<span data-ttu-id="44907-103">Legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="44907-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="44907-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44907-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44907-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44907-105">DESCRIPTION</span></span>
<span data-ttu-id="44907-106">Das Cmdlet " **Set-AzImageOsDisk** " legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="44907-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="44907-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44907-107">EXAMPLES</span></span>

### <span data-ttu-id="44907-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44907-108">Example 1</span></span>
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

<span data-ttu-id="44907-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="44907-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="44907-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="44907-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="44907-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="44907-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="44907-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="44907-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="44907-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="44907-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="44907-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="44907-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="44907-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="44907-115">PARAMETERS</span></span>

### <span data-ttu-id="44907-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="44907-116">-BlobUri</span></span>
<span data-ttu-id="44907-117">Gibt den URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="44907-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="44907-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="44907-118">-Caching</span></span>
<span data-ttu-id="44907-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="44907-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="44907-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44907-120">-DefaultProfile</span></span>
<span data-ttu-id="44907-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44907-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44907-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="44907-122">-DiskSizeGB</span></span>
<span data-ttu-id="44907-123">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="44907-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="44907-124">-Bild</span><span class="sxs-lookup"><span data-stu-id="44907-124">-Image</span></span>
<span data-ttu-id="44907-125">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="44907-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="44907-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="44907-126">-ManagedDiskId</span></span>
<span data-ttu-id="44907-127">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="44907-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="44907-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="44907-128">-OsState</span></span>
<span data-ttu-id="44907-129">Gibt den Betriebssystemstatus an.</span><span class="sxs-lookup"><span data-stu-id="44907-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="44907-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="44907-130">-OsType</span></span>
<span data-ttu-id="44907-131">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="44907-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="44907-132">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="44907-132">-SnapshotId</span></span>
<span data-ttu-id="44907-133">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="44907-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="44907-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="44907-134">-StorageAccountType</span></span>
<span data-ttu-id="44907-135">Der Speicher Kontotyp des BS-Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="44907-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="44907-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44907-136">-Confirm</span></span>
<span data-ttu-id="44907-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44907-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44907-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44907-138">-WhatIf</span></span>
<span data-ttu-id="44907-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44907-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44907-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44907-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44907-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44907-141">CommonParameters</span></span>
<span data-ttu-id="44907-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44907-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44907-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44907-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44907-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44907-144">INPUTS</span></span>

### <span data-ttu-id="44907-145">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="44907-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="44907-146">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="44907-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="44907-147">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="44907-147">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="44907-148">System. String</span><span class="sxs-lookup"><span data-stu-id="44907-148">System.String</span></span>

### <span data-ttu-id="44907-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="44907-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="44907-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="44907-150">System.Int32</span></span>

## <span data-ttu-id="44907-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44907-151">OUTPUTS</span></span>

### <span data-ttu-id="44907-152">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="44907-152">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="44907-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="44907-153">NOTES</span></span>

## <span data-ttu-id="44907-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44907-154">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003078"
---
# <span data-ttu-id="99c04-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="99c04-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="99c04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99c04-102">SYNOPSIS</span></span>
<span data-ttu-id="99c04-103">Legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="99c04-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="99c04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c04-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99c04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99c04-105">DESCRIPTION</span></span>
<span data-ttu-id="99c04-106">Das Cmdlet " **Set-AzImageOsDisk** " legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="99c04-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="99c04-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99c04-107">EXAMPLES</span></span>

### <span data-ttu-id="99c04-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99c04-108">Example 1</span></span>
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

<span data-ttu-id="99c04-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="99c04-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="99c04-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="99c04-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="99c04-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="99c04-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="99c04-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="99c04-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="99c04-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="99c04-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="99c04-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="99c04-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="99c04-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="99c04-115">PARAMETERS</span></span>

### <span data-ttu-id="99c04-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="99c04-116">-BlobUri</span></span>
<span data-ttu-id="99c04-117">Gibt den URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="99c04-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="99c04-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="99c04-118">-Caching</span></span>
<span data-ttu-id="99c04-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="99c04-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="99c04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c04-120">-DefaultProfile</span></span>
<span data-ttu-id="99c04-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99c04-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99c04-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="99c04-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="99c04-123">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="99c04-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="99c04-124">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="99c04-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="99c04-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="99c04-125">-DiskSizeGB</span></span>
<span data-ttu-id="99c04-126">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="99c04-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="99c04-127">-Bild</span><span class="sxs-lookup"><span data-stu-id="99c04-127">-Image</span></span>
<span data-ttu-id="99c04-128">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="99c04-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="99c04-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="99c04-129">-ManagedDiskId</span></span>
<span data-ttu-id="99c04-130">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="99c04-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="99c04-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="99c04-131">-OsState</span></span>
<span data-ttu-id="99c04-132">Gibt den Betriebssystemstatus an.</span><span class="sxs-lookup"><span data-stu-id="99c04-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="99c04-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="99c04-133">-OsType</span></span>
<span data-ttu-id="99c04-134">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="99c04-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="99c04-135">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="99c04-135">-SnapshotId</span></span>
<span data-ttu-id="99c04-136">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="99c04-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="99c04-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="99c04-137">-StorageAccountType</span></span>
<span data-ttu-id="99c04-138">Der Speicher Kontotyp des BS-Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="99c04-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="99c04-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99c04-139">-Confirm</span></span>
<span data-ttu-id="99c04-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99c04-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c04-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c04-141">-WhatIf</span></span>
<span data-ttu-id="99c04-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99c04-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99c04-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99c04-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c04-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c04-144">CommonParameters</span></span>
<span data-ttu-id="99c04-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c04-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c04-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99c04-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c04-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99c04-147">INPUTS</span></span>

### <span data-ttu-id="99c04-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="99c04-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="99c04-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="99c04-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="99c04-150">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="99c04-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="99c04-151">System. String</span><span class="sxs-lookup"><span data-stu-id="99c04-151">System.String</span></span>

### <span data-ttu-id="99c04-152">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="99c04-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="99c04-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="99c04-153">System.Int32</span></span>

## <span data-ttu-id="99c04-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99c04-154">OUTPUTS</span></span>

### <span data-ttu-id="99c04-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="99c04-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="99c04-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="99c04-156">NOTES</span></span>

## <span data-ttu-id="99c04-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99c04-157">RELATED LINKS</span></span>

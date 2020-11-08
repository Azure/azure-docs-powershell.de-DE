---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 45f3e8f76e6f8ff3a5684fbd8f9ebf42e7a8e252
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009305"
---
# <span data-ttu-id="c1d85-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="c1d85-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="c1d85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1d85-102">SYNOPSIS</span></span>
<span data-ttu-id="c1d85-103">Legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="c1d85-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="c1d85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1d85-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <String>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1d85-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1d85-105">DESCRIPTION</span></span>
<span data-ttu-id="c1d85-106">Das Cmdlet " **Set-AzImageOsDisk** " legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="c1d85-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="c1d85-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1d85-107">EXAMPLES</span></span>

### <span data-ttu-id="c1d85-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1d85-108">Example 1</span></span>
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

<span data-ttu-id="c1d85-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c1d85-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="c1d85-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="c1d85-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="c1d85-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="c1d85-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="c1d85-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c1d85-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="c1d85-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c1d85-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="c1d85-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c1d85-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="c1d85-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1d85-115">PARAMETERS</span></span>

### <span data-ttu-id="c1d85-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="c1d85-116">-BlobUri</span></span>
<span data-ttu-id="c1d85-117">Gibt den URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="c1d85-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="c1d85-118">-Caching</span></span>
<span data-ttu-id="c1d85-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="c1d85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1d85-120">-DefaultProfile</span></span>
<span data-ttu-id="c1d85-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1d85-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1d85-122">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="c1d85-122">-DiskEncryptionSetId</span></span>
<span data-ttu-id="c1d85-123">Gibt die Ressourcen-ID des vom Kunden verwalteten Datenträger Verschlüsselungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-123">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="c1d85-124">Dies kann nur für verwalteten Datenträger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1d85-124">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="c1d85-125">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c1d85-125">-DiskSizeGB</span></span>
<span data-ttu-id="c1d85-126">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-126">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="c1d85-127">-Bild</span><span class="sxs-lookup"><span data-stu-id="c1d85-127">-Image</span></span>
<span data-ttu-id="c1d85-128">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-128">Specifies a local image object.</span></span>

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

### <span data-ttu-id="c1d85-129">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="c1d85-129">-ManagedDiskId</span></span>
<span data-ttu-id="c1d85-130">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-130">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="c1d85-131">-OsState</span><span class="sxs-lookup"><span data-stu-id="c1d85-131">-OsState</span></span>
<span data-ttu-id="c1d85-132">Gibt den Betriebssystemstatus an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-132">Specifies the OS state.</span></span>

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

### <span data-ttu-id="c1d85-133">-OsType</span><span class="sxs-lookup"><span data-stu-id="c1d85-133">-OsType</span></span>
<span data-ttu-id="c1d85-134">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-134">Specifies the OS type.</span></span>

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

### <span data-ttu-id="c1d85-135">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="c1d85-135">-SnapshotId</span></span>
<span data-ttu-id="c1d85-136">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="c1d85-136">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="c1d85-137">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c1d85-137">-StorageAccountType</span></span>
<span data-ttu-id="c1d85-138">Der Speicher Kontotyp des BS-Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="c1d85-138">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="c1d85-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1d85-139">-Confirm</span></span>
<span data-ttu-id="c1d85-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1d85-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1d85-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1d85-141">-WhatIf</span></span>
<span data-ttu-id="c1d85-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1d85-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1d85-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1d85-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1d85-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1d85-144">CommonParameters</span></span>
<span data-ttu-id="c1d85-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1d85-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1d85-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1d85-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1d85-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1d85-147">INPUTS</span></span>

### <span data-ttu-id="c1d85-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c1d85-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

### <span data-ttu-id="c1d85-149">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c1d85-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c1d85-150">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c1d85-150">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c1d85-151">System. String</span><span class="sxs-lookup"><span data-stu-id="c1d85-151">System.String</span></span>

### <span data-ttu-id="c1d85-152">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. CachingTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="c1d85-152">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="c1d85-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c1d85-153">System.Int32</span></span>

## <span data-ttu-id="c1d85-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1d85-154">OUTPUTS</span></span>

### <span data-ttu-id="c1d85-155">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="c1d85-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="c1d85-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1d85-156">NOTES</span></span>

## <span data-ttu-id="c1d85-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1d85-157">RELATED LINKS</span></span>

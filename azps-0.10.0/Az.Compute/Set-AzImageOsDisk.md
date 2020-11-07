---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azimageosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzImageOsDisk.md
ms.openlocfilehash: 5bc92ea5aa49cb97be457fd937c7b9deb492bb0e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844284"
---
# <span data-ttu-id="f1e64-101">Set-AzImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="f1e64-101">Set-AzImageOsDisk</span></span>

## <span data-ttu-id="f1e64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1e64-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e64-103">Legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="f1e64-103">Sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="f1e64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1e64-104">SYNTAX</span></span>

```
Set-AzImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1e64-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e64-106">Das Cmdlet " **Set-AzImageOsDisk** " legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="f1e64-106">The **Set-AzImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="f1e64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1e64-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1e64-108">Example 1</span></span>
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

<span data-ttu-id="f1e64-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f1e64-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="f1e64-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="f1e64-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="f1e64-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="f1e64-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="f1e64-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1e64-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="f1e64-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f1e64-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="f1e64-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f1e64-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f1e64-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1e64-115">PARAMETERS</span></span>

### <span data-ttu-id="f1e64-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="f1e64-116">-BlobUri</span></span>
<span data-ttu-id="f1e64-117">Gibt den URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-117">Specifies the Uri of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="f1e64-118">-Caching</span></span>
<span data-ttu-id="f1e64-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e64-120">-DefaultProfile</span></span>
<span data-ttu-id="f1e64-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f1e64-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="f1e64-122">-DiskSizeGB</span></span>
<span data-ttu-id="f1e64-123">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-123">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-124">-Bild</span><span class="sxs-lookup"><span data-stu-id="f1e64-124">-Image</span></span>
<span data-ttu-id="f1e64-125">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-125">Specifies a local image object.</span></span>

```yaml
Type: PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="f1e64-126">-ManagedDiskId</span></span>
<span data-ttu-id="f1e64-127">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-127">Specifies the ID of a managed disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="f1e64-128">-OsState</span></span>
<span data-ttu-id="f1e64-129">Gibt den Betriebssystemstatus an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-129">Specifies the OS state.</span></span>

```yaml
Type: OperatingSystemStateTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Generalized, Specialized

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="f1e64-130">-OsType</span></span>
<span data-ttu-id="f1e64-131">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-131">Specifies the OS type.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-132">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="f1e64-132">-SnapshotId</span></span>
<span data-ttu-id="f1e64-133">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="f1e64-133">Specifies the ID of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="f1e64-134">-StorageAccountType</span></span>
<span data-ttu-id="f1e64-135">Der Speicher Kontotyp des BS-Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="f1e64-135">The Storage Account type of Os Image Disk</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1e64-136">-Confirm</span></span>
<span data-ttu-id="f1e64-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1e64-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e64-138">-WhatIf</span></span>
<span data-ttu-id="f1e64-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1e64-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1e64-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1e64-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e64-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e64-141">CommonParameters</span></span>
<span data-ttu-id="f1e64-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e64-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e64-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e64-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e64-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1e64-144">INPUTS</span></span>

### <span data-ttu-id="f1e64-145">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="f1e64-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="f1e64-146">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f1e64-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f1e64-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1e64-147">OUTPUTS</span></span>

### <span data-ttu-id="f1e64-148">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="f1e64-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="f1e64-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1e64-149">NOTES</span></span>

## <span data-ttu-id="f1e64-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1e64-150">RELATED LINKS</span></span>


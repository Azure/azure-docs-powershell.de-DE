---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azimagedatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzImageDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzImageDataDisk.md
ms.openlocfilehash: b6c1a7e8947a079a864aae31d12aedf244ecb81b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93840972"
---
# <span data-ttu-id="50fac-101">Add-AzImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="50fac-101">Add-AzImageDataDisk</span></span>

## <span data-ttu-id="50fac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="50fac-102">SYNOPSIS</span></span>
<span data-ttu-id="50fac-103">Fügt einen Datenträger zu einem Bild obejct hinzu.</span><span class="sxs-lookup"><span data-stu-id="50fac-103">Adds a data disk to an image obejct.</span></span>

## <span data-ttu-id="50fac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="50fac-104">SYNTAX</span></span>

```
Add-AzImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50fac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50fac-105">DESCRIPTION</span></span>
<span data-ttu-id="50fac-106">Mit dem Cmdlet " **Add-AzImageDataDisk** " wird ein Datenlaufwerk zu einem Image-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="50fac-106">The **Add-AzImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="50fac-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="50fac-107">EXAMPLES</span></span>

### <span data-ttu-id="50fac-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="50fac-108">Example 1</span></span>
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

<span data-ttu-id="50fac-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="50fac-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="50fac-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri-, $dataDiskVhdUri 1-und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="50fac-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="50fac-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="50fac-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="50fac-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild ein Betriebssystemdatenträger und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="50fac-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="50fac-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="50fac-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="50fac-114">Der endgültige Befehl erstellt ein Bild mit dem Namen ImageName01 in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="50fac-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="50fac-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="50fac-115">PARAMETERS</span></span>

### <span data-ttu-id="50fac-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="50fac-116">-BlobUri</span></span>
<span data-ttu-id="50fac-117">Gibt den Link als URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="50fac-117">Specifies the link, as a URI, of the blob.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fac-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="50fac-118">-Caching</span></span>
<span data-ttu-id="50fac-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="50fac-119">Specifies the caching mode of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50fac-120">-DefaultProfile</span></span>
<span data-ttu-id="50fac-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="50fac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50fac-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="50fac-122">-DiskSizeGB</span></span>
<span data-ttu-id="50fac-123">Gibt die Größe des Datenträgers in Gigabyte (GB) an.</span><span class="sxs-lookup"><span data-stu-id="50fac-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="50fac-124">-Bild</span><span class="sxs-lookup"><span data-stu-id="50fac-124">-Image</span></span>
<span data-ttu-id="50fac-125">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="50fac-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="50fac-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="50fac-126">-Lun</span></span>
<span data-ttu-id="50fac-127">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="50fac-127">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50fac-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="50fac-128">-ManagedDiskId</span></span>
<span data-ttu-id="50fac-129">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="50fac-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="50fac-130">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="50fac-130">-SnapshotId</span></span>
<span data-ttu-id="50fac-131">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="50fac-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="50fac-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="50fac-132">-StorageAccountType</span></span>
<span data-ttu-id="50fac-133">Der Typ des Speicher Kontotyps des Daten Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="50fac-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="50fac-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="50fac-134">-Confirm</span></span>
<span data-ttu-id="50fac-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="50fac-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50fac-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50fac-136">-WhatIf</span></span>
<span data-ttu-id="50fac-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="50fac-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50fac-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="50fac-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50fac-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50fac-139">CommonParameters</span></span>
<span data-ttu-id="50fac-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50fac-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50fac-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50fac-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50fac-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="50fac-142">INPUTS</span></span>

### <span data-ttu-id="50fac-143">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="50fac-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="50fac-144">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50fac-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="50fac-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="50fac-145">OUTPUTS</span></span>

### <span data-ttu-id="50fac-146">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="50fac-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="50fac-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="50fac-147">NOTES</span></span>

## <span data-ttu-id="50fac-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="50fac-148">RELATED LINKS</span></span>


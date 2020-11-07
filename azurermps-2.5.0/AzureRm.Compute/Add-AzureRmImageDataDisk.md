---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermimagedatadisk
schema: 2.0.0
ms.openlocfilehash: b4412cb85534d1aae780b16450726920921d811e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848548"
---
# <span data-ttu-id="358be-101">Add-AzureRmImageDataDisk</span><span class="sxs-lookup"><span data-stu-id="358be-101">Add-AzureRmImageDataDisk</span></span>

## <span data-ttu-id="358be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="358be-102">SYNOPSIS</span></span>
<span data-ttu-id="358be-103">Fügt einen Daten Datenträger zu einem Image-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="358be-103">Adds a data disk to an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="358be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="358be-104">SYNTAX</span></span>

```
Add-AzureRmImageDataDisk [-Image] <PSImage> [[-Lun] <Int32>] [[-BlobUri] <String>] [[-Caching] <CachingTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>]
 [-ManagedDiskId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358be-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="358be-105">DESCRIPTION</span></span>
<span data-ttu-id="358be-106">Mit dem Cmdlet " **Add-AzureRmImageDataDisk** " wird ein Datenlaufwerk zu einem Image-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="358be-106">The **Add-AzureRmImageDataDisk** cmdlet adds a data disk to an image object.</span></span>

## <span data-ttu-id="358be-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="358be-107">EXAMPLES</span></span>

### <span data-ttu-id="358be-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="358be-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="358be-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="358be-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="358be-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri-, $dataDiskVhdUri 1-und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="358be-110">The next three commands assign paths of operating system disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="358be-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="358be-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="358be-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild ein Betriebssystemdatenträger und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="358be-112">The next three commands each adds an operating system disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="358be-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="358be-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="358be-114">Der endgültige Befehl erstellt ein Bild mit dem Namen ImageName01 in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="358be-114">The final command creates an image named ImageName01 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="358be-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="358be-115">PARAMETERS</span></span>

### <span data-ttu-id="358be-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="358be-116">-BlobUri</span></span>
<span data-ttu-id="358be-117">Gibt den Link als URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="358be-117">Specifies the link, as a URI, of the blob.</span></span>

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

### <span data-ttu-id="358be-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="358be-118">-Caching</span></span>
<span data-ttu-id="358be-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="358be-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="358be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358be-120">-DefaultProfile</span></span>
<span data-ttu-id="358be-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="358be-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="358be-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="358be-122">-DiskSizeGB</span></span>
<span data-ttu-id="358be-123">Gibt die Größe des Datenträgers in Gigabyte (GB) an.</span><span class="sxs-lookup"><span data-stu-id="358be-123">Specifies the size of the disk in Gigabytes (GB).</span></span>

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

### <span data-ttu-id="358be-124">-Bild</span><span class="sxs-lookup"><span data-stu-id="358be-124">-Image</span></span>
<span data-ttu-id="358be-125">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="358be-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="358be-126">-LUN</span><span class="sxs-lookup"><span data-stu-id="358be-126">-Lun</span></span>
<span data-ttu-id="358be-127">Gibt die logische Einheitsnummer an (LUN).</span><span class="sxs-lookup"><span data-stu-id="358be-127">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="358be-128">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="358be-128">-ManagedDiskId</span></span>
<span data-ttu-id="358be-129">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="358be-129">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="358be-130">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="358be-130">-SnapshotId</span></span>
<span data-ttu-id="358be-131">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="358be-131">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="358be-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="358be-132">-StorageAccountType</span></span>
<span data-ttu-id="358be-133">Der Typ des Speicher Kontotyps des Daten Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="358be-133">The Storage Account type of the data image disk</span></span>

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

### <span data-ttu-id="358be-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="358be-134">-Confirm</span></span>
<span data-ttu-id="358be-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="358be-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358be-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358be-136">-WhatIf</span></span>
<span data-ttu-id="358be-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="358be-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="358be-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="358be-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358be-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358be-139">CommonParameters</span></span>
<span data-ttu-id="358be-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358be-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358be-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358be-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358be-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="358be-142">INPUTS</span></span>

### <span data-ttu-id="358be-143">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="358be-143">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="358be-144">System. Int32 System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="358be-144">System.Int32 System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="358be-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="358be-145">OUTPUTS</span></span>

### <span data-ttu-id="358be-146">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="358be-146">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="358be-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="358be-147">NOTES</span></span>

## <span data-ttu-id="358be-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="358be-148">RELATED LINKS</span></span>


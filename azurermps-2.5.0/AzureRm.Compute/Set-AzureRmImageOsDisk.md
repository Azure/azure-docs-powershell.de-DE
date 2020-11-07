---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermimageosdisk
schema: 2.0.0
ms.openlocfilehash: 9d7d7436e6c653c257fb549854338a277d621ee0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849695"
---
# <span data-ttu-id="6e12e-101">Set-AzureRmImageOsDisk</span><span class="sxs-lookup"><span data-stu-id="6e12e-101">Set-AzureRmImageOsDisk</span></span>

## <span data-ttu-id="6e12e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e12e-102">SYNOPSIS</span></span>
<span data-ttu-id="6e12e-103">Legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="6e12e-103">Sets the operating system disk properties on an image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e12e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e12e-104">SYNTAX</span></span>

```
Set-AzureRmImageOsDisk [-Image] <PSImage> [[-OsType] <OperatingSystemTypes>]
 [[-OsState] <OperatingSystemStateTypes>] [[-BlobUri] <String>] [-Caching <CachingTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-SnapshotId <String>] [-ManagedDiskId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e12e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e12e-105">DESCRIPTION</span></span>
<span data-ttu-id="6e12e-106">Das Cmdlet " **Set-AzureRmImageOsDisk** " legt die Datenträgereigenschaften des Betriebssystems für ein Image-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="6e12e-106">The **Set-AzureRmImageOsDisk** cmdlet sets the operating system disk properties on an image object.</span></span>

## <span data-ttu-id="6e12e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e12e-107">EXAMPLES</span></span>

### <span data-ttu-id="6e12e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6e12e-108">Example 1</span></span>
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

<span data-ttu-id="6e12e-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6e12e-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="6e12e-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="6e12e-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="6e12e-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="6e12e-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="6e12e-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6e12e-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="6e12e-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6e12e-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="6e12e-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6e12e-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6e12e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e12e-115">PARAMETERS</span></span>

### <span data-ttu-id="6e12e-116">-BlobUri</span><span class="sxs-lookup"><span data-stu-id="6e12e-116">-BlobUri</span></span>
<span data-ttu-id="6e12e-117">Gibt den URI des BLOB an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-117">Specifies the Uri of the blob.</span></span>

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

### <span data-ttu-id="6e12e-118">-Caching</span><span class="sxs-lookup"><span data-stu-id="6e12e-118">-Caching</span></span>
<span data-ttu-id="6e12e-119">Gibt den Zwischenspeichermodus des Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-119">Specifies the caching mode of the disk.</span></span>

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

### <span data-ttu-id="6e12e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e12e-120">-DefaultProfile</span></span>
<span data-ttu-id="6e12e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6e12e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e12e-122">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6e12e-122">-DiskSizeGB</span></span>
<span data-ttu-id="6e12e-123">Gibt die Größe des Datenträgers in GB an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-123">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="6e12e-124">-Bild</span><span class="sxs-lookup"><span data-stu-id="6e12e-124">-Image</span></span>
<span data-ttu-id="6e12e-125">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-125">Specifies a local image object.</span></span>

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

### <span data-ttu-id="6e12e-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="6e12e-126">-ManagedDiskId</span></span>
<span data-ttu-id="6e12e-127">Gibt die ID eines verwalteten Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-127">Specifies the ID of a managed disk.</span></span>

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

### <span data-ttu-id="6e12e-128">-OsState</span><span class="sxs-lookup"><span data-stu-id="6e12e-128">-OsState</span></span>
<span data-ttu-id="6e12e-129">Gibt den Betriebssystemstatus an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-129">Specifies the OS state.</span></span>

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

### <span data-ttu-id="6e12e-130">-OsType</span><span class="sxs-lookup"><span data-stu-id="6e12e-130">-OsType</span></span>
<span data-ttu-id="6e12e-131">Gibt den Betriebssystemtyp an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-131">Specifies the OS type.</span></span>

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

### <span data-ttu-id="6e12e-132">-Snapshot-Nr</span><span class="sxs-lookup"><span data-stu-id="6e12e-132">-SnapshotId</span></span>
<span data-ttu-id="6e12e-133">Gibt die ID eines Snapshots an.</span><span class="sxs-lookup"><span data-stu-id="6e12e-133">Specifies the ID of a snapshot.</span></span>

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

### <span data-ttu-id="6e12e-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6e12e-134">-StorageAccountType</span></span>
<span data-ttu-id="6e12e-135">Der Speicher Kontotyp des BS-Bild Datenträgers</span><span class="sxs-lookup"><span data-stu-id="6e12e-135">The Storage Account type of Os Image Disk</span></span>

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

### <span data-ttu-id="6e12e-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e12e-136">-Confirm</span></span>
<span data-ttu-id="6e12e-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e12e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e12e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e12e-138">-WhatIf</span></span>
<span data-ttu-id="6e12e-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e12e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e12e-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e12e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e12e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e12e-141">CommonParameters</span></span>
<span data-ttu-id="6e12e-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e12e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e12e-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e12e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e12e-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e12e-144">INPUTS</span></span>

### <span data-ttu-id="6e12e-145">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="6e12e-145">Microsoft.Azure.Management.Compute.Models.Image</span></span>
<span data-ttu-id="6e12e-146">System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. Compute. Models. OperatingSystemStateTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] System. String System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6e12e-146">System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.String System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="6e12e-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e12e-147">OUTPUTS</span></span>

### <span data-ttu-id="6e12e-148">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="6e12e-148">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="6e12e-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e12e-149">NOTES</span></span>

## <span data-ttu-id="6e12e-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e12e-150">RELATED LINKS</span></span>


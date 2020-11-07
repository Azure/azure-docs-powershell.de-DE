---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermimageconfig
schema: 2.0.0
ms.openlocfilehash: ef9fc830b59568ad039b265fb182dbbdbd13a00d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848520"
---
# <span data-ttu-id="8445d-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="8445d-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="8445d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8445d-102">SYNOPSIS</span></span>
<span data-ttu-id="8445d-103">Erstellt ein konfigurierbares Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8445d-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8445d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8445d-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8445d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8445d-105">DESCRIPTION</span></span>
<span data-ttu-id="8445d-106">Mit dem Cmdlet **New-AzureRmImageConfig** wird ein konfigurierbares Image-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8445d-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="8445d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8445d-107">EXAMPLES</span></span>

### <span data-ttu-id="8445d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8445d-108">Example 1</span></span>
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

<span data-ttu-id="8445d-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="8445d-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="8445d-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="8445d-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="8445d-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="8445d-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="8445d-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8445d-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="8445d-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8445d-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="8445d-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8445d-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="8445d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8445d-115">PARAMETERS</span></span>

### <span data-ttu-id="8445d-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="8445d-116">-DataDisk</span></span>
<span data-ttu-id="8445d-117">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="8445d-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8445d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8445d-118">-DefaultProfile</span></span>
<span data-ttu-id="8445d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8445d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8445d-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="8445d-120">-Location</span></span>
<span data-ttu-id="8445d-121">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="8445d-121">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8445d-122">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="8445d-122">-OsDisk</span></span>
<span data-ttu-id="8445d-123">Gibt den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="8445d-123">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8445d-124">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8445d-124">-SourceVirtualMachineId</span></span>
<span data-ttu-id="8445d-125">Gibt die ID der virtuellen Quellmaschine an.</span><span class="sxs-lookup"><span data-stu-id="8445d-125">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="8445d-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="8445d-126">-Tag</span></span>
<span data-ttu-id="8445d-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8445d-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8445d-128">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8445d-128">For example:</span></span>

<span data-ttu-id="8445d-129">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8445d-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8445d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8445d-130">-Confirm</span></span>
<span data-ttu-id="8445d-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8445d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8445d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8445d-132">-WhatIf</span></span>
<span data-ttu-id="8445d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8445d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8445d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8445d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8445d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8445d-135">CommonParameters</span></span>
<span data-ttu-id="8445d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8445d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8445d-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8445d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8445d-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8445d-138">INPUTS</span></span>

### <span data-ttu-id="8445d-139">Keine</span><span class="sxs-lookup"><span data-stu-id="8445d-139">None</span></span>
<span data-ttu-id="8445d-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8445d-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8445d-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8445d-141">OUTPUTS</span></span>

### <span data-ttu-id="8445d-142">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="8445d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="8445d-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="8445d-143">NOTES</span></span>

## <span data-ttu-id="8445d-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8445d-144">RELATED LINKS</span></span>


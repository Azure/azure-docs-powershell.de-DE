---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: 56834ad267b4ac60613afc4dbd08499eae212512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996156"
---
# <span data-ttu-id="b7a3f-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="b7a3f-101">New-AzImageConfig</span></span>

## <span data-ttu-id="b7a3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a3f-103">Erstellt ein konfigurierbares Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="b7a3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7a3f-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7a3f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7a3f-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a3f-106">Mit dem Cmdlet **New-AzImageConfig** wird ein konfigurierbares Image-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="b7a3f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7a3f-107">EXAMPLES</span></span>

### <span data-ttu-id="b7a3f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b7a3f-108">Example 1</span></span>
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

<span data-ttu-id="b7a3f-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="b7a3f-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="b7a3f-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="b7a3f-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="b7a3f-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="b7a3f-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="b7a3f-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="b7a3f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7a3f-115">PARAMETERS</span></span>

### <span data-ttu-id="b7a3f-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="b7a3f-116">-DataDisk</span></span>
<span data-ttu-id="b7a3f-117">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-117">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a3f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a3f-118">-DefaultProfile</span></span>
<span data-ttu-id="b7a3f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7a3f-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="b7a3f-120">-HyperVGeneration</span></span>
<span data-ttu-id="b7a3f-121">Gibt den HyperVGeneration-Typ für den virtuellen Computer an, der aus dem Bild erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="b7a3f-122">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="b7a3f-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="b7a3f-123">-Location</span></span>
<span data-ttu-id="b7a3f-124">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-124">Specifies a location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a3f-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="b7a3f-125">-OsDisk</span></span>
<span data-ttu-id="b7a3f-126">Gibt den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-126">Specifies the operating system Disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ImageOSDisk
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a3f-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b7a3f-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="b7a3f-128">Gibt die ID der virtuellen Quellmaschine an.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="b7a3f-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="b7a3f-129">-Tag</span></span>
<span data-ttu-id="b7a3f-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="b7a3f-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7a3f-131">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="b7a3f-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a3f-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="b7a3f-132">-ZoneResilient</span></span>
<span data-ttu-id="b7a3f-133">Aktivieren der Zone-Widerstandsfähigkeit</span><span class="sxs-lookup"><span data-stu-id="b7a3f-133">Enable zone resilient</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a3f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7a3f-134">-Confirm</span></span>
<span data-ttu-id="b7a3f-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7a3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7a3f-136">-WhatIf</span></span>
<span data-ttu-id="b7a3f-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7a3f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7a3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a3f-139">CommonParameters</span></span>
<span data-ttu-id="b7a3f-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a3f-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7a3f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a3f-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7a3f-142">INPUTS</span></span>

### <span data-ttu-id="b7a3f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b7a3f-143">System.String</span></span>

### <span data-ttu-id="b7a3f-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7a3f-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b7a3f-145">Microsoft. Azure. Management. Compute. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="b7a3f-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="b7a3f-146">Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="b7a3f-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="b7a3f-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7a3f-147">OUTPUTS</span></span>

### <span data-ttu-id="b7a3f-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="b7a3f-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="b7a3f-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7a3f-149">NOTES</span></span>

## <span data-ttu-id="b7a3f-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7a3f-150">RELATED LINKS</span></span>

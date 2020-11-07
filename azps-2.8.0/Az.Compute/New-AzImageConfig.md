---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azimageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzImageConfig.md
ms.openlocfilehash: c76ccab31b3c5c11216a1a929e2a78df55713325
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93652071"
---
# <span data-ttu-id="7d472-101">New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="7d472-101">New-AzImageConfig</span></span>

## <span data-ttu-id="7d472-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d472-102">SYNOPSIS</span></span>
<span data-ttu-id="7d472-103">Erstellt ein konfigurierbares Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7d472-103">Creates a configurable image object.</span></span>

## <span data-ttu-id="7d472-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d472-104">SYNTAX</span></span>

```
New-AzImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-HyperVGeneration <String>] [-DataDisk <ImageDataDisk[]>] [-ZoneResilient]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d472-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d472-105">DESCRIPTION</span></span>
<span data-ttu-id="7d472-106">Mit dem Cmdlet **New-AzImageConfig** wird ein konfigurierbares Image-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="7d472-106">The **New-AzImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="7d472-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d472-107">EXAMPLES</span></span>

### <span data-ttu-id="7d472-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d472-108">Example 1</span></span>
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

<span data-ttu-id="7d472-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7d472-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>
<span data-ttu-id="7d472-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="7d472-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span> <span data-ttu-id="7d472-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="7d472-111">This approach is only for readability of the following commands.</span></span>
<span data-ttu-id="7d472-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7d472-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="7d472-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7d472-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>
<span data-ttu-id="7d472-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="7d472-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="7d472-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d472-115">PARAMETERS</span></span>

### <span data-ttu-id="7d472-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="7d472-116">-DataDisk</span></span>
<span data-ttu-id="7d472-117">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="7d472-117">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="7d472-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d472-118">-DefaultProfile</span></span>
<span data-ttu-id="7d472-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d472-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d472-120">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="7d472-120">-HyperVGeneration</span></span>
<span data-ttu-id="7d472-121">Gibt den HyperVGeneration-Typ für den virtuellen Computer an, der aus dem Bild erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d472-121">Specifies the HyperVGeneration Type for the virtual machine created from the image.</span></span>  <span data-ttu-id="7d472-122">Zulässige Werte sind v1 und v2.</span><span class="sxs-lookup"><span data-stu-id="7d472-122">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="7d472-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="7d472-123">-Location</span></span>
<span data-ttu-id="7d472-124">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="7d472-124">Specifies a location.</span></span>

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

### <span data-ttu-id="7d472-125">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="7d472-125">-OsDisk</span></span>
<span data-ttu-id="7d472-126">Gibt den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="7d472-126">Specifies the operating system Disk.</span></span>

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

### <span data-ttu-id="7d472-127">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7d472-127">-SourceVirtualMachineId</span></span>
<span data-ttu-id="7d472-128">Gibt die ID der virtuellen Quellmaschine an.</span><span class="sxs-lookup"><span data-stu-id="7d472-128">Specifies the source virtual machine ID.</span></span>

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

### <span data-ttu-id="7d472-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="7d472-129">-Tag</span></span>
<span data-ttu-id="7d472-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="7d472-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7d472-131">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="7d472-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7d472-132">-ZoneResilient</span><span class="sxs-lookup"><span data-stu-id="7d472-132">-ZoneResilient</span></span>
<span data-ttu-id="7d472-133">Aktivieren der Zone-Widerstandsfähigkeit</span><span class="sxs-lookup"><span data-stu-id="7d472-133">Enable zone resilient</span></span>

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

### <span data-ttu-id="7d472-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7d472-134">-Confirm</span></span>
<span data-ttu-id="7d472-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d472-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d472-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d472-136">-WhatIf</span></span>
<span data-ttu-id="7d472-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d472-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d472-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d472-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d472-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d472-139">CommonParameters</span></span>
<span data-ttu-id="7d472-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d472-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d472-141">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d472-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d472-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d472-142">INPUTS</span></span>

### <span data-ttu-id="7d472-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7d472-143">System.String</span></span>

### <span data-ttu-id="7d472-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7d472-144">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7d472-145">Microsoft. Azure. Management. Compute. Models. ImageOSDisk</span><span class="sxs-lookup"><span data-stu-id="7d472-145">Microsoft.Azure.Management.Compute.Models.ImageOSDisk</span></span>

### <span data-ttu-id="7d472-146">Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="7d472-146">Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="7d472-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d472-147">OUTPUTS</span></span>

### <span data-ttu-id="7d472-148">Microsoft. Azure. Commands. Compute. Automation. Models. PSImage</span><span class="sxs-lookup"><span data-stu-id="7d472-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSImage</span></span>

## <span data-ttu-id="7d472-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d472-149">NOTES</span></span>

## <span data-ttu-id="7d472-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d472-150">RELATED LINKS</span></span>

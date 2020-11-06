---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: e3b053d4e8e9ccf9c68d8eb5fabe479f7f58ced1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497701"
---
# <span data-ttu-id="ea311-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="ea311-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea311-102">SYNOPSIS</span></span>
<span data-ttu-id="ea311-103">Legt bestimmte Aktionen für einen angegebenen VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="ea311-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea311-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea311-104">SYNTAX</span></span>

### <span data-ttu-id="ea311-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea311-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Reimage] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea311-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="ea311-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-ReimageAll] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea311-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea311-107">DESCRIPTION</span></span>
<span data-ttu-id="ea311-108">Das Cmdlet " **Set-AzureRmVmss** " legt bestimmte Aktionen für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ea311-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ea311-109">Die einzige Aktion, die dieses Cmdlet unterstützt, ist reimage.</span><span class="sxs-lookup"><span data-stu-id="ea311-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="ea311-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea311-110">EXAMPLES</span></span>

### <span data-ttu-id="ea311-111">Beispiel 1: umbilden einer VMSS</span><span class="sxs-lookup"><span data-stu-id="ea311-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ea311-112">Mit diesem Befehl wird der VMSS mit dem Namen ContosoVMSS, der zur Ressourcengruppe mit dem Namen contosogroup gehört, erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="ea311-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="ea311-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea311-113">PARAMETERS</span></span>

### <span data-ttu-id="ea311-114">-Reimage</span><span class="sxs-lookup"><span data-stu-id="ea311-114">-Reimage</span></span>
<span data-ttu-id="ea311-115">Gibt an, dass das Cmdlet die VMSS.</span><span class="sxs-lookup"><span data-stu-id="ea311-115">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea311-116">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="ea311-116">-ReimageAll</span></span>
<span data-ttu-id="ea311-117">Gibt an, dass das Cmdlet alle Datenträger im VMSS umbildet.</span><span class="sxs-lookup"><span data-stu-id="ea311-117">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea311-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea311-118">-ResourceGroupName</span></span>
<span data-ttu-id="ea311-119">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="ea311-119">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea311-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ea311-120">-VMScaleSetName</span></span>
<span data-ttu-id="ea311-121">Art der Name des VMSS, für das dieses Cmdlet Aktionen festlegt.</span><span class="sxs-lookup"><span data-stu-id="ea311-121">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea311-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea311-122">-Confirm</span></span>
<span data-ttu-id="ea311-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea311-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea311-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea311-124">-WhatIf</span></span>
<span data-ttu-id="ea311-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea311-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea311-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea311-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea311-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea311-127">CommonParameters</span></span>
<span data-ttu-id="ea311-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea311-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea311-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea311-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea311-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea311-130">INPUTS</span></span>

### <span data-ttu-id="ea311-131">Keine</span><span class="sxs-lookup"><span data-stu-id="ea311-131">None</span></span>
<span data-ttu-id="ea311-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ea311-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea311-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea311-133">OUTPUTS</span></span>

### <span data-ttu-id="ea311-134">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ea311-134">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ea311-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea311-135">NOTES</span></span>

## <span data-ttu-id="ea311-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea311-136">RELATED LINKS</span></span>

[<span data-ttu-id="ea311-137">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-137">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="ea311-138">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-138">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ea311-139">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-139">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ea311-140">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-140">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ea311-141">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ea311-142">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ea311-143">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ea311-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



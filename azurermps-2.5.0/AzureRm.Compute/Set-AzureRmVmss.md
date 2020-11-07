---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849367"
---
# <span data-ttu-id="b15fa-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="b15fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b15fa-102">SYNOPSIS</span></span>
<span data-ttu-id="b15fa-103">Legt bestimmte Aktionen für einen angegebenen VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="b15fa-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b15fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b15fa-104">SYNTAX</span></span>

### <span data-ttu-id="b15fa-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b15fa-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b15fa-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b15fa-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b15fa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b15fa-107">DESCRIPTION</span></span>
<span data-ttu-id="b15fa-108">Das Cmdlet " **Set-AzureRmVmss** " legt bestimmte Aktionen für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="b15fa-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b15fa-109">Die einzige Aktion, die dieses Cmdlet unterstützt, ist reimage.</span><span class="sxs-lookup"><span data-stu-id="b15fa-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="b15fa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b15fa-110">EXAMPLES</span></span>

### <span data-ttu-id="b15fa-111">Beispiel 1: umbilden einer VMSS</span><span class="sxs-lookup"><span data-stu-id="b15fa-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b15fa-112">Mit diesem Befehl wird der VMSS mit dem Namen ContosoVMSS, der zur Ressourcengruppe mit dem Namen contosogroup gehört, erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="b15fa-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b15fa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b15fa-113">PARAMETERS</span></span>

### <span data-ttu-id="b15fa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b15fa-114">-AsJob</span></span>
<span data-ttu-id="b15fa-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="b15fa-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15fa-116">-DefaultProfile</span></span>
<span data-ttu-id="b15fa-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b15fa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b15fa-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b15fa-118">-InstanceId</span></span>
<span data-ttu-id="b15fa-119">Die Instanz-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b15fa-119">The instance ID of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b15fa-120">-Reimage</span><span class="sxs-lookup"><span data-stu-id="b15fa-120">-Reimage</span></span>
<span data-ttu-id="b15fa-121">Gibt an, dass das Cmdlet die VMSS.</span><span class="sxs-lookup"><span data-stu-id="b15fa-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15fa-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="b15fa-122">-ReimageAll</span></span>
<span data-ttu-id="b15fa-123">Gibt an, dass das Cmdlet alle Datenträger im VMSS umbildet.</span><span class="sxs-lookup"><span data-stu-id="b15fa-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15fa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15fa-124">-ResourceGroupName</span></span>
<span data-ttu-id="b15fa-125">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="b15fa-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b15fa-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b15fa-126">-VMScaleSetName</span></span>
<span data-ttu-id="b15fa-127">Art der Name des VMSS, für das dieses Cmdlet Aktionen festlegt.</span><span class="sxs-lookup"><span data-stu-id="b15fa-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="b15fa-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b15fa-128">-Confirm</span></span>
<span data-ttu-id="b15fa-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b15fa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b15fa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15fa-130">-WhatIf</span></span>
<span data-ttu-id="b15fa-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b15fa-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b15fa-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b15fa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b15fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15fa-133">CommonParameters</span></span>
<span data-ttu-id="b15fa-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b15fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15fa-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b15fa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15fa-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b15fa-136">INPUTS</span></span>

### <span data-ttu-id="b15fa-137">Keine</span><span class="sxs-lookup"><span data-stu-id="b15fa-137">None</span></span>
<span data-ttu-id="b15fa-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b15fa-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b15fa-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b15fa-139">OUTPUTS</span></span>

### <span data-ttu-id="b15fa-140">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b15fa-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b15fa-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b15fa-141">NOTES</span></span>

## <span data-ttu-id="b15fa-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b15fa-142">RELATED LINKS</span></span>

[<span data-ttu-id="b15fa-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b15fa-144">Neu – AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b15fa-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b15fa-146">Neustart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b15fa-147">Anfang-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b15fa-148">Stopp-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="b15fa-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b15fa-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)



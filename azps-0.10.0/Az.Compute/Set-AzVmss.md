---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844179"
---
# <span data-ttu-id="9477f-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-101">Set-AzVmss</span></span>

## <span data-ttu-id="9477f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9477f-102">SYNOPSIS</span></span>
<span data-ttu-id="9477f-103">Legt bestimmte Aktionen für einen angegebenen VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="9477f-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="9477f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9477f-104">SYNTAX</span></span>

### <span data-ttu-id="9477f-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="9477f-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9477f-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="9477f-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9477f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9477f-107">DESCRIPTION</span></span>
<span data-ttu-id="9477f-108">Das Cmdlet " **Set-AzVmss** " legt bestimmte Aktionen für den virtuellen Computer-Skalierungs Satz fest (VMSS).</span><span class="sxs-lookup"><span data-stu-id="9477f-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="9477f-109">Die einzige Aktion, die dieses Cmdlet unterstützt, ist reimage.</span><span class="sxs-lookup"><span data-stu-id="9477f-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="9477f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9477f-110">EXAMPLES</span></span>

### <span data-ttu-id="9477f-111">Beispiel 1: umbilden einer VMSS</span><span class="sxs-lookup"><span data-stu-id="9477f-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="9477f-112">Mit diesem Befehl wird der VMSS mit dem Namen ContosoVMSS, der zur Ressourcengruppe mit dem Namen contosogroup gehört, erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="9477f-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="9477f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9477f-113">PARAMETERS</span></span>

### <span data-ttu-id="9477f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9477f-114">-AsJob</span></span>
<span data-ttu-id="9477f-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="9477f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9477f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9477f-116">-DefaultProfile</span></span>
<span data-ttu-id="9477f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9477f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9477f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9477f-118">-InstanceId</span></span>
<span data-ttu-id="9477f-119">Die Instanz-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="9477f-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="9477f-120">-Reimage</span><span class="sxs-lookup"><span data-stu-id="9477f-120">-Reimage</span></span>
<span data-ttu-id="9477f-121">Gibt an, dass das Cmdlet die VMSS.</span><span class="sxs-lookup"><span data-stu-id="9477f-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="9477f-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="9477f-122">-ReimageAll</span></span>
<span data-ttu-id="9477f-123">Gibt an, dass das Cmdlet alle Datenträger im VMSS umbildet.</span><span class="sxs-lookup"><span data-stu-id="9477f-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="9477f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9477f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9477f-125">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="9477f-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="9477f-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9477f-126">-VMScaleSetName</span></span>
<span data-ttu-id="9477f-127">Art der Name des VMSS, für das dieses Cmdlet Aktionen festlegt.</span><span class="sxs-lookup"><span data-stu-id="9477f-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="9477f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9477f-128">-Confirm</span></span>
<span data-ttu-id="9477f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9477f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9477f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9477f-130">-WhatIf</span></span>
<span data-ttu-id="9477f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9477f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9477f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9477f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9477f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9477f-133">CommonParameters</span></span>
<span data-ttu-id="9477f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9477f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9477f-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9477f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9477f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9477f-136">INPUTS</span></span>

### <span data-ttu-id="9477f-137">Keine</span><span class="sxs-lookup"><span data-stu-id="9477f-137">None</span></span>
<span data-ttu-id="9477f-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9477f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9477f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9477f-139">OUTPUTS</span></span>

### <span data-ttu-id="9477f-140">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="9477f-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="9477f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="9477f-141">NOTES</span></span>

## <span data-ttu-id="9477f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9477f-142">RELATED LINKS</span></span>

[<span data-ttu-id="9477f-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="9477f-144">Neu – AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="9477f-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="9477f-146">Neustart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="9477f-147">Anfang-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="9477f-148">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="9477f-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="9477f-149">Update-AzVmss</span></span>](./Update-AzVmss.md)



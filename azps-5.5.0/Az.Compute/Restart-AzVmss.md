---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: c686eec33a2f4a9f972acbdb7261f86fc45a6fa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171174"
---
# <span data-ttu-id="dd066-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-101">Restart-AzVmss</span></span>

## <span data-ttu-id="dd066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd066-102">SYNOPSIS</span></span>
<span data-ttu-id="dd066-103">Startet den VMSS oder einen virtuellen Computer innerhalb der VMSS neu.</span><span class="sxs-lookup"><span data-stu-id="dd066-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="dd066-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd066-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd066-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd066-105">DESCRIPTION</span></span>
<span data-ttu-id="dd066-106">Das **Cmdlet Restart-AzVmss** startet den Virtual Machine Scale Set (VMSS) neu.</span><span class="sxs-lookup"><span data-stu-id="dd066-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="dd066-107">Dieses Cmdlet kann auch verwendet werden, um einen bestimmten virtuellen Computer innerhalb des VMSS mithilfe des *Parameters "InstanceId" neu zu* starten.</span><span class="sxs-lookup"><span data-stu-id="dd066-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="dd066-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dd066-108">EXAMPLES</span></span>

### <span data-ttu-id="dd066-109">Beispiel 1: Neustarten der VMSS</span><span class="sxs-lookup"><span data-stu-id="dd066-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="dd066-110">Dieser Befehl startet die VMSS mit dem Namen VMSS001 neu, die zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="dd066-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="dd066-111">Beispiel 2: Neustarten eines bestimmten virtuellen Computers innerhalb der VMSS</span><span class="sxs-lookup"><span data-stu-id="dd066-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="dd066-112">Dieser Befehl startet einen virtuellen Computer mit der Instanz-ID 1 in der VMSS namens VMSS001 neu, die zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="dd066-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="dd066-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd066-113">PARAMETERS</span></span>

### <span data-ttu-id="dd066-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd066-114">-AsJob</span></span>
<span data-ttu-id="dd066-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="dd066-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dd066-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd066-116">-DefaultProfile</span></span>
<span data-ttu-id="dd066-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd066-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd066-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="dd066-118">-InstanceId</span></span>
<span data-ttu-id="dd066-119">Gibt als Zeichenfolgenarray die ID der Instanzen an, die neu gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dd066-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd066-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd066-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd066-121">Gibt den Namen der Ressourcengruppe der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="dd066-121">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd066-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="dd066-122">-VMScaleSetName</span></span>
<span data-ttu-id="dd066-123">Arten des Namens der VMSS, die dieses Cmdlet neu startet.</span><span class="sxs-lookup"><span data-stu-id="dd066-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd066-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd066-124">-Confirm</span></span>
<span data-ttu-id="dd066-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd066-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd066-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dd066-126">-WhatIf</span></span>
<span data-ttu-id="dd066-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd066-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd066-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd066-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd066-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd066-129">CommonParameters</span></span>
<span data-ttu-id="dd066-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd066-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd066-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd066-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd066-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dd066-132">INPUTS</span></span>

### <span data-ttu-id="dd066-133">System.String</span><span class="sxs-lookup"><span data-stu-id="dd066-133">System.String</span></span>

### <span data-ttu-id="dd066-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dd066-134">System.String[]</span></span>

## <span data-ttu-id="dd066-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dd066-135">OUTPUTS</span></span>

### <span data-ttu-id="dd066-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="dd066-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dd066-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dd066-137">NOTES</span></span>

## <span data-ttu-id="dd066-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dd066-138">RELATED LINKS</span></span>

[<span data-ttu-id="dd066-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="dd066-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="dd066-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="dd066-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="dd066-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="dd066-144">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="dd066-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="dd066-145">Update-AzVmss</span></span>](./Update-AzVmss.md)



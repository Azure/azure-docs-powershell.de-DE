---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: a29e21bba3d04ca301d5f2bf3d2b5f9050fe9765
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940576"
---
# <span data-ttu-id="b7268-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-101">Restart-AzVmss</span></span>

## <span data-ttu-id="b7268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7268-102">SYNOPSIS</span></span>
<span data-ttu-id="b7268-103">Startet den VMSS oder einen virtuellen Computer innerhalb des VMSS neu.</span><span class="sxs-lookup"><span data-stu-id="b7268-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="b7268-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7268-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7268-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7268-105">DESCRIPTION</span></span>
<span data-ttu-id="b7268-106">Das **Cmdlet Restart-AzVmss** startet den VmSS (Virtual Machine Scale Set) neu.</span><span class="sxs-lookup"><span data-stu-id="b7268-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b7268-107">Dieses Cmdlet kann auch verwendet werden, um einen bestimmten virtuellen Computer innerhalb des VMSS mit dem *Parameter InstanzId neu zu* starten.</span><span class="sxs-lookup"><span data-stu-id="b7268-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="b7268-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7268-108">EXAMPLES</span></span>

### <span data-ttu-id="b7268-109">Beispiel 1: Neustarten des VMSS</span><span class="sxs-lookup"><span data-stu-id="b7268-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="b7268-110">Mit diesem Befehl wird der VMSS mit dem Namen VMSS001 neu gestartet, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="b7268-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="b7268-111">Beispiel 2: Neustart eines bestimmten virtuellen Computers im VMSS</span><span class="sxs-lookup"><span data-stu-id="b7268-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="b7268-112">Mit diesem Befehl wird ein virtueller Computer neu gestartet, der die Instanz-ID 1 im VMSS mit dem Namen VMSS001 hat, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="b7268-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b7268-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b7268-113">PARAMETERS</span></span>

### <span data-ttu-id="b7268-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7268-114">-AsJob</span></span>
<span data-ttu-id="b7268-115">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="b7268-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b7268-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7268-116">-DefaultProfile</span></span>
<span data-ttu-id="b7268-117">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7268-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7268-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b7268-118">-InstanceId</span></span>
<span data-ttu-id="b7268-119">Gibt als Zeichenfolgenarray die ID der Instanzen an, die neu gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b7268-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="b7268-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7268-120">-ResourceGroupName</span></span>
<span data-ttu-id="b7268-121">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="b7268-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b7268-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b7268-122">-VMScaleSetName</span></span>
<span data-ttu-id="b7268-123">Speziert den Namen des VMSS, den dieses Cmdlet neu startet.</span><span class="sxs-lookup"><span data-stu-id="b7268-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="b7268-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b7268-124">-Confirm</span></span>
<span data-ttu-id="b7268-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7268-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7268-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7268-126">-WhatIf</span></span>
<span data-ttu-id="b7268-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7268-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7268-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7268-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7268-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7268-129">CommonParameters</span></span>
<span data-ttu-id="b7268-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7268-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7268-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7268-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7268-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7268-132">INPUTS</span></span>

### <span data-ttu-id="b7268-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b7268-133">System.String</span></span>

### <span data-ttu-id="b7268-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b7268-134">System.String[]</span></span>

## <span data-ttu-id="b7268-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7268-135">OUTPUTS</span></span>

### <span data-ttu-id="b7268-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b7268-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b7268-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b7268-137">NOTES</span></span>

## <span data-ttu-id="b7268-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b7268-138">RELATED LINKS</span></span>

[<span data-ttu-id="b7268-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="b7268-140">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="b7268-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="b7268-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b7268-143">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b7268-144">Stopp-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="b7268-145">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b7268-145">Update-AzVmss</span></span>](./Update-AzVmss.md)



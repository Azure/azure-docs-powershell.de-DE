---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 0371dd5ba008089ff8d8731e0ebb30e6b3caf8fe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934256"
---
# <span data-ttu-id="b9b73-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b9b73-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="b9b73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9b73-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b73-103">Bricht den aktuellen Skalierungssatz für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b9b73-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b9b73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9b73-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b73-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9b73-105">DESCRIPTION</span></span>
<span data-ttu-id="b9b73-106">Bricht den aktuellen Skalierungssatz für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="b9b73-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="b9b73-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9b73-107">EXAMPLES</span></span>

### <span data-ttu-id="b9b73-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9b73-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b9b73-109">Mit diesem Befehl wird das fortlaufende Rollup des VM-Skalierungssets "VMSS001" in der Ressourcengruppe "Group001" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b9b73-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="b9b73-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9b73-110">PARAMETERS</span></span>

### <span data-ttu-id="b9b73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9b73-111">-AsJob</span></span>
<span data-ttu-id="b9b73-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b9b73-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9b73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b73-113">-DefaultProfile</span></span>
<span data-ttu-id="b9b73-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9b73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9b73-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b9b73-115">-Force</span></span>
<span data-ttu-id="b9b73-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="b9b73-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9b73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b73-117">-ResourceGroupName</span></span>
<span data-ttu-id="b9b73-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9b73-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9b73-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b9b73-119">-VMScaleSetName</span></span>
<span data-ttu-id="b9b73-120">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="b9b73-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="b9b73-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b9b73-121">-Confirm</span></span>
<span data-ttu-id="b9b73-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9b73-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9b73-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9b73-123">-WhatIf</span></span>
<span data-ttu-id="b9b73-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9b73-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b73-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9b73-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9b73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b73-126">CommonParameters</span></span>
<span data-ttu-id="b9b73-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b73-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9b73-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b73-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9b73-129">INPUTS</span></span>

### <span data-ttu-id="b9b73-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b9b73-130">System.String</span></span>

## <span data-ttu-id="b9b73-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9b73-131">OUTPUTS</span></span>

### <span data-ttu-id="b9b73-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b9b73-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b9b73-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b9b73-133">NOTES</span></span>

## <span data-ttu-id="b9b73-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b9b73-134">RELATED LINKS</span></span>

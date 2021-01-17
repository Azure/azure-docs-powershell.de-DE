---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmssrollingupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmssRollingUpgrade.md
ms.openlocfilehash: 331f390890e6349c5a48f9b57c3d0e99fa972532
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302600"
---
# <span data-ttu-id="576dc-101">Stop-AzVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="576dc-101">Stop-AzVmssRollingUpgrade</span></span>

## <span data-ttu-id="576dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576dc-102">SYNOPSIS</span></span>
<span data-ttu-id="576dc-103">Bricht das fortlaufende Upgrade des aktuellen Skalierungssets für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="576dc-103">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="576dc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="576dc-104">SYNTAX</span></span>

```
Stop-AzVmssRollingUpgrade [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576dc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="576dc-105">DESCRIPTION</span></span>
<span data-ttu-id="576dc-106">Bricht das fortlaufende Upgrade des aktuellen Skalierungssets für den virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="576dc-106">Cancels the current virtual machine scale set rolling upgrade.</span></span>

## <span data-ttu-id="576dc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="576dc-107">EXAMPLES</span></span>

### <span data-ttu-id="576dc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="576dc-108">Example 1</span></span>
```
PS C:\> Stop-AzVmssRollingUpgrade -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="576dc-109">Dieser Befehl bricht das fortlaufende Rollup des VM-Skalierungs-Set "VMSS001" in der Ressourcengruppe "Group001" ab.</span><span class="sxs-lookup"><span data-stu-id="576dc-109">This command cancels on-going rolling upgrade of VM scale set "VMSS001" in resource group "Group001".</span></span>

## <span data-ttu-id="576dc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="576dc-110">PARAMETERS</span></span>

### <span data-ttu-id="576dc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="576dc-111">-AsJob</span></span>
<span data-ttu-id="576dc-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="576dc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="576dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576dc-113">-DefaultProfile</span></span>
<span data-ttu-id="576dc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="576dc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="576dc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="576dc-115">-Force</span></span>
<span data-ttu-id="576dc-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="576dc-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="576dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="576dc-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="576dc-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="576dc-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="576dc-119">-VMScaleSetName</span></span>
<span data-ttu-id="576dc-120">Der Name des VM-Skalierungssets.</span><span class="sxs-lookup"><span data-stu-id="576dc-120">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="576dc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="576dc-121">-Confirm</span></span>
<span data-ttu-id="576dc-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="576dc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576dc-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="576dc-123">-WhatIf</span></span>
<span data-ttu-id="576dc-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="576dc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576dc-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="576dc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576dc-126">CommonParameters</span></span>
<span data-ttu-id="576dc-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="576dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576dc-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="576dc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576dc-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="576dc-129">INPUTS</span></span>

### <span data-ttu-id="576dc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="576dc-130">System.String</span></span>

## <span data-ttu-id="576dc-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="576dc-131">OUTPUTS</span></span>

### <span data-ttu-id="576dc-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="576dc-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="576dc-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="576dc-133">NOTES</span></span>

## <span data-ttu-id="576dc-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="576dc-134">RELATED LINKS</span></span>

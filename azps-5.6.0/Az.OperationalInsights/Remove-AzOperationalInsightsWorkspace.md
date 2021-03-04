---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 916e818b628608fcae7001797af298317ff96a4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937880"
---
# <span data-ttu-id="ea7a2-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea7a2-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="ea7a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7a2-103">Entfernt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-103">Removes a workspace.</span></span>

## <span data-ttu-id="ea7a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea7a2-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea7a2-105">DESCRIPTION</span></span>
<span data-ttu-id="ea7a2-106">Das **Cmdlet Remove-AzOperationalInsightsWorkspace** löscht einen vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="ea7a2-107">Wenn dieser Arbeitsbereich zum Zeitpunkt der Erstellung über den *Parameter CustomerId* mit einem vorhandenen Konto verknüpft wurde, wird das ursprüngliche Konto im Portal Operational Insights nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="ea7a2-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea7a2-108">EXAMPLES</span></span>

### <span data-ttu-id="ea7a2-109">Beispiel 1: Entfernen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="ea7a2-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="ea7a2-110">Mit diesem Befehl wird der Arbeitsbereich "MyWorkspace" aus der Ressourcengruppe "ContosoResourceGroup" entfernt.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="ea7a2-111">Beispiel 2: Entfernen eines Arbeitsbereichs mithilfe der Pipeline und ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="ea7a2-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="ea7a2-112">Dieser Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkspace zu erhalten, und übergibt ihn dann mithilfe des Pipelineoperators an das **Remove-AzOperationalInsightsWorkspace-Cmdlet,** um ihn zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="ea7a2-113">Da der *Parameter Erzwingen* angegeben ist, werden Sie vom Befehl vor dem Entfernen des Arbeitsbereichs nicht aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="ea7a2-114">Beispiel 3: Erzwingen des Löscharbeitsbereichs (kann nicht wiederhergestellt werden)</span><span class="sxs-lookup"><span data-stu-id="ea7a2-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="ea7a2-115">Erzwingen sie das Löschen eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-115">Force delete a workspace.</span></span>

## <span data-ttu-id="ea7a2-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea7a2-116">PARAMETERS</span></span>

### <span data-ttu-id="ea7a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7a2-117">-DefaultProfile</span></span>
<span data-ttu-id="ea7a2-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ea7a2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea7a2-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="ea7a2-119">-Force</span></span>
<span data-ttu-id="ea7a2-120">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea7a2-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="ea7a2-121">-ForceDelete</span></span>
<span data-ttu-id="ea7a2-122">Erzwingen des Löscharbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="ea7a2-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="ea7a2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ea7a2-123">-Name</span></span>
<span data-ttu-id="ea7a2-124">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-124">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="ea7a2-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="ea7a2-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea7a2-127">-Confirm</span></span>
<span data-ttu-id="ea7a2-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7a2-129">-WhatIf</span></span>
<span data-ttu-id="ea7a2-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7a2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea7a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7a2-132">CommonParameters</span></span>
<span data-ttu-id="ea7a2-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea7a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7a2-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea7a2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7a2-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea7a2-135">INPUTS</span></span>

### <span data-ttu-id="ea7a2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ea7a2-136">System.String</span></span>

## <span data-ttu-id="ea7a2-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea7a2-137">OUTPUTS</span></span>

### <span data-ttu-id="ea7a2-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="ea7a2-138">System.Void</span></span>

## <span data-ttu-id="ea7a2-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ea7a2-139">NOTES</span></span>

## <span data-ttu-id="ea7a2-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ea7a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="ea7a2-141">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ea7a2-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="ea7a2-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea7a2-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



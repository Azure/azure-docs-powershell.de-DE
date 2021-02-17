---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169548"
---
# <span data-ttu-id="38975-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="38975-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="38975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38975-102">SYNOPSIS</span></span>
<span data-ttu-id="38975-103">Entfernt einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="38975-103">Removes a workspace.</span></span>

## <span data-ttu-id="38975-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38975-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38975-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38975-105">DESCRIPTION</span></span>
<span data-ttu-id="38975-106">Das **Cmdlet "Remove-AzOperationalInsightsWorkspace"** löscht einen vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="38975-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="38975-107">Wenn dieser Arbeitsbereich zum Zeitpunkt der Erstellung über den Parameter *"CustomerId"* mit einem vorhandenen Konto verknüpft wurde, wird das ursprüngliche Konto nicht im Portal für operationale Einblicke gelöscht.</span><span class="sxs-lookup"><span data-stu-id="38975-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="38975-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38975-108">EXAMPLES</span></span>

### <span data-ttu-id="38975-109">Beispiel 1: Entfernen eines Arbeitsbereichs nach Name</span><span class="sxs-lookup"><span data-stu-id="38975-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="38975-110">Mit diesem Befehl wird der Arbeitsbereich "MyWorkspace" aus der Ressourcengruppe "ContosoResourceGroup" entfernt.</span><span class="sxs-lookup"><span data-stu-id="38975-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="38975-111">Beispiel 2: Entfernen eines Arbeitsbereichs mithilfe der Pipeline und ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="38975-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="38975-112">Dieser Befehl verwendet das Cmdlet Get-AzOperationalInsightsWorkspace, um den Arbeitsbereich "MyWorkspace" zu erhalten, und übergibt ihn dann mithilfe des Pipelineoperators an das Cmdlet **"Remove-AzOperationalInsightsWorkspace",** um ihn zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="38975-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="38975-113">Da der *Parameter "Force"* angegeben ist, werden Sie vom Befehl vor dem Entfernen des Arbeitsbereichs nicht dazu aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="38975-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="38975-114">Beispiel 3: Erzwingen des Löschens eines Arbeitsbereichs (kann nicht wiederhergestellt werden)</span><span class="sxs-lookup"><span data-stu-id="38975-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="38975-115">Erzwingen des Löschens eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="38975-115">Force delete a workspace.</span></span>

## <span data-ttu-id="38975-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38975-116">PARAMETERS</span></span>

### <span data-ttu-id="38975-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38975-117">-DefaultProfile</span></span>
<span data-ttu-id="38975-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="38975-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38975-119">-Force</span><span class="sxs-lookup"><span data-stu-id="38975-119">-Force</span></span>
<span data-ttu-id="38975-120">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="38975-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38975-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="38975-121">-ForceDelete</span></span>
<span data-ttu-id="38975-122">Erzwingen des Löschens eines Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="38975-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="38975-123">-Name</span><span class="sxs-lookup"><span data-stu-id="38975-123">-Name</span></span>
<span data-ttu-id="38975-124">Gibt den Namen des Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="38975-124">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="38975-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38975-125">-ResourceGroupName</span></span>
<span data-ttu-id="38975-126">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="38975-126">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="38975-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38975-127">-Confirm</span></span>
<span data-ttu-id="38975-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38975-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38975-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="38975-129">-WhatIf</span></span>
<span data-ttu-id="38975-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38975-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38975-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38975-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38975-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38975-132">CommonParameters</span></span>
<span data-ttu-id="38975-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38975-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38975-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38975-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38975-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38975-135">INPUTS</span></span>

### <span data-ttu-id="38975-136">System.String</span><span class="sxs-lookup"><span data-stu-id="38975-136">System.String</span></span>

## <span data-ttu-id="38975-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38975-137">OUTPUTS</span></span>

### <span data-ttu-id="38975-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="38975-138">System.Void</span></span>

## <span data-ttu-id="38975-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38975-139">NOTES</span></span>

## <span data-ttu-id="38975-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38975-140">RELATED LINKS</span></span>

[<span data-ttu-id="38975-141">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="38975-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="38975-142">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="38975-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)



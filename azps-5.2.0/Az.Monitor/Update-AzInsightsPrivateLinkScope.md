---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294802"
---
# <span data-ttu-id="7a771-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7a771-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="7a771-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a771-102">SYNOPSIS</span></span>
<span data-ttu-id="7a771-103">Update für privaten Verknüpfungsbereich</span><span class="sxs-lookup"><span data-stu-id="7a771-103">Update for private link scope</span></span>

## <span data-ttu-id="7a771-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a771-104">SYNTAX</span></span>

### <span data-ttu-id="7a771-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a771-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a771-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a771-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a771-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a771-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a771-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a771-108">DESCRIPTION</span></span>
<span data-ttu-id="7a771-109">Update für privaten Verknüpfungsbereich</span><span class="sxs-lookup"><span data-stu-id="7a771-109">Update for private link scope</span></span>

## <span data-ttu-id="7a771-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a771-110">EXAMPLES</span></span>

### <span data-ttu-id="7a771-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a771-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="7a771-112">Privaten Verknüpfungsbereich mit dem Namen "scope_name" unter der Ressourcengruppe "rg_name" aktualisieren, um das Tag "key:value" zu verwenden</span><span class="sxs-lookup"><span data-stu-id="7a771-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="7a771-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7a771-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="7a771-114">Privaten Verknüpfungsbereich mit Ressourcen-ID aktualisieren, um das Tag "key:value" zu verwenden</span><span class="sxs-lookup"><span data-stu-id="7a771-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="7a771-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7a771-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="7a771-116">Aktualisieren des Bereichs privater Verknüpfungen mit dem Objekt für den privaten Verknüpfungsbereich der Eingabe, um das Tag "key:value" zu verwenden</span><span class="sxs-lookup"><span data-stu-id="7a771-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="7a771-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a771-117">PARAMETERS</span></span>

### <span data-ttu-id="7a771-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a771-118">-DefaultProfile</span></span>
<span data-ttu-id="7a771-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a771-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a771-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a771-120">-InputObject</span></span>
<span data-ttu-id="7a771-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7a771-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a771-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7a771-122">-Name</span></span>
<span data-ttu-id="7a771-123">Name des Bereichs für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="7a771-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a771-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a771-124">-ResourceGroupName</span></span>
<span data-ttu-id="7a771-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="7a771-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a771-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a771-126">-ResourceId</span></span>
<span data-ttu-id="7a771-127">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7a771-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a771-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="7a771-128">-Tags</span></span>
<span data-ttu-id="7a771-129">Kategorien</span><span class="sxs-lookup"><span data-stu-id="7a771-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a771-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a771-130">-Confirm</span></span>
<span data-ttu-id="7a771-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a771-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a771-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7a771-132">-WhatIf</span></span>
<span data-ttu-id="7a771-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a771-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a771-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a771-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a771-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a771-135">CommonParameters</span></span>
<span data-ttu-id="7a771-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a771-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a771-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a771-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a771-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a771-138">INPUTS</span></span>

### <span data-ttu-id="7a771-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7a771-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="7a771-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7a771-140">System.String</span></span>

## <span data-ttu-id="7a771-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a771-141">OUTPUTS</span></span>

### <span data-ttu-id="7a771-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7a771-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="7a771-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a771-143">NOTES</span></span>

## <span data-ttu-id="7a771-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a771-144">RELATED LINKS</span></span>

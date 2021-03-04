---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ef53c93669faea2e9f952c0887e6cb0b105cf19b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925496"
---
# <span data-ttu-id="d4aec-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4aec-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="d4aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4aec-102">SYNOPSIS</span></span>
<span data-ttu-id="d4aec-103">Update für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="d4aec-103">Update for private link scope</span></span>

## <span data-ttu-id="d4aec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4aec-104">SYNTAX</span></span>

### <span data-ttu-id="d4aec-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4aec-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4aec-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4aec-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4aec-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4aec-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4aec-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4aec-108">DESCRIPTION</span></span>
<span data-ttu-id="d4aec-109">Update für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="d4aec-109">Update for private link scope</span></span>

## <span data-ttu-id="d4aec-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4aec-110">EXAMPLES</span></span>

### <span data-ttu-id="d4aec-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4aec-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="d4aec-112">Aktualisieren des privaten Linkbereichs mit dem Namen "scope_name" unter der Ressourcengruppe "rg_name" zum Verwenden des Tags "key:value"</span><span class="sxs-lookup"><span data-stu-id="d4aec-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="d4aec-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4aec-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="d4aec-114">Aktualisieren des privaten Linkbereichs mit Ressourcen-ID zur Verwendung des Tags "key:value"</span><span class="sxs-lookup"><span data-stu-id="d4aec-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="d4aec-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d4aec-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="d4aec-116">Aktualisieren des privaten Linkbereichs mit dem Privaten Linkbereichsobjekt für die Verwendung des Tags "key:value"</span><span class="sxs-lookup"><span data-stu-id="d4aec-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="d4aec-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d4aec-117">PARAMETERS</span></span>

### <span data-ttu-id="d4aec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4aec-118">-DefaultProfile</span></span>
<span data-ttu-id="d4aec-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4aec-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4aec-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4aec-120">-InputObject</span></span>
<span data-ttu-id="d4aec-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4aec-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="d4aec-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d4aec-122">-Name</span></span>
<span data-ttu-id="d4aec-123">Name des Privaten Linkbereichs</span><span class="sxs-lookup"><span data-stu-id="d4aec-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d4aec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4aec-124">-ResourceGroupName</span></span>
<span data-ttu-id="d4aec-125">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d4aec-125">Resource Group Name</span></span>

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

### <span data-ttu-id="d4aec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4aec-126">-ResourceId</span></span>
<span data-ttu-id="d4aec-127">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d4aec-127">Resource Id</span></span>

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

### <span data-ttu-id="d4aec-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="d4aec-128">-Tags</span></span>
<span data-ttu-id="d4aec-129">Tags</span><span class="sxs-lookup"><span data-stu-id="d4aec-129">Tags</span></span>

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

### <span data-ttu-id="d4aec-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4aec-130">-Confirm</span></span>
<span data-ttu-id="d4aec-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4aec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4aec-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4aec-132">-WhatIf</span></span>
<span data-ttu-id="d4aec-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4aec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4aec-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4aec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4aec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4aec-135">CommonParameters</span></span>
<span data-ttu-id="d4aec-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4aec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4aec-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4aec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4aec-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4aec-138">INPUTS</span></span>

### <span data-ttu-id="d4aec-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4aec-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="d4aec-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d4aec-140">System.String</span></span>

## <span data-ttu-id="d4aec-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4aec-141">OUTPUTS</span></span>

### <span data-ttu-id="d4aec-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d4aec-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="d4aec-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d4aec-143">NOTES</span></span>

## <span data-ttu-id="d4aec-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d4aec-144">RELATED LINKS</span></span>

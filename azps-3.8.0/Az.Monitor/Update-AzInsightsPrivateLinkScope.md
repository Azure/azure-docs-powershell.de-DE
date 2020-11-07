---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845080"
---
# <span data-ttu-id="e21dc-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e21dc-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="e21dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e21dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e21dc-103">Update für den Bereich "privater Link"</span><span class="sxs-lookup"><span data-stu-id="e21dc-103">Update for private link scope</span></span>

## <span data-ttu-id="e21dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e21dc-104">SYNTAX</span></span>

### <span data-ttu-id="e21dc-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e21dc-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e21dc-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e21dc-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e21dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e21dc-108">DESCRIPTION</span></span>
<span data-ttu-id="e21dc-109">Update für den Bereich "privater Link"</span><span class="sxs-lookup"><span data-stu-id="e21dc-109">Update for private link scope</span></span>

## <span data-ttu-id="e21dc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e21dc-110">EXAMPLES</span></span>

### <span data-ttu-id="e21dc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e21dc-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="e21dc-112">Aktualisieren des Bereichs "privater Link" mit dem Namen "scope_name" unter Ressourcengruppe "rg_name", um das Tag "Schlüssel: Wert" zu verwenden</span><span class="sxs-lookup"><span data-stu-id="e21dc-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="e21dc-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e21dc-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="e21dc-114">Aktualisieren des Bereichs "privater Link" mit der Ressourcen-ID zum Verwenden des Tags "Schlüssel: Wert"</span><span class="sxs-lookup"><span data-stu-id="e21dc-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="e21dc-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e21dc-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="e21dc-116">Aktualisieren des Bereichs "privater Link" mit dem Bereich "Eingabe privater Link", um das Tag "Schlüssel: Wert" zu verwenden</span><span class="sxs-lookup"><span data-stu-id="e21dc-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="e21dc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="e21dc-117">PARAMETERS</span></span>

### <span data-ttu-id="e21dc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21dc-118">-DefaultProfile</span></span>
<span data-ttu-id="e21dc-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e21dc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21dc-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e21dc-120">-InputObject</span></span>
<span data-ttu-id="e21dc-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e21dc-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="e21dc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e21dc-122">-Name</span></span>
<span data-ttu-id="e21dc-123">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="e21dc-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="e21dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="e21dc-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e21dc-125">Resource Group Name</span></span>

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

### <span data-ttu-id="e21dc-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e21dc-126">-ResourceId</span></span>
<span data-ttu-id="e21dc-127">Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e21dc-127">Resource Id</span></span>

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

### <span data-ttu-id="e21dc-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="e21dc-128">-Tags</span></span>
<span data-ttu-id="e21dc-129">Tags</span><span class="sxs-lookup"><span data-stu-id="e21dc-129">Tags</span></span>

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

### <span data-ttu-id="e21dc-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e21dc-130">-Confirm</span></span>
<span data-ttu-id="e21dc-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e21dc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21dc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21dc-132">-WhatIf</span></span>
<span data-ttu-id="e21dc-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e21dc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e21dc-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e21dc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21dc-135">CommonParameters</span></span>
<span data-ttu-id="e21dc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e21dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21dc-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e21dc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21dc-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e21dc-138">INPUTS</span></span>

### <span data-ttu-id="e21dc-139">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e21dc-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="e21dc-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e21dc-140">System.String</span></span>

## <span data-ttu-id="e21dc-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e21dc-141">OUTPUTS</span></span>

### <span data-ttu-id="e21dc-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e21dc-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="e21dc-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="e21dc-143">NOTES</span></span>

## <span data-ttu-id="e21dc-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e21dc-144">RELATED LINKS</span></span>

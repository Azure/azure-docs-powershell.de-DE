---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179066"
---
# <span data-ttu-id="dbf64-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="dbf64-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="dbf64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbf64-102">SYNOPSIS</span></span>
<span data-ttu-id="dbf64-103">Erstellen einer Ressource für privaten Linkbereich</span><span class="sxs-lookup"><span data-stu-id="dbf64-103">create for private link scoped resource</span></span>

## <span data-ttu-id="dbf64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbf64-104">SYNTAX</span></span>

### <span data-ttu-id="dbf64-105">ByResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dbf64-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbf64-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dbf64-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbf64-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbf64-107">DESCRIPTION</span></span>
<span data-ttu-id="dbf64-108">Erstellen für private Linkbereich Ressource, Bereich Ressource könnte Log Analytics Workspace oder Application Insights-Komponente sein</span><span class="sxs-lookup"><span data-stu-id="dbf64-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="dbf64-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbf64-109">EXAMPLES</span></span>

### <span data-ttu-id="dbf64-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbf64-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="dbf64-111">Erstellen einer Bereich-Ressource "scoped_resource_name" mit der Komponente "Application Insights" verknüpft "ai_name"</span><span class="sxs-lookup"><span data-stu-id="dbf64-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="dbf64-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbf64-112">PARAMETERS</span></span>

### <span data-ttu-id="dbf64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbf64-113">-DefaultProfile</span></span>
<span data-ttu-id="dbf64-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbf64-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbf64-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dbf64-115">-InputObject</span></span>
<span data-ttu-id="dbf64-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dbf64-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="dbf64-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="dbf64-117">-LinkedResourceId</span></span>
<span data-ttu-id="dbf64-118">La/AI-Ressourcen-ID, die verknüpft werden soll</span><span class="sxs-lookup"><span data-stu-id="dbf64-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf64-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dbf64-119">-Name</span></span>
<span data-ttu-id="dbf64-120">Name der Bereichs Ressource</span><span class="sxs-lookup"><span data-stu-id="dbf64-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbf64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbf64-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbf64-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="dbf64-122">Resource Group Name</span></span>

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

### <span data-ttu-id="dbf64-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="dbf64-123">-ScopeName</span></span>
<span data-ttu-id="dbf64-124">Name des privaten Link Bereichs</span><span class="sxs-lookup"><span data-stu-id="dbf64-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="dbf64-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbf64-125">-Confirm</span></span>
<span data-ttu-id="dbf64-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbf64-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbf64-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbf64-127">-WhatIf</span></span>
<span data-ttu-id="dbf64-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbf64-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbf64-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbf64-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbf64-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbf64-130">CommonParameters</span></span>
<span data-ttu-id="dbf64-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbf64-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbf64-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbf64-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbf64-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbf64-133">INPUTS</span></span>

### <span data-ttu-id="dbf64-134">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dbf64-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="dbf64-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dbf64-135">System.String</span></span>

## <span data-ttu-id="dbf64-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbf64-136">OUTPUTS</span></span>

### <span data-ttu-id="dbf64-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="dbf64-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="dbf64-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbf64-138">NOTES</span></span>

## <span data-ttu-id="dbf64-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbf64-139">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 7a6914d6259cafaedff68b28e8691311245ef6f0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937976"
---
# <span data-ttu-id="3bd77-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="3bd77-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="3bd77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bd77-102">SYNOPSIS</span></span>
<span data-ttu-id="3bd77-103">Fügt Leistungsindikatoren zu allen Linux-Computern in einem Arbeitsbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="3bd77-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3bd77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bd77-104">SYNTAX</span></span>

### <span data-ttu-id="3bd77-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bd77-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bd77-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3bd77-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bd77-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bd77-107">DESCRIPTION</span></span>
<span data-ttu-id="3bd77-108">Das **Cmdlet New-AzOperationalInsightsLinuxPerformanceObjectDataSource** fügt Leistungsindikatoren hinzu, aus denen Azure Operational Insights Daten auf allen Linux-Computern in einem Arbeitsbereich sammelt.</span><span class="sxs-lookup"><span data-stu-id="3bd77-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="3bd77-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3bd77-109">EXAMPLES</span></span>

## <span data-ttu-id="3bd77-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3bd77-110">PARAMETERS</span></span>

### <span data-ttu-id="3bd77-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="3bd77-111">-CounterNames</span></span>
<span data-ttu-id="3bd77-112">Gibt ein Array mit Namen von Zählern an.</span><span class="sxs-lookup"><span data-stu-id="3bd77-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bd77-113">-DefaultProfile</span></span>
<span data-ttu-id="3bd77-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3bd77-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3bd77-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3bd77-115">-Force</span></span>
<span data-ttu-id="3bd77-116">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="3bd77-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3bd77-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3bd77-117">-InstanceName</span></span>
<span data-ttu-id="3bd77-118">Gibt einen Instanznamen an.</span><span class="sxs-lookup"><span data-stu-id="3bd77-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="3bd77-119">-IntervalSeconds</span></span>
<span data-ttu-id="3bd77-120">Gibt das Intervall der Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="3bd77-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3bd77-121">-Name</span></span>
<span data-ttu-id="3bd77-122">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="3bd77-122">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="3bd77-123">-ObjectName</span></span>
<span data-ttu-id="3bd77-124">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="3bd77-124">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bd77-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bd77-126">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="3bd77-126">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-127">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="3bd77-127">-Workspace</span></span>
<span data-ttu-id="3bd77-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3bd77-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3bd77-129">-WorkspaceName</span></span>
<span data-ttu-id="3bd77-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3bd77-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bd77-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3bd77-131">-Confirm</span></span>
<span data-ttu-id="3bd77-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3bd77-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bd77-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bd77-133">-WhatIf</span></span>
<span data-ttu-id="3bd77-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3bd77-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bd77-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bd77-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bd77-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bd77-136">CommonParameters</span></span>
<span data-ttu-id="3bd77-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bd77-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bd77-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bd77-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bd77-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3bd77-139">INPUTS</span></span>

### <span data-ttu-id="3bd77-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3bd77-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3bd77-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3bd77-141">System.String</span></span>

### <span data-ttu-id="3bd77-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3bd77-142">System.String[]</span></span>

### <span data-ttu-id="3bd77-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3bd77-143">System.Int32</span></span>

## <span data-ttu-id="3bd77-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3bd77-144">OUTPUTS</span></span>

### <span data-ttu-id="3bd77-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3bd77-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3bd77-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3bd77-146">NOTES</span></span>

## <span data-ttu-id="3bd77-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3bd77-147">RELATED LINKS</span></span>

[<span data-ttu-id="3bd77-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3bd77-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="3bd77-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3bd77-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)



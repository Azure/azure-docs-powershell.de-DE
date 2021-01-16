---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298880"
---
# <span data-ttu-id="7d472-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="7d472-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="7d472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d472-102">SYNOPSIS</span></span>
<span data-ttu-id="7d472-103">Fügt Leistungszähler zu allen Linux-Computern in einem Arbeitsbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="7d472-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="7d472-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d472-104">SYNTAX</span></span>

### <span data-ttu-id="7d472-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d472-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d472-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7d472-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d472-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7d472-107">DESCRIPTION</span></span>
<span data-ttu-id="7d472-108">Das **Cmdlet "New-AzOperationalInsightsLinuxPerformanceObjectDataSource"** fügt Leistungszähler hinzu, aus denen Azure Operational Insights Daten auf allen Linux-Computern in einem Arbeitsbereich sammelt.</span><span class="sxs-lookup"><span data-stu-id="7d472-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="7d472-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7d472-109">EXAMPLES</span></span>

## <span data-ttu-id="7d472-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d472-110">PARAMETERS</span></span>

### <span data-ttu-id="7d472-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="7d472-111">-CounterNames</span></span>
<span data-ttu-id="7d472-112">Gibt ein Array von Namen von Leistungsindikatoren an.</span><span class="sxs-lookup"><span data-stu-id="7d472-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="7d472-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d472-113">-DefaultProfile</span></span>
<span data-ttu-id="7d472-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="7d472-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d472-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7d472-115">-Force</span></span>
<span data-ttu-id="7d472-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="7d472-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d472-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7d472-117">-InstanceName</span></span>
<span data-ttu-id="7d472-118">Gibt einen Instanznamen an.</span><span class="sxs-lookup"><span data-stu-id="7d472-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="7d472-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="7d472-119">-IntervalSeconds</span></span>
<span data-ttu-id="7d472-120">Gibt das Sammlungsintervall an.</span><span class="sxs-lookup"><span data-stu-id="7d472-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="7d472-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d472-121">-Name</span></span>
<span data-ttu-id="7d472-122">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="7d472-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="7d472-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="7d472-123">-ObjectName</span></span>
<span data-ttu-id="7d472-124">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="7d472-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="7d472-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d472-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d472-126">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="7d472-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="7d472-127">-Workspace</span><span class="sxs-lookup"><span data-stu-id="7d472-127">-Workspace</span></span>
<span data-ttu-id="7d472-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7d472-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7d472-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d472-129">-WorkspaceName</span></span>
<span data-ttu-id="7d472-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7d472-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7d472-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d472-131">-Confirm</span></span>
<span data-ttu-id="7d472-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d472-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d472-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7d472-133">-WhatIf</span></span>
<span data-ttu-id="7d472-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d472-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d472-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d472-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d472-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d472-136">CommonParameters</span></span>
<span data-ttu-id="7d472-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d472-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d472-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d472-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d472-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7d472-139">INPUTS</span></span>

### <span data-ttu-id="7d472-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d472-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7d472-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7d472-141">System.String</span></span>

### <span data-ttu-id="7d472-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7d472-142">System.String[]</span></span>

### <span data-ttu-id="7d472-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7d472-143">System.Int32</span></span>

## <span data-ttu-id="7d472-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7d472-144">OUTPUTS</span></span>

### <span data-ttu-id="7d472-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7d472-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7d472-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7d472-146">NOTES</span></span>

## <span data-ttu-id="7d472-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7d472-147">RELATED LINKS</span></span>

[<span data-ttu-id="7d472-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="7d472-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="7d472-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="7d472-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)



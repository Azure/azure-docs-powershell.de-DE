---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 656d25e69e2739df7e196ba9e584c3890bf4028f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166183"
---
# <span data-ttu-id="6e6a3-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="6e6a3-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="6e6a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6e6a3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e6a3-103">Fügt allen Linux-Computern in einem Arbeitsbereich Leistungsindikatoren hinzu.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="6e6a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e6a3-104">SYNTAX</span></span>

### <span data-ttu-id="6e6a3-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6e6a3-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e6a3-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6e6a3-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e6a3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e6a3-107">DESCRIPTION</span></span>
<span data-ttu-id="6e6a3-108">Das Cmdlet **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** fügt Leistungsindikatoren hinzu, aus denen Azure Operational Insights Daten auf allen Linux-Computern in einem Arbeitsbereich sammelt.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="6e6a3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e6a3-109">EXAMPLES</span></span>

## <span data-ttu-id="6e6a3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e6a3-110">PARAMETERS</span></span>

### <span data-ttu-id="6e6a3-111">-Gegen Namen</span><span class="sxs-lookup"><span data-stu-id="6e6a3-111">-CounterNames</span></span>
<span data-ttu-id="6e6a3-112">Gibt ein Array mit Namen von Zählern an.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="6e6a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e6a3-113">-DefaultProfile</span></span>
<span data-ttu-id="6e6a3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6e6a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e6a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6e6a3-115">-Force</span></span>
<span data-ttu-id="6e6a3-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e6a3-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6e6a3-117">-InstanceName</span></span>
<span data-ttu-id="6e6a3-118">Gibt den Namen einer Instanz an.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="6e6a3-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="6e6a3-119">-IntervalSeconds</span></span>
<span data-ttu-id="6e6a3-120">Gibt das Intervall der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="6e6a3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6e6a3-121">-Name</span></span>
<span data-ttu-id="6e6a3-122">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="6e6a3-123">-Objektname</span><span class="sxs-lookup"><span data-stu-id="6e6a3-123">-ObjectName</span></span>
<span data-ttu-id="6e6a3-124">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="6e6a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e6a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="6e6a3-126">Gibt den Namen einer Ressourcengruppe an, die Linux-Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="6e6a3-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="6e6a3-127">-Workspace</span></span>
<span data-ttu-id="6e6a3-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6e6a3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e6a3-129">-WorkspaceName</span></span>
<span data-ttu-id="6e6a3-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="6e6a3-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6e6a3-131">-Confirm</span></span>
<span data-ttu-id="6e6a3-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e6a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e6a3-133">-WhatIf</span></span>
<span data-ttu-id="6e6a3-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e6a3-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e6a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e6a3-136">CommonParameters</span></span>
<span data-ttu-id="6e6a3-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e6a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e6a3-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e6a3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e6a3-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6e6a3-139">INPUTS</span></span>

### <span data-ttu-id="6e6a3-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6e6a3-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6e6a3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6e6a3-141">System.String</span></span>

### <span data-ttu-id="6e6a3-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="6e6a3-142">System.String[]</span></span>

### <span data-ttu-id="6e6a3-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6e6a3-143">System.Int32</span></span>

## <span data-ttu-id="6e6a3-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6e6a3-144">OUTPUTS</span></span>

### <span data-ttu-id="6e6a3-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="6e6a3-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="6e6a3-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="6e6a3-146">NOTES</span></span>

## <span data-ttu-id="6e6a3-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6e6a3-147">RELATED LINKS</span></span>

[<span data-ttu-id="6e6a3-148">Deaktivieren-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="6e6a3-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="6e6a3-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="6e6a3-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)



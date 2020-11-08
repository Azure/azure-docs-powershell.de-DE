---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004707"
---
# <span data-ttu-id="c2603-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="c2603-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="c2603-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2603-102">SYNOPSIS</span></span>
<span data-ttu-id="c2603-103">Fügt eine Windows-Leistungsindikator-Datenquelle für verbundene Computer hinzu, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2603-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="c2603-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2603-104">SYNTAX</span></span>

### <span data-ttu-id="c2603-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2603-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2603-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c2603-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2603-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2603-107">DESCRIPTION</span></span>
<span data-ttu-id="c2603-108">Mit dem Cmdlet **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** wird eine Windows-Leistungsindikator-Datenquelle für verbundene Computer hinzugefügt, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2603-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="c2603-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2603-109">EXAMPLES</span></span>

## <span data-ttu-id="c2603-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2603-110">PARAMETERS</span></span>

### <span data-ttu-id="c2603-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="c2603-111">-CounterName</span></span>
<span data-ttu-id="c2603-112">Gibt den Namen eines Indikators an.</span><span class="sxs-lookup"><span data-stu-id="c2603-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2603-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2603-113">-DefaultProfile</span></span>
<span data-ttu-id="c2603-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c2603-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2603-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c2603-115">-Force</span></span>
<span data-ttu-id="c2603-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="c2603-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2603-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2603-117">-InstanceName</span></span>
<span data-ttu-id="c2603-118">Gibt den Namen einer Instanz an.</span><span class="sxs-lookup"><span data-stu-id="c2603-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="c2603-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c2603-119">-IntervalSeconds</span></span>
<span data-ttu-id="c2603-120">Gibt das Intervall der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="c2603-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="c2603-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c2603-121">-Name</span></span>
<span data-ttu-id="c2603-122">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="c2603-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="c2603-123">-Objektname</span><span class="sxs-lookup"><span data-stu-id="c2603-123">-ObjectName</span></span>
<span data-ttu-id="c2603-124">Gibt den Namen eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="c2603-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="c2603-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2603-125">-ResourceGroupName</span></span>
<span data-ttu-id="c2603-126">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="c2603-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="c2603-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="c2603-127">-UseLegacyCollector</span></span>
<span data-ttu-id="c2603-128">Verwenden Sie den Legacy-Kollektor oder den Standard Kollektor.</span><span class="sxs-lookup"><span data-stu-id="c2603-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="c2603-129">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="c2603-129">-Workspace</span></span>
<span data-ttu-id="c2603-130">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c2603-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2603-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c2603-131">-WorkspaceName</span></span>
<span data-ttu-id="c2603-132">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c2603-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c2603-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2603-133">-Confirm</span></span>
<span data-ttu-id="c2603-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2603-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2603-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2603-135">-WhatIf</span></span>
<span data-ttu-id="c2603-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2603-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2603-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2603-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2603-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2603-138">CommonParameters</span></span>
<span data-ttu-id="c2603-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2603-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2603-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2603-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2603-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2603-141">INPUTS</span></span>

### <span data-ttu-id="c2603-142">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c2603-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c2603-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c2603-143">System.String</span></span>

### <span data-ttu-id="c2603-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c2603-144">System.Int32</span></span>

## <span data-ttu-id="c2603-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2603-145">OUTPUTS</span></span>

### <span data-ttu-id="c2603-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c2603-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c2603-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2603-147">NOTES</span></span>

## <span data-ttu-id="c2603-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2603-148">RELATED LINKS</span></span>

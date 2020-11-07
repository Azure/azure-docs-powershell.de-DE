---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 4230eadc005ca53600feb2e6bc7ee2e001d7b209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660048"
---
# <span data-ttu-id="7c124-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7c124-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="7c124-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c124-102">SYNOPSIS</span></span>
<span data-ttu-id="7c124-103">Sammelt Ereignisprotokolle von Computern, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c124-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="7c124-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c124-104">SYNTAX</span></span>

### <span data-ttu-id="7c124-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c124-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c124-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7c124-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c124-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c124-107">DESCRIPTION</span></span>
<span data-ttu-id="7c124-108">Das Cmdlet **New-AzOperationalInsightsWindowsEventDataSource** fügt eine Datenquelle hinzu, die Windows-Ereignisprotokolle von verbundenen Computern, auf denen das BetriebssystemWindows ausgeführt wird, in Azure Operating Insights sammelt.</span><span class="sxs-lookup"><span data-stu-id="7c124-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="7c124-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c124-109">EXAMPLES</span></span>

## <span data-ttu-id="7c124-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c124-110">PARAMETERS</span></span>

### <span data-ttu-id="7c124-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="7c124-111">-CollectErrors</span></span>
<span data-ttu-id="7c124-112">Gibt an, dass operative Einblicke Fehlermeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="7c124-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="7c124-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="7c124-113">-CollectInformation</span></span>
<span data-ttu-id="7c124-114">Gibt an, dass operative Einblicke Informationsnachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="7c124-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="7c124-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="7c124-115">-CollectWarnings</span></span>
<span data-ttu-id="7c124-116">Gibt an, dass operative Einblicke Warnmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="7c124-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="7c124-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c124-117">-DefaultProfile</span></span>
<span data-ttu-id="7c124-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7c124-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c124-119">-Eventlogname</span><span class="sxs-lookup"><span data-stu-id="7c124-119">-EventLogName</span></span>
<span data-ttu-id="7c124-120">Gibt den Namen des Ereignisprotokolls an.</span><span class="sxs-lookup"><span data-stu-id="7c124-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="7c124-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7c124-121">-Force</span></span>
<span data-ttu-id="7c124-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7c124-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c124-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7c124-123">-Name</span></span>
<span data-ttu-id="7c124-124">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="7c124-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="7c124-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c124-125">-ResourceGroupName</span></span>
<span data-ttu-id="7c124-126">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="7c124-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="7c124-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7c124-127">-Workspace</span></span>
<span data-ttu-id="7c124-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7c124-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7c124-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c124-129">-WorkspaceName</span></span>
<span data-ttu-id="7c124-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7c124-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="7c124-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c124-131">-Confirm</span></span>
<span data-ttu-id="7c124-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c124-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c124-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c124-133">-WhatIf</span></span>
<span data-ttu-id="7c124-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c124-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c124-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c124-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c124-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c124-136">CommonParameters</span></span>
<span data-ttu-id="7c124-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c124-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c124-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c124-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c124-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c124-139">INPUTS</span></span>

### <span data-ttu-id="7c124-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7c124-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7c124-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7c124-141">System.String</span></span>

## <span data-ttu-id="7c124-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c124-142">OUTPUTS</span></span>

### <span data-ttu-id="7c124-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="7c124-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="7c124-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c124-144">NOTES</span></span>

## <span data-ttu-id="7c124-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c124-145">RELATED LINKS</span></span>

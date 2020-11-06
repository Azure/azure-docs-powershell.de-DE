---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5f3200459cbcca9806a1a7185798889b3457760d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498234"
---
# <span data-ttu-id="155cc-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="155cc-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="155cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="155cc-102">SYNOPSIS</span></span>
<span data-ttu-id="155cc-103">Sammelt Ereignisprotokolle von Computern, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="155cc-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="155cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="155cc-104">SYNTAX</span></span>

### <span data-ttu-id="155cc-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="155cc-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="155cc-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="155cc-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="155cc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="155cc-107">DESCRIPTION</span></span>
<span data-ttu-id="155cc-108">Das Cmdlet **New-AzureRmOperationalInsightsWindowsEventDataSource** fügt eine Datenquelle hinzu, die Windows-Ereignisprotokolle von verbundenen Computern, auf denen das BetriebssystemWindows ausgeführt wird, in Azure Operating Insights sammelt.</span><span class="sxs-lookup"><span data-stu-id="155cc-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="155cc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="155cc-109">EXAMPLES</span></span>

## <span data-ttu-id="155cc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="155cc-110">PARAMETERS</span></span>

### <span data-ttu-id="155cc-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="155cc-111">-CollectErrors</span></span>
<span data-ttu-id="155cc-112">Gibt an, dass operative Einblicke Fehlermeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="155cc-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="155cc-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="155cc-113">-CollectInformation</span></span>
<span data-ttu-id="155cc-114">Gibt an, dass operative Einblicke Informationsnachrichten sammelt.</span><span class="sxs-lookup"><span data-stu-id="155cc-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="155cc-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="155cc-115">-CollectWarnings</span></span>
<span data-ttu-id="155cc-116">Gibt an, dass operative Einblicke Warnmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="155cc-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="155cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155cc-117">-DefaultProfile</span></span>
<span data-ttu-id="155cc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="155cc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="155cc-119">-Eventlogname</span><span class="sxs-lookup"><span data-stu-id="155cc-119">-EventLogName</span></span>
<span data-ttu-id="155cc-120">Gibt den Namen des Ereignisprotokolls an.</span><span class="sxs-lookup"><span data-stu-id="155cc-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="155cc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="155cc-121">-Force</span></span>
<span data-ttu-id="155cc-122">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="155cc-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="155cc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="155cc-123">-Name</span></span>
<span data-ttu-id="155cc-124">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="155cc-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="155cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="155cc-126">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="155cc-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="155cc-127">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="155cc-127">-Workspace</span></span>
<span data-ttu-id="155cc-128">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="155cc-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="155cc-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="155cc-129">-WorkspaceName</span></span>
<span data-ttu-id="155cc-130">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="155cc-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="155cc-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="155cc-131">-Confirm</span></span>
<span data-ttu-id="155cc-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="155cc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="155cc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="155cc-133">-WhatIf</span></span>
<span data-ttu-id="155cc-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="155cc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="155cc-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="155cc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="155cc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155cc-136">CommonParameters</span></span>
<span data-ttu-id="155cc-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="155cc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155cc-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="155cc-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155cc-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="155cc-139">INPUTS</span></span>

### <span data-ttu-id="155cc-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="155cc-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="155cc-141">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="155cc-141">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="155cc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="155cc-142">System.String</span></span>

## <span data-ttu-id="155cc-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="155cc-143">OUTPUTS</span></span>

### <span data-ttu-id="155cc-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="155cc-144">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="155cc-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="155cc-145">NOTES</span></span>

## <span data-ttu-id="155cc-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="155cc-146">RELATED LINKS</span></span>

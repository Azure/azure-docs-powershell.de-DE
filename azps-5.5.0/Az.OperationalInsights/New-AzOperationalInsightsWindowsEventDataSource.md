---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 5d7c10227876c2ee5b8eeab12623457be0f64aa8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100151313"
---
# <span data-ttu-id="45440-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="45440-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="45440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45440-102">SYNOPSIS</span></span>
<span data-ttu-id="45440-103">Sammelt Ereignisprotokolle von Computern, auf denen das Betriebssystem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45440-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="45440-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45440-104">SYNTAX</span></span>

### <span data-ttu-id="45440-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="45440-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45440-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="45440-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45440-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45440-107">DESCRIPTION</span></span>
<span data-ttu-id="45440-108">Das **Cmdlet "New-AzOperationalInsightsWindowsEventDataSource"** fügt eine Datenquelle hinzu, die die Windows-Ereignisprotokolle von verbundenen Computern sammelt, auf denen das Betriebssystem Windows in Azure Operational Insights ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45440-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="45440-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45440-109">EXAMPLES</span></span>

### <span data-ttu-id="45440-110">Beispiel 1: Erstellen einer System-Windows-Ereignisdatenquelle</span><span class="sxs-lookup"><span data-stu-id="45440-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="45440-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45440-111">PARAMETERS</span></span>

### <span data-ttu-id="45440-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="45440-112">-CollectErrors</span></span>
<span data-ttu-id="45440-113">Zeigt an, dass Operational Insights Fehlermeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="45440-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="45440-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="45440-114">-CollectInformation</span></span>
<span data-ttu-id="45440-115">Gibt an, dass operationale Einblicke Informationsmeldungen sammeln.</span><span class="sxs-lookup"><span data-stu-id="45440-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="45440-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="45440-116">-CollectWarnings</span></span>
<span data-ttu-id="45440-117">Gibt an, dass operationale Einblicke Warnmeldungen sammelt.</span><span class="sxs-lookup"><span data-stu-id="45440-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="45440-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45440-118">-DefaultProfile</span></span>
<span data-ttu-id="45440-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="45440-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45440-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="45440-120">-EventLogName</span></span>
<span data-ttu-id="45440-121">Gibt den Namen des Ereignisprotokolls an.</span><span class="sxs-lookup"><span data-stu-id="45440-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="45440-122">-Force</span><span class="sxs-lookup"><span data-stu-id="45440-122">-Force</span></span>
<span data-ttu-id="45440-123">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="45440-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45440-124">-Name</span><span class="sxs-lookup"><span data-stu-id="45440-124">-Name</span></span>
<span data-ttu-id="45440-125">Gibt einen Namen für die Datenquelle an.</span><span class="sxs-lookup"><span data-stu-id="45440-125">Specifies a name for the data source.</span></span> <span data-ttu-id="45440-126">Der Name wird nicht im Azure Portal verfügbar gemacht, und es kann eine beliebige Zeichenfolge verwendet werden, solange er eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="45440-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="45440-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45440-127">-ResourceGroupName</span></span>
<span data-ttu-id="45440-128">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="45440-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="45440-129">-Workspace</span><span class="sxs-lookup"><span data-stu-id="45440-129">-Workspace</span></span>
<span data-ttu-id="45440-130">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="45440-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="45440-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="45440-131">-WorkspaceName</span></span>
<span data-ttu-id="45440-132">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet betrieben wird.</span><span class="sxs-lookup"><span data-stu-id="45440-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="45440-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45440-133">-Confirm</span></span>
<span data-ttu-id="45440-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45440-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45440-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="45440-135">-WhatIf</span></span>
<span data-ttu-id="45440-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45440-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45440-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45440-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45440-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45440-138">CommonParameters</span></span>
<span data-ttu-id="45440-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45440-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45440-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45440-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45440-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45440-141">INPUTS</span></span>

### <span data-ttu-id="45440-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="45440-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="45440-143">System.String</span><span class="sxs-lookup"><span data-stu-id="45440-143">System.String</span></span>

## <span data-ttu-id="45440-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45440-144">OUTPUTS</span></span>

### <span data-ttu-id="45440-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="45440-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="45440-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45440-146">NOTES</span></span>

## <span data-ttu-id="45440-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45440-147">RELATED LINKS</span></span>

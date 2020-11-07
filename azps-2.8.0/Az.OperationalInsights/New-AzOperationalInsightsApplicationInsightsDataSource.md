---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 23b3816615f4f546987b87059b651f9a281ab70e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824096"
---
# <span data-ttu-id="b6621-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b6621-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="b6621-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b6621-102">SYNOPSIS</span></span>
<span data-ttu-id="b6621-103">Sammeln von Protokollen von angegebenen Application-Insights Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6621-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="b6621-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b6621-104">SYNTAX</span></span>

### <span data-ttu-id="b6621-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b6621-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6621-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="b6621-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6621-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="b6621-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6621-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="b6621-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6621-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="b6621-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b6621-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b6621-110">DESCRIPTION</span></span>
<span data-ttu-id="b6621-111">Das Cmdlet **New-AzOperationalInsightsApplicationInsightsDataSource** ermöglicht die Sammlung von Protokollen aus einer bestimmten Application-Insights Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6621-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="b6621-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b6621-112">EXAMPLES</span></span>

### <span data-ttu-id="b6621-113">Beispiel 1: Erstellen von Anwendungsdatenquellen im Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="b6621-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="b6621-114">Mit diesem Befehl wird eine Anwendung-Insights-Datenquelle für eine bestimmte Anwendung in einem bestimmten Arbeitsbereich der Protokollanalyse erstellt.</span><span class="sxs-lookup"><span data-stu-id="b6621-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="b6621-115">Dadurch kann die Sammlung von Protokollen aus der angegebenen Anwendung in den Arbeitsbereich der Protokollanalyse übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="b6621-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="b6621-116">Beispiel 2: Abrufen des Arbeitsbereichsobjekts und Erstellen der Datenquelle für Anwendungs Einblicke durch die Anwendungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="b6621-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="b6621-117">Dieser Befehl zeigt, wie Sie ein Protokollanalyse-Workspace-Objekt abrufen und dann die Ausgabe übergeben, um eine zugeordnete Anwendung-Insights-Datenquelle durch die Anwendungsressourcen-ID zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6621-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="b6621-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b6621-118">PARAMETERS</span></span>

### <span data-ttu-id="b6621-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b6621-119">-ApplicationName</span></span>
<span data-ttu-id="b6621-120">Der Name der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6621-120">The name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6621-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="b6621-122">Der Ressourcengruppenname der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6621-122">The resource group name of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="b6621-123">-ApplicationResourceId</span></span>
<span data-ttu-id="b6621-124">Die Ressourcen-ID der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6621-124">The linked application resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationResourceId, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6621-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="b6621-126">Die Abonnement-ID der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b6621-126">The subscription id of the linked application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceNameByApplicationParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6621-127">-DefaultProfile</span></span>
<span data-ttu-id="b6621-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b6621-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6621-129">-Force</span><span class="sxs-lookup"><span data-stu-id="b6621-129">-Force</span></span>
<span data-ttu-id="b6621-130">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="b6621-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b6621-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6621-131">-ResourceGroupName</span></span>
<span data-ttu-id="b6621-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b6621-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-133">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="b6621-133">-Workspace</span></span>
<span data-ttu-id="b6621-134">Der Arbeitsbereich, der die Datenquelle enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="b6621-134">The workspace that will contain the data source.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByApplicationParameters, ByWorkspaceObjectByApplicationResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b6621-135">-WorkspaceName</span></span>
<span data-ttu-id="b6621-136">Der Name des Arbeitsbereichs, der die Datenquelle enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="b6621-136">The name of the workspace that will contain the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByApplicationParameters, ByWorkspaceNameByApplicationResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6621-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b6621-137">-Confirm</span></span>
<span data-ttu-id="b6621-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b6621-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6621-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6621-139">-WhatIf</span></span>
<span data-ttu-id="b6621-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b6621-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6621-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b6621-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6621-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6621-142">CommonParameters</span></span>
<span data-ttu-id="b6621-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6621-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6621-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6621-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6621-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b6621-145">INPUTS</span></span>

### <span data-ttu-id="b6621-146">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b6621-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b6621-147">System. String</span><span class="sxs-lookup"><span data-stu-id="b6621-147">System.String</span></span>

## <span data-ttu-id="b6621-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b6621-148">OUTPUTS</span></span>

### <span data-ttu-id="b6621-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b6621-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b6621-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="b6621-150">NOTES</span></span>

## <span data-ttu-id="b6621-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b6621-151">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E3D7A3FE-40D4-4495-BA39-493F85F304AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsapplicationinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsApplicationInsightsDataSource.md
ms.openlocfilehash: 0f238a417ac83cac82305ceb9c9ce20586328976
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172326"
---
# <span data-ttu-id="c0880-101">New-AzOperationalInsightsApplicationInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="c0880-101">New-AzOperationalInsightsApplicationInsightsDataSource</span></span>

## <span data-ttu-id="c0880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0880-102">SYNOPSIS</span></span>
<span data-ttu-id="c0880-103">Erfassen Sie Protokolle aus einer Application-Insights Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c0880-103">Collect logs from given Application-Insights application.</span></span>

## <span data-ttu-id="c0880-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0880-104">SYNTAX</span></span>

### <span data-ttu-id="c0880-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0880-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0880-106">ByWorkspaceObjectByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="c0880-106">ByWorkspaceObjectByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0880-107">ByWorkspaceObjectByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="c0880-107">ByWorkspaceObjectByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-Workspace] <PSWorkspace>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0880-108">ByWorkspaceNameByApplicationParameters</span><span class="sxs-lookup"><span data-stu-id="c0880-108">ByWorkspaceNameByApplicationParameters</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationSubscriptionId <String> -ApplicationResourceGroupName <String> -ApplicationName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0880-109">ByWorkspaceNameByApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="c0880-109">ByWorkspaceNameByApplicationResourceId</span></span>
```
New-AzOperationalInsightsApplicationInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 -ApplicationResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0880-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0880-110">DESCRIPTION</span></span>
<span data-ttu-id="c0880-111">Das **Cmdlet "New-AzOperationalInsightsApplicationInsightsDataSource"** ermöglicht die Sammlung von Protokollen aus einer bestimmten Application-Insights Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c0880-111">The **New-AzOperationalInsightsApplicationInsightsDataSource** cmdlet enables the collection of logs from a given Application-Insights application.</span></span>

## <span data-ttu-id="c0880-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0880-112">EXAMPLES</span></span>

### <span data-ttu-id="c0880-113">Beispiel 1: Erstellen einer Datenquelle für Anwendungseinblicke im Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="c0880-113">Example 1: Create application-insights data source in workspace</span></span>
```
PS C:\> New-AzOperationalInsightsApplicationInsightsDataSource -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -ApplicationSubscriptionId "e791a474-ee54-46a2-bb06-5e058302d234" -ApplicationResourceGroupName "ContosoResourceGroup" -ApplicationName "MyAIApplication"

Name              : subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="c0880-114">Mit diesem Befehl wird eine Datenquelle für Anwendungserkenntnisse einer bestimmten Anwendung in einem bestimmten Protokollanalysearbeitsbereich erstellt.</span><span class="sxs-lookup"><span data-stu-id="c0880-114">This command creates an application-insights data source of a given application in a given log analytics workspace.</span></span> <span data-ttu-id="c0880-115">Dies ermöglicht die Sammlung von Protokollen aus einer bestimmten Anwendung in den Protokollanalysearbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="c0880-115">This enables the collection of logs from given application to the log analytics workspace.</span></span>

### <span data-ttu-id="c0880-116">Beispiel 2: Erhalten eines Arbeitsbereichsobjekts und Erstellen einer Datenquelle für Anwendungseinblicke mit der Anwendungsressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c0880-116">Example 2: Get workspace object and create application-insights data source by the application resource id</span></span>
```
PS C:\> Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup" | New-AzOperationalInsightsApplicationInsightsDataSource -ApplicationResourceId "/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication"

Name              : subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
ResourceGroupName : ContosoResourceGroup
WorkspaceName     : MyWorkspace
ResourceId        : /subscriptions/aaaaa474-ee54-4aaa-bb06-5e058302daaa/resourceGroups/ContosoResourceGroup/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace/datasources/subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication
Kind              : ApplicationInsights
Properties        : {"linkedResourceId":"subscriptions/e791a474-ee54-46a2-bb06-5e058302d234/resourceGroups/ContosoResourceGroup/providers/microsoft.insights/components/MyAIApplication","status":"Succeeded"}

```

<span data-ttu-id="c0880-117">Dieser Befehl veranschaulicht das Abrufen eines Log analytics-Arbeitsbereichsobjekts und das anschließende Übergeben der Ausgabe zum Erstellen einer zugeordneten Datenquelle für Anwendungseinblicke durch die Anwendungsressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c0880-117">This command demonstrates getting a log analytics workspace object and then passing the output to create an associated application-insights data source by the application resource id.</span></span> 

## <span data-ttu-id="c0880-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0880-118">PARAMETERS</span></span>

### <span data-ttu-id="c0880-119">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="c0880-119">-ApplicationName</span></span>
<span data-ttu-id="c0880-120">Der Name der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c0880-120">The name of the linked application.</span></span>

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

### <span data-ttu-id="c0880-121">-ApplicationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0880-121">-ApplicationResourceGroupName</span></span>
<span data-ttu-id="c0880-122">Der Ressourcengruppenname der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c0880-122">The resource group name of the linked application.</span></span>

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

### <span data-ttu-id="c0880-123">-ApplicationResourceId</span><span class="sxs-lookup"><span data-stu-id="c0880-123">-ApplicationResourceId</span></span>
<span data-ttu-id="c0880-124">Die verknüpfte Anwendungsressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c0880-124">The linked application resource id.</span></span>

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

### <span data-ttu-id="c0880-125">-ApplicationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0880-125">-ApplicationSubscriptionId</span></span>
<span data-ttu-id="c0880-126">Die Abonnement-ID der verknüpften Anwendung.</span><span class="sxs-lookup"><span data-stu-id="c0880-126">The subscription id of the linked application.</span></span>

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

### <span data-ttu-id="c0880-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0880-127">-DefaultProfile</span></span>
<span data-ttu-id="c0880-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0880-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0880-129">-Force</span><span class="sxs-lookup"><span data-stu-id="c0880-129">-Force</span></span>
<span data-ttu-id="c0880-130">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="c0880-130">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c0880-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0880-131">-ResourceGroupName</span></span>
<span data-ttu-id="c0880-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c0880-132">The resource group name.</span></span>

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

### <span data-ttu-id="c0880-133">-Workspace</span><span class="sxs-lookup"><span data-stu-id="c0880-133">-Workspace</span></span>
<span data-ttu-id="c0880-134">Der Arbeitsbereich, der die Datenquelle enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="c0880-134">The workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="c0880-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0880-135">-WorkspaceName</span></span>
<span data-ttu-id="c0880-136">Der Name des Arbeitsbereichs, der die Datenquelle enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="c0880-136">The name of the workspace that will contain the data source.</span></span>

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

### <span data-ttu-id="c0880-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0880-137">-Confirm</span></span>
<span data-ttu-id="c0880-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0880-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0880-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c0880-139">-WhatIf</span></span>
<span data-ttu-id="c0880-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0880-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0880-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0880-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0880-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0880-142">CommonParameters</span></span>
<span data-ttu-id="c0880-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0880-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0880-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0880-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0880-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0880-145">INPUTS</span></span>

### <span data-ttu-id="c0880-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0880-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c0880-147">System.String</span><span class="sxs-lookup"><span data-stu-id="c0880-147">System.String</span></span>

## <span data-ttu-id="c0880-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0880-148">OUTPUTS</span></span>

### <span data-ttu-id="c0880-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c0880-149">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c0880-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c0880-150">NOTES</span></span>

## <span data-ttu-id="c0880-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c0880-151">RELATED LINKS</span></span>

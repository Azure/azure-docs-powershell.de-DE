---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378620"
---
# <span data-ttu-id="4752d-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="4752d-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="4752d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4752d-102">SYNOPSIS</span></span>
<span data-ttu-id="4752d-103">Linkdienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="4752d-103">link service for workspace</span></span>

## <span data-ttu-id="4752d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4752d-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4752d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4752d-105">DESCRIPTION</span></span>
<span data-ttu-id="4752d-106">Linkdienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="4752d-106">link service for workspace</span></span>

## <span data-ttu-id="4752d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4752d-107">EXAMPLES</span></span>

### <span data-ttu-id="4752d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4752d-108">Example 1</span></span>
```powershell
Set-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster -WriteAccessResourceId /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="4752d-109">Verknüpfungscluster für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="4752d-109">link cluster for workspace</span></span>

## <span data-ttu-id="4752d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4752d-110">PARAMETERS</span></span>

### <span data-ttu-id="4752d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4752d-111">-AsJob</span></span>
<span data-ttu-id="4752d-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4752d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4752d-113">-DefaultProfile</span></span>
<span data-ttu-id="4752d-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4752d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="4752d-115">-LinkedServiceName</span></span>
<span data-ttu-id="4752d-116">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4752d-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4752d-117">-ResourceGroupName</span></span>
<span data-ttu-id="4752d-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4752d-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4752d-119">-ResourceId</span></span>
<span data-ttu-id="4752d-120">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="4752d-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="4752d-121">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, die Lesezugriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="4752d-121">This should be used for linking resources which require read access</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-122">-Tags</span><span class="sxs-lookup"><span data-stu-id="4752d-122">-Tags</span></span>
<span data-ttu-id="4752d-123">Tags.</span><span class="sxs-lookup"><span data-stu-id="4752d-123">Tags.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4752d-124">-WorkspaceName</span></span>
<span data-ttu-id="4752d-125">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="4752d-125">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="4752d-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="4752d-127">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="4752d-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="4752d-128">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, die Schreibzugriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="4752d-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="4752d-129">Cluster muss über den Bereitstellungszustand "Succeeded" und gültige Keyvault-Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="4752d-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4752d-130">-Confirm</span></span>
<span data-ttu-id="4752d-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4752d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4752d-132">-WhatIf</span></span>
<span data-ttu-id="4752d-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4752d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4752d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4752d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4752d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4752d-135">CommonParameters</span></span>
<span data-ttu-id="4752d-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4752d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4752d-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4752d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4752d-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4752d-138">INPUTS</span></span>

### <span data-ttu-id="4752d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4752d-139">System.String</span></span>

## <span data-ttu-id="4752d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4752d-140">OUTPUTS</span></span>

### <span data-ttu-id="4752d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="4752d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="4752d-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4752d-142">NOTES</span></span>

## <span data-ttu-id="4752d-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4752d-143">RELATED LINKS</span></span>

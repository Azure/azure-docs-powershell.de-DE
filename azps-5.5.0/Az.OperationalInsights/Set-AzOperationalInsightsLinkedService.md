---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153940"
---
# <span data-ttu-id="a4cec-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="a4cec-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="a4cec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4cec-102">SYNOPSIS</span></span>
<span data-ttu-id="a4cec-103">Linkdienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a4cec-103">link service for workspace</span></span>

## <span data-ttu-id="a4cec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a4cec-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4cec-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4cec-105">DESCRIPTION</span></span>
<span data-ttu-id="a4cec-106">Linkdienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a4cec-106">link service for workspace</span></span>

## <span data-ttu-id="a4cec-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a4cec-107">EXAMPLES</span></span>

### <span data-ttu-id="a4cec-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a4cec-108">Example 1</span></span>
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

<span data-ttu-id="a4cec-109">Verknüpfungscluster für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a4cec-109">link cluster for workspace</span></span>

## <span data-ttu-id="a4cec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4cec-110">PARAMETERS</span></span>

### <span data-ttu-id="a4cec-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4cec-111">-AsJob</span></span>
<span data-ttu-id="a4cec-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a4cec-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4cec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4cec-113">-DefaultProfile</span></span>
<span data-ttu-id="a4cec-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4cec-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4cec-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="a4cec-115">-LinkedServiceName</span></span>
<span data-ttu-id="a4cec-116">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a4cec-116">The Workspace name.</span></span>

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

### <span data-ttu-id="a4cec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4cec-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4cec-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a4cec-118">The resource group name.</span></span>

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

### <span data-ttu-id="a4cec-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cec-119">-ResourceId</span></span>
<span data-ttu-id="a4cec-120">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4cec-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="a4cec-121">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, die Lesezugriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="a4cec-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="a4cec-122">-Tags</span><span class="sxs-lookup"><span data-stu-id="a4cec-122">-Tags</span></span>
<span data-ttu-id="a4cec-123">Tags.</span><span class="sxs-lookup"><span data-stu-id="a4cec-123">Tags.</span></span>

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

### <span data-ttu-id="a4cec-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a4cec-124">-WorkspaceName</span></span>
<span data-ttu-id="a4cec-125">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="a4cec-125">The Workspace name.</span></span>

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

### <span data-ttu-id="a4cec-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="a4cec-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="a4cec-127">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="a4cec-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="a4cec-128">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, die Schreibzugriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="a4cec-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="a4cec-129">Cluster muss über den Bereitstellungszustand "Succeeded" und gültige Keyvault-Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="a4cec-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="a4cec-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4cec-130">-Confirm</span></span>
<span data-ttu-id="a4cec-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a4cec-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4cec-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a4cec-132">-WhatIf</span></span>
<span data-ttu-id="a4cec-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4cec-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4cec-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a4cec-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4cec-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4cec-135">CommonParameters</span></span>
<span data-ttu-id="a4cec-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4cec-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4cec-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4cec-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4cec-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a4cec-138">INPUTS</span></span>

### <span data-ttu-id="a4cec-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a4cec-139">System.String</span></span>

## <span data-ttu-id="a4cec-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a4cec-140">OUTPUTS</span></span>

### <span data-ttu-id="a4cec-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="a4cec-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="a4cec-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a4cec-142">NOTES</span></span>

## <span data-ttu-id="a4cec-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a4cec-143">RELATED LINKS</span></span>

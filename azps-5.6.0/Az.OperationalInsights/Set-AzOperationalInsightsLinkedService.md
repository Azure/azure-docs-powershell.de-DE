---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 141723a0e920f18aed9808ed3c5f205534c48185
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937864"
---
# <span data-ttu-id="74842-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="74842-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="74842-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74842-102">SYNOPSIS</span></span>
<span data-ttu-id="74842-103">Linkdienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="74842-103">link service for workspace</span></span>

## <span data-ttu-id="74842-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74842-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74842-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74842-105">DESCRIPTION</span></span>
<span data-ttu-id="74842-106">Linkdienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="74842-106">link service for workspace</span></span>

## <span data-ttu-id="74842-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="74842-107">EXAMPLES</span></span>

### <span data-ttu-id="74842-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74842-108">Example 1</span></span>
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

<span data-ttu-id="74842-109">Linkcluster für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="74842-109">link cluster for workspace</span></span>

## <span data-ttu-id="74842-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="74842-110">PARAMETERS</span></span>

### <span data-ttu-id="74842-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74842-111">-AsJob</span></span>
<span data-ttu-id="74842-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="74842-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74842-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74842-113">-DefaultProfile</span></span>
<span data-ttu-id="74842-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74842-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74842-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="74842-115">-LinkedServiceName</span></span>
<span data-ttu-id="74842-116">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="74842-116">The Workspace name.</span></span>

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

### <span data-ttu-id="74842-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74842-117">-ResourceGroupName</span></span>
<span data-ttu-id="74842-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="74842-118">The resource group name.</span></span>

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

### <span data-ttu-id="74842-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74842-119">-ResourceId</span></span>
<span data-ttu-id="74842-120">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="74842-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="74842-121">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, die Lesezugriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="74842-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="74842-122">-Tags</span><span class="sxs-lookup"><span data-stu-id="74842-122">-Tags</span></span>
<span data-ttu-id="74842-123">Tags.</span><span class="sxs-lookup"><span data-stu-id="74842-123">Tags.</span></span>

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

### <span data-ttu-id="74842-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74842-124">-WorkspaceName</span></span>
<span data-ttu-id="74842-125">Der Name des Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="74842-125">The Workspace name.</span></span>

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

### <span data-ttu-id="74842-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="74842-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="74842-127">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="74842-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="74842-128">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, die Schreibzugriff erfordern.</span><span class="sxs-lookup"><span data-stu-id="74842-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="74842-129">Cluster muss über den Bereitstellungszustand "Erfolgreich" und gültige Keyvaulteigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="74842-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="74842-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="74842-130">-Confirm</span></span>
<span data-ttu-id="74842-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="74842-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74842-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74842-132">-WhatIf</span></span>
<span data-ttu-id="74842-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="74842-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74842-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="74842-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74842-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74842-135">CommonParameters</span></span>
<span data-ttu-id="74842-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74842-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74842-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74842-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74842-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="74842-138">INPUTS</span></span>

### <span data-ttu-id="74842-139">System.String</span><span class="sxs-lookup"><span data-stu-id="74842-139">System.String</span></span>

## <span data-ttu-id="74842-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="74842-140">OUTPUTS</span></span>

### <span data-ttu-id="74842-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="74842-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="74842-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="74842-142">NOTES</span></span>

## <span data-ttu-id="74842-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="74842-143">RELATED LINKS</span></span>

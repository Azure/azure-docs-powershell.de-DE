---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 3535cc8956643351a6637134cc7dcdd805ed80c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178284"
---
# <span data-ttu-id="f5944-101">Set-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5944-101">Set-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="f5944-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5944-102">SYNOPSIS</span></span>
<span data-ttu-id="f5944-103">Link Dienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f5944-103">link service for workspace</span></span>

## <span data-ttu-id="f5944-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5944-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-Tags <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-WriteAccessResourceId <String>] [-ResourceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5944-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5944-105">DESCRIPTION</span></span>
<span data-ttu-id="f5944-106">Link Dienst für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f5944-106">link service for workspace</span></span>

## <span data-ttu-id="f5944-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5944-107">EXAMPLES</span></span>

### <span data-ttu-id="f5944-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5944-108">Example 1</span></span>
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

<span data-ttu-id="f5944-109">Link Cluster für Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="f5944-109">link cluster for workspace</span></span>

## <span data-ttu-id="f5944-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5944-110">PARAMETERS</span></span>

### <span data-ttu-id="f5944-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5944-111">-AsJob</span></span>
<span data-ttu-id="f5944-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f5944-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5944-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5944-113">-DefaultProfile</span></span>
<span data-ttu-id="f5944-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5944-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5944-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="f5944-115">-LinkedServiceName</span></span>
<span data-ttu-id="f5944-116">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="f5944-116">The Workspace name.</span></span>

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

### <span data-ttu-id="f5944-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5944-117">-ResourceGroupName</span></span>
<span data-ttu-id="f5944-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f5944-118">The resource group name.</span></span>

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

### <span data-ttu-id="f5944-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f5944-119">-ResourceId</span></span>
<span data-ttu-id="f5944-120">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5944-120">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="f5944-121">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, für die Lesezugriff erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f5944-121">This should be used for linking resources which require read access</span></span>

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

### <span data-ttu-id="f5944-122">-Tags</span><span class="sxs-lookup"><span data-stu-id="f5944-122">-Tags</span></span>
<span data-ttu-id="f5944-123">Tags.</span><span class="sxs-lookup"><span data-stu-id="f5944-123">Tags.</span></span>

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

### <span data-ttu-id="f5944-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f5944-124">-WorkspaceName</span></span>
<span data-ttu-id="f5944-125">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="f5944-125">The Workspace name.</span></span>

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

### <span data-ttu-id="f5944-126">-WriteAccessResourceId</span><span class="sxs-lookup"><span data-stu-id="f5944-126">-WriteAccessResourceId</span></span>
<span data-ttu-id="f5944-127">Die Ressourcen-ID der Ressource, die mit dem Arbeitsbereich verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5944-127">The resource id of the resource that will be linked to the workspace.</span></span>
<span data-ttu-id="f5944-128">Dies sollte zum Verknüpfen von Ressourcen verwendet werden, für die Schreibzugriff erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f5944-128">This should be used for linking resources which require write access.</span></span>
<span data-ttu-id="f5944-129">Für Cluster muss der Bereitstellungsstatus "erfolgreich" und die gültigen keyvault-Eigenschaften vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f5944-129">Cluster must have provisioning state "Succeeded" and valid keyvault properties.</span></span>

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

### <span data-ttu-id="f5944-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f5944-130">-Confirm</span></span>
<span data-ttu-id="f5944-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f5944-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5944-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5944-132">-WhatIf</span></span>
<span data-ttu-id="f5944-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f5944-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5944-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5944-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5944-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5944-135">CommonParameters</span></span>
<span data-ttu-id="f5944-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5944-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5944-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f5944-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5944-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5944-138">INPUTS</span></span>

### <span data-ttu-id="f5944-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f5944-139">System.String</span></span>

## <span data-ttu-id="f5944-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5944-140">OUTPUTS</span></span>

### <span data-ttu-id="f5944-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="f5944-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="f5944-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5944-142">NOTES</span></span>

## <span data-ttu-id="f5944-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5944-143">RELATED LINKS</span></span>

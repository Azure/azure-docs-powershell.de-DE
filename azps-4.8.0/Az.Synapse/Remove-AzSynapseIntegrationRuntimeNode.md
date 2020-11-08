---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: cb2c632b47e512d31a5349be9b6091a9981f5459
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010118"
---
# <span data-ttu-id="fbb44-101">Remove-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="fbb44-101">Remove-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="fbb44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbb44-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb44-103">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fbb44-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="fbb44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbb44-104">SYNTAX</span></span>

### <span data-ttu-id="fbb44-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbb44-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb44-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb44-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -NodeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbb44-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb44-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -ResourceId <String> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb44-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb44-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -NodeName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb44-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbb44-109">DESCRIPTION</span></span>
<span data-ttu-id="fbb44-110">Das Cmdlet **Remove-AzSynapseIntegrationRuntimeNode** entfernt einen Knoten in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fbb44-110">The **Remove-AzSynapseIntegrationRuntimeNode** cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="fbb44-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbb44-111">EXAMPLES</span></span>

### <span data-ttu-id="fbb44-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbb44-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="fbb44-113">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fbb44-113">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="fbb44-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbb44-114">PARAMETERS</span></span>

### <span data-ttu-id="fbb44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb44-115">-DefaultProfile</span></span>
<span data-ttu-id="fbb44-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbb44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb44-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fbb44-117">-Force</span></span>
<span data-ttu-id="fbb44-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="fbb44-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fbb44-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fbb44-119">-InputObject</span></span>
<span data-ttu-id="fbb44-120">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="fbb44-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="fbb44-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="fbb44-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fbb44-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-123">-Nodename</span><span class="sxs-lookup"><span data-stu-id="fbb44-123">-NodeName</span></span>
<span data-ttu-id="fbb44-124">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fbb44-124">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb44-125">-ResourceGroupName</span></span>
<span data-ttu-id="fbb44-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbb44-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fbb44-127">-ResourceId</span></span>
<span data-ttu-id="fbb44-128">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="fbb44-128">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fbb44-129">-WorkspaceName</span></span>
<span data-ttu-id="fbb44-130">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="fbb44-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-131">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="fbb44-131">-WorkspaceObject</span></span>
<span data-ttu-id="fbb44-132">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="fbb44-132">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb44-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fbb44-133">-Confirm</span></span>
<span data-ttu-id="fbb44-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbb44-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb44-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb44-135">-WhatIf</span></span>
<span data-ttu-id="fbb44-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbb44-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb44-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbb44-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb44-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb44-138">CommonParameters</span></span>
<span data-ttu-id="fbb44-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb44-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb44-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbb44-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb44-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbb44-141">INPUTS</span></span>

### <span data-ttu-id="fbb44-142">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="fbb44-142">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="fbb44-143">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fbb44-143">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="fbb44-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb44-144">System.String</span></span>

## <span data-ttu-id="fbb44-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbb44-145">OUTPUTS</span></span>

### <span data-ttu-id="fbb44-146">System. void</span><span class="sxs-lookup"><span data-stu-id="fbb44-146">System.Void</span></span>

## <span data-ttu-id="fbb44-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbb44-147">NOTES</span></span>

## <span data-ttu-id="fbb44-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbb44-148">RELATED LINKS</span></span>

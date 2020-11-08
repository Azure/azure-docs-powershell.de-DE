---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 57b6c6619a45e515c7aff2e30edc346ff39af9ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178120"
---
# <span data-ttu-id="54ad8-101">Remove-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="54ad8-101">Remove-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="54ad8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="54ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="54ad8-103">Entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="54ad8-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="54ad8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="54ad8-104">SYNTAX</span></span>

### <span data-ttu-id="54ad8-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="54ad8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ad8-106">RemoveByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54ad8-106">RemoveByParentObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ad8-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54ad8-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -ResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54ad8-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54ad8-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54ad8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54ad8-109">DESCRIPTION</span></span>
<span data-ttu-id="54ad8-110">Das Cmdlet **Remove-AzSynapseIntegrationRuntime** entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="54ad8-110">The **Remove-AzSynapseIntegrationRuntime** cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="54ad8-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="54ad8-111">EXAMPLES</span></span>

### <span data-ttu-id="54ad8-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54ad8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="54ad8-113">Dieser Befehl entfernt die Integrationslaufzeit mit dem Namen "Test-reservierte-IR" aus dem Arbeitsbereich mit dem Namen ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="54ad8-113">This command removes the integration runtime named 'test-reserved-ir' from the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="54ad8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="54ad8-114">PARAMETERS</span></span>

### <span data-ttu-id="54ad8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54ad8-115">-DefaultProfile</span></span>
<span data-ttu-id="54ad8-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="54ad8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54ad8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54ad8-117">-Force</span></span>
<span data-ttu-id="54ad8-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="54ad8-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="54ad8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="54ad8-119">-InputObject</span></span>
<span data-ttu-id="54ad8-120">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="54ad8-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="54ad8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="54ad8-121">-Name</span></span>
<span data-ttu-id="54ad8-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="54ad8-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet, RemoveByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54ad8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54ad8-123">-ResourceGroupName</span></span>
<span data-ttu-id="54ad8-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54ad8-124">Resource group name.</span></span>

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

### <span data-ttu-id="54ad8-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="54ad8-125">-ResourceId</span></span>
<span data-ttu-id="54ad8-126">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="54ad8-126">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="54ad8-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="54ad8-127">-WorkspaceName</span></span>
<span data-ttu-id="54ad8-128">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="54ad8-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="54ad8-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="54ad8-129">-WorkspaceObject</span></span>
<span data-ttu-id="54ad8-130">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="54ad8-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="54ad8-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54ad8-131">-Confirm</span></span>
<span data-ttu-id="54ad8-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54ad8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54ad8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54ad8-133">-WhatIf</span></span>
<span data-ttu-id="54ad8-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54ad8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54ad8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54ad8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54ad8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54ad8-136">CommonParameters</span></span>
<span data-ttu-id="54ad8-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54ad8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54ad8-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54ad8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54ad8-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="54ad8-139">INPUTS</span></span>

### <span data-ttu-id="54ad8-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="54ad8-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="54ad8-141">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="54ad8-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="54ad8-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="54ad8-142">OUTPUTS</span></span>

### <span data-ttu-id="54ad8-143">System. void</span><span class="sxs-lookup"><span data-stu-id="54ad8-143">System.Void</span></span>

## <span data-ttu-id="54ad8-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="54ad8-144">NOTES</span></span>

## <span data-ttu-id="54ad8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="54ad8-145">RELATED LINKS</span></span>

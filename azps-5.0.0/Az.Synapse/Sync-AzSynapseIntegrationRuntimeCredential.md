---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/sync-azsynapseintegrationruntimecredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Sync-AzSynapseIntegrationRuntimeCredential.md
ms.openlocfilehash: feb9d74cf49dfa8ae5455b303ee78f443a08e942
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175366"
---
# <span data-ttu-id="88f3d-101">Sync-AzSynapseIntegrationRuntimeCredential</span><span class="sxs-lookup"><span data-stu-id="88f3d-101">Sync-AzSynapseIntegrationRuntimeCredential</span></span>

## <span data-ttu-id="88f3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="88f3d-103">Synchronisiert Anmeldeinformationen zwischen Integrationslauf Zeit Knoten.</span><span class="sxs-lookup"><span data-stu-id="88f3d-103">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="88f3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88f3d-104">SYNTAX</span></span>

### <span data-ttu-id="88f3d-105">StopByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="88f3d-105">StopByNameParameterSet (Default)</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88f3d-106">StopByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f3d-106">StopByParentObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -IntegrationRuntimeName <String>
 -WorkspaceObject <PSSynapseWorkspace> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88f3d-107">StopByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f3d-107">StopByResourceIdParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -ResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88f3d-108">StopByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88f3d-108">StopByInputObjectParameterSet</span></span>
```
Sync-AzSynapseIntegrationRuntimeCredential -InputObject <PSIntegrationRuntime> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88f3d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88f3d-109">DESCRIPTION</span></span>
<span data-ttu-id="88f3d-110">Das Cmdlet " **Sync-AzSynapseIntegrationRuntimeCredential** " synchronisiert lokale Anmeldeinformationen zwischen Integrationslauf Zeit Knoten, wodurch die Anmeldeinformationen in allen Knoten identisch sind.</span><span class="sxs-lookup"><span data-stu-id="88f3d-110">The **Sync-AzSynapseIntegrationRuntimeCredential** cmdlet synchronizes on-premises credentials among integration runtime nodes, which forces the credentials to be identical in all nodes.</span></span>

## <span data-ttu-id="88f3d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88f3d-111">EXAMPLES</span></span>

### <span data-ttu-id="88f3d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88f3d-112">Example 1</span></span>
```powershell
PS C:\> Sync-AzSynapseIntegrationRuntimeCredential -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir'
```

<span data-ttu-id="88f3d-113">Synchronisiert Anmeldeinformationen zwischen Integrationslauf Zeit Knoten.</span><span class="sxs-lookup"><span data-stu-id="88f3d-113">Synchronizes credentials among integration runtime nodes.</span></span>

## <span data-ttu-id="88f3d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="88f3d-114">PARAMETERS</span></span>

### <span data-ttu-id="88f3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88f3d-115">-DefaultProfile</span></span>
<span data-ttu-id="88f3d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88f3d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88f3d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="88f3d-117">-Force</span></span>
<span data-ttu-id="88f3d-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="88f3d-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="88f3d-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88f3d-119">-InputObject</span></span>
<span data-ttu-id="88f3d-120">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="88f3d-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: StopByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88f3d-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="88f3d-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="88f3d-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="88f3d-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet, StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f3d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88f3d-123">-ResourceGroupName</span></span>
<span data-ttu-id="88f3d-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88f3d-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f3d-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="88f3d-125">-ResourceId</span></span>
<span data-ttu-id="88f3d-126">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="88f3d-126">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f3d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88f3d-127">-WorkspaceName</span></span>
<span data-ttu-id="88f3d-128">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="88f3d-128">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88f3d-129">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="88f3d-129">-WorkspaceObject</span></span>
<span data-ttu-id="88f3d-130">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="88f3d-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: StopByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88f3d-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88f3d-131">-Confirm</span></span>
<span data-ttu-id="88f3d-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88f3d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88f3d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88f3d-133">-WhatIf</span></span>
<span data-ttu-id="88f3d-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88f3d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88f3d-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88f3d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88f3d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88f3d-136">CommonParameters</span></span>
<span data-ttu-id="88f3d-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88f3d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88f3d-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88f3d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88f3d-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88f3d-139">INPUTS</span></span>

### <span data-ttu-id="88f3d-140">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="88f3d-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="88f3d-141">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="88f3d-141">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="88f3d-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88f3d-142">OUTPUTS</span></span>

### <span data-ttu-id="88f3d-143">System. void</span><span class="sxs-lookup"><span data-stu-id="88f3d-143">System.Void</span></span>

## <span data-ttu-id="88f3d-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="88f3d-144">NOTES</span></span>

## <span data-ttu-id="88f3d-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88f3d-145">RELATED LINKS</span></span>

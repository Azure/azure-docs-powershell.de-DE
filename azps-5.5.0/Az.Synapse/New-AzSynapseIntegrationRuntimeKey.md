---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165625"
---
# <span data-ttu-id="abda7-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="abda7-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="abda7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abda7-102">SYNOPSIS</span></span>
<span data-ttu-id="abda7-103">Regenerieren Sie den selbst gehosteten Integrations-Runtime-Schlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="abda7-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="abda7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abda7-104">SYNTAX</span></span>

### <span data-ttu-id="abda7-105">NewByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="abda7-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="abda7-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abda7-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abda7-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abda7-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abda7-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abda7-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abda7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abda7-109">DESCRIPTION</span></span>
<span data-ttu-id="abda7-110">Das Cmdlet **"New-AzSynapseIntegrationRuntimeKey"** generiert den Integrationslaufzeitschlüssel erneut mit dem Schlüsselnamen, der durch den Parameter "KeyName" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abda7-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="abda7-111">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="abda7-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="abda7-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="abda7-112">EXAMPLES</span></span>

### <span data-ttu-id="abda7-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="abda7-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="abda7-114">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="abda7-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="abda7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abda7-115">PARAMETERS</span></span>

### <span data-ttu-id="abda7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abda7-116">-DefaultProfile</span></span>
<span data-ttu-id="abda7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abda7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abda7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="abda7-118">-Force</span></span>
<span data-ttu-id="abda7-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="abda7-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="abda7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abda7-120">-InputObject</span></span>
<span data-ttu-id="abda7-121">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="abda7-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: NewByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="abda7-122">-KeyName</span></span>
<span data-ttu-id="abda7-123">Der Name des Authentifizierungsschlüssels der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="abda7-123">The authentication key name of the self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AuthKey1, AuthKey2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="abda7-124">-Name</span></span>
<span data-ttu-id="abda7-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="abda7-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet, NewByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abda7-126">-ResourceGroupName</span></span>
<span data-ttu-id="abda7-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="abda7-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abda7-128">-ResourceId</span></span>
<span data-ttu-id="abda7-129">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="abda7-129">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="abda7-130">-WorkspaceName</span></span>
<span data-ttu-id="abda7-131">Name des Synapse-Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="abda7-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="abda7-132">-WorkspaceObject</span></span>
<span data-ttu-id="abda7-133">Arbeitsbereichseingabeobjekts, das in der Regel über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="abda7-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abda7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abda7-134">-Confirm</span></span>
<span data-ttu-id="abda7-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abda7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abda7-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="abda7-136">-WhatIf</span></span>
<span data-ttu-id="abda7-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abda7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abda7-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abda7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abda7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abda7-139">CommonParameters</span></span>
<span data-ttu-id="abda7-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abda7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abda7-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abda7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abda7-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="abda7-142">INPUTS</span></span>

### <span data-ttu-id="abda7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="abda7-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="abda7-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="abda7-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="abda7-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="abda7-145">OUTPUTS</span></span>

### <span data-ttu-id="abda7-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="abda7-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="abda7-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="abda7-147">NOTES</span></span>

## <span data-ttu-id="abda7-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="abda7-148">RELATED LINKS</span></span>

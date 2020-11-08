---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 836dcabaa190b66daf5a4f3f2fdaf300fe47ccdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178140"
---
# <span data-ttu-id="76d00-101">New-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="76d00-101">New-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="76d00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76d00-102">SYNOPSIS</span></span>
<span data-ttu-id="76d00-103">Generieren Sie den selbst gehosteten Integrationslauf Zeitschlüssel erneut.</span><span class="sxs-lookup"><span data-stu-id="76d00-103">Regenerate self-hosted integration runtime key.</span></span>

## <span data-ttu-id="76d00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76d00-104">SYNTAX</span></span>

### <span data-ttu-id="76d00-105">NewByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="76d00-105">NewByNameParameterSet (Default)</span></span>
```
New-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -KeyName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76d00-106">NewByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76d00-106">NewByParentObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace> -KeyName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76d00-107">NewByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76d00-107">NewByResourceIdParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -ResourceId <String> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76d00-108">NewByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76d00-108">NewByInputObjectParameterSet</span></span>
```
New-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime> -KeyName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76d00-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76d00-109">DESCRIPTION</span></span>
<span data-ttu-id="76d00-110">Das Cmdlet **New-AzSynapseIntegrationRuntimeKey** regeneriert den Integrationslauf Zeitschlüssel mit dem Schlüsselnamen, der durch den Parameter "keyname" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="76d00-110">The cmdlet **New-AzSynapseIntegrationRuntimeKey** regenerates the integration runtime key with the key name specified by 'KeyName' parameter.</span></span> <span data-ttu-id="76d00-111">Der vorherige Schlüssel ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="76d00-111">The previous key will is invalid.</span></span>

## <span data-ttu-id="76d00-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76d00-112">EXAMPLES</span></span>

### <span data-ttu-id="76d00-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="76d00-113">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -KeyName authKey2
```

<span data-ttu-id="76d00-114">Das Cmdlet generiert den Schlüssel "authKey2" für die Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" neu.</span><span class="sxs-lookup"><span data-stu-id="76d00-114">The cmdlet regenerates key 'authKey2' for integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="76d00-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="76d00-115">PARAMETERS</span></span>

### <span data-ttu-id="76d00-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d00-116">-DefaultProfile</span></span>
<span data-ttu-id="76d00-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76d00-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76d00-118">-Force</span><span class="sxs-lookup"><span data-stu-id="76d00-118">-Force</span></span>
<span data-ttu-id="76d00-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="76d00-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76d00-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76d00-120">-InputObject</span></span>
<span data-ttu-id="76d00-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="76d00-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="76d00-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="76d00-122">-KeyName</span></span>
<span data-ttu-id="76d00-123">Der Authentifizierungsschlüssel Name der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="76d00-123">The authentication key name of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="76d00-124">-Name</span><span class="sxs-lookup"><span data-stu-id="76d00-124">-Name</span></span>
<span data-ttu-id="76d00-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="76d00-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="76d00-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76d00-126">-ResourceGroupName</span></span>
<span data-ttu-id="76d00-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="76d00-127">Resource group name.</span></span>

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

### <span data-ttu-id="76d00-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="76d00-128">-ResourceId</span></span>
<span data-ttu-id="76d00-129">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="76d00-129">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="76d00-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76d00-130">-WorkspaceName</span></span>
<span data-ttu-id="76d00-131">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="76d00-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="76d00-132">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="76d00-132">-WorkspaceObject</span></span>
<span data-ttu-id="76d00-133">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="76d00-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="76d00-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76d00-134">-Confirm</span></span>
<span data-ttu-id="76d00-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76d00-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76d00-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76d00-136">-WhatIf</span></span>
<span data-ttu-id="76d00-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76d00-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76d00-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76d00-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76d00-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d00-139">CommonParameters</span></span>
<span data-ttu-id="76d00-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d00-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d00-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76d00-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d00-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76d00-142">INPUTS</span></span>

### <span data-ttu-id="76d00-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76d00-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="76d00-144">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="76d00-144">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="76d00-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76d00-145">OUTPUTS</span></span>

### <span data-ttu-id="76d00-146">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="76d00-146">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="76d00-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="76d00-147">NOTES</span></span>

## <span data-ttu-id="76d00-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76d00-148">RELATED LINKS</span></span>

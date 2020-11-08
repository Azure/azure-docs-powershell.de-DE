---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapseintegrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseIntegrationRuntimeUpgrade.md
ms.openlocfilehash: 59630bd0ffcf5bebfc68f647cff444466727a990
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165425"
---
# <span data-ttu-id="ff033-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="ff033-101">Invoke-AzSynapseIntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="ff033-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff033-102">SYNOPSIS</span></span>
<span data-ttu-id="ff033-103">Upgrades der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff033-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="ff033-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff033-104">SYNTAX</span></span>

### <span data-ttu-id="ff033-105">InvokeByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff033-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff033-106">InvokeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff033-106">InvokeByParentObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff033-107">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff033-107">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff033-108">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff033-108">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzSynapseIntegrationRuntimeUpgrade -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff033-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff033-109">DESCRIPTION</span></span>
<span data-ttu-id="ff033-110">Das Cmdlet **Invoke-AzSynapseIntegrationRuntimeUpgrade** aktualisiert die selbst gehostete Integrationslaufzeit, wenn die neue Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ff033-110">The **Invoke-AzSynapseIntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="ff033-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff033-111">EXAMPLES</span></span>

### <span data-ttu-id="ff033-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ff033-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSynapseIntegrationRuntimeUpgrade -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="ff033-113">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Arbeitsbereich ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ff033-113">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

## <span data-ttu-id="ff033-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff033-114">PARAMETERS</span></span>

### <span data-ttu-id="ff033-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff033-115">-DefaultProfile</span></span>
<span data-ttu-id="ff033-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff033-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff033-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ff033-117">-InputObject</span></span>
<span data-ttu-id="ff033-118">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="ff033-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: InvokeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff033-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ff033-119">-Name</span></span>
<span data-ttu-id="ff033-120">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff033-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet, InvokeByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff033-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff033-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff033-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ff033-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff033-123">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ff033-123">-ResourceId</span></span>
<span data-ttu-id="ff033-124">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ff033-124">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff033-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff033-125">-WorkspaceName</span></span>
<span data-ttu-id="ff033-126">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="ff033-126">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff033-127">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="ff033-127">-WorkspaceObject</span></span>
<span data-ttu-id="ff033-128">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="ff033-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: InvokeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff033-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ff033-129">-Confirm</span></span>
<span data-ttu-id="ff033-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ff033-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff033-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff033-131">-WhatIf</span></span>
<span data-ttu-id="ff033-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ff033-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff033-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ff033-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff033-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff033-134">CommonParameters</span></span>
<span data-ttu-id="ff033-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff033-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff033-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff033-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff033-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff033-137">INPUTS</span></span>

### <span data-ttu-id="ff033-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff033-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ff033-139">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ff033-139">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ff033-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff033-140">OUTPUTS</span></span>

### <span data-ttu-id="ff033-141">System. void</span><span class="sxs-lookup"><span data-stu-id="ff033-141">System.Void</span></span>

## <span data-ttu-id="ff033-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff033-142">NOTES</span></span>

## <span data-ttu-id="ff033-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff033-143">RELATED LINKS</span></span>

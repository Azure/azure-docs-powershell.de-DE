---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302367"
---
# <span data-ttu-id="908e7-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="908e7-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="908e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="908e7-102">SYNOPSIS</span></span>
<span data-ttu-id="908e7-103">Ruft eine Integration Runtime-Knoten Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="908e7-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="908e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="908e7-104">SYNTAX</span></span>

### <span data-ttu-id="908e7-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="908e7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="908e7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="908e7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908e7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="908e7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="908e7-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="908e7-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="908e7-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="908e7-109">DESCRIPTION</span></span>
<span data-ttu-id="908e7-110">Das Cmdlet " **Get-AzSynapseIntegrationRuntimeNode** " Ruft die Detailinformationen eines Integrationslauf Zeit Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="908e7-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="908e7-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="908e7-111">EXAMPLES</span></span>

### <span data-ttu-id="908e7-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="908e7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="908e7-113">Das Cmdlet ruft Informationen zu Knoten mit dem Namen "Node_1" in der selbst gehosteten Integrationslaufzeit "Test-SelfHost-IR" in Workspace ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="908e7-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="908e7-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="908e7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="908e7-115">Das Cmdlet ruft Informationen zu Knoten mit dem Namen "Node_1" in der selbst gehosteten Integrationslaufzeit "Test-SelfHost-IR" im Arbeitsbereich "Test-DF-EU2" ab, einschließlich der IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="908e7-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="908e7-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="908e7-116">PARAMETERS</span></span>

### <span data-ttu-id="908e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="908e7-117">-DefaultProfile</span></span>
<span data-ttu-id="908e7-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="908e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="908e7-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="908e7-119">-InputObject</span></span>
<span data-ttu-id="908e7-120">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="908e7-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="908e7-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="908e7-122">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="908e7-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-123">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="908e7-123">-IpAddress</span></span>
<span data-ttu-id="908e7-124">Die IP-Adresse des Integrationslauf Zeit Knotens.</span><span class="sxs-lookup"><span data-stu-id="908e7-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="908e7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="908e7-125">-Name</span></span>
<span data-ttu-id="908e7-126">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="908e7-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="908e7-127">-ResourceGroupName</span></span>
<span data-ttu-id="908e7-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="908e7-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="908e7-129">-ResourceId</span></span>
<span data-ttu-id="908e7-130">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="908e7-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="908e7-131">-WorkspaceName</span></span>
<span data-ttu-id="908e7-132">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="908e7-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-133">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="908e7-133">-WorkspaceObject</span></span>
<span data-ttu-id="908e7-134">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="908e7-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="908e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="908e7-135">CommonParameters</span></span>
<span data-ttu-id="908e7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="908e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="908e7-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="908e7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="908e7-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="908e7-138">INPUTS</span></span>

### <span data-ttu-id="908e7-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="908e7-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="908e7-140">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="908e7-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="908e7-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="908e7-141">OUTPUTS</span></span>

### <span data-ttu-id="908e7-142">Microsoft. Azure. Commands. Synapse. Models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="908e7-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="908e7-143">Microsoft. Azure. Commands. Synapse. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="908e7-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="908e7-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="908e7-144">NOTES</span></span>

## <span data-ttu-id="908e7-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="908e7-145">RELATED LINKS</span></span>

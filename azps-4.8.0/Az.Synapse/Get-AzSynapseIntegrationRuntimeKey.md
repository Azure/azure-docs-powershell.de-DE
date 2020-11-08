---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeKey.md
ms.openlocfilehash: 08ce91d6d9a942dd20078e0c3b5b537360aac9fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007697"
---
# <span data-ttu-id="215bb-101">Get-AzSynapseIntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="215bb-101">Get-AzSynapseIntegrationRuntimeKey</span></span>

## <span data-ttu-id="215bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="215bb-102">SYNOPSIS</span></span>
<span data-ttu-id="215bb-103">Ruft Schlüssel für eine selbst gehostete Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="215bb-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="215bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="215bb-104">SYNTAX</span></span>

### <span data-ttu-id="215bb-105">GetByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="215bb-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeKey [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="215bb-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="215bb-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="215bb-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="215bb-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="215bb-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="215bb-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeKey -InputObject <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="215bb-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="215bb-109">DESCRIPTION</span></span>
<span data-ttu-id="215bb-110">Das Cmdlet " **Get-AzSynapseIntegrationRuntimeKey** " ruft Schlüssel für eine Integrationslaufzeit ab.</span><span class="sxs-lookup"><span data-stu-id="215bb-110">The **Get-AzSynapseIntegrationRuntimeKey** cmdlet gets keys for an integration runtime.</span></span> <span data-ttu-id="215bb-111">Die Schlüssel werden zum Registrieren eines Integrationslauf Zeit Knotens verwendet.</span><span class="sxs-lookup"><span data-stu-id="215bb-111">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="215bb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="215bb-112">EXAMPLES</span></span>

### <span data-ttu-id="215bb-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="215bb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeKey -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir'
```

<span data-ttu-id="215bb-114">Das Cmdlet ruft Schlüssel für eine Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" ab.</span><span class="sxs-lookup"><span data-stu-id="215bb-114">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="215bb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="215bb-115">PARAMETERS</span></span>

### <span data-ttu-id="215bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215bb-116">-DefaultProfile</span></span>
<span data-ttu-id="215bb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="215bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="215bb-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="215bb-118">-InputObject</span></span>
<span data-ttu-id="215bb-119">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="215bb-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="215bb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="215bb-120">-Name</span></span>
<span data-ttu-id="215bb-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="215bb-121">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="215bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="215bb-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="215bb-123">Resource group name.</span></span>

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

### <span data-ttu-id="215bb-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="215bb-124">-ResourceId</span></span>
<span data-ttu-id="215bb-125">Ressourcenbezeichner der Synapse-Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="215bb-125">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="215bb-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="215bb-126">-WorkspaceName</span></span>
<span data-ttu-id="215bb-127">Name des Synapse-Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="215bb-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="215bb-128">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="215bb-128">-WorkspaceObject</span></span>
<span data-ttu-id="215bb-129">Arbeitsbereichs Eingabeobjekt, in der Regel durch die Pipeline übergeben.</span><span class="sxs-lookup"><span data-stu-id="215bb-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="215bb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215bb-130">CommonParameters</span></span>
<span data-ttu-id="215bb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="215bb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215bb-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="215bb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215bb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="215bb-133">INPUTS</span></span>

### <span data-ttu-id="215bb-134">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="215bb-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="215bb-135">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="215bb-135">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="215bb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="215bb-136">OUTPUTS</span></span>

### <span data-ttu-id="215bb-137">Microsoft. Azure. Commands. Synapse. Models. PSIntegrationRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="215bb-137">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="215bb-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="215bb-138">NOTES</span></span>

## <span data-ttu-id="215bb-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="215bb-139">RELATED LINKS</span></span>

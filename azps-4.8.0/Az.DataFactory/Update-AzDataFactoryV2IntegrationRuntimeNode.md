---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167021"
---
# <span data-ttu-id="b5772-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b5772-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="b5772-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b5772-102">SYNOPSIS</span></span>
<span data-ttu-id="b5772-103">Aktualisiert den Self-Hosted Integration Runtime-Knoten.</span><span class="sxs-lookup"><span data-stu-id="b5772-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="b5772-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5772-104">SYNTAX</span></span>

### <span data-ttu-id="b5772-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b5772-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5772-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5772-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5772-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b5772-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5772-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b5772-108">DESCRIPTION</span></span>
<span data-ttu-id="b5772-109">Das Cmdlet **Update-AzDataFactoryV2IntegrationRuntimeNode** aktualisiert Eigenschaften des Self-Hosted Integration Runtime-Knotens in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b5772-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="b5772-110">Derzeit wird nur die Aktualisierung von "ConcurrentJobsLimit" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5772-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="b5772-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5772-111">EXAMPLES</span></span>

### <span data-ttu-id="b5772-112">Beispiel 1: Update-Self-Hosted Integration Runtime-Knoten</span><span class="sxs-lookup"><span data-stu-id="b5772-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="b5772-113">Das Cmdlet aktualisiert "ConcurrentJobsLimit" auf "3" für den Knoten "Node_1" in der selbst gehosteten Integrationslaufzeit "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="b5772-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b5772-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5772-114">PARAMETERS</span></span>

### <span data-ttu-id="b5772-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="b5772-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="b5772-116">Die Anzahl von gleichzeitigen Aufträgen, die auf dem Integrationslauf Zeit Knoten ausgeführt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="b5772-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="b5772-117">Werte zwischen 1 und maxConcurrentJobs sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="b5772-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5772-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b5772-118">-DataFactoryName</span></span>
<span data-ttu-id="b5772-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="b5772-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5772-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5772-120">-DefaultProfile</span></span>
<span data-ttu-id="b5772-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b5772-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5772-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b5772-122">-InputObject</span></span>
<span data-ttu-id="b5772-123">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="b5772-123">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5772-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b5772-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b5772-125">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="b5772-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5772-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b5772-126">-Name</span></span>
<span data-ttu-id="b5772-127">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="b5772-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b5772-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5772-128">-ResourceGroupName</span></span>
<span data-ttu-id="b5772-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b5772-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5772-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b5772-130">-ResourceId</span></span>
<span data-ttu-id="b5772-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b5772-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5772-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b5772-132">-Confirm</span></span>
<span data-ttu-id="b5772-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5772-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5772-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5772-134">-WhatIf</span></span>
<span data-ttu-id="b5772-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5772-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5772-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5772-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5772-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5772-137">CommonParameters</span></span>
<span data-ttu-id="b5772-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5772-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5772-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5772-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5772-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b5772-140">INPUTS</span></span>

### <span data-ttu-id="b5772-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b5772-141">System.String</span></span>

### <span data-ttu-id="b5772-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b5772-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b5772-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b5772-143">OUTPUTS</span></span>

### <span data-ttu-id="b5772-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b5772-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b5772-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b5772-145">NOTES</span></span>
<span data-ttu-id="b5772-146">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="b5772-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b5772-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b5772-147">RELATED LINKS</span></span>

<span data-ttu-id="b5772-148">[Satz-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="b5772-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>


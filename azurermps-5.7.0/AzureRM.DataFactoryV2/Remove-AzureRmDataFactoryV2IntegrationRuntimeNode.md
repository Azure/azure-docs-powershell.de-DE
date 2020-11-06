---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: bc16145569fd46b80e6d7a5afc1755f36346fa9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476826"
---
# <span data-ttu-id="dfe83-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="dfe83-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="dfe83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfe83-102">SYNOPSIS</span></span>
<span data-ttu-id="dfe83-103">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="dfe83-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfe83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfe83-104">SYNTAX</span></span>

### <span data-ttu-id="dfe83-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="dfe83-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe83-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dfe83-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfe83-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="dfe83-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfe83-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfe83-108">DESCRIPTION</span></span>
<span data-ttu-id="dfe83-109">Das Remove-AzureRmDataFactoryV2IntegrationRuntimeNode-Cmdlet entfernt einen Knoten in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="dfe83-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="dfe83-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfe83-110">EXAMPLES</span></span>

### <span data-ttu-id="dfe83-111">Beispiel 1: Entfernen eines Knotens aus einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="dfe83-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="dfe83-112">Dieser Befehl entfernt einen Knoten mit dem Namen "Node_1" in der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="dfe83-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="dfe83-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfe83-113">PARAMETERS</span></span>

### <span data-ttu-id="dfe83-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dfe83-114">-DataFactoryName</span></span>
<span data-ttu-id="dfe83-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="dfe83-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfe83-116">-DefaultProfile</span></span>
<span data-ttu-id="dfe83-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dfe83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dfe83-118">-Force</span></span>
<span data-ttu-id="dfe83-119">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="dfe83-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dfe83-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dfe83-120">-InputObject</span></span>
<span data-ttu-id="dfe83-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="dfe83-121">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dfe83-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="dfe83-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="dfe83-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="dfe83-124">-NodeName</span></span>
<span data-ttu-id="dfe83-125">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="dfe83-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfe83-126">-ResourceGroupName</span></span>
<span data-ttu-id="dfe83-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dfe83-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="dfe83-128">-ResourceId</span></span>
<span data-ttu-id="dfe83-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="dfe83-129">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfe83-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfe83-130">-Confirm</span></span>
<span data-ttu-id="dfe83-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfe83-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfe83-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfe83-132">-WhatIf</span></span>
<span data-ttu-id="dfe83-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfe83-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="dfe83-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfe83-134">CommonParameters</span></span>
<span data-ttu-id="dfe83-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfe83-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfe83-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfe83-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfe83-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfe83-137">INPUTS</span></span>

### <span data-ttu-id="dfe83-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dfe83-138">System.String</span></span>
<span data-ttu-id="dfe83-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dfe83-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dfe83-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfe83-140">OUTPUTS</span></span>

### <span data-ttu-id="dfe83-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="dfe83-141">System.Object</span></span>

## <span data-ttu-id="dfe83-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfe83-142">NOTES</span></span>

## <span data-ttu-id="dfe83-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfe83-143">RELATED LINKS</span></span>


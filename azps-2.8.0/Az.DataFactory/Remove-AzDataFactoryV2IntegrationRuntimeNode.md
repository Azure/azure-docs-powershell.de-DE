---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: dbf5b4eba8c6fe2dc55e55a58df79ed9b7d08afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651696"
---
# <span data-ttu-id="a45c8-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a45c8-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="a45c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a45c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a45c8-103">Entfernen Sie einen Knoten mit dem angegebenen Namen in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a45c8-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="a45c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a45c8-104">SYNTAX</span></span>

### <span data-ttu-id="a45c8-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a45c8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a45c8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a45c8-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a45c8-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a45c8-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a45c8-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a45c8-108">DESCRIPTION</span></span>
<span data-ttu-id="a45c8-109">Das Remove-AzDataFactoryV2IntegrationRuntimeNode-Cmdlet entfernt einen Knoten in einer Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a45c8-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="a45c8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a45c8-110">EXAMPLES</span></span>

### <span data-ttu-id="a45c8-111">Beispiel 1: Entfernen eines Knotens aus einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="a45c8-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="a45c8-112">Dieser Befehl entfernt einen Knoten mit dem Namen "Node_1" in der Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" im Abonnement für die Ressourcengruppe "RG-Test-dfv2" und Data Factory mit dem Namen "Test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="a45c8-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="a45c8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a45c8-113">PARAMETERS</span></span>

### <span data-ttu-id="a45c8-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a45c8-114">-DataFactoryName</span></span>
<span data-ttu-id="a45c8-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a45c8-115">The data factory name.</span></span>

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

### <span data-ttu-id="a45c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45c8-116">-DefaultProfile</span></span>
<span data-ttu-id="a45c8-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a45c8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a45c8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a45c8-118">-Force</span></span>
<span data-ttu-id="a45c8-119">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="a45c8-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a45c8-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a45c8-120">-InputObject</span></span>
<span data-ttu-id="a45c8-121">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="a45c8-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="a45c8-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a45c8-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a45c8-123">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a45c8-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="a45c8-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="a45c8-124">-NodeName</span></span>
<span data-ttu-id="a45c8-125">Der Knotenname der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a45c8-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="a45c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a45c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="a45c8-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a45c8-127">The resource group name.</span></span>

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

### <span data-ttu-id="a45c8-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a45c8-128">-ResourceId</span></span>
<span data-ttu-id="a45c8-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a45c8-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a45c8-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a45c8-130">-Confirm</span></span>
<span data-ttu-id="a45c8-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a45c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a45c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a45c8-132">-WhatIf</span></span>
<span data-ttu-id="a45c8-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a45c8-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a45c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45c8-134">CommonParameters</span></span>
<span data-ttu-id="a45c8-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a45c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45c8-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a45c8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45c8-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a45c8-137">INPUTS</span></span>

### <span data-ttu-id="a45c8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a45c8-138">System.String</span></span>

### <span data-ttu-id="a45c8-139">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a45c8-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a45c8-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a45c8-140">OUTPUTS</span></span>

### <span data-ttu-id="a45c8-141">System. void</span><span class="sxs-lookup"><span data-stu-id="a45c8-141">System.Void</span></span>

## <span data-ttu-id="a45c8-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="a45c8-142">NOTES</span></span>

## <span data-ttu-id="a45c8-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a45c8-143">RELATED LINKS</span></span>

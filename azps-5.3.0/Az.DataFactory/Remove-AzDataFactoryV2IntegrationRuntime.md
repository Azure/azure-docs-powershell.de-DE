---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470552"
---
# <span data-ttu-id="1e01f-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e01f-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="1e01f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e01f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e01f-103">Entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1e01f-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="1e01f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1e01f-104">SYNTAX</span></span>

### <span data-ttu-id="1e01f-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e01f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e01f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1e01f-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e01f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1e01f-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e01f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e01f-108">DESCRIPTION</span></span>
<span data-ttu-id="1e01f-109">Das Remove-AzDataFactoryV2IntegrationRuntime entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1e01f-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="1e01f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1e01f-110">EXAMPLES</span></span>

### <span data-ttu-id="1e01f-111">Beispiel 1: Entfernen einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="1e01f-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="1e01f-112">Mit diesem Befehl wird die Integrationslaufzeit mit dem Namen "test-reserved-ir" aus der Daten factory mit dem Namen "test-df" entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e01f-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="1e01f-113">Dieser Befehl gibt den Wert "$True" $True.</span><span class="sxs-lookup"><span data-stu-id="1e01f-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="1e01f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e01f-114">PARAMETERS</span></span>

### <span data-ttu-id="1e01f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e01f-115">-DataFactoryName</span></span>
<span data-ttu-id="1e01f-116">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1e01f-116">The data factory name.</span></span>

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

### <span data-ttu-id="1e01f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e01f-117">-DefaultProfile</span></span>
<span data-ttu-id="1e01f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e01f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e01f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1e01f-119">-Force</span></span>
<span data-ttu-id="1e01f-120">Führt das Cmdlet ohne Bestätigungsaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="1e01f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1e01f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e01f-121">-InputObject</span></span>
<span data-ttu-id="1e01f-122">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1e01f-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="1e01f-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1e01f-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="1e01f-124">Der Name der verknüpften Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1e01f-124">The linked data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e01f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1e01f-125">-Name</span></span>
<span data-ttu-id="1e01f-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="1e01f-126">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e01f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e01f-127">-ResourceGroupName</span></span>
<span data-ttu-id="1e01f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1e01f-128">The resource group name.</span></span>

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

### <span data-ttu-id="1e01f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e01f-129">-ResourceId</span></span>
<span data-ttu-id="1e01f-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1e01f-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1e01f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e01f-131">-Confirm</span></span>
<span data-ttu-id="1e01f-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e01f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e01f-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1e01f-133">-WhatIf</span></span>
<span data-ttu-id="1e01f-134">Zeigt, was geschieht, wenn das Cmdlet ausgeführt, aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e01f-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1e01f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e01f-135">CommonParameters</span></span>
<span data-ttu-id="1e01f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e01f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e01f-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e01f-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e01f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1e01f-138">INPUTS</span></span>

### <span data-ttu-id="1e01f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1e01f-139">System.String</span></span>

### <span data-ttu-id="1e01f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e01f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1e01f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1e01f-141">OUTPUTS</span></span>

### <span data-ttu-id="1e01f-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="1e01f-142">System.Void</span></span>

## <span data-ttu-id="1e01f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1e01f-143">NOTES</span></span>
<span data-ttu-id="1e01f-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="1e01f-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1e01f-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1e01f-145">RELATED LINKS</span></span>

[<span data-ttu-id="1e01f-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e01f-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="1e01f-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1e01f-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()


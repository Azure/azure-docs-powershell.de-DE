---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 9478c190d33608706006ff7fe792b4ee8f14b9d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651700"
---
# <span data-ttu-id="a3203-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3203-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="a3203-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3203-102">SYNOPSIS</span></span>
<span data-ttu-id="a3203-103">Entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a3203-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="a3203-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3203-104">SYNTAX</span></span>

### <span data-ttu-id="a3203-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3203-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3203-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3203-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3203-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a3203-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3203-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3203-108">DESCRIPTION</span></span>
<span data-ttu-id="a3203-109">Das Remove-AzDataFactoryV2IntegrationRuntime-Cmdlet entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a3203-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="a3203-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3203-110">EXAMPLES</span></span>

### <span data-ttu-id="a3203-111">Beispiel 1: Entfernen einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="a3203-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="a3203-112">Dieser Befehl entfernt die Integrationslaufzeit mit dem Namen "Test-reservierte-IR" aus der Data Factory mit dem Namen "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="a3203-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="a3203-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="a3203-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="a3203-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3203-114">PARAMETERS</span></span>

### <span data-ttu-id="a3203-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a3203-115">-DataFactoryName</span></span>
<span data-ttu-id="a3203-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a3203-116">The data factory name.</span></span>

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

### <span data-ttu-id="a3203-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3203-117">-DefaultProfile</span></span>
<span data-ttu-id="a3203-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3203-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3203-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a3203-119">-Force</span></span>
<span data-ttu-id="a3203-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="a3203-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a3203-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3203-121">-InputObject</span></span>
<span data-ttu-id="a3203-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3203-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="a3203-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a3203-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="a3203-124">Der Name der verknüpften Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a3203-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="a3203-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a3203-125">-Name</span></span>
<span data-ttu-id="a3203-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="a3203-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="a3203-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3203-127">-ResourceGroupName</span></span>
<span data-ttu-id="a3203-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a3203-128">The resource group name.</span></span>

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

### <span data-ttu-id="a3203-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a3203-129">-ResourceId</span></span>
<span data-ttu-id="a3203-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a3203-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a3203-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3203-131">-Confirm</span></span>
<span data-ttu-id="a3203-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3203-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3203-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3203-133">-WhatIf</span></span>
<span data-ttu-id="a3203-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3203-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a3203-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3203-135">CommonParameters</span></span>
<span data-ttu-id="a3203-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3203-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3203-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3203-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3203-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3203-138">INPUTS</span></span>

### <span data-ttu-id="a3203-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a3203-139">System.String</span></span>

### <span data-ttu-id="a3203-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3203-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a3203-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3203-141">OUTPUTS</span></span>

### <span data-ttu-id="a3203-142">System. void</span><span class="sxs-lookup"><span data-stu-id="a3203-142">System.Void</span></span>

## <span data-ttu-id="a3203-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3203-143">NOTES</span></span>
<span data-ttu-id="a3203-144">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="a3203-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="a3203-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3203-145">RELATED LINKS</span></span>

[<span data-ttu-id="a3203-146">Satz-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3203-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="a3203-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a3203-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()


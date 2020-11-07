---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847188"
---
# <span data-ttu-id="70c58-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="70c58-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="70c58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="70c58-102">SYNOPSIS</span></span>
<span data-ttu-id="70c58-103">Entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="70c58-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="70c58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="70c58-104">SYNTAX</span></span>

### <span data-ttu-id="70c58-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="70c58-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c58-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="70c58-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70c58-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="70c58-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="70c58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="70c58-108">DESCRIPTION</span></span>
<span data-ttu-id="70c58-109">Das Remove-AzDataFactoryV2IntegrationRuntime-Cmdlet entfernt eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="70c58-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="70c58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="70c58-110">EXAMPLES</span></span>

### <span data-ttu-id="70c58-111">Beispiel 1: Entfernen einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="70c58-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="70c58-112">Dieser Befehl entfernt die Integrationslaufzeit mit dem Namen "Test-reservierte-IR" aus der Data Factory mit dem Namen "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="70c58-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="70c58-113">Dieser Befehl gibt den Wert $true zurück.</span><span class="sxs-lookup"><span data-stu-id="70c58-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="70c58-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="70c58-114">PARAMETERS</span></span>

### <span data-ttu-id="70c58-115">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="70c58-115">-DataFactoryName</span></span>
<span data-ttu-id="70c58-116">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="70c58-116">The data factory name.</span></span>

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

### <span data-ttu-id="70c58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70c58-117">-DefaultProfile</span></span>
<span data-ttu-id="70c58-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="70c58-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70c58-119">-Force</span><span class="sxs-lookup"><span data-stu-id="70c58-119">-Force</span></span>
<span data-ttu-id="70c58-120">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="70c58-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="70c58-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70c58-121">-InputObject</span></span>
<span data-ttu-id="70c58-122">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="70c58-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="70c58-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="70c58-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="70c58-124">Der Name der verknüpften Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="70c58-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="70c58-125">-Name</span><span class="sxs-lookup"><span data-stu-id="70c58-125">-Name</span></span>
<span data-ttu-id="70c58-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="70c58-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="70c58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70c58-127">-ResourceGroupName</span></span>
<span data-ttu-id="70c58-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="70c58-128">The resource group name.</span></span>

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

### <span data-ttu-id="70c58-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="70c58-129">-ResourceId</span></span>
<span data-ttu-id="70c58-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="70c58-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="70c58-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="70c58-131">-Confirm</span></span>
<span data-ttu-id="70c58-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="70c58-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70c58-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70c58-133">-WhatIf</span></span>
<span data-ttu-id="70c58-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70c58-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="70c58-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70c58-135">CommonParameters</span></span>
<span data-ttu-id="70c58-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70c58-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70c58-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70c58-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70c58-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="70c58-138">INPUTS</span></span>

### <span data-ttu-id="70c58-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70c58-139">System.String</span></span>

### <span data-ttu-id="70c58-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="70c58-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="70c58-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="70c58-141">OUTPUTS</span></span>

### <span data-ttu-id="70c58-142">System. void</span><span class="sxs-lookup"><span data-stu-id="70c58-142">System.Void</span></span>

## <span data-ttu-id="70c58-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="70c58-143">NOTES</span></span>
<span data-ttu-id="70c58-144">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="70c58-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="70c58-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="70c58-145">RELATED LINKS</span></span>

[<span data-ttu-id="70c58-146">Satz-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="70c58-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="70c58-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="70c58-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()


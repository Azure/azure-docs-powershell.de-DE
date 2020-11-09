---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2integrationruntimeupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade.md
ms.openlocfilehash: c7ffe4348d11658da6e7c9caeccaa14f17a6329b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298468"
---
# <span data-ttu-id="24116-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="24116-101">Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade</span></span>

## <span data-ttu-id="24116-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24116-102">SYNOPSIS</span></span>
<span data-ttu-id="24116-103">Upgrades der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="24116-103">Upgrades self-hosted integration runtime.</span></span>

## <span data-ttu-id="24116-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24116-104">SYNTAX</span></span>

### <span data-ttu-id="24116-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="24116-105">ByIntegrationRuntimeName (Default)</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24116-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="24116-106">ByResourceId</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24116-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="24116-107">ByIntegrationRuntimeObject</span></span>
```
Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24116-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24116-108">DESCRIPTION</span></span>
<span data-ttu-id="24116-109">Das Cmdlet **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** aktualisiert die selbst gehostete Integrationslaufzeit, wenn die neue Version verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="24116-109">The **Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade** cmdlet upgrades self-hosted integration runtime if the new version is available.</span></span>

## <span data-ttu-id="24116-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24116-110">EXAMPLES</span></span>

### <span data-ttu-id="24116-111">Beispiel 1: Upgraden einer selbst gehosteten Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="24116-111">Example 1: Upgrades a self-hosted integration runtime</span></span>
```
PS C:\> Invoke-AzDataFactoryV2IntegrationRuntimeUpgrade -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'
```

<span data-ttu-id="24116-112">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "Test-SelfHost-IR" in Data Factory "Test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="24116-112">The cmdlet upgrades self-hosted integration runtime named 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

## <span data-ttu-id="24116-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="24116-113">PARAMETERS</span></span>

### <span data-ttu-id="24116-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="24116-114">-DataFactoryName</span></span>
<span data-ttu-id="24116-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="24116-115">The data factory name.</span></span>

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

### <span data-ttu-id="24116-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24116-116">-DefaultProfile</span></span>
<span data-ttu-id="24116-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24116-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24116-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="24116-118">-InputObject</span></span>
<span data-ttu-id="24116-119">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="24116-119">The integration runtime object.</span></span>

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

### <span data-ttu-id="24116-120">-Name</span><span class="sxs-lookup"><span data-stu-id="24116-120">-Name</span></span>
<span data-ttu-id="24116-121">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="24116-121">The integration runtime name.</span></span>

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

### <span data-ttu-id="24116-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24116-122">-ResourceGroupName</span></span>
<span data-ttu-id="24116-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="24116-123">The resource group name.</span></span>

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

### <span data-ttu-id="24116-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="24116-124">-ResourceId</span></span>
<span data-ttu-id="24116-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="24116-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="24116-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24116-126">-Confirm</span></span>
<span data-ttu-id="24116-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24116-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24116-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24116-128">-WhatIf</span></span>
<span data-ttu-id="24116-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24116-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24116-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24116-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24116-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24116-131">CommonParameters</span></span>
<span data-ttu-id="24116-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24116-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24116-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24116-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24116-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24116-134">INPUTS</span></span>

### <span data-ttu-id="24116-135">System. String</span><span class="sxs-lookup"><span data-stu-id="24116-135">System.String</span></span>

### <span data-ttu-id="24116-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="24116-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="24116-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24116-137">OUTPUTS</span></span>

### <span data-ttu-id="24116-138">System. void</span><span class="sxs-lookup"><span data-stu-id="24116-138">System.Void</span></span>

## <span data-ttu-id="24116-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="24116-139">NOTES</span></span>
<span data-ttu-id="24116-140">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="24116-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="24116-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24116-141">RELATED LINKS</span></span>

<span data-ttu-id="24116-142">[Satz-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="24116-142">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>


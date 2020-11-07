---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 487a4592217ac725fa46ef717c6e556cc433fcb4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847068"
---
# <span data-ttu-id="19ed6-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="19ed6-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="19ed6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="19ed6-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="19ed6-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="19ed6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19ed6-104">SYNTAX</span></span>

### <span data-ttu-id="19ed6-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="19ed6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ed6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="19ed6-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19ed6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="19ed6-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19ed6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19ed6-108">DESCRIPTION</span></span>
<span data-ttu-id="19ed6-109">Das **Update-AzDataFactoryV2IntegrationRuntime-** Cmdlet aktualisiert die Eigenschaften der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="19ed6-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="19ed6-110">Derzeit unterstützt das Cmdlet nur das Aktualisieren von "AutoUpdate" und "AutoUpdateDelayOffset" für die selbst gehostete Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="19ed6-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="19ed6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19ed6-111">EXAMPLES</span></span>

### <span data-ttu-id="19ed6-112">Beispiel 1: Aktualisieren einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="19ed6-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="19ed6-113">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="19ed6-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="19ed6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19ed6-114">PARAMETERS</span></span>

### <span data-ttu-id="19ed6-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="19ed6-115">-AutoUpdate</span></span>
<span data-ttu-id="19ed6-116">Aktivieren oder Deaktivieren der automatischen Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="19ed6-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ed6-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="19ed6-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="19ed6-118">Die Uhrzeit in Stunden des Tages für die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="19ed6-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19ed6-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="19ed6-119">-DataFactoryName</span></span>
<span data-ttu-id="19ed6-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="19ed6-120">The data factory name.</span></span>

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

### <span data-ttu-id="19ed6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19ed6-121">-DefaultProfile</span></span>
<span data-ttu-id="19ed6-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19ed6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19ed6-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="19ed6-123">-InputObject</span></span>
<span data-ttu-id="19ed6-124">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="19ed6-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="19ed6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="19ed6-125">-Name</span></span>
<span data-ttu-id="19ed6-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="19ed6-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="19ed6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19ed6-127">-ResourceGroupName</span></span>
<span data-ttu-id="19ed6-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="19ed6-128">The resource group name.</span></span>

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

### <span data-ttu-id="19ed6-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="19ed6-129">-ResourceId</span></span>
<span data-ttu-id="19ed6-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="19ed6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="19ed6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19ed6-131">-Confirm</span></span>
<span data-ttu-id="19ed6-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19ed6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19ed6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19ed6-133">-WhatIf</span></span>
<span data-ttu-id="19ed6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19ed6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19ed6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19ed6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19ed6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19ed6-136">CommonParameters</span></span>
<span data-ttu-id="19ed6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19ed6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19ed6-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19ed6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19ed6-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19ed6-139">INPUTS</span></span>

### <span data-ttu-id="19ed6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="19ed6-140">System.String</span></span>

### <span data-ttu-id="19ed6-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="19ed6-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="19ed6-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19ed6-142">OUTPUTS</span></span>

### <span data-ttu-id="19ed6-143">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="19ed6-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="19ed6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="19ed6-144">NOTES</span></span>
<span data-ttu-id="19ed6-145">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="19ed6-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="19ed6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19ed6-146">RELATED LINKS</span></span>

<span data-ttu-id="19ed6-147">[Satz-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="19ed6-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>


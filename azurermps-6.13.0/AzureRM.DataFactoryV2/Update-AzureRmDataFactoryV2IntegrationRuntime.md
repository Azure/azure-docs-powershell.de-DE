---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 2c20752dd1e29962f128f687344b3b165f0a09ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496233"
---
# <span data-ttu-id="cf152-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf152-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="cf152-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cf152-102">SYNOPSIS</span></span>
<span data-ttu-id="cf152-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf152-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf152-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf152-104">SYNTAX</span></span>

### <span data-ttu-id="cf152-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="cf152-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf152-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf152-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf152-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cf152-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf152-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf152-108">DESCRIPTION</span></span>
<span data-ttu-id="cf152-109">Das **Update-AzureRmDataFactoryV2IntegrationRuntime-** Cmdlet aktualisiert die Eigenschaften der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf152-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="cf152-110">Derzeit unterstützt das Cmdlet nur das Aktualisieren von "AutoUpdate" und "AutoUpdateDelayOffset" für die selbst gehostete Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf152-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="cf152-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cf152-111">EXAMPLES</span></span>

### <span data-ttu-id="cf152-112">Beispiel 1: Aktualisieren einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="cf152-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="cf152-113">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "Test-SelfHost-IR".</span><span class="sxs-lookup"><span data-stu-id="cf152-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cf152-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf152-114">PARAMETERS</span></span>

### <span data-ttu-id="cf152-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="cf152-115">-AutoUpdate</span></span>
<span data-ttu-id="cf152-116">Aktivieren oder Deaktivieren der automatischen Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf152-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="cf152-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="cf152-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="cf152-118">Die Uhrzeit in Stunden des Tages für die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf152-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="cf152-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cf152-119">-DataFactoryName</span></span>
<span data-ttu-id="cf152-120">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="cf152-120">The data factory name.</span></span>

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

### <span data-ttu-id="cf152-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf152-121">-DefaultProfile</span></span>
<span data-ttu-id="cf152-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cf152-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf152-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf152-123">-InputObject</span></span>
<span data-ttu-id="cf152-124">Das Integrationslauf Zeit Objekt.</span><span class="sxs-lookup"><span data-stu-id="cf152-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="cf152-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cf152-125">-Name</span></span>
<span data-ttu-id="cf152-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="cf152-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="cf152-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf152-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf152-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cf152-128">The resource group name.</span></span>

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

### <span data-ttu-id="cf152-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="cf152-129">-ResourceId</span></span>
<span data-ttu-id="cf152-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cf152-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="cf152-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="cf152-131">-Confirm</span></span>
<span data-ttu-id="cf152-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cf152-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf152-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf152-133">-WhatIf</span></span>
<span data-ttu-id="cf152-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cf152-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf152-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf152-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf152-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf152-136">CommonParameters</span></span>
<span data-ttu-id="cf152-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf152-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf152-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf152-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf152-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cf152-139">INPUTS</span></span>

### <span data-ttu-id="cf152-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cf152-140">System.String</span></span>

### <span data-ttu-id="cf152-141">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="cf152-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="cf152-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cf152-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="cf152-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cf152-143">OUTPUTS</span></span>

### <span data-ttu-id="cf152-144">Microsoft. Azure. Commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="cf152-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="cf152-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="cf152-145">NOTES</span></span>
<span data-ttu-id="cf152-146">Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Daten, Factorys, kopieren, Aktivitäten, Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="cf152-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="cf152-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cf152-147">RELATED LINKS</span></span>

<span data-ttu-id="cf152-148">[Satz-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="cf152-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 487a4592217ac725fa46ef717c6e556cc433fcb4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370346"
---
# <span data-ttu-id="ac8bd-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac8bd-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ac8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8bd-103">Aktualisiert eine Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="ac8bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac8bd-104">SYNTAX</span></span>

### <span data-ttu-id="ac8bd-105">ByIntegrationRuntimeName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac8bd-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac8bd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac8bd-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac8bd-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ac8bd-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac8bd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac8bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ac8bd-109">Das **Cmdlet "Update-AzDataFactoryV2IntegrationRuntime"** aktualisiert Integrationslaufzeiteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="ac8bd-110">Derzeit unterstützt das Cmdlet nur das Aktualisieren von "AutoUpdate" und "AutoUpdateDelayOffset" für selbst gehostete Integrationslaufzeiten.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="ac8bd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac8bd-111">EXAMPLES</span></span>

### <span data-ttu-id="ac8bd-112">Beispiel 1: Aktualisieren einer Integrationslaufzeit</span><span class="sxs-lookup"><span data-stu-id="ac8bd-112">Example 1: Updates an integration runtime</span></span>
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

<span data-ttu-id="ac8bd-113">Das Cmdlet aktualisiert die selbst gehostete Integrationslaufzeit mit dem Namen "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="ac8bd-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="ac8bd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac8bd-114">PARAMETERS</span></span>

### <span data-ttu-id="ac8bd-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ac8bd-115">-AutoUpdate</span></span>
<span data-ttu-id="ac8bd-116">Aktivieren oder deaktivieren Sie die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="ac8bd-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="ac8bd-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="ac8bd-118">Die Uhrzeit in Stunden des Tages für die automatische Aktualisierung der selbst gehosteten Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="ac8bd-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac8bd-119">-DataFactoryName</span></span>
<span data-ttu-id="ac8bd-120">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-120">The data factory name.</span></span>

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

### <span data-ttu-id="ac8bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8bd-121">-DefaultProfile</span></span>
<span data-ttu-id="ac8bd-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac8bd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac8bd-123">-InputObject</span></span>
<span data-ttu-id="ac8bd-124">Das Integrations-Runtime-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="ac8bd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ac8bd-125">-Name</span></span>
<span data-ttu-id="ac8bd-126">Der Name der Integrationslaufzeit.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="ac8bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac8bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac8bd-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-128">The resource group name.</span></span>

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

### <span data-ttu-id="ac8bd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac8bd-129">-ResourceId</span></span>
<span data-ttu-id="ac8bd-130">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ac8bd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac8bd-131">-Confirm</span></span>
<span data-ttu-id="ac8bd-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8bd-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ac8bd-133">-WhatIf</span></span>
<span data-ttu-id="ac8bd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac8bd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8bd-136">CommonParameters</span></span>
<span data-ttu-id="ac8bd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8bd-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac8bd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8bd-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac8bd-139">INPUTS</span></span>

### <span data-ttu-id="ac8bd-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ac8bd-140">System.String</span></span>

### <span data-ttu-id="ac8bd-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ac8bd-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ac8bd-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac8bd-142">OUTPUTS</span></span>

### <span data-ttu-id="ac8bd-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="ac8bd-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="ac8bd-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ac8bd-144">NOTES</span></span>
<span data-ttu-id="ac8bd-145">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys, copy, activities, integration runtime</span><span class="sxs-lookup"><span data-stu-id="ac8bd-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="ac8bd-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ac8bd-146">RELATED LINKS</span></span>

<span data-ttu-id="ac8bd-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
 [Get-AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="ac8bd-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>


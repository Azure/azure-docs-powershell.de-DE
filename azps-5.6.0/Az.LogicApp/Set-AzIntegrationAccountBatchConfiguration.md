---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: b1495f4b7473225697567ca3e9d87e98107ce001
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928992"
---
# <span data-ttu-id="42202-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42202-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="42202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42202-102">SYNOPSIS</span></span>
<span data-ttu-id="42202-103">Ändert die Batchkonfiguration eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="42202-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42202-104">SYNTAX</span></span>

### <span data-ttu-id="42202-105">ByIntegrationAccountAndParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="42202-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="42202-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="42202-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="42202-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="42202-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="42202-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="42202-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="42202-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42202-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="42202-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42202-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42202-114">DESCRIPTION</span></span>
<span data-ttu-id="42202-115">Das **Cmdlet Set-AzIntegrationAccountBatchConfiguration** ändert eine Batchkonfiguration eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="42202-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42202-116">EXAMPLES</span></span>

### <span data-ttu-id="42202-117">Beispiel 1: Ändern einer Batchkonfiguration mithilfe der lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="42202-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="42202-118">Ändern Sie eine Batchkonfiguration mit dem Namen "sampleBatchConfig" mithilfe der lokalen Datei, die sich im Dateipfad befindet, der in "$batchConfigurationFilePath" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="42202-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="42202-119">Beispiel 2: Ändern einer Batchkonfiguration mithilfe einer JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="42202-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="42202-120">Ändern Sie eine Batchkonfiguration mit dem Namen "sampleBatchConfig" mithilfe der in "$batchConfigurationContent" enthaltenen JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="42202-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="42202-121">Beispiel 3: Ändern einer Batchkonfiguration mithilfe von Parametern</span><span class="sxs-lookup"><span data-stu-id="42202-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="42202-122">Ändern Sie eine Batchkonfiguration namens "sampleBatchConfig", indem Sie alle erforderlichen Parameter manuell bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="42202-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="42202-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="42202-123">PARAMETERS</span></span>

### <span data-ttu-id="42202-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="42202-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="42202-125">Die Konfiguration der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-125">The integration account batch configuration definition.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndJson, ByInputObjectAndJson, ByResourceIdAndJson
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="42202-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="42202-127">Der Pfad für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-127">The integration account batch configuration file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="42202-128">-BatchGroupName</span></span>
<span data-ttu-id="42202-129">Name der Gruppengruppe für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-129">The integration account batch configuration group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="42202-130">-BatchSize</span></span>
<span data-ttu-id="42202-131">Batchkonfigurationsbatchgröße des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-131">The integration account batch configuration batch size.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42202-132">-DefaultProfile</span></span>
<span data-ttu-id="42202-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="42202-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42202-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42202-134">-InputObject</span></span>
<span data-ttu-id="42202-135">Batchkonfiguration eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-135">An integration account batch configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42202-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="42202-136">-MessageCount</span></span>
<span data-ttu-id="42202-137">Die Anzahl der Nachrichten für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-137">The integration account batch configuration message count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-138">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="42202-138">-Metadata</span></span>
<span data-ttu-id="42202-139">Die Metadaten für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-139">The integration account batch configuration metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-140">-Name</span><span class="sxs-lookup"><span data-stu-id="42202-140">-Name</span></span>
<span data-ttu-id="42202-141">Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-141">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="42202-142">-ParentName</span></span>
<span data-ttu-id="42202-143">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-143">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42202-144">-ResourceGroupName</span></span>
<span data-ttu-id="42202-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="42202-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByIntegrationAccountAndJson, ByIntegrationAccountAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42202-146">-ResourceId</span></span>
<span data-ttu-id="42202-147">Die Ressourcen-ID für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-147">The integration account batch configuration resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndJson, ByResourceIdAndFilePath, ByResourceIdAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42202-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="42202-148">-ScheduleFrequency</span></span>
<span data-ttu-id="42202-149">Die Häufigkeit der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-149">The integration account batch configuration schedule frequency.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:
Accepted values: Month, Week, Day, Hour, Minute, Second

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="42202-150">-ScheduleInterval</span></span>
<span data-ttu-id="42202-151">Das Zeitintervall für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-151">The integration account batch configuration schedule interval.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="42202-152">-ScheduleStartTime</span></span>
<span data-ttu-id="42202-153">Der Startzeitplan für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-153">The integration account batch configuration schedule start time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="42202-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="42202-155">Zeitzone für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="42202-155">The integration account batch configuration schedule time zone.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndParameters, ByInputObjectAndParameters, ByResourceIdAndParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42202-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42202-156">-Confirm</span></span>
<span data-ttu-id="42202-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42202-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42202-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42202-158">-WhatIf</span></span>
<span data-ttu-id="42202-159">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42202-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42202-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42202-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42202-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42202-161">CommonParameters</span></span>
<span data-ttu-id="42202-162">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42202-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42202-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42202-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42202-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42202-164">INPUTS</span></span>

### <span data-ttu-id="42202-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42202-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="42202-166">System.String</span><span class="sxs-lookup"><span data-stu-id="42202-166">System.String</span></span>

## <span data-ttu-id="42202-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42202-167">OUTPUTS</span></span>

### <span data-ttu-id="42202-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="42202-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="42202-169">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="42202-169">NOTES</span></span>

## <span data-ttu-id="42202-170">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="42202-170">RELATED LINKS</span></span>

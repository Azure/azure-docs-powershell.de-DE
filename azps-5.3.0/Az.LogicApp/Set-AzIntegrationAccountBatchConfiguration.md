---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 443f93d6e9099986c9412730ba24eae3655a2b48
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459091"
---
# <span data-ttu-id="e3806-101">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3806-101">Set-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e3806-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3806-102">SYNOPSIS</span></span>
<span data-ttu-id="e3806-103">Ändert die Konfiguration eines Integrationskontobatches.</span><span class="sxs-lookup"><span data-stu-id="e3806-103">Modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="e3806-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3806-104">SYNTAX</span></span>

### <span data-ttu-id="e3806-105">ByIntegrationAccountAndParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="e3806-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="e3806-106">ByIntegrationAccountAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e3806-107">ByIntegrationAccountAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="e3806-108">ByInputObjectAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e3806-109">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="e3806-110">ByInputObjectAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -InputObject <PSIntegrationAccountBatchConfiguration>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="e3806-111">ByResourceIdAndJson</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationDefinition <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e3806-112">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> -BatchConfigurationFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3806-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="e3806-113">ByResourceIdAndParameters</span></span>
```
Set-AzIntegrationAccountBatchConfiguration -ResourceId <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3806-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3806-114">DESCRIPTION</span></span>
<span data-ttu-id="e3806-115">Das **Cmdlet "Set-AzIntegrationAccountBatchConfiguration"** ändert die Batchkonfiguration eines Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-115">The **Set-AzIntegrationAccountBatchConfiguration** cmdlet modifies an integration account batch configuration.</span></span>

## <span data-ttu-id="e3806-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3806-116">EXAMPLES</span></span>

### <span data-ttu-id="e3806-117">Beispiel 1: Ändern einer Batchkonfiguration mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="e3806-117">Example 1: Modify a batch configuration using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e3806-118">Ändern Sie eine Batchkonfiguration namens "sampleBatchConfig" mit der lokalen Datei, die sich im Dateipfad in "$batchConfigurationFilePath" befindet.</span><span class="sxs-lookup"><span data-stu-id="e3806-118">Modify a batch configuration named "sampleBatchConfig" using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="e3806-119">Beispiel 2: Ändern einer Batchkonfiguration mithilfe einer JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e3806-119">Example 2: Modify a batch configuration using a JSON string</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e3806-120">Ändern Sie eine Batchkonfiguration namens "sampleBatchConfig" mithilfe der JSON-Zeichenfolge, die in "$batchConfigurationContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e3806-120">Modify a batch configuration named "sampleBatchConfig" using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="e3806-121">Beispiel 3: Ändern einer Batchkonfiguration mithilfe von Parametern</span><span class="sxs-lookup"><span data-stu-id="e3806-121">Example 3: Modify a batch configuration using parameters</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="e3806-122">Ändern Sie eine Batchkonfiguration namens "sampleBatchConfig", indem Sie alle erforderlichen Parameter manuell bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e3806-122">Modify a batch configuration named "sampleBatchConfig" by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="e3806-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3806-123">PARAMETERS</span></span>

### <span data-ttu-id="e3806-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="e3806-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="e3806-125">Die Konfigurationsdefinition für den Integrationskontobatch.</span><span class="sxs-lookup"><span data-stu-id="e3806-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="e3806-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="e3806-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="e3806-127">Der Konfigurationsdateipfad des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="e3806-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="e3806-128">-BatchGroupName</span></span>
<span data-ttu-id="e3806-129">Der Name der Gruppe für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="e3806-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="e3806-130">-BatchSize</span></span>
<span data-ttu-id="e3806-131">Die Batchkonfigurationsbatchgröße des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="e3806-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3806-132">-DefaultProfile</span></span>
<span data-ttu-id="e3806-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3806-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3806-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3806-134">-InputObject</span></span>
<span data-ttu-id="e3806-135">Eine Batchkonfiguration für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="e3806-135">An integration account batch configuration.</span></span>

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

### <span data-ttu-id="e3806-136">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="e3806-136">-MessageCount</span></span>
<span data-ttu-id="e3806-137">Die Anzahl der Nachrichten im Batchkonfigurationsbatch des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-137">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="e3806-138">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e3806-138">-Metadata</span></span>
<span data-ttu-id="e3806-139">Die Metadaten der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-139">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="e3806-140">-Name</span><span class="sxs-lookup"><span data-stu-id="e3806-140">-Name</span></span>
<span data-ttu-id="e3806-141">Der Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-141">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="e3806-142">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e3806-142">-ParentName</span></span>
<span data-ttu-id="e3806-143">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-143">The integration account name.</span></span>

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

### <span data-ttu-id="e3806-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3806-144">-ResourceGroupName</span></span>
<span data-ttu-id="e3806-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e3806-145">The resource group name.</span></span>

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

### <span data-ttu-id="e3806-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3806-146">-ResourceId</span></span>
<span data-ttu-id="e3806-147">Die Konfigurationsressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-147">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="e3806-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="e3806-148">-ScheduleFrequency</span></span>
<span data-ttu-id="e3806-149">Zeitplanhäufigkeit für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="e3806-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="e3806-150">-ScheduleInterval</span></span>
<span data-ttu-id="e3806-151">Das Zeitplanintervall für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="e3806-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="e3806-152">-ScheduleStartTime</span></span>
<span data-ttu-id="e3806-153">Startzeit des Batchkonfigurationszeitplans für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="e3806-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="e3806-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="e3806-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="e3806-155">Zeitzone des Zeitplans für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="e3806-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="e3806-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3806-156">-Confirm</span></span>
<span data-ttu-id="e3806-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3806-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3806-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e3806-158">-WhatIf</span></span>
<span data-ttu-id="e3806-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3806-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3806-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3806-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3806-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3806-161">CommonParameters</span></span>
<span data-ttu-id="e3806-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3806-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3806-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3806-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3806-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3806-164">INPUTS</span></span>

### <span data-ttu-id="e3806-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3806-165">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

### <span data-ttu-id="e3806-166">System.String</span><span class="sxs-lookup"><span data-stu-id="e3806-166">System.String</span></span>

## <span data-ttu-id="e3806-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3806-167">OUTPUTS</span></span>

### <span data-ttu-id="e3806-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3806-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="e3806-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3806-169">NOTES</span></span>

## <span data-ttu-id="e3806-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3806-170">RELATED LINKS</span></span>

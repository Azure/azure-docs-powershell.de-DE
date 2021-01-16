---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363626"
---
# <span data-ttu-id="396e9-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="396e9-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="396e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="396e9-102">SYNOPSIS</span></span>
<span data-ttu-id="396e9-103">Erstellt eine Batchkonfiguration für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="396e9-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="396e9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="396e9-104">SYNTAX</span></span>

### <span data-ttu-id="396e9-105">ByIntegrationAccountAndParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="396e9-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="396e9-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="396e9-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="396e9-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="396e9-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="396e9-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="396e9-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="396e9-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="396e9-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="396e9-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="396e9-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="396e9-114">DESCRIPTION</span></span>
<span data-ttu-id="396e9-115">Das **Cmdlet "Get-AzIntegrationAccountBatchConfiguration"** erstellt eine neue Batchkonfiguration in einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="396e9-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="396e9-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="396e9-116">EXAMPLES</span></span>

### <span data-ttu-id="396e9-117">Beispiel 1: Erstellen einer neuen Batchkonfiguration mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="396e9-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="396e9-118">Erstellt eine neue Batchkonfiguration unter Verwendung der lokalen Datei, die sich im Dateipfad in "$batchConfigurationFilePath" befindet.</span><span class="sxs-lookup"><span data-stu-id="396e9-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="396e9-119">Beispiel 2: Erstellen einer neuen Batchkonfiguration mithilfe einer JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="396e9-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="396e9-120">Erstellt eine neue Batchkonfiguration mit der in "$batchConfigurationContent" enthaltenen JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="396e9-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="396e9-121">Beispiel 3: Erstellen einer neuen Batchkonfiguration mithilfe von Parametern</span><span class="sxs-lookup"><span data-stu-id="396e9-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="396e9-122">Erstellt eine neue Batchkonfiguration, indem alle erforderlichen Parameter manuell angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="396e9-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="396e9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="396e9-123">PARAMETERS</span></span>

### <span data-ttu-id="396e9-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="396e9-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="396e9-125">Die Konfigurationsdefinition für den Integrationskontobatch.</span><span class="sxs-lookup"><span data-stu-id="396e9-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="396e9-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="396e9-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="396e9-127">Der Konfigurationsdateipfad des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="396e9-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="396e9-128">-BatchGroupName</span></span>
<span data-ttu-id="396e9-129">Der Name der Gruppe für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="396e9-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="396e9-130">-BatchSize</span></span>
<span data-ttu-id="396e9-131">Die Batchkonfigurationsbatchgröße des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="396e9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396e9-132">-DefaultProfile</span></span>
<span data-ttu-id="396e9-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="396e9-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="396e9-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="396e9-134">-MessageCount</span></span>
<span data-ttu-id="396e9-135">Die Anzahl der Nachrichten im Batchkonfigurationsbatch des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="396e9-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="396e9-136">-Metadata</span></span>
<span data-ttu-id="396e9-137">Die Metadaten der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="396e9-138">-Name</span><span class="sxs-lookup"><span data-stu-id="396e9-138">-Name</span></span>
<span data-ttu-id="396e9-139">Der Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-139">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396e9-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="396e9-140">-ParentName</span></span>
<span data-ttu-id="396e9-141">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-141">The integration account name.</span></span>

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

### <span data-ttu-id="396e9-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="396e9-142">-ParentObject</span></span>
<span data-ttu-id="396e9-143">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="396e9-143">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndJson, ByInputObjectAndFilePath, ByInputObjectAndParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="396e9-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="396e9-144">-ParentResourceId</span></span>
<span data-ttu-id="396e9-145">Die Konfigurationsressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="396e9-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396e9-146">-ResourceGroupName</span></span>
<span data-ttu-id="396e9-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="396e9-147">The resource group name.</span></span>

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

### <span data-ttu-id="396e9-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="396e9-148">-ScheduleFrequency</span></span>
<span data-ttu-id="396e9-149">Zeitplanhäufigkeit für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="396e9-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="396e9-150">-ScheduleInterval</span></span>
<span data-ttu-id="396e9-151">Das Zeitplanintervall für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="396e9-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="396e9-152">-ScheduleStartTime</span></span>
<span data-ttu-id="396e9-153">Startzeit des Batchkonfigurationszeitplans für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="396e9-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="396e9-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="396e9-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="396e9-155">Zeitzone des Zeitplans für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="396e9-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="396e9-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="396e9-156">-Confirm</span></span>
<span data-ttu-id="396e9-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="396e9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="396e9-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="396e9-158">-WhatIf</span></span>
<span data-ttu-id="396e9-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="396e9-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="396e9-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="396e9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="396e9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396e9-161">CommonParameters</span></span>
<span data-ttu-id="396e9-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396e9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396e9-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="396e9-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396e9-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="396e9-164">INPUTS</span></span>

### <span data-ttu-id="396e9-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="396e9-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="396e9-166">System.String</span><span class="sxs-lookup"><span data-stu-id="396e9-166">System.String</span></span>

## <span data-ttu-id="396e9-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="396e9-167">OUTPUTS</span></span>

### <span data-ttu-id="396e9-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="396e9-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="396e9-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="396e9-169">NOTES</span></span>

## <span data-ttu-id="396e9-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="396e9-170">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170399"
---
# <span data-ttu-id="192c1-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="192c1-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="192c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="192c1-102">SYNOPSIS</span></span>
<span data-ttu-id="192c1-103">Erstellt eine Batchkonfiguration für ein Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="192c1-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="192c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="192c1-104">SYNTAX</span></span>

### <span data-ttu-id="192c1-105">ByIntegrationAccountAndParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="192c1-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="192c1-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="192c1-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="192c1-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="192c1-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="192c1-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="192c1-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="192c1-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="192c1-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="192c1-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="192c1-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="192c1-114">DESCRIPTION</span></span>
<span data-ttu-id="192c1-115">Das **Cmdlet "Get-AzIntegrationAccountBatchConfiguration"** erstellt eine neue Batchkonfiguration in einem Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="192c1-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="192c1-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="192c1-116">EXAMPLES</span></span>

### <span data-ttu-id="192c1-117">Beispiel 1: Erstellen einer neuen Batchkonfiguration mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="192c1-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="192c1-118">Erstellt eine neue Batchkonfiguration unter Verwendung der lokalen Datei, die sich im Dateipfad in "$batchConfigurationFilePath" befindet.</span><span class="sxs-lookup"><span data-stu-id="192c1-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="192c1-119">Beispiel 2: Erstellen einer neuen Batchkonfiguration mithilfe einer JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="192c1-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="192c1-120">Erstellt eine neue Batchkonfiguration mit der in "$batchConfigurationContent" enthaltenen JSON-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="192c1-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="192c1-121">Beispiel 3: Erstellen einer neuen Batchkonfiguration mithilfe von Parametern</span><span class="sxs-lookup"><span data-stu-id="192c1-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="192c1-122">Erstellt eine neue Batchkonfiguration durch manuelles Bereitstellen aller erforderlichen Parameter.</span><span class="sxs-lookup"><span data-stu-id="192c1-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="192c1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="192c1-123">PARAMETERS</span></span>

### <span data-ttu-id="192c1-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="192c1-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="192c1-125">Die Konfigurationsdefinition für den Integrationskontobatch.</span><span class="sxs-lookup"><span data-stu-id="192c1-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="192c1-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="192c1-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="192c1-127">Der Konfigurationsdateipfad des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="192c1-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="192c1-128">-BatchGroupName</span></span>
<span data-ttu-id="192c1-129">Der Name der Gruppe für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="192c1-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="192c1-130">-BatchSize</span></span>
<span data-ttu-id="192c1-131">Die Batchkonfigurationsbatchgröße des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="192c1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="192c1-132">-DefaultProfile</span></span>
<span data-ttu-id="192c1-133">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="192c1-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="192c1-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="192c1-134">-MessageCount</span></span>
<span data-ttu-id="192c1-135">Die Anzahl der Nachrichten im Batchkonfigurationsbatch des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="192c1-136">-Metadata</span><span class="sxs-lookup"><span data-stu-id="192c1-136">-Metadata</span></span>
<span data-ttu-id="192c1-137">Die Metadaten der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="192c1-138">-Name</span><span class="sxs-lookup"><span data-stu-id="192c1-138">-Name</span></span>
<span data-ttu-id="192c1-139">Der Name der Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="192c1-140">-ParentName</span><span class="sxs-lookup"><span data-stu-id="192c1-140">-ParentName</span></span>
<span data-ttu-id="192c1-141">Der Name des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-141">The integration account name.</span></span>

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

### <span data-ttu-id="192c1-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="192c1-142">-ParentObject</span></span>
<span data-ttu-id="192c1-143">Ein Integrationskontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="192c1-143">An integration account object.</span></span>

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

### <span data-ttu-id="192c1-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="192c1-144">-ParentResourceId</span></span>
<span data-ttu-id="192c1-145">Die Konfigurationsressourcen-ID des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="192c1-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="192c1-146">-ResourceGroupName</span></span>
<span data-ttu-id="192c1-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="192c1-147">The resource group name.</span></span>

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

### <span data-ttu-id="192c1-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="192c1-148">-ScheduleFrequency</span></span>
<span data-ttu-id="192c1-149">Zeitplanhäufigkeit für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="192c1-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="192c1-150">-ScheduleInterval</span></span>
<span data-ttu-id="192c1-151">Das Zeitplanintervall für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="192c1-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="192c1-152">-ScheduleStartTime</span></span>
<span data-ttu-id="192c1-153">Startzeit des Batchkonfigurationszeitplans für das Integrationskonto.</span><span class="sxs-lookup"><span data-stu-id="192c1-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="192c1-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="192c1-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="192c1-155">Zeitzone des Zeitplans für die Batchkonfiguration des Integrationskontos.</span><span class="sxs-lookup"><span data-stu-id="192c1-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="192c1-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="192c1-156">-Confirm</span></span>
<span data-ttu-id="192c1-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="192c1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="192c1-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="192c1-158">-WhatIf</span></span>
<span data-ttu-id="192c1-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="192c1-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="192c1-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="192c1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="192c1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="192c1-161">CommonParameters</span></span>
<span data-ttu-id="192c1-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="192c1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="192c1-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="192c1-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="192c1-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="192c1-164">INPUTS</span></span>

### <span data-ttu-id="192c1-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="192c1-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="192c1-166">System.String</span><span class="sxs-lookup"><span data-stu-id="192c1-166">System.String</span></span>

## <span data-ttu-id="192c1-167">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="192c1-167">OUTPUTS</span></span>

### <span data-ttu-id="192c1-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="192c1-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="192c1-169">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="192c1-169">NOTES</span></span>

## <span data-ttu-id="192c1-170">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="192c1-170">RELATED LINKS</span></span>

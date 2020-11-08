---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: c31768cff6af5f36212dbf32b08b016fa47c8a63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180354"
---
# <span data-ttu-id="1ae1b-101">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ae1b-101">New-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1ae1b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1ae1b-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae1b-103">Erstellt eine batchkonfiguration für das Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-103">Creates an integration account batch configuration.</span></span>

## <span data-ttu-id="1ae1b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ae1b-104">SYNTAX</span></span>

### <span data-ttu-id="1ae1b-105">ByIntegrationAccountAndParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="1ae1b-105">ByIntegrationAccountAndParameters (Default)</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-106">ByIntegrationAccountAndJson</span><span class="sxs-lookup"><span data-stu-id="1ae1b-106">ByIntegrationAccountAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-107">ByIntegrationAccountAndFilePath</span><span class="sxs-lookup"><span data-stu-id="1ae1b-107">ByIntegrationAccountAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-108">ByInputObjectAndJson</span><span class="sxs-lookup"><span data-stu-id="1ae1b-108">ByInputObjectAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-109">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="1ae1b-109">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-110">ByInputObjectAndParameters</span><span class="sxs-lookup"><span data-stu-id="1ae1b-110">ByInputObjectAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> -Name <String>
 [-BatchGroupName <String>] [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>]
 [-ScheduleFrequency <String>] [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-111">ByResourceIdAndJson</span><span class="sxs-lookup"><span data-stu-id="1ae1b-111">ByResourceIdAndJson</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationDefinition <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-112">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="1ae1b-112">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String>
 -BatchConfigurationFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ae1b-113">ByResourceIdAndParameters</span><span class="sxs-lookup"><span data-stu-id="1ae1b-113">ByResourceIdAndParameters</span></span>
```
New-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> -Name <String> [-BatchGroupName <String>]
 [-MessageCount <Int32>] [-BatchSize <Int32>] [-ScheduleInterval <Int32>] [-ScheduleFrequency <String>]
 [-ScheduleTimeZone <String>] [-ScheduleStartTime <DateTime>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ae1b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1ae1b-114">DESCRIPTION</span></span>
<span data-ttu-id="1ae1b-115">Das Cmdlet " **Get-AzIntegrationAccountBatchConfiguration** " erstellt eine neue batchkonfiguration in einem Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-115">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet creates a new batch configuration in an integration account.</span></span>

## <span data-ttu-id="1ae1b-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1ae1b-116">EXAMPLES</span></span>

### <span data-ttu-id="1ae1b-117">Beispiel 1: Erstellen einer neuen batchkonfiguration mithilfe einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="1ae1b-117">Example 1: Create new batch configuration using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationFilePath $batchConfigurationFilePath

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1ae1b-118">Erstellt eine neue batchkonfiguration unter Verwendung der lokalen Datei, die sich im Dateipfad befindet, der in "$batchConfigurationFilePath" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-118">Creates a new batch configuration using the local file located at the file path contained in "$batchConfigurationFilePath".</span></span>

### <span data-ttu-id="1ae1b-119">Beispiel 2: Erstellen einer neuen batchkonfiguration mithilfe einer JSON-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1ae1b-119">Example 2: Create new batch configuration using a JSON string</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -BatchConfigurationDefinition $batchConfigurationContent

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1ae1b-120">Erstellt eine neue batchkonfiguration mithilfe der JSON-Zeichenfolge, die in "$batchConfigurationContent" enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-120">Creates a new batch configuration using the a JSON string contained in "$batchConfigurationContent".</span></span>

### <span data-ttu-id="1ae1b-121">Beispiel 3: Erstellen einer neuen batchkonfiguration mithilfe von Parametern</span><span class="sxs-lookup"><span data-stu-id="1ae1b-121">Example 3: Create new batch configuration using parameters</span></span>
```powershell
PS C:\> New-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig" -MessageCount 199 -BatchSize 5 -ScheduleInterval 1 -ScheduleFrequency "Month"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="1ae1b-122">Erstellt eine neue batchkonfiguration, indem alle erforderlichen Parameter manuell bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-122">Creates a new batch configuration by manually providing all of the necessary parameters.</span></span>

## <span data-ttu-id="1ae1b-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ae1b-123">PARAMETERS</span></span>

### <span data-ttu-id="1ae1b-124">-BatchConfigurationDefinition</span><span class="sxs-lookup"><span data-stu-id="1ae1b-124">-BatchConfigurationDefinition</span></span>
<span data-ttu-id="1ae1b-125">Die Konfigurationsdefinition für das Integrations Konto-Batch.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-125">The integration account batch configuration definition.</span></span>

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

### <span data-ttu-id="1ae1b-126">-BatchConfigurationFilePath</span><span class="sxs-lookup"><span data-stu-id="1ae1b-126">-BatchConfigurationFilePath</span></span>
<span data-ttu-id="1ae1b-127">Der Pfad für die Konfigurationsdatei des Integrations Konto-Batches.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-127">The integration account batch configuration file path.</span></span>

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

### <span data-ttu-id="1ae1b-128">-BatchGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae1b-128">-BatchGroupName</span></span>
<span data-ttu-id="1ae1b-129">Der Gruppenname der Integrations Konto-batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-129">The integration account batch configuration group name.</span></span>

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

### <span data-ttu-id="1ae1b-130">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="1ae1b-130">-BatchSize</span></span>
<span data-ttu-id="1ae1b-131">Die Batchgröße der batchkonfiguration für das Integrations Konto.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-131">The integration account batch configuration batch size.</span></span>

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

### <span data-ttu-id="1ae1b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae1b-132">-DefaultProfile</span></span>
<span data-ttu-id="1ae1b-133">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae1b-134">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="1ae1b-134">-MessageCount</span></span>
<span data-ttu-id="1ae1b-135">Die Anzahl der Konfigurations Nachrichten in der Integrations Konto-batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-135">The integration account batch configuration message count.</span></span>

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

### <span data-ttu-id="1ae1b-136">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1ae1b-136">-Metadata</span></span>
<span data-ttu-id="1ae1b-137">Die Metadaten für die batchkonfiguration der Integrations Konten.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-137">The integration account batch configuration metadata.</span></span>

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

### <span data-ttu-id="1ae1b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="1ae1b-138">-Name</span></span>
<span data-ttu-id="1ae1b-139">Der Konfigurationsname des Integrations Konto-Batches.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-139">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="1ae1b-140">-Übergeordneter</span><span class="sxs-lookup"><span data-stu-id="1ae1b-140">-ParentName</span></span>
<span data-ttu-id="1ae1b-141">Der Name des Integrations Kontos.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-141">The integration account name.</span></span>

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

### <span data-ttu-id="1ae1b-142">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1ae1b-142">-ParentObject</span></span>
<span data-ttu-id="1ae1b-143">Ein Integrations Kontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-143">An integration account object.</span></span>

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

### <span data-ttu-id="1ae1b-144">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1ae1b-144">-ParentResourceId</span></span>
<span data-ttu-id="1ae1b-145">Die Ressourcen-ID der Integrations Konto-batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-145">The integration account batch configuration resource id.</span></span>

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

### <span data-ttu-id="1ae1b-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae1b-146">-ResourceGroupName</span></span>
<span data-ttu-id="1ae1b-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-147">The resource group name.</span></span>

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

### <span data-ttu-id="1ae1b-148">-ScheduleFrequency</span><span class="sxs-lookup"><span data-stu-id="1ae1b-148">-ScheduleFrequency</span></span>
<span data-ttu-id="1ae1b-149">Die Häufigkeit des Terminplans für das Integrations Konto für batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-149">The integration account batch configuration schedule frequency.</span></span>

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

### <span data-ttu-id="1ae1b-150">-ScheduleInterval</span><span class="sxs-lookup"><span data-stu-id="1ae1b-150">-ScheduleInterval</span></span>
<span data-ttu-id="1ae1b-151">Das Zeitplan Intervall für das Integrations Konto-batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-151">The integration account batch configuration schedule interval.</span></span>

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

### <span data-ttu-id="1ae1b-152">-ScheduleStartTime</span><span class="sxs-lookup"><span data-stu-id="1ae1b-152">-ScheduleStartTime</span></span>
<span data-ttu-id="1ae1b-153">Die Start Zeit für das Integrations Konto in der batchkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-153">The integration account batch configuration schedule start time.</span></span>

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

### <span data-ttu-id="1ae1b-154">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="1ae1b-154">-ScheduleTimeZone</span></span>
<span data-ttu-id="1ae1b-155">Das Integrations Konto-batchkonfiguration-Zeit Zonen Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-155">The integration account batch configuration schedule time zone.</span></span>

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

### <span data-ttu-id="1ae1b-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1ae1b-156">-Confirm</span></span>
<span data-ttu-id="1ae1b-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ae1b-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ae1b-158">-WhatIf</span></span>
<span data-ttu-id="1ae1b-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ae1b-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ae1b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae1b-161">CommonParameters</span></span>
<span data-ttu-id="1ae1b-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae1b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae1b-163">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ae1b-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae1b-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1ae1b-164">INPUTS</span></span>

### <span data-ttu-id="1ae1b-165">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1ae1b-165">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="1ae1b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="1ae1b-166">System.String</span></span>

## <span data-ttu-id="1ae1b-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1ae1b-167">OUTPUTS</span></span>

### <span data-ttu-id="1ae1b-168">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ae1b-168">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="1ae1b-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="1ae1b-169">NOTES</span></span>

## <span data-ttu-id="1ae1b-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1ae1b-170">RELATED LINKS</span></span>

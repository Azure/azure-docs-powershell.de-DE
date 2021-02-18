---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: a1ccbf6ee912c26bc4ecbe3b58a9db12dac112e6
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409714"
---
# <span data-ttu-id="b3480-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b3480-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="b3480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3480-102">SYNOPSIS</span></span>
<span data-ttu-id="b3480-103">Legt die Protokoll- und Metrikeinstellungen für die Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="b3480-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="b3480-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3480-104">SYNTAX</span></span>

### <span data-ttu-id="b3480-105">OldSetDiagnosticSetting (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3480-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-ExportToResourceSpecific] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3480-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="b3480-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3480-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3480-107">DESCRIPTION</span></span>
<span data-ttu-id="b3480-108">Das **Cmdlet "Set-AzDiagnosticSetting"** aktiviert oder deaktiviert jedes "Grain" und "log category" für die bestimmte Ressource.</span><span class="sxs-lookup"><span data-stu-id="b3480-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="b3480-109">Die Protokolle und Metriken werden im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b3480-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="b3480-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b3480-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b3480-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3480-111">EXAMPLES</span></span>

### <span data-ttu-id="b3480-112">Beispiel 1: Aktivieren aller Metriken und Protokolle für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="b3480-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="b3480-113">Dieser Befehl aktiviert alle verfügbaren Metriken und Protokolle für "Resource01".</span><span class="sxs-lookup"><span data-stu-id="b3480-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="b3480-114">Beispiel 2: Deaktivieren aller Metriken und Protokolle</span><span class="sxs-lookup"><span data-stu-id="b3480-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="b3480-115">Mit diesem Befehl werden alle verfügbaren Metriken und Protokolle für die Ressource "Resource01" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3480-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="b3480-116">Beispiel 3: Aktivieren/Deaktivieren mehrerer Metrikkategorien</span><span class="sxs-lookup"><span data-stu-id="b3480-116">Example 3: Enable/disable multiple metrics categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False -MetricCategory MetricCategory1,MetricCategory2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="b3480-117">Mit diesem Befehl werden die Metrikkategorien "Kategorie1" und "Kategorie2" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3480-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="b3480-118">Alle anderen Kategorien bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="b3480-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="b3480-119">Beispiel 4: Aktivieren/Deaktivieren mehrerer Protokollkategorien</span><span class="sxs-lookup"><span data-stu-id="b3480-119">Example 4: Enable/disable multiple log categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
   Enabled   : False
   Category  : MetricCategory1
   Timegrain : PT1M
   Enabled   : False
   Category  : MetricCategory2
   Timegrain : PT1H
   Enabled   : True
   Category  : MetricCategory3
   Timegrain : PT1H
Logs
   Enabled  : True
   Category : Category1
   Enabled  : True
   Category : Category2
   Enabled  : True
   Category : Category3
   Enabled  : False
   Category : Category4
```

<span data-ttu-id="b3480-120">Mit diesem Befehl werden "Kategorie1" und "Kategorie2" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3480-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="b3480-121">Alle anderen Metriken und Protokollkategorien bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="b3480-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="b3480-122">Beispiel 4: Aktivieren einer Zeitmask und mehrerer Kategorien</span><span class="sxs-lookup"><span data-stu-id="b3480-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="b3480-123">Dieser Befehl aktiviert nur "Kategorie1", "Kategorie2" und "Zeitmask PT1M".</span><span class="sxs-lookup"><span data-stu-id="b3480-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="b3480-124">Alle anderen Zeitkörner und Kategorien bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="b3480-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="b3480-125">Beispiel 5: Verwenden der Pipeline</span><span class="sxs-lookup"><span data-stu-id="b3480-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting -Enabled $True -Category Category1,Category2
```

<span data-ttu-id="b3480-126">Dieser Befehl verwendet die PowerShell-Pipeline, um eine Diagnoseeinstellung (ohne Änderung) festlegen.</span><span class="sxs-lookup"><span data-stu-id="b3480-126">This command uses the PowerShell pipeline to set (no change made) a diagnostic setting.</span></span>

## <span data-ttu-id="b3480-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3480-127">PARAMETERS</span></span>

### <span data-ttu-id="b3480-128">-Category</span><span class="sxs-lookup"><span data-stu-id="b3480-128">-Category</span></span>
<span data-ttu-id="b3480-129">Gibt die Liste der zu aktivierenden oder zu deaktivierenden Protokollkategorien entsprechend dem Wert von *"Enabled" an.*</span><span class="sxs-lookup"><span data-stu-id="b3480-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="b3480-130">Wenn keine Kategorie angegeben ist, gilt dieser Befehl für alle unterstützten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3480-130">If no category is specified, this command operates on all supported categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3480-131">-DefaultProfile</span></span>
<span data-ttu-id="b3480-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3480-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3480-133">-Enabled</span><span class="sxs-lookup"><span data-stu-id="b3480-133">-Enabled</span></span>
<span data-ttu-id="b3480-134">Gibt an, ob die Diagnose aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3480-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="b3480-135">Geben $True, um die Diagnose zu aktivieren, oder $False, um die Diagnose zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="b3480-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="b3480-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="b3480-137">Die Id der Ereignishubautorisierungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="b3480-137">The event hub authorization rule id</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="b3480-138">-EventHubName</span></span>
<span data-ttu-id="b3480-139">Der Name des Ereignishubs</span><span class="sxs-lookup"><span data-stu-id="b3480-139">The event hub name</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-140">-ExportToResourceSpecific</span><span class="sxs-lookup"><span data-stu-id="b3480-140">-ExportToResourceSpecific</span></span>
<span data-ttu-id="b3480-141">Flag, das angibt, dass der Export nach LA in eine ressourcenspezifische Tabelle ,a.k.a. ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="b3480-141">Flag indicating that the export to LA must be done to a resource specific table, a.k.a.</span></span> <span data-ttu-id="b3480-142">dedizierte oder feste Schematabelle im  Gegensatz zur standardmäßigen dynamischen Schematabelle **"AzureDiagnostics".**</span><span class="sxs-lookup"><span data-stu-id="b3480-142">dedicated or fixed schema table, as opposed to the **default** dynamic schema table called **AzureDiagnostics**.</span></span>

<span data-ttu-id="b3480-143">Dieses Argument ist nur wirksam, wenn das Argument **"-workspaceId"** ebenfalls angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b3480-143">This argument is effective only when the argument **-workspaceId** is also given.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3480-144">-InputObject</span></span>
<span data-ttu-id="b3480-145">Das Eingabeobjekt (möglich über die Pipeline) Der Name und die resourceId werden aus diesem Objekt extrahiert.</span><span class="sxs-lookup"><span data-stu-id="b3480-145">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings
Parameter Sets: NewSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-146">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="b3480-146">-MetricCategory</span></span>
<span data-ttu-id="b3480-147">Die Liste der metrischen Kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3480-147">The list of metric categories.</span></span>
<span data-ttu-id="b3480-148">Wenn keine Kategorie angegeben ist, gilt dieser Befehl für alle unterstützten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="b3480-148">If no category is specified, this command operates on all supported categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-149">-Name</span><span class="sxs-lookup"><span data-stu-id="b3480-149">-Name</span></span>
<span data-ttu-id="b3480-150">Der Name der Diagnoseeinstellung.</span><span class="sxs-lookup"><span data-stu-id="b3480-150">The name of the diagnostic setting.</span></span> <span data-ttu-id="b3480-151">Der Standardwert ist **"service".**</span><span class="sxs-lookup"><span data-stu-id="b3480-151">The default value is **service**.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3480-152">-ResourceId</span></span>
<span data-ttu-id="b3480-153">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="b3480-153">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-154">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="b3480-154">-RetentionEnabled</span></span>
<span data-ttu-id="b3480-155">Gibt an, ob die Aufbewahrung von Diagnoseinformationen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b3480-155">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-156">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b3480-156">-RetentionInDays</span></span>
<span data-ttu-id="b3480-157">Gibt die Aufbewahrungsrichtlinie in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="b3480-157">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-158">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="b3480-158">-ServiceBusRuleId</span></span>
<span data-ttu-id="b3480-159">Die Regel-ID des Dienstbuss.</span><span class="sxs-lookup"><span data-stu-id="b3480-159">The Service Bus Rule id.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-160">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b3480-160">-StorageAccountId</span></span>
<span data-ttu-id="b3480-161">Gibt die ID des Speicherkontos an, in dem die Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b3480-161">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-162">-Timegrain</span><span class="sxs-lookup"><span data-stu-id="b3480-162">-Timegrain</span></span>
<span data-ttu-id="b3480-163">Gibt die Zeitkörner an, die entsprechend dem Wert von "Enabled" für Metriken aktiviert oder deaktiviert *werden sollen.*</span><span class="sxs-lookup"><span data-stu-id="b3480-163">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="b3480-164">Wenn Sie keine Zeitkörner angeben, wird dieser Befehl für alle verfügbaren Zeitkörner ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3480-164">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-165">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b3480-165">-WorkspaceId</span></span>
<span data-ttu-id="b3480-166">Die Ressourcen-ID des Log Analytics-Arbeitsbereichs, an den Protokolle/Metriken gesendet werden</span><span class="sxs-lookup"><span data-stu-id="b3480-166">The resource Id of the Log Analytics workspace to send logs/metrics to</span></span>

```yaml
Type: System.String
Parameter Sets: OldSetDiagnosticSetting
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3480-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3480-167">-Confirm</span></span>
<span data-ttu-id="b3480-168">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3480-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3480-169">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b3480-169">-WhatIf</span></span>
<span data-ttu-id="b3480-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3480-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3480-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3480-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3480-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3480-172">CommonParameters</span></span>
<span data-ttu-id="b3480-173">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3480-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3480-174">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3480-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3480-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3480-175">INPUTS</span></span>

### <span data-ttu-id="b3480-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="b3480-176">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="b3480-177">System.String</span><span class="sxs-lookup"><span data-stu-id="b3480-177">System.String</span></span>

### <span data-ttu-id="b3480-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3480-178">System.Boolean</span></span>

### <span data-ttu-id="b3480-179">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b3480-179">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b3480-180">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b3480-180">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b3480-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b3480-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b3480-182">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3480-182">OUTPUTS</span></span>

### <span data-ttu-id="b3480-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="b3480-183">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="b3480-184">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3480-184">NOTES</span></span>

## <span data-ttu-id="b3480-185">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3480-185">RELATED LINKS</span></span>

<span data-ttu-id="b3480-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="b3480-186">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>

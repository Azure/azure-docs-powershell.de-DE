---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDiagnosticSetting.md
ms.openlocfilehash: bcebb7e4e272a22878c240946f04ffd5013a8999
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822623"
---
# <span data-ttu-id="d4e78-101">Set-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4e78-101">Set-AzDiagnosticSetting</span></span>

## <span data-ttu-id="d4e78-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4e78-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e78-103">Legt die Einstellungen für Protokolle und Metriken für die Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="d4e78-103">Sets the logs and metrics settings for the resource.</span></span>

## <span data-ttu-id="d4e78-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4e78-104">SYNTAX</span></span>

### <span data-ttu-id="d4e78-105">OldSetDiagnosticSetting (Standard)</span><span class="sxs-lookup"><span data-stu-id="d4e78-105">OldSetDiagnosticSetting (Default)</span></span>
```
Set-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-StorageAccountId <String>]
 [-ServiceBusRuleId <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleId <String>]
 [-Enabled <Boolean>] [-Category <System.Collections.Generic.List`1[System.String]>]
 [-MetricCategory <System.Collections.Generic.List`1[System.String]>]
 [-Timegrain <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e78-106">NewSetDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d4e78-106">NewSetDiagnosticSetting</span></span>
```
Set-AzDiagnosticSetting -InputObject <PSServiceDiagnosticSettings> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e78-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4e78-107">DESCRIPTION</span></span>
<span data-ttu-id="d4e78-108">Das Cmdlet " **Satz-AzDiagnosticSetting** " aktiviert oder deaktiviert jede Zeit Körnung und Protokoll Kategorie für die jeweilige Ressource.</span><span class="sxs-lookup"><span data-stu-id="d4e78-108">The **Set-AzDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>
<span data-ttu-id="d4e78-109">Die Protokolle und Metriken werden im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d4e78-109">The logs and metrics are stored in the specified storage account.</span></span>
<span data-ttu-id="d4e78-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d4e78-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="d4e78-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4e78-111">EXAMPLES</span></span>

### <span data-ttu-id="d4e78-112">Beispiel 1: Aktivieren aller Metriken und Protokolle für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="d4e78-112">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="d4e78-113">Dieser Befehl aktiviert alle verfügbaren Metriken und Protokolle für Resource01.</span><span class="sxs-lookup"><span data-stu-id="d4e78-113">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="d4e78-114">Beispiel 2: Deaktivieren aller Metriken und Protokolle</span><span class="sxs-lookup"><span data-stu-id="d4e78-114">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="d4e78-115">Mit diesem Befehl werden alle verfügbaren Metriken und Protokolle für die Ressource Resource01 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d4e78-115">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="d4e78-116">Beispiel 3: Aktivieren/Deaktivieren mehrerer Metriken Kategorien</span><span class="sxs-lookup"><span data-stu-id="d4e78-116">Example 3: Enable/disable multiple metrics categories</span></span>
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

<span data-ttu-id="d4e78-117">Mit diesem Befehl werden die Metriken Kategorien "Kategorie1" und "Kategorie2" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d4e78-117">This command disables the metrics categories called Category1 and Category2.</span></span>
<span data-ttu-id="d4e78-118">Alle anderen Kategorien bleiben identisch.</span><span class="sxs-lookup"><span data-stu-id="d4e78-118">All the other categories remain the same.</span></span>

### <span data-ttu-id="d4e78-119">Beispiel 4: Aktivieren/Deaktivieren mehrerer Protokollkategorien</span><span class="sxs-lookup"><span data-stu-id="d4e78-119">Example 4: Enable/disable multiple log categories</span></span>
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

<span data-ttu-id="d4e78-120">Dieser Befehl aktiviert Kategorie1 und Kategorie2.</span><span class="sxs-lookup"><span data-stu-id="d4e78-120">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="d4e78-121">Alle anderen Metriken und Protokollkategorien bleiben identisch.</span><span class="sxs-lookup"><span data-stu-id="d4e78-121">All the other metrics and logs categories remain the same.</span></span>

### <span data-ttu-id="d4e78-122">Beispiel 4: Aktivieren einer Zeit Körnung und mehrerer Kategorien</span><span class="sxs-lookup"><span data-stu-id="d4e78-122">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Category Category1,Category2 -Timegrain PT1M
```

<span data-ttu-id="d4e78-123">Dieser Befehl aktiviert nur Kategorie1-, Kategorie2-und Time Grain-PT1M.</span><span class="sxs-lookup"><span data-stu-id="d4e78-123">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="d4e78-124">Alle anderen Zeit Körnungen und-Kategorien sind unverändert.</span><span class="sxs-lookup"><span data-stu-id="d4e78-124">All other time grains and categories are unchanged.</span></span>

### <span data-ttu-id="d4e78-125">Beispiel 5: Verwenden von Pipeline</span><span class="sxs-lookup"><span data-stu-id="d4e78-125">Example 5: Using pipeline</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "Resource01" | Set-AzDiagnosticSetting
```

<span data-ttu-id="d4e78-126">Dieser Befehl verwendet die PowerShell-Pipeline, um eine Diagnose Einstellung festzulegen (nicht geändert).</span><span class="sxs-lookup"><span data-stu-id="d4e78-126">This command uses the PowerShell pipeline to set (not change made) a diagnostic setting.</span></span>

## <span data-ttu-id="d4e78-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4e78-127">PARAMETERS</span></span>

### <span data-ttu-id="d4e78-128">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="d4e78-128">-Category</span></span>
<span data-ttu-id="d4e78-129">Gibt die Liste der Protokollkategorien an, die entsprechend dem Wert von *Enabled aktiviert* oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4e78-129">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="d4e78-130">Wenn keine Kategorie angegeben wird, funktioniert dieser Befehl für alle unterstützten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="d4e78-130">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="d4e78-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e78-131">-DefaultProfile</span></span>
<span data-ttu-id="d4e78-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d4e78-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e78-133">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="d4e78-133">-Enabled</span></span>
<span data-ttu-id="d4e78-134">Gibt an, ob die Diagnose aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4e78-134">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="d4e78-135">Geben Sie $true an, um die Diagnose zu aktivieren, oder $false, um die Diagnose zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d4e78-135">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

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

### <span data-ttu-id="d4e78-136">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="d4e78-136">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="d4e78-137">Die Ereignis-Hub-Autorisierungsregel-ID</span><span class="sxs-lookup"><span data-stu-id="d4e78-137">The event hub authorization rule id</span></span>

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

### <span data-ttu-id="d4e78-138">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="d4e78-138">-EventHubName</span></span>
<span data-ttu-id="d4e78-139">Der Name des Ereignis Hubs</span><span class="sxs-lookup"><span data-stu-id="d4e78-139">The event hub name</span></span>

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

### <span data-ttu-id="d4e78-140">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4e78-140">-InputObject</span></span>
<span data-ttu-id="d4e78-141">Das Eingabeobjekt (möglich aus der Pipeline.) Der Name und die Quell-Nr werden aus diesem Objekt extrahiert.</span><span class="sxs-lookup"><span data-stu-id="d4e78-141">The input object (possible from the pipeline.) The name and resourceId will be extracted from this object.</span></span>

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

### <span data-ttu-id="d4e78-142">-MetricCategory</span><span class="sxs-lookup"><span data-stu-id="d4e78-142">-MetricCategory</span></span>
<span data-ttu-id="d4e78-143">Die Liste der metrischen Kategorien.</span><span class="sxs-lookup"><span data-stu-id="d4e78-143">The list of metric categories.</span></span> <span data-ttu-id="d4e78-144">Wenn keine Kategorie angegeben wird, funktioniert dieser Befehl für alle unterstützten Kategorien.</span><span class="sxs-lookup"><span data-stu-id="d4e78-144">If no category is specified, this command operates on all supported categories.</span></span> 

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

### <span data-ttu-id="d4e78-145">-Name</span><span class="sxs-lookup"><span data-stu-id="d4e78-145">-Name</span></span>
<span data-ttu-id="d4e78-146">Der Name der Diagnose Einstellung.</span><span class="sxs-lookup"><span data-stu-id="d4e78-146">The name of the diagnostic setting.</span></span> <span data-ttu-id="d4e78-147">Der Standardwert ist **Service**.</span><span class="sxs-lookup"><span data-stu-id="d4e78-147">The default value is **service**.</span></span>

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

### <span data-ttu-id="d4e78-148">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d4e78-148">-ResourceId</span></span>
<span data-ttu-id="d4e78-149">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="d4e78-149">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="d4e78-150">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="d4e78-150">-RetentionEnabled</span></span>
<span data-ttu-id="d4e78-151">Gibt an, ob die Beibehaltung von Diagnoseinformationen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d4e78-151">Indicates whether retention of diagnostic information is enabled.</span></span>

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

### <span data-ttu-id="d4e78-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d4e78-152">-RetentionInDays</span></span>
<span data-ttu-id="d4e78-153">Gibt die Aufbewahrungsrichtlinie in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="d4e78-153">Specifies the retention policy, in days.</span></span>

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

### <span data-ttu-id="d4e78-154">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="d4e78-154">-ServiceBusRuleId</span></span>
<span data-ttu-id="d4e78-155">Die ServiceBus-Regel-ID.</span><span class="sxs-lookup"><span data-stu-id="d4e78-155">The Service Bus Rule id.</span></span>

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

### <span data-ttu-id="d4e78-156">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d4e78-156">-StorageAccountId</span></span>
<span data-ttu-id="d4e78-157">Gibt die ID des speicherkontos an, in dem die Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4e78-157">Specifies the ID of the Storage account in which to save the data.</span></span>

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

### <span data-ttu-id="d4e78-158">-Zeitkorn</span><span class="sxs-lookup"><span data-stu-id="d4e78-158">-Timegrain</span></span>
<span data-ttu-id="d4e78-159">Gibt die Zeit Körnungen an, die für Metriken entsprechend dem Wert von *Enabled aktiviert* oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4e78-159">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="d4e78-160">Wenn Sie kein Zeit Korn angeben, wird dieser Befehl für alle verfügbaren Zeit Körnungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4e78-160">If you do not specify a time grain, this command operates on all available time grains.</span></span>

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

### <span data-ttu-id="d4e78-161">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="d4e78-161">-WorkspaceId</span></span>
<span data-ttu-id="d4e78-162">Die ID des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="d4e78-162">The Id of the workspace</span></span>

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

### <span data-ttu-id="d4e78-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4e78-163">-Confirm</span></span>
<span data-ttu-id="d4e78-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4e78-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e78-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e78-165">-WhatIf</span></span>
<span data-ttu-id="d4e78-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4e78-166">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4e78-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4e78-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e78-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e78-168">CommonParameters</span></span>
<span data-ttu-id="d4e78-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e78-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e78-170">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4e78-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e78-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4e78-171">INPUTS</span></span>

### <span data-ttu-id="d4e78-172">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="d4e78-172">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

### <span data-ttu-id="d4e78-173">System. String</span><span class="sxs-lookup"><span data-stu-id="d4e78-173">System.String</span></span>

### <span data-ttu-id="d4e78-174">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4e78-174">System.Boolean</span></span>

### <span data-ttu-id="d4e78-175">System. Collections. Generic. List ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e78-175">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d4e78-176">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e78-176">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d4e78-177">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e78-177">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d4e78-178">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4e78-178">OUTPUTS</span></span>

### <span data-ttu-id="d4e78-179">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="d4e78-179">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="d4e78-180">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4e78-180">NOTES</span></span>

## <span data-ttu-id="d4e78-181">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4e78-181">RELATED LINKS</span></span>

<span data-ttu-id="d4e78-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="d4e78-182">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>

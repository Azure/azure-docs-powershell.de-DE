---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663573"
---
# <span data-ttu-id="15fc4-101">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="15fc4-101">Set-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="15fc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="15fc4-103">Legt die Einstellungen für Protokolle und Metriken für die Ressource fest.</span><span class="sxs-lookup"><span data-stu-id="15fc4-103">Sets the logs and metrics settings for the resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15fc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15fc4-104">SYNTAX</span></span>

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15fc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="15fc4-106">Das Cmdlet " **Satz-AzureRmDiagnosticSetting** " aktiviert oder deaktiviert jede Zeit Körnung und Protokoll Kategorie für die jeweilige Ressource.</span><span class="sxs-lookup"><span data-stu-id="15fc4-106">The **Set-AzureRmDiagnosticSetting** cmdlet enables or disables each time grain and log category for the particular resource.</span></span>

<span data-ttu-id="15fc4-107">Die Protokolle und Metriken werden im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="15fc4-107">The logs and metrics are stored in the specified storage account.</span></span>

## <span data-ttu-id="15fc4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15fc4-108">EXAMPLES</span></span>

### <span data-ttu-id="15fc4-109">Beispiel 1: Aktivieren aller Metriken und Protokolle für eine Ressource</span><span class="sxs-lookup"><span data-stu-id="15fc4-109">Example 1: Enable all metrics and logs for a resource</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

<span data-ttu-id="15fc4-110">Dieser Befehl aktiviert alle verfügbaren Metriken und Protokolle für Resource01.</span><span class="sxs-lookup"><span data-stu-id="15fc4-110">This command enables all available metrics and logs for Resource01.</span></span>

### <span data-ttu-id="15fc4-111">Beispiel 2: Deaktivieren aller Metriken und Protokolle</span><span class="sxs-lookup"><span data-stu-id="15fc4-111">Example 2: Disable all metrics and logs</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

<span data-ttu-id="15fc4-112">Mit diesem Befehl werden alle verfügbaren Metriken und Protokolle für die Ressource Resource01 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="15fc4-112">This command disables all available metrics and logs for the resource Resource01.</span></span>

### <span data-ttu-id="15fc4-113">Beispiel 3: Aktivieren mehrerer Kategorien</span><span class="sxs-lookup"><span data-stu-id="15fc4-113">Example 3: Enable multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
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

<span data-ttu-id="15fc4-114">Dieser Befehl aktiviert Kategorie1 und Kategorie2.</span><span class="sxs-lookup"><span data-stu-id="15fc4-114">This command enables Category1 and Category2.</span></span>
<span data-ttu-id="15fc4-115">Alle zeitkörnungen und anderen Kategorien bleiben identisch.</span><span class="sxs-lookup"><span data-stu-id="15fc4-115">All timegrains and other categories remain the same.</span></span>

### <span data-ttu-id="15fc4-116">Beispiel 4: Aktivieren einer Zeit Körnung und mehrerer Kategorien</span><span class="sxs-lookup"><span data-stu-id="15fc4-116">Example 4: Enable a time grain and multiple categories</span></span>
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

<span data-ttu-id="15fc4-117">Dieser Befehl aktiviert nur Kategorie1-, Kategorie2-und Time Grain-PT1M.</span><span class="sxs-lookup"><span data-stu-id="15fc4-117">This command enables only Category1, Category2, and time grain PT1M.</span></span>
<span data-ttu-id="15fc4-118">Alle anderen Zeit Körnungen und-Kategorien sind unverändert.</span><span class="sxs-lookup"><span data-stu-id="15fc4-118">All other time grains and categories are unchanged.</span></span>

## <span data-ttu-id="15fc4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="15fc4-119">PARAMETERS</span></span>

### <span data-ttu-id="15fc4-120">-Kategorien</span><span class="sxs-lookup"><span data-stu-id="15fc4-120">-Categories</span></span>
<span data-ttu-id="15fc4-121">Gibt die Liste der Protokollkategorien an, die entsprechend dem Wert von *Enabled aktiviert* oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15fc4-121">Specifies the list of log categories to enable or disable, according to the value of *Enabled*.</span></span>
<span data-ttu-id="15fc4-122">Wenn Sie keine Kategorie angeben, funktioniert dieser Befehl für alle Kategorien.</span><span class="sxs-lookup"><span data-stu-id="15fc4-122">If you do not specify a category, this command operates on all categories.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-123">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="15fc4-123">-Enabled</span></span>
<span data-ttu-id="15fc4-124">Gibt an, ob die Diagnose aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="15fc4-124">Indicates whether to enable diagnostics.</span></span>
<span data-ttu-id="15fc4-125">Geben Sie $true an, um die Diagnose zu aktivieren, oder $false, um die Diagnose zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="15fc4-125">Specify $True to enable diagnostics, or $False to disable diagnostics.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="15fc4-126">-ResourceId</span></span>
<span data-ttu-id="15fc4-127">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="15fc4-127">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-128">-RetentionEnabled</span><span class="sxs-lookup"><span data-stu-id="15fc4-128">-RetentionEnabled</span></span>
<span data-ttu-id="15fc4-129">Gibt an, ob die Beibehaltung von Diagnoseinformationen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="15fc4-129">Indicates whether retention of diagnostic information is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="15fc4-130">-RetentionInDays</span></span>
<span data-ttu-id="15fc4-131">Gibt die Aufbewahrungsrichtlinie in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="15fc4-131">Specifies the retention policy, in days.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-132">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="15fc4-132">-ServiceBusRuleId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-133">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="15fc4-133">-StorageAccountId</span></span>
<span data-ttu-id="15fc4-134">Gibt die ID des speicherkontos an, in dem die Daten gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15fc4-134">Specifies the ID of the Storage account in which to save the data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-135">-Zeitkörnungen</span><span class="sxs-lookup"><span data-stu-id="15fc4-135">-Timegrains</span></span>
<span data-ttu-id="15fc4-136">Gibt die Zeit Körnungen an, die für Metriken entsprechend dem Wert von *Enabled aktiviert* oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15fc4-136">Specifies the time grains to enable or disable for metrics, according to the value of *Enabled*.</span></span>
<span data-ttu-id="15fc4-137">Wenn Sie kein Zeit Korn angeben, wird dieser Befehl für alle verfügbaren Zeit Körnungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15fc4-137">If you do not specify a time grain, this command operates on all available time grains.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-138">-Arbeitsbereichs-Nr</span><span class="sxs-lookup"><span data-stu-id="15fc4-138">-WorkspaceId</span></span>
<span data-ttu-id="15fc4-139">Die ID des Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="15fc4-139">The Id of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15fc4-140">-DefaultProfile</span></span>
<span data-ttu-id="15fc4-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15fc4-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15fc4-142">-EventHubAuthorizationRuleId</span><span class="sxs-lookup"><span data-stu-id="15fc4-142">-EventHubAuthorizationRuleId</span></span>
<span data-ttu-id="15fc4-143">Die Ereignis-Hub-Regel-ID</span><span class="sxs-lookup"><span data-stu-id="15fc4-143">The event hub rule id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15fc4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15fc4-144">CommonParameters</span></span>
<span data-ttu-id="15fc4-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15fc4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15fc4-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15fc4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15fc4-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15fc4-147">INPUTS</span></span>

## <span data-ttu-id="15fc4-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15fc4-148">OUTPUTS</span></span>

### <span data-ttu-id="15fc4-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="15fc4-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="15fc4-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="15fc4-150">NOTES</span></span>

## <span data-ttu-id="15fc4-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15fc4-151">RELATED LINKS</span></span>

[<span data-ttu-id="15fc4-152">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="15fc4-152">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)



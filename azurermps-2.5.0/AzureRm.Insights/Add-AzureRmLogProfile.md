---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 4302aa7dbc0cf31b9a7aa61678d871e9da140d51
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849335"
---
# <span data-ttu-id="b20c9-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b20c9-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="b20c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b20c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b20c9-103">Erstellt ein neues Aktivitätsprotokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="b20c9-103">Creates a new activity log profile.</span></span> <span data-ttu-id="b20c9-104">Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure-Speicherkonto zu archivieren oder in einem Azure-Ereignis-Hub im gleichen Abonnement zu streamen.</span><span class="sxs-lookup"><span data-stu-id="b20c9-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b20c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b20c9-105">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b20c9-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b20c9-106">DESCRIPTION</span></span>
<span data-ttu-id="b20c9-107">Das Cmdlet **Add-AzureRmLogProfile** erstellt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="b20c9-107">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="b20c9-108">**Speicher** Konto – nur das Standardspeicher Konto (das Premium Speicherkonto wird nicht unterstützt) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b20c9-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="b20c9-109">Es kann entweder vom Typ Arm oder klassisch sein.</span><span class="sxs-lookup"><span data-stu-id="b20c9-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="b20c9-110">Wenn Sie bei einem Speicherkonto angemeldet ist, werden die Kosten für die Speicherung des Aktivitätsprotokolls zu normalen Standardspeicher Gebühren berechnet.</span><span class="sxs-lookup"><span data-stu-id="b20c9-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="b20c9-111">Pro Abonnement kann nur jeweils ein Protokoll Profil vorhanden sein. nur ein Speicherkonto pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b20c9-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="b20c9-112">**Ereignis-Hub** -es kann nur jeweils ein Protokoll Profil pro Abonnement vorhanden sein. nur ein Ereignis-Hub pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b20c9-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="b20c9-113">Wenn das Aktivitätsprotokoll zu einem Ereignis-Hub gestreamt wird, gelten die standardmäßigen Event Hub-Preise.</span><span class="sxs-lookup"><span data-stu-id="b20c9-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="b20c9-114">Im Aktivitätsprotokoll können Ereignisse zu einer Region gehören oder "Global" sein.</span><span class="sxs-lookup"><span data-stu-id="b20c9-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="b20c9-115">Global bedeutet im Wesentlichen, dass diese Ereignisse Regions Agnostiker sind und unabhängig von der Region sind, wobei die Mehrzahl der Ereignisse in diese Kategorie fällt.</span><span class="sxs-lookup"><span data-stu-id="b20c9-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="b20c9-116">Wenn das Aktivitätsprotokoll Profil aus dem Portal gesetzt wird, wird implizit "Global" zusammen mit allen anderen in der Benutzeroberfläche ausgewählten Regionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b20c9-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="b20c9-117">Wenn Sie das Cmdlet verwenden, muss der Speicherort als "Global" explizit außer in einer anderen Region erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="b20c9-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="b20c9-118">**Hinweis** : Wenn Sie **"Global" nicht in den Speicherorten festgelegt haben, wird der Großteil des Aktivitätsprotokolls nicht exportiert.**</span><span class="sxs-lookup"><span data-stu-id="b20c9-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="b20c9-119">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b20c9-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b20c9-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b20c9-120">EXAMPLES</span></span>

### <span data-ttu-id="b20c9-121">Beispiel 1: Hinzufügen eines neuen Protokoll Profils zum Exportieren des Aktivitätsprotokolls, das der Standort Bedingung entspricht, zu einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="b20c9-121">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="b20c9-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="b20c9-122">PARAMETERS</span></span>

### <span data-ttu-id="b20c9-123">-Kategorie</span><span class="sxs-lookup"><span data-stu-id="b20c9-123">-Category</span></span>
<span data-ttu-id="b20c9-124">Gibt die Liste der Kategorien an.</span><span class="sxs-lookup"><span data-stu-id="b20c9-124">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="b20c9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b20c9-125">-DefaultProfile</span></span>
<span data-ttu-id="b20c9-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b20c9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b20c9-127">-Standort</span><span class="sxs-lookup"><span data-stu-id="b20c9-127">-Location</span></span>
<span data-ttu-id="b20c9-128">Gibt den Speicherort des Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="b20c9-128">Specifies the location of the log profile.</span></span>
<span data-ttu-id="b20c9-129">Gültige Werte: führen Sie die folgenden Cmdlets aus, um die aktuelle Liste der Speicherorte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b20c9-129">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="b20c9-130">Get-AzureLocation | Auswählen von DisplayName</span><span class="sxs-lookup"><span data-stu-id="b20c9-130">Get-AzureLocation | Select DisplayName</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b20c9-131">-Name</span><span class="sxs-lookup"><span data-stu-id="b20c9-131">-Name</span></span>
<span data-ttu-id="b20c9-132">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="b20c9-132">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="b20c9-133">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b20c9-133">-RetentionInDays</span></span>
<span data-ttu-id="b20c9-134">Gibt die Aufbewahrungsrichtlinie in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="b20c9-134">Specifies the retention policy, in days.</span></span> <span data-ttu-id="b20c9-135">Dies ist die Anzahl der Tage, die die Protokolle im angegebenen Speicherkonto aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="b20c9-135">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="b20c9-136">Um die Daten für immer beizubehalten, setzen Sie diesen Wert auf **0**.</span><span class="sxs-lookup"><span data-stu-id="b20c9-136">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="b20c9-137">Wenn Sie nicht angegeben ist, wird standardmäßig **0** verwendet.</span><span class="sxs-lookup"><span data-stu-id="b20c9-137">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="b20c9-138">Für die Datenaufbewahrung gelten normale Standardspeicher-oder Event Hub-Abrechnungsgebühren.</span><span class="sxs-lookup"><span data-stu-id="b20c9-138">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="b20c9-139">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="b20c9-139">-ServiceBusRuleId</span></span>
<span data-ttu-id="b20c9-140">Gibt die ID der ServiceBus-Regel an.</span><span class="sxs-lookup"><span data-stu-id="b20c9-140">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="b20c9-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b20c9-141">-StorageAccountId</span></span>
<span data-ttu-id="b20c9-142">Gibt die ID des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="b20c9-142">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="b20c9-143">ID ist die vollqualifizierte Ressourcen-ID des speicherkontos, beispielsweise</span><span class="sxs-lookup"><span data-stu-id="b20c9-143">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="b20c9-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="b20c9-144">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="b20c9-145">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b20c9-145">-Confirm</span></span>
<span data-ttu-id="b20c9-146">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b20c9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b20c9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b20c9-147">-WhatIf</span></span>
<span data-ttu-id="b20c9-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b20c9-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b20c9-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b20c9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b20c9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20c9-150">CommonParameters</span></span>
<span data-ttu-id="b20c9-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b20c9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20c9-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b20c9-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20c9-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b20c9-153">INPUTS</span></span>

### <span data-ttu-id="b20c9-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b20c9-154">System.String</span></span>

### <span data-ttu-id="b20c9-155">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b20c9-155">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b20c9-156">System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b20c9-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="b20c9-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b20c9-157">OUTPUTS</span></span>

### <span data-ttu-id="b20c9-158">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="b20c9-158">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="b20c9-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="b20c9-159">NOTES</span></span>

## <span data-ttu-id="b20c9-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b20c9-160">RELATED LINKS</span></span>

[<span data-ttu-id="b20c9-161">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b20c9-161">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="b20c9-162">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="b20c9-162">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)



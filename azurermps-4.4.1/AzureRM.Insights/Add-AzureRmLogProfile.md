---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogProfile.md
ms.openlocfilehash: 40efc9e6afbb4f1424fcbcfe70e3376eb9ab5a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504953"
---
# <span data-ttu-id="76825-101">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="76825-101">Add-AzureRmLogProfile</span></span>

## <span data-ttu-id="76825-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76825-102">SYNOPSIS</span></span>
<span data-ttu-id="76825-103">Erstellt ein neues Aktivitätsprotokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="76825-103">Creates a new activity log profile.</span></span> <span data-ttu-id="76825-104">Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure-Speicherkonto zu archivieren oder in einem Azure-Ereignis-Hub im gleichen Abonnement zu streamen.</span><span class="sxs-lookup"><span data-stu-id="76825-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="76825-105">**Speicher** Konto – nur das Standardspeicher Konto (das Premium Speicherkonto wird nicht unterstützt) wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="76825-105">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="76825-106">Es kann entweder vom Typ Arm oder klassisch sein.</span><span class="sxs-lookup"><span data-stu-id="76825-106">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="76825-107">Wenn Sie bei einem Speicherkonto angemeldet ist, werden die Kosten für die Speicherung des Aktivitätsprotokolls zu normalen Standardspeicher Gebühren berechnet.</span><span class="sxs-lookup"><span data-stu-id="76825-107">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="76825-108">Pro Abonnement kann nur jeweils ein Protokoll Profil vorhanden sein. nur ein Speicherkonto pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76825-108">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="76825-109">**Ereignis-Hub** -es kann nur jeweils ein Protokoll Profil pro Abonnement vorhanden sein. nur ein Ereignis-Hub pro Abonnement kann zum Exportieren des Aktivitätsprotokolls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76825-109">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="76825-110">Wenn das Aktivitätsprotokoll zu einem Ereignis-Hub gestreamt wird, gelten die standardmäßigen Event Hub-Preise.</span><span class="sxs-lookup"><span data-stu-id="76825-110">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="76825-111">Im Aktivitätsprotokoll können Ereignisse zu einer Region gehören oder "Global" sein.</span><span class="sxs-lookup"><span data-stu-id="76825-111">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="76825-112">Global bedeutet im Wesentlichen, dass diese Ereignisse Regions Agnostiker sind und unabhängig von der Region sind, wobei die Mehrzahl der Ereignisse in diese Kategorie fällt.</span><span class="sxs-lookup"><span data-stu-id="76825-112">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="76825-113">Wenn das Aktivitätsprotokoll Profil aus dem Portal gesetzt wird, wird implizit "Global" zusammen mit allen anderen in der Benutzeroberfläche ausgewählten Regionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="76825-113">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="76825-114">Wenn Sie das Cmdlet verwenden, muss der Speicherort als "Global" explizit außer in einer anderen Region erwähnt werden.</span><span class="sxs-lookup"><span data-stu-id="76825-114">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="76825-115">**Hinweis** : Wenn Sie **"Global" nicht in den Speicherorten festgelegt haben, wird der Großteil des Aktivitätsprotokolls nicht exportiert.**</span><span class="sxs-lookup"><span data-stu-id="76825-115">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76825-116">Syntax</span><span class="sxs-lookup"><span data-stu-id="76825-116">SYNTAX</span></span>

```
Add-AzureRmLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Locations <System.Collections.Generic.List`1[System.String]>
 [-Categories <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76825-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76825-117">DESCRIPTION</span></span>
<span data-ttu-id="76825-118">Das Cmdlet **Add-AzureRmLogProfile** erstellt ein Protokoll Profil.</span><span class="sxs-lookup"><span data-stu-id="76825-118">The **Add-AzureRmLogProfile** cmdlet creates a log profile.</span></span>

## <span data-ttu-id="76825-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76825-119">EXAMPLES</span></span>

### <span data-ttu-id="76825-120">Beispiel 1: Hinzufügen eines neuen Protokoll Profils zum Exportieren des Aktivitätsprotokolls, das der Standort Bedingung entspricht, zu einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="76825-120">Example 1 : Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```
Add-AzureRmLogProfile -Locations "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="76825-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="76825-121">PARAMETERS</span></span>

### <span data-ttu-id="76825-122">-Kategorien</span><span class="sxs-lookup"><span data-stu-id="76825-122">-Categories</span></span>
<span data-ttu-id="76825-123">Gibt die Liste der Kategorien an.</span><span class="sxs-lookup"><span data-stu-id="76825-123">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="76825-124">-Standorte</span><span class="sxs-lookup"><span data-stu-id="76825-124">-Locations</span></span>
<span data-ttu-id="76825-125">Gibt den Speicherort des Protokoll Profils an.</span><span class="sxs-lookup"><span data-stu-id="76825-125">Specifies the location of the log profile.</span></span>
<span data-ttu-id="76825-126">Gültige Werte: führen Sie die folgenden Cmdlets aus, um die aktuelle Liste der Speicherorte abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76825-126">Valid values: Run below cmdlet to get the latest list of locations.</span></span> 

<span data-ttu-id="76825-127">Get-AzureLocation | Auswählen von DisplayName</span><span class="sxs-lookup"><span data-stu-id="76825-127">Get-AzureLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="76825-128">-Name</span><span class="sxs-lookup"><span data-stu-id="76825-128">-Name</span></span>
<span data-ttu-id="76825-129">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="76825-129">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="76825-130">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="76825-130">-RetentionInDays</span></span>
<span data-ttu-id="76825-131">Gibt die Aufbewahrungsrichtlinie in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="76825-131">Specifies the retention policy, in days.</span></span> <span data-ttu-id="76825-132">Dies ist die Anzahl der Tage, die die Protokolle im angegebenen Speicherkonto aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="76825-132">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="76825-133">Um die Daten für immer beizubehalten, setzen Sie diesen Wert auf **0**.</span><span class="sxs-lookup"><span data-stu-id="76825-133">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="76825-134">Wenn Sie nicht angegeben ist, wird standardmäßig **0** verwendet.</span><span class="sxs-lookup"><span data-stu-id="76825-134">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="76825-135">Für die Datenaufbewahrung gelten normale Standardspeicher-oder Event Hub-Abrechnungsgebühren.</span><span class="sxs-lookup"><span data-stu-id="76825-135">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="76825-136">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="76825-136">-ServiceBusRuleId</span></span>
<span data-ttu-id="76825-137">Gibt die ID der ServiceBus-Regel an.</span><span class="sxs-lookup"><span data-stu-id="76825-137">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="76825-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="76825-138">-StorageAccountId</span></span>
<span data-ttu-id="76825-139">Gibt die ID des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="76825-139">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="76825-140">ID ist die vollqualifizierte Ressourcen-ID des speicherkontos, beispielsweise</span><span class="sxs-lookup"><span data-stu-id="76825-140">ID is the fully qualified Resource ID of the storage account for example</span></span>  

<span data-ttu-id="76825-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="76825-141">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="76825-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76825-142">-DefaultProfile</span></span>
<span data-ttu-id="76825-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76825-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76825-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76825-144">CommonParameters</span></span>
<span data-ttu-id="76825-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76825-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76825-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76825-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76825-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76825-147">INPUTS</span></span>

## <span data-ttu-id="76825-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76825-148">OUTPUTS</span></span>

### <span data-ttu-id="76825-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="76825-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="76825-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="76825-150">NOTES</span></span>

## <span data-ttu-id="76825-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76825-151">RELATED LINKS</span></span>

[<span data-ttu-id="76825-152">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="76825-152">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)

[<span data-ttu-id="76825-153">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="76825-153">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)



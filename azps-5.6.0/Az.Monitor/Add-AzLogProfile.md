---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932776"
---
# <span data-ttu-id="f0d16-101">Add-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0d16-101">Add-AzLogProfile</span></span>

## <span data-ttu-id="f0d16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d16-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d16-103">Erstellt ein neues Aktivitätsprotokollprofil.</span><span class="sxs-lookup"><span data-stu-id="f0d16-103">Creates a new activity log profile.</span></span> <span data-ttu-id="f0d16-104">Dieses Profil wird verwendet, um das Aktivitätsprotokoll entweder in einem Azure-Speicherkonto zu archivieren oder es an einen Azure-Ereignishub im gleichen Abonnement zu streamen.</span><span class="sxs-lookup"><span data-stu-id="f0d16-104">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

## <span data-ttu-id="f0d16-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0d16-105">SYNTAX</span></span>

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d16-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0d16-106">DESCRIPTION</span></span>
<span data-ttu-id="f0d16-107">Das **Add-AzLogProfile-Cmdlet** erstellt ein Protokollprofil.</span><span class="sxs-lookup"><span data-stu-id="f0d16-107">The **Add-AzLogProfile** cmdlet creates a log profile.</span></span>
- <span data-ttu-id="f0d16-108">**Speicherkonto** : Es wird nur das Standardspeicherkonto (Premiumspeicherkonto wird nicht unterstützt) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f0d16-108">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="f0d16-109">Sie kann entweder vom Typ ARM oder klassisch sein.</span><span class="sxs-lookup"><span data-stu-id="f0d16-109">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="f0d16-110">Wenn es bei einem Speicherkonto protokolliert wird, werden die Kosten für das Speichern des Aktivitätsprotokolls zu normalen Standardspeicherraten abgerechnet.</span><span class="sxs-lookup"><span data-stu-id="f0d16-110">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="f0d16-111">Es kann nur ein Protokollprofil pro Abonnement sein, damit nur ein Speicherkonto pro Abonnement zum Exportieren des Aktivitätsprotokolls verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0d16-111">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 
- <span data-ttu-id="f0d16-112">**Ereignishub** : Es kann nur ein Protokollprofil pro Abonnement sein, damit nur ein Ereignishub pro Abonnement zum Exportieren des Aktivitätsprotokolls verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f0d16-112">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="f0d16-113">Wenn das Aktivitätsprotokoll an einen Ereignishub gestreamt wird, gelten standardmäßige Preise für Event Hubs.</span><span class="sxs-lookup"><span data-stu-id="f0d16-113">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> <span data-ttu-id="f0d16-114">Im Aktivitätsprotokoll können Ereignisse eine Region betreffen oder "Global" sein.</span><span class="sxs-lookup"><span data-stu-id="f0d16-114">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="f0d16-115">Global bedeutet im Wesentlichen, dass diese Ereignisse regionagnostisch sind und unabhängig von der Region sind, tatsächlich fallen die meisten Ereignisse in diese Kategorie.</span><span class="sxs-lookup"><span data-stu-id="f0d16-115">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="f0d16-116">Wenn das Aktivitätsprotokollprofil über das Portal festgelegt wurde, wird implizit "Global" zusammen mit allen anderen auf der Benutzeroberfläche ausgewählten Regionen addiert.</span><span class="sxs-lookup"><span data-stu-id="f0d16-116">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="f0d16-117">Bei Verwendung des Cmdlets muss der Speicherort als "Global" explizit erwähnt werden, abgesehen von jeder anderen Region.</span><span class="sxs-lookup"><span data-stu-id="f0d16-117">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 
<span data-ttu-id="f0d16-118">**Hinweis:** Wenn **Sie "Global" nicht in** den Speicherorten festlegen, wird ein Großteil des Aktivitätsprotokolls nicht exportiert.</span><span class="sxs-lookup"><span data-stu-id="f0d16-118">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> <span data-ttu-id="f0d16-119">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h. es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f0d16-119">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="f0d16-120">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0d16-120">EXAMPLES</span></span>

### <span data-ttu-id="f0d16-121">Beispiel 1: Hinzufügen eines neuen Protokollprofils zum Exportieren des Aktivitätsprotokolls, das mit der Standortbedingung in ein Speicherkonto übereinstimmen soll</span><span class="sxs-lookup"><span data-stu-id="f0d16-121">Example 1: Add a new log profile to export the activity log matching the location condition to a storage account</span></span>
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### <span data-ttu-id="f0d16-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f0d16-122">Example 2</span></span>

<span data-ttu-id="f0d16-123">Erstellt ein neues Aktivitätsprotokollprofil.</span><span class="sxs-lookup"><span data-stu-id="f0d16-123">Creates a new activity log profile.</span></span> <span data-ttu-id="f0d16-124">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="f0d16-124">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## <span data-ttu-id="f0d16-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0d16-125">PARAMETERS</span></span>

### <span data-ttu-id="f0d16-126">-Category</span><span class="sxs-lookup"><span data-stu-id="f0d16-126">-Category</span></span>
<span data-ttu-id="f0d16-127">Gibt die Liste der Kategorien an.</span><span class="sxs-lookup"><span data-stu-id="f0d16-127">Specifies the list of categories.</span></span>

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

### <span data-ttu-id="f0d16-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d16-128">-DefaultProfile</span></span>
<span data-ttu-id="f0d16-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f0d16-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0d16-130">-Location</span><span class="sxs-lookup"><span data-stu-id="f0d16-130">-Location</span></span>
<span data-ttu-id="f0d16-131">Gibt den Speicherort des Protokollprofils an.</span><span class="sxs-lookup"><span data-stu-id="f0d16-131">Specifies the location of the log profile.</span></span>
<span data-ttu-id="f0d16-132">Gültige Werte: Führen Sie unter cmdlet aus, um die neueste Liste der Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0d16-132">Valid values: Run below cmdlet to get the latest list of locations.</span></span> <span data-ttu-id="f0d16-133">Get-AzLocation | Wählen Sie Anzeigename aus.</span><span class="sxs-lookup"><span data-stu-id="f0d16-133">Get-AzLocation | Select DisplayName</span></span>

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

### <span data-ttu-id="f0d16-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f0d16-134">-Name</span></span>
<span data-ttu-id="f0d16-135">Gibt den Namen des Profils an.</span><span class="sxs-lookup"><span data-stu-id="f0d16-135">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="f0d16-136">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f0d16-136">-RetentionInDays</span></span>
<span data-ttu-id="f0d16-137">Gibt die Aufbewahrungsrichtlinie in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="f0d16-137">Specifies the retention policy, in days.</span></span> <span data-ttu-id="f0d16-138">Dies ist die Anzahl der Tage, in der die Protokolle im angegebenen Speicherkonto aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="f0d16-138">This is the number of days the logs are preserved in the storage account specified.</span></span> <span data-ttu-id="f0d16-139">Um die Daten für immer zu behalten, legen Sie dies auf **0 festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="f0d16-139">To retain the data forever set this to **0**.</span></span> <span data-ttu-id="f0d16-140">Wenn sie nicht angegeben ist, wird standardmäßig **0 festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="f0d16-140">If it's not specified, then it defaults to **0**.</span></span> <span data-ttu-id="f0d16-141">Normale Standardspeicher- oder Ereignishubabrechnungssätze gelten für die Datenaufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="f0d16-141">Normal standard storage or event hub billing rates will apply for data retention.</span></span>

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

### <span data-ttu-id="f0d16-142">-ServiceBusRuleId</span><span class="sxs-lookup"><span data-stu-id="f0d16-142">-ServiceBusRuleId</span></span>
<span data-ttu-id="f0d16-143">Gibt die ID der Dienstbusregel an.</span><span class="sxs-lookup"><span data-stu-id="f0d16-143">Specifies the ID of the Service Bus rule.</span></span>

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

### <span data-ttu-id="f0d16-144">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f0d16-144">-StorageAccountId</span></span>
<span data-ttu-id="f0d16-145">Gibt die ID des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="f0d16-145">Specifies the ID of the Storage account.</span></span> <span data-ttu-id="f0d16-146">ID ist die vollqualifizierte Ressourcen-ID des Speicherkontos, z. B.</span><span class="sxs-lookup"><span data-stu-id="f0d16-146">ID is the fully qualified Resource ID of the storage account for example</span></span>  
<span data-ttu-id="f0d16-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span><span class="sxs-lookup"><span data-stu-id="f0d16-147">/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount</span></span>

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

### <span data-ttu-id="f0d16-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0d16-148">-Confirm</span></span>
<span data-ttu-id="f0d16-149">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0d16-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d16-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d16-150">-WhatIf</span></span>
<span data-ttu-id="f0d16-151">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0d16-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0d16-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0d16-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d16-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d16-153">CommonParameters</span></span>
<span data-ttu-id="f0d16-154">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0d16-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d16-155">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0d16-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d16-156">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0d16-156">INPUTS</span></span>

### <span data-ttu-id="f0d16-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f0d16-157">System.String</span></span>

### <span data-ttu-id="f0d16-158">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0d16-158">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0d16-159">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0d16-159">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f0d16-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0d16-160">OUTPUTS</span></span>

### <span data-ttu-id="f0d16-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0d16-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile</span></span>

## <span data-ttu-id="f0d16-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0d16-162">NOTES</span></span>

## <span data-ttu-id="f0d16-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0d16-163">RELATED LINKS</span></span>

[<span data-ttu-id="f0d16-164">Get-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0d16-164">Get-AzLogProfile</span></span>](./Get-AzLogProfile.md)

[<span data-ttu-id="f0d16-165">Remove-AzLogProfile</span><span class="sxs-lookup"><span data-stu-id="f0d16-165">Remove-AzLogProfile</span></span>](./Remove-AzLogProfile.md)



---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504961"
---
# <span data-ttu-id="2b0e3-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b0e3-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="2b0e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b0e3-103">Fügt eine Protokoll Warnungsregel hinzu oder ersetzt Sie.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b0e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b0e3-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b0e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b0e3-106">Das **Add-AzureRmLogAlertRule-** Cmdlet fügt eine Ereignis Warnungsregel hinzu oder ersetzt diese.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="2b0e3-107">Die hinzugefügte Regel ist einer Ressourcengruppe zugeordnet und hat einen Namen.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="2b0e3-108">Wie in früheren Versionen angekündigt: **das Cmdlet "Add-AzureRMLogAlertRule" wird in einer zukünftigen Version als veraltet markiert.**</span><span class="sxs-lookup"><span data-stu-id="2b0e3-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="2b0e3-109">Nach dem 1. Oktober 2017 die Verwendung dieses Cmdlets hat keine Auswirkungen mehr, da diese Funktionalität in Aktivitätsprotokoll Benachrichtigungen umgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="2b0e3-110">Weitere Informationen finden Sie unter **_https://aka.ms/migratemealerts_** .</span><span class="sxs-lookup"><span data-stu-id="2b0e3-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="2b0e3-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b0e3-111">EXAMPLES</span></span>

### <span data-ttu-id="2b0e3-112">Beispiel 1: Hinzufügen einer Protokoll Warnungsregel</span><span class="sxs-lookup"><span data-stu-id="2b0e3-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="2b0e3-113">Mit diesem Befehl wird eine ereignisbasierte Warnungsregel hinzugefügt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="2b0e3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b0e3-114">PARAMETERS</span></span>

### <span data-ttu-id="2b0e3-115">-Aktionen</span><span class="sxs-lookup"><span data-stu-id="2b0e3-115">-Actions</span></span>
<span data-ttu-id="2b0e3-116">Gibt eine durch trennzeichengetrennte Liste von Aktionen an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-116">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0e3-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b0e3-117">-Description</span></span>
<span data-ttu-id="2b0e3-118">Gibt eine Beschreibung der Regel an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-118">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="2b0e3-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="2b0e3-119">-DisableRule</span></span>
<span data-ttu-id="2b0e3-120">Deaktiviert eine Regel.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-120">Disables a rule.</span></span>
<span data-ttu-id="2b0e3-121">Wenn Sie diesen Parameter nicht angeben, wird die Regel aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b0e3-122">-Ebene</span><span class="sxs-lookup"><span data-stu-id="2b0e3-122">-Level</span></span>
<span data-ttu-id="2b0e3-123">Gibt die Ebene des Ereignisses an, das die Regel überwacht.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="2b0e3-124">Geben Sie diesen Parameter nur für ereignisbasierte Regeln an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-124">Specify this parameter only for event-based rules.</span></span>

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

### <span data-ttu-id="2b0e3-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="2b0e3-125">-Location</span></span>
<span data-ttu-id="2b0e3-126">Gibt den Speicherort für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="2b0e3-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2b0e3-127">-Name</span></span>
<span data-ttu-id="2b0e3-128">Gibt den Namen der Regel an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="2b0e3-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="2b0e3-129">-OperationName</span></span>
<span data-ttu-id="2b0e3-130">Gibt den Namen des Vorgangs an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="2b0e3-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0e3-131">-ResourceGroup</span></span>
<span data-ttu-id="2b0e3-132">Gibt den Namen der Ressourcengruppe für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="2b0e3-133">-Status</span><span class="sxs-lookup"><span data-stu-id="2b0e3-133">-Status</span></span>
<span data-ttu-id="2b0e3-134">Gibt den Status an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-134">Specifies the status.</span></span>

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

### <span data-ttu-id="2b0e3-135">-Substatus</span><span class="sxs-lookup"><span data-stu-id="2b0e3-135">-SubStatus</span></span>
<span data-ttu-id="2b0e3-136">Gibt den unter Status an.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-136">Specifies the substatus.</span></span>

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

### <span data-ttu-id="2b0e3-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2b0e3-137">-TargetResourceGroup</span></span>
<span data-ttu-id="2b0e3-138">Gibt die Ressourcengruppe der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="2b0e3-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2b0e3-139">-TargetResourceId</span></span>
<span data-ttu-id="2b0e3-140">Gibt die ID der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-140">Specifies the ID of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="2b0e3-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="2b0e3-141">-TargetResourceProvider</span></span>
<span data-ttu-id="2b0e3-142">Gibt den Ressourcenanbieter der Ressource an, die von der Regel überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

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

### <span data-ttu-id="2b0e3-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b0e3-143">-DefaultProfile</span></span>
<span data-ttu-id="2b0e3-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b0e3-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b0e3-145">CommonParameters</span></span>
<span data-ttu-id="2b0e3-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b0e3-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b0e3-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b0e3-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b0e3-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b0e3-148">INPUTS</span></span>

## <span data-ttu-id="2b0e3-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b0e3-149">OUTPUTS</span></span>

### <span data-ttu-id="2b0e3-150">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2b0e3-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="2b0e3-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b0e3-151">NOTES</span></span>

## <span data-ttu-id="2b0e3-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b0e3-152">RELATED LINKS</span></span>

[<span data-ttu-id="2b0e3-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b0e3-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="2b0e3-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2b0e3-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="2b0e3-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2b0e3-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="2b0e3-156">Neu – AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="2b0e3-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="2b0e3-157">Neu – AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2b0e3-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



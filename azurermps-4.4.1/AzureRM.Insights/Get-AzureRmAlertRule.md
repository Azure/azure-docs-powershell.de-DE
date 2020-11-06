---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504933"
---
# <span data-ttu-id="ba1c5-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="ba1c5-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="ba1c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1c5-103">Ruft Warnungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba1c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba1c5-104">SYNTAX</span></span>

### <span data-ttu-id="ba1c5-105">Parameter für Get-AzureRmAlertRule-Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ba1c5-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba1c5-106">Parameter für Get-AzureRmAlertRule-Cmdlet mit Name</span><span class="sxs-lookup"><span data-stu-id="ba1c5-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba1c5-107">Parameter für Get-AzureRmAlertRule-Cmdlet mithilfe des Ziel Ressourcen-URIs</span><span class="sxs-lookup"><span data-stu-id="ba1c5-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba1c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="ba1c5-109">Das Cmdlet " **Get-AzureRmAlertRule** " Ruft eine Warnungsregel anhand des Namens oder des URIs oder aller Warnungsregeln einer angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="ba1c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba1c5-110">EXAMPLES</span></span>

### <span data-ttu-id="ba1c5-111">Beispiel 1: Abrufen von Warnungsregeln für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ba1c5-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="ba1c5-112">Mit diesem Befehl werden alle Warnungsregeln für die Ressourcengruppe Default-Web-centralus abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="ba1c5-113">Die Ausgabe enthält keine Details zu den Regeln, da der *DetailedOutput* -Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="ba1c5-114">Beispiel 2: Abrufen einer Warnungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="ba1c5-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="ba1c5-115">Dieser Befehl ruft die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ba1c5-116">Da der *DetailedOutput* -Parameter nicht angegeben wird, enthält die Ausgabe nur grundlegende Informationen zur Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="ba1c5-117">Beispiel 3: Abrufen einer Warnungsregel nach Namen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="ba1c5-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="ba1c5-118">Dieser Befehl ruft die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="ba1c5-119">Der *DetailedOutput* -Parameter wird angegeben, sodass die Ausgabe detailliert ist.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="ba1c5-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba1c5-120">PARAMETERS</span></span>

### <span data-ttu-id="ba1c5-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="ba1c5-121">-DetailedOutput</span></span>
<span data-ttu-id="ba1c5-122">Zeigt alle Details in der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="ba1c5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ba1c5-123">-Name</span></span>
<span data-ttu-id="ba1c5-124">Gibt den Namen der abzurufenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1c5-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba1c5-125">-ResourceGroup</span></span>
<span data-ttu-id="ba1c5-126">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-126">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ba1c5-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ba1c5-127">-TargetResourceId</span></span>
<span data-ttu-id="ba1c5-128">Gibt die ID der Zielressource an.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1c5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1c5-129">-DefaultProfile</span></span>
<span data-ttu-id="ba1c5-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba1c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1c5-131">CommonParameters</span></span>
<span data-ttu-id="ba1c5-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba1c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1c5-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba1c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1c5-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba1c5-134">INPUTS</span></span>

## <span data-ttu-id="ba1c5-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba1c5-135">OUTPUTS</span></span>

### <span data-ttu-id="ba1c5-136">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSManagementItemDescriptor]</span><span class="sxs-lookup"><span data-stu-id="ba1c5-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="ba1c5-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba1c5-137">NOTES</span></span>

## <span data-ttu-id="ba1c5-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba1c5-138">RELATED LINKS</span></span>

[<span data-ttu-id="ba1c5-139">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ba1c5-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="ba1c5-140">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ba1c5-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="ba1c5-141">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ba1c5-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="ba1c5-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="ba1c5-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="ba1c5-143">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="ba1c5-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



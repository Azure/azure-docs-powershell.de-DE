---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476757"
---
# <span data-ttu-id="90d7e-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="90d7e-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="90d7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="90d7e-103">Ruft Warnungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="90d7e-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90d7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90d7e-104">SYNTAX</span></span>

### <span data-ttu-id="90d7e-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="90d7e-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d7e-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="90d7e-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90d7e-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="90d7e-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90d7e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90d7e-108">DESCRIPTION</span></span>
<span data-ttu-id="90d7e-109">Das Cmdlet " **Get-AzureRmAlertRule** " Ruft eine Warnungsregel anhand des Namens oder des URIs oder aller Warnungsregeln einer angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="90d7e-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="90d7e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90d7e-110">EXAMPLES</span></span>

### <span data-ttu-id="90d7e-111">Beispiel 1: Abrufen von Warnungsregeln für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="90d7e-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="90d7e-112">Mit diesem Befehl werden alle Warnungsregeln für die Ressourcengruppe Default-Web-centralus abgerufen.</span><span class="sxs-lookup"><span data-stu-id="90d7e-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="90d7e-113">Die Ausgabe enthält keine Details zu den Regeln, da der *DetailedOutput* -Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="90d7e-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="90d7e-114">Beispiel 2: Abrufen einer Warnungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="90d7e-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="90d7e-115">Dieser Befehl ruft die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="90d7e-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="90d7e-116">Da der *DetailedOutput* -Parameter nicht angegeben wird, enthält die Ausgabe nur grundlegende Informationen zur Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="90d7e-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="90d7e-117">Beispiel 3: Abrufen einer Warnungsregel nach Namen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="90d7e-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="90d7e-118">Dieser Befehl ruft die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="90d7e-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="90d7e-119">Der *DetailedOutput* -Parameter wird angegeben, sodass die Ausgabe detailliert ist.</span><span class="sxs-lookup"><span data-stu-id="90d7e-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="90d7e-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="90d7e-120">PARAMETERS</span></span>

### <span data-ttu-id="90d7e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d7e-121">-DefaultProfile</span></span>
<span data-ttu-id="90d7e-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="90d7e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d7e-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="90d7e-123">-DetailedOutput</span></span>
<span data-ttu-id="90d7e-124">Zeigt alle Details in der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="90d7e-124">Displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d7e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="90d7e-125">-Name</span></span>
<span data-ttu-id="90d7e-126">Gibt den Namen der abzurufenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="90d7e-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d7e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d7e-127">-ResourceGroupName</span></span>
<span data-ttu-id="90d7e-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="90d7e-128">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d7e-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="90d7e-129">-TargetResourceId</span></span>
<span data-ttu-id="90d7e-130">Gibt die ID der Zielressource an.</span><span class="sxs-lookup"><span data-stu-id="90d7e-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d7e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d7e-131">CommonParameters</span></span>
<span data-ttu-id="90d7e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d7e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d7e-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d7e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d7e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90d7e-134">INPUTS</span></span>

### <span data-ttu-id="90d7e-135">Keine</span><span class="sxs-lookup"><span data-stu-id="90d7e-135">None</span></span>
<span data-ttu-id="90d7e-136">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="90d7e-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="90d7e-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90d7e-137">OUTPUTS</span></span>

### <span data-ttu-id="90d7e-138">Liste<Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule></span><span class="sxs-lookup"><span data-stu-id="90d7e-138">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule></span></span>

## <span data-ttu-id="90d7e-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="90d7e-139">NOTES</span></span>

## <span data-ttu-id="90d7e-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90d7e-140">RELATED LINKS</span></span>

[<span data-ttu-id="90d7e-141">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="90d7e-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="90d7e-142">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="90d7e-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="90d7e-143">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="90d7e-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="90d7e-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="90d7e-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="90d7e-145">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="90d7e-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850831"
---
# <span data-ttu-id="fa161-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa161-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="fa161-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa161-102">SYNOPSIS</span></span>
<span data-ttu-id="fa161-103">Ruft Warnungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="fa161-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa161-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa161-104">SYNTAX</span></span>

### <span data-ttu-id="fa161-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fa161-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa161-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="fa161-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa161-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="fa161-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa161-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa161-108">DESCRIPTION</span></span>
<span data-ttu-id="fa161-109">Das Cmdlet " **Get-AzureRmAlertRule** " Ruft eine Warnungsregel anhand des Namens oder des URIs oder aller Warnungsregeln einer angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="fa161-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="fa161-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa161-110">EXAMPLES</span></span>

### <span data-ttu-id="fa161-111">Beispiel 1: Abrufen von Warnungsregeln für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fa161-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="fa161-112">Mit diesem Befehl werden alle Warnungsregeln für die Ressourcengruppe Default-Web-centralus abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fa161-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="fa161-113">Die Ausgabe enthält keine Details zu den Regeln, da der *DetailedOutput* -Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="fa161-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="fa161-114">Beispiel 2: Abrufen einer Warnungsregel nach Namen</span><span class="sxs-lookup"><span data-stu-id="fa161-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="fa161-115">Dieser Befehl ruft die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="fa161-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="fa161-116">Da der *DetailedOutput* -Parameter nicht angegeben wird, enthält die Ausgabe nur grundlegende Informationen zur Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="fa161-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="fa161-117">Beispiel 3: Abrufen einer Warnungsregel nach Namen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="fa161-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="fa161-118">Dieser Befehl ruft die Warnungsregel mit dem Namen myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="fa161-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="fa161-119">Der *DetailedOutput* -Parameter wird angegeben, sodass die Ausgabe detailliert ist.</span><span class="sxs-lookup"><span data-stu-id="fa161-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="fa161-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa161-120">PARAMETERS</span></span>

### <span data-ttu-id="fa161-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa161-121">-DefaultProfile</span></span>
<span data-ttu-id="fa161-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fa161-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa161-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fa161-123">-DetailedOutput</span></span>
<span data-ttu-id="fa161-124">Zeigt alle Details in der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="fa161-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="fa161-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fa161-125">-Name</span></span>
<span data-ttu-id="fa161-126">Gibt den Namen der abzurufenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="fa161-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa161-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa161-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa161-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fa161-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa161-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="fa161-129">-TargetResourceId</span></span>
<span data-ttu-id="fa161-130">Gibt die ID der Zielressource an.</span><span class="sxs-lookup"><span data-stu-id="fa161-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa161-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa161-131">CommonParameters</span></span>
<span data-ttu-id="fa161-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa161-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa161-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa161-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa161-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa161-134">INPUTS</span></span>

### <span data-ttu-id="fa161-135">System. String</span><span class="sxs-lookup"><span data-stu-id="fa161-135">System.String</span></span>

### <span data-ttu-id="fa161-136">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fa161-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa161-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa161-137">OUTPUTS</span></span>

### <span data-ttu-id="fa161-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa161-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="fa161-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa161-139">NOTES</span></span>

## <span data-ttu-id="fa161-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa161-140">RELATED LINKS</span></span>



[<span data-ttu-id="fa161-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa161-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="fa161-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa161-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="fa161-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="fa161-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="fa161-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="fa161-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



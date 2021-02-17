---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 7164c1f37c3205e3bc2d71f2b820290217aff432
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403101"
---
# <span data-ttu-id="530fe-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="530fe-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="530fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="530fe-102">SYNOPSIS</span></span>
<span data-ttu-id="530fe-103">Ruft Benachrichtigungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="530fe-103">Gets alert rules.</span></span>

## <span data-ttu-id="530fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="530fe-104">SYNTAX</span></span>

### <span data-ttu-id="530fe-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="530fe-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="530fe-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="530fe-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="530fe-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="530fe-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="530fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="530fe-108">DESCRIPTION</span></span>
<span data-ttu-id="530fe-109">Das **Cmdlet "Get-AzAlertRule"** ruft eine Warnungsregel nach name oder URI oder allen Warnungsregeln aus einer angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="530fe-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="530fe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="530fe-110">EXAMPLES</span></span>

### <span data-ttu-id="530fe-111">Beispiel 1: Erhalten von Warnungsregeln für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="530fe-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="530fe-112">Dieser Befehl ruft alle Warnungsregeln für die Ressourcengruppe "Default-Web-CentralUS" ab.</span><span class="sxs-lookup"><span data-stu-id="530fe-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="530fe-113">Die Ausgabe enthält keine Details zu den Regeln, da der *Parameter "DetailedOutput"* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="530fe-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="530fe-114">Beispiel 2: Erhalten einer Warnungsregel nach Name</span><span class="sxs-lookup"><span data-stu-id="530fe-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="530fe-115">Dieser Befehl ruft die Warnungsregel namens "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" ab.</span><span class="sxs-lookup"><span data-stu-id="530fe-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="530fe-116">Da der *Parameter "DetailedOutput"* nicht angegeben wird, enthält die Ausgabe nur grundlegende Informationen zur Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="530fe-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="530fe-117">Beispiel 3: Erhalten einer Warnungsregel nach Namen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="530fe-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="530fe-118">Dieser Befehl ruft die Warnungsregel namens "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" ab.</span><span class="sxs-lookup"><span data-stu-id="530fe-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="530fe-119">Der *Parameter "DetailedOutput"* wird angegeben, sodass die Ausgabe detailliert ist.</span><span class="sxs-lookup"><span data-stu-id="530fe-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="530fe-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="530fe-120">PARAMETERS</span></span>

### <span data-ttu-id="530fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="530fe-121">-DefaultProfile</span></span>
<span data-ttu-id="530fe-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="530fe-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="530fe-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="530fe-123">-DetailedOutput</span></span>
<span data-ttu-id="530fe-124">Zeigt alle Details in der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="530fe-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="530fe-125">-Name</span><span class="sxs-lookup"><span data-stu-id="530fe-125">-Name</span></span>
<span data-ttu-id="530fe-126">Gibt den Namen der zu erhaltenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="530fe-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="530fe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="530fe-127">-ResourceGroupName</span></span>
<span data-ttu-id="530fe-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="530fe-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="530fe-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="530fe-129">-TargetResourceId</span></span>
<span data-ttu-id="530fe-130">Gibt die ID der Zielressource an.</span><span class="sxs-lookup"><span data-stu-id="530fe-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="530fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="530fe-131">CommonParameters</span></span>
<span data-ttu-id="530fe-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="530fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="530fe-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="530fe-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="530fe-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="530fe-134">INPUTS</span></span>

### <span data-ttu-id="530fe-135">System.String</span><span class="sxs-lookup"><span data-stu-id="530fe-135">System.String</span></span>

### <span data-ttu-id="530fe-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="530fe-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="530fe-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="530fe-137">OUTPUTS</span></span>

### <span data-ttu-id="530fe-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="530fe-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="530fe-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="530fe-139">NOTES</span></span>

## <span data-ttu-id="530fe-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="530fe-140">RELATED LINKS</span></span>


[<span data-ttu-id="530fe-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="530fe-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="530fe-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="530fe-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="530fe-143">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="530fe-143">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="530fe-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="530fe-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)



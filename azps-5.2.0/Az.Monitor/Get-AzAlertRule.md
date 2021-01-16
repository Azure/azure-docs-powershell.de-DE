---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98294503"
---
# <span data-ttu-id="55130-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="55130-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="55130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55130-102">SYNOPSIS</span></span>
<span data-ttu-id="55130-103">Ruft Benachrichtigungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="55130-103">Gets alert rules.</span></span>

## <span data-ttu-id="55130-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55130-104">SYNTAX</span></span>

### <span data-ttu-id="55130-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="55130-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="55130-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="55130-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55130-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="55130-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55130-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55130-108">DESCRIPTION</span></span>
<span data-ttu-id="55130-109">Das **Cmdlet "Get-AzAlertRule"** ruft eine Warnungsregel nach name oder URI oder allen Warnungsregeln aus einer angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="55130-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="55130-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="55130-110">EXAMPLES</span></span>

### <span data-ttu-id="55130-111">Beispiel 1: Erhalten von Warnungsregeln für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="55130-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="55130-112">Dieser Befehl ruft alle Warnungsregeln für die Ressourcengruppe "Default-Web-CentralUS" ab.</span><span class="sxs-lookup"><span data-stu-id="55130-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="55130-113">Die Ausgabe enthält keine Details zu den Regeln, da der *Parameter "DetailedOutput"* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="55130-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="55130-114">Beispiel 2: Erhalten einer Warnungsregel nach Name</span><span class="sxs-lookup"><span data-stu-id="55130-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="55130-115">Dieser Befehl ruft die Warnungsregel namens "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" ab.</span><span class="sxs-lookup"><span data-stu-id="55130-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="55130-116">Da der *Parameter "DetailedOutput"* nicht angegeben wird, enthält die Ausgabe nur grundlegende Informationen zur Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="55130-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="55130-117">Beispiel 3: Erhalten einer Warnungsregel nach Namen mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="55130-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="55130-118">Dieser Befehl ruft die Warnungsregel namens "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" ab.</span><span class="sxs-lookup"><span data-stu-id="55130-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="55130-119">Der *Parameter "DetailedOutput"* wird angegeben, sodass die Ausgabe detailliert ist.</span><span class="sxs-lookup"><span data-stu-id="55130-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="55130-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55130-120">PARAMETERS</span></span>

### <span data-ttu-id="55130-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55130-121">-DefaultProfile</span></span>
<span data-ttu-id="55130-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="55130-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55130-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="55130-123">-DetailedOutput</span></span>
<span data-ttu-id="55130-124">Zeigt alle Details in der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="55130-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="55130-125">-Name</span><span class="sxs-lookup"><span data-stu-id="55130-125">-Name</span></span>
<span data-ttu-id="55130-126">Gibt den Namen der zu erhaltenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="55130-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="55130-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55130-127">-ResourceGroupName</span></span>
<span data-ttu-id="55130-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="55130-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="55130-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="55130-129">-TargetResourceId</span></span>
<span data-ttu-id="55130-130">Gibt die ID der Zielressource an.</span><span class="sxs-lookup"><span data-stu-id="55130-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="55130-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55130-131">CommonParameters</span></span>
<span data-ttu-id="55130-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55130-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55130-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55130-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55130-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="55130-134">INPUTS</span></span>

### <span data-ttu-id="55130-135">System.String</span><span class="sxs-lookup"><span data-stu-id="55130-135">System.String</span></span>

### <span data-ttu-id="55130-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="55130-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="55130-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="55130-137">OUTPUTS</span></span>

### <span data-ttu-id="55130-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="55130-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="55130-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="55130-139">NOTES</span></span>

## <span data-ttu-id="55130-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="55130-140">RELATED LINKS</span></span>

[<span data-ttu-id="55130-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="55130-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="55130-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="55130-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="55130-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="55130-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="55130-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="55130-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="55130-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="55130-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)



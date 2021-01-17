---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470406"
---
# <span data-ttu-id="30990-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="30990-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="30990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30990-102">SYNOPSIS</span></span>
<span data-ttu-id="30990-103">Ruft Benachrichtigungsregeln ab.</span><span class="sxs-lookup"><span data-stu-id="30990-103">Gets alert rules.</span></span>

## <span data-ttu-id="30990-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="30990-104">SYNTAX</span></span>

### <span data-ttu-id="30990-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30990-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="30990-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="30990-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30990-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="30990-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30990-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30990-108">DESCRIPTION</span></span>
<span data-ttu-id="30990-109">Das **Cmdlet "Get-AzAlertRule"** ruft eine Warnungsregel nach name oder URI oder allen Warnungsregeln aus einer angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="30990-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="30990-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="30990-110">EXAMPLES</span></span>

### <span data-ttu-id="30990-111">Beispiel 1: Erhalten von Warnungsregeln für eine Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="30990-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="30990-112">Dieser Befehl ruft alle Warnungsregeln für die Ressourcengruppe mit dem Namen Default-Web-CentralUS ab.</span><span class="sxs-lookup"><span data-stu-id="30990-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="30990-113">Die Ausgabe enthält keine Details zu den Regeln, da der *Parameter "DetailedOutput"* nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="30990-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="30990-114">Beispiel 2: Erhalten einer Warnungsregel nach Name</span><span class="sxs-lookup"><span data-stu-id="30990-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="30990-115">Dieser Befehl ruft die Warnungsregel mit dem Namen "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" ab.</span><span class="sxs-lookup"><span data-stu-id="30990-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="30990-116">Da der *Parameter "DetailedOutput"* nicht angegeben wird, enthält die Ausgabe nur grundlegende Informationen zur Warnungsregel.</span><span class="sxs-lookup"><span data-stu-id="30990-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="30990-117">Beispiel 3: Erhalten einer Warnungsregel nach Name mit detaillierter Ausgabe</span><span class="sxs-lookup"><span data-stu-id="30990-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="30990-118">Dieser Befehl ruft die Warnungsregel namens "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" ab.</span><span class="sxs-lookup"><span data-stu-id="30990-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="30990-119">Der *Parameter "DetailedOutput"* wird angegeben, sodass die Ausgabe detailliert ist.</span><span class="sxs-lookup"><span data-stu-id="30990-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="30990-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30990-120">PARAMETERS</span></span>

### <span data-ttu-id="30990-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30990-121">-DefaultProfile</span></span>
<span data-ttu-id="30990-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="30990-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30990-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="30990-123">-DetailedOutput</span></span>
<span data-ttu-id="30990-124">Zeigt alle Details in der Ausgabe an.</span><span class="sxs-lookup"><span data-stu-id="30990-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="30990-125">-Name</span><span class="sxs-lookup"><span data-stu-id="30990-125">-Name</span></span>
<span data-ttu-id="30990-126">Gibt den Namen der zu erhaltenden Warnungsregel an.</span><span class="sxs-lookup"><span data-stu-id="30990-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="30990-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30990-127">-ResourceGroupName</span></span>
<span data-ttu-id="30990-128">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="30990-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="30990-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="30990-129">-TargetResourceId</span></span>
<span data-ttu-id="30990-130">Gibt die ID der Zielressource an.</span><span class="sxs-lookup"><span data-stu-id="30990-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="30990-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30990-131">CommonParameters</span></span>
<span data-ttu-id="30990-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30990-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30990-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30990-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30990-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="30990-134">INPUTS</span></span>

### <span data-ttu-id="30990-135">System.String</span><span class="sxs-lookup"><span data-stu-id="30990-135">System.String</span></span>

### <span data-ttu-id="30990-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="30990-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="30990-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="30990-137">OUTPUTS</span></span>

### <span data-ttu-id="30990-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="30990-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="30990-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="30990-139">NOTES</span></span>

## <span data-ttu-id="30990-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="30990-140">RELATED LINKS</span></span>

[<span data-ttu-id="30990-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="30990-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="30990-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="30990-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="30990-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="30990-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="30990-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="30990-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="30990-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="30990-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)



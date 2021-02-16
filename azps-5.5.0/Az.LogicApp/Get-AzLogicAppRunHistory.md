---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 855cab84e4ab9de2cd7afae2a25dbc867a192e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154852"
---
# <span data-ttu-id="3ab8b-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3ab8b-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="3ab8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab8b-102">SYNOPSIS</span></span>

<span data-ttu-id="3ab8b-103">Ruft den Ausführungsverlauf einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="3ab8b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ab8b-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ab8b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3ab8b-105">DESCRIPTION</span></span>

<span data-ttu-id="3ab8b-106">Das **Cmdlet "Get-AzLogicAppRunHistory"** ruft den Ausführungsverlauf einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="3ab8b-107">Dieses Cmdlet gibt eine Sammlung von **"WorkflowRun"-Objekten** zurück.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="3ab8b-108">Geben Sie die Logik-App und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="3ab8b-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3ab8b-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3ab8b-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3ab8b-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3ab8b-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3ab8b-113">EXAMPLES</span></span>

### <span data-ttu-id="3ab8b-114">Beispiel 1: Herunterladen des Ausführungsverlaufs einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="3ab8b-114">Example 1: Get the run history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="3ab8b-115">Dieser Befehl ruft den Ausführungsverlauf einer Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="3ab8b-116">Beispiel 2: Ausführen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="3ab8b-116">Example 2: Get a logic app run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="3ab8b-117">Dieser Befehl ruft eine bestimmte Logik-App ab, die für die Logik-App namens LogicApp03 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="3ab8b-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3ab8b-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="3ab8b-119">Dieser Befehl ruft den gesamten Ausführungsverlauf einer Logik-App mit dem Namen LogicApp03 ab, indem er auf "NextPageLink" folgt.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="3ab8b-120">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="3ab8b-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="3ab8b-121">Dieser Befehl ruft die ersten beiden Seiten des Ausführungsverlaufs einer Logik-App namens LogicApp03 ab, indem er dem "NextPageLink" folgt und die Ergebnisgröße auf zwei Seiten begrenzt.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="3ab8b-122">Jede Seite enthält 30 Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="3ab8b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ab8b-123">PARAMETERS</span></span>

### <span data-ttu-id="3ab8b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab8b-124">-DefaultProfile</span></span>

<span data-ttu-id="3ab8b-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3ab8b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ab8b-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="3ab8b-126">-FollowNextPageLink</span></span>

<span data-ttu-id="3ab8b-127">Gibt an, dass das Cmdlet den Links auf der nächsten Seite folgen soll.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab8b-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="3ab8b-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="3ab8b-129">Gibt an, wie oft die Links auf der nächsten Seite folgen sollen, wenn "FollowNextPageLink" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab8b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="3ab8b-130">-Name</span></span>

<span data-ttu-id="3ab8b-131">Gibt den Namen der Logik-App an, für die dieses Cmdlet den Ausführungsverlauf erhält.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab8b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ab8b-132">-ResourceGroupName</span></span>

<span data-ttu-id="3ab8b-133">Gibt den Namen einer Ressourcengruppe an, die die Logik-App enthält.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="3ab8b-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="3ab8b-134">-RunName</span></span>

<span data-ttu-id="3ab8b-135">Gibt den Ausführungsnamen einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="3ab8b-136">Dieses Cmdlet ruft die workflow-Ausführung ab, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="3ab8b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab8b-137">CommonParameters</span></span>

<span data-ttu-id="3ab8b-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ab8b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab8b-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ab8b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab8b-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3ab8b-140">INPUTS</span></span>

### <span data-ttu-id="3ab8b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3ab8b-141">System.String</span></span>

## <span data-ttu-id="3ab8b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3ab8b-142">OUTPUTS</span></span>

### <span data-ttu-id="3ab8b-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="3ab8b-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="3ab8b-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3ab8b-144">NOTES</span></span>

## <span data-ttu-id="3ab8b-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3ab8b-145">RELATED LINKS</span></span>

[<span data-ttu-id="3ab8b-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="3ab8b-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="3ab8b-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3ab8b-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="3ab8b-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="3ab8b-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)

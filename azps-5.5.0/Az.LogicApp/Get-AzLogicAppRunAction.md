---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 175667480977e55cc93486f252a8f84080c64b5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147601"
---
# <span data-ttu-id="d6598-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="d6598-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="d6598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6598-102">SYNOPSIS</span></span>

<span data-ttu-id="d6598-103">Ruft eine Aktion aus einer ausgeführten Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="d6598-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="d6598-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6598-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6598-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d6598-105">DESCRIPTION</span></span>

<span data-ttu-id="d6598-106">Das **Cmdlet "Get-AzLogicAppRunAction"** ruft eine Aktion aus einer ausgeführten Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="d6598-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="d6598-107">Dieses Cmdlet gibt ein **WorkflowRunAction-Objekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="d6598-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="d6598-108">Geben Sie die Logik-App, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="d6598-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="d6598-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="d6598-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d6598-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="d6598-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d6598-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d6598-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d6598-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="d6598-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d6598-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d6598-113">EXAMPLES</span></span>

### <span data-ttu-id="d6598-114">Beispiel 1: Erhalten einer Aktion aus einer ausgeführten Logik-App</span><span class="sxs-lookup"><span data-stu-id="d6598-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="d6598-115">Dieser Befehl ruft eine bestimmte Aktion der Logik-App mit dem Namen "LogicApp05" für die Ausführung mit dem Bezeichner 08585925184423369718380498702CU26 ab.</span><span class="sxs-lookup"><span data-stu-id="d6598-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="d6598-116">Beispiel 2: Alle Aktionen aus einer ausgeführten Logik-App</span><span class="sxs-lookup"><span data-stu-id="d6598-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="d6598-117">Dieser Befehl ruft alle Aktionen der Logik-App aus einer Ausführung mit dem Bezeichner 08585925184423369718380498702CU26 einer Logik-App namens LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="d6598-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="d6598-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6598-118">PARAMETERS</span></span>

### <span data-ttu-id="d6598-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="d6598-119">-ActionName</span></span>

<span data-ttu-id="d6598-120">Gibt den Namen einer Aktion in einer ausgeführten Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="d6598-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="d6598-121">Dieses Cmdlet ruft die Aktion ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d6598-121">This cmdlet gets the action that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6598-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6598-122">-DefaultProfile</span></span>

<span data-ttu-id="d6598-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d6598-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6598-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="d6598-124">-FollowNextPageLink</span></span>

<span data-ttu-id="d6598-125">Gibt an, dass das Cmdlet den Links auf der nächsten Seite folgen soll.</span><span class="sxs-lookup"><span data-stu-id="d6598-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="d6598-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="d6598-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="d6598-127">Gibt an, wie oft die Links auf der nächsten Seite folgen sollen, wenn "FollowNextPageLink" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d6598-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="d6598-128">-Name</span><span class="sxs-lookup"><span data-stu-id="d6598-128">-Name</span></span>

<span data-ttu-id="d6598-129">Gibt den Namen einer Logik-App an, für die dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="d6598-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6598-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6598-130">-ResourceGroupName</span></span>

<span data-ttu-id="d6598-131">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="d6598-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="d6598-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="d6598-132">-RunName</span></span>

<span data-ttu-id="d6598-133">Gibt den Namen einer Ausführung einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="d6598-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="d6598-134">Dieses Cmdlet ruft eine Aktion für die Ausführung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d6598-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="d6598-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6598-135">CommonParameters</span></span>

<span data-ttu-id="d6598-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6598-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6598-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6598-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6598-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d6598-138">INPUTS</span></span>

### <span data-ttu-id="d6598-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d6598-139">System.String</span></span>

## <span data-ttu-id="d6598-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d6598-140">OUTPUTS</span></span>

### <span data-ttu-id="d6598-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="d6598-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="d6598-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d6598-142">NOTES</span></span>

## <span data-ttu-id="d6598-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d6598-143">RELATED LINKS</span></span>

[<span data-ttu-id="d6598-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="d6598-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="d6598-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d6598-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)

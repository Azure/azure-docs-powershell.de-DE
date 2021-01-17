---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386251"
---
# <span data-ttu-id="c731f-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="c731f-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="c731f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c731f-102">SYNOPSIS</span></span>
<span data-ttu-id="c731f-103">Ruft eine Aktion aus einer ausgeführten Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="c731f-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="c731f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c731f-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c731f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c731f-105">DESCRIPTION</span></span>
<span data-ttu-id="c731f-106">Das **Cmdlet "Get-AzLogicAppRunAction"** ruft eine Aktion aus einer ausgeführten Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="c731f-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="c731f-107">Dieses Cmdlet gibt ein **WorkflowRunAction-Objekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="c731f-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="c731f-108">Geben Sie die Logik-App, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="c731f-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="c731f-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="c731f-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c731f-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="c731f-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c731f-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="c731f-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c731f-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c731f-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c731f-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c731f-113">EXAMPLES</span></span>

### <span data-ttu-id="c731f-114">Beispiel 1: Erhalten einer Aktion aus einer ausgeführten Logik-App</span><span class="sxs-lookup"><span data-stu-id="c731f-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="c731f-115">Dieser Befehl ruft eine bestimmte Logik-App-Aktion aus der Logik-App namens LogicApp05 für die Ausführung mit dem Namen "LogicAppRun56" ab.</span><span class="sxs-lookup"><span data-stu-id="c731f-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="c731f-116">Beispiel 2: Alle Aktionen aus einer ausgeführten Logik-App erhalten</span><span class="sxs-lookup"><span data-stu-id="c731f-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="c731f-117">Dieser Befehl ruft alle Aktionen der Logik-App aus einer Ausführung namens "LogicAppRun56" einer Logik-App mit dem Namen "LogicApp05" ab.</span><span class="sxs-lookup"><span data-stu-id="c731f-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="c731f-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="c731f-118">Example 3</span></span>

<span data-ttu-id="c731f-119">Dieser Befehl ruft alle Aktionen der Logik-App aus einer Ausführung namens "LogicAppRun56" einer Logik-App mit dem Namen "LogicApp05" ab.</span><span class="sxs-lookup"><span data-stu-id="c731f-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="c731f-120">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="c731f-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="c731f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c731f-121">PARAMETERS</span></span>

### <span data-ttu-id="c731f-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="c731f-122">-ActionName</span></span>
<span data-ttu-id="c731f-123">Gibt den Namen einer Aktion in einer ausgeführten Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="c731f-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="c731f-124">Dieses Cmdlet ruft die Aktion ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c731f-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="c731f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c731f-125">-DefaultProfile</span></span>
<span data-ttu-id="c731f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c731f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c731f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c731f-127">-Name</span></span>
<span data-ttu-id="c731f-128">Gibt den Namen einer Logik-App an, für die dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="c731f-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="c731f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c731f-129">-ResourceGroupName</span></span>
<span data-ttu-id="c731f-130">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="c731f-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="c731f-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="c731f-131">-RunName</span></span>
<span data-ttu-id="c731f-132">Gibt den Namen einer Ausführung einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="c731f-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="c731f-133">Dieses Cmdlet ruft eine Aktion für die Ausführung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="c731f-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="c731f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c731f-134">CommonParameters</span></span>
<span data-ttu-id="c731f-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c731f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c731f-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c731f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c731f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c731f-137">INPUTS</span></span>

### <span data-ttu-id="c731f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c731f-138">System.String</span></span>

## <span data-ttu-id="c731f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c731f-139">OUTPUTS</span></span>

### <span data-ttu-id="c731f-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="c731f-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="c731f-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c731f-141">NOTES</span></span>

## <span data-ttu-id="c731f-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c731f-142">RELATED LINKS</span></span>

[<span data-ttu-id="c731f-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="c731f-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="c731f-144">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="c731f-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



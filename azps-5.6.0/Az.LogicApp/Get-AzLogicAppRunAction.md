---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947099"
---
# <span data-ttu-id="4cfbc-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="4cfbc-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="4cfbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cfbc-102">SYNOPSIS</span></span>

<span data-ttu-id="4cfbc-103">Ruft eine Aktion aus einer ausgeführten Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="4cfbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cfbc-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cfbc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cfbc-105">DESCRIPTION</span></span>

<span data-ttu-id="4cfbc-106">Das **Get-AzLogicAppRunAction-Cmdlet** ruft eine Aktion aus einer ausgeführten Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="4cfbc-107">Dieses Cmdlet gibt ein **WorkflowRunAction-Objekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="4cfbc-108">Geben Sie die Logik-App, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="4cfbc-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4cfbc-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4cfbc-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4cfbc-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4cfbc-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4cfbc-113">EXAMPLES</span></span>

### <span data-ttu-id="4cfbc-114">Beispiel 1: Ausführen einer Aktion aus einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="4cfbc-114">Example 1: Get an action from a Logic App run</span></span>

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

<span data-ttu-id="4cfbc-115">Dieser Befehl ruft eine bestimmte Logik-App-Aktion aus der Logik-App namens LogicApp05 für die Ausführung mit dem Bezeichner 08585925184423369718380498702CU26 ab.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="4cfbc-116">Beispiel 2: Alle Aktionen aus einer Ausgeführten Logik-App herunterladen</span><span class="sxs-lookup"><span data-stu-id="4cfbc-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="4cfbc-117">Dieser Befehl ruft alle Logik-App-Aktionen aus einer Ausführung mit dem Bezeichner 0858592518423369718380498702CU26 einer Logik-App namens LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="4cfbc-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4cfbc-118">PARAMETERS</span></span>

### <span data-ttu-id="4cfbc-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="4cfbc-119">-ActionName</span></span>

<span data-ttu-id="4cfbc-120">Gibt den Namen einer Aktion in einer ausgeführten Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="4cfbc-121">Dieses Cmdlet ruft die Aktion ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cfbc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfbc-122">-DefaultProfile</span></span>

<span data-ttu-id="4cfbc-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4cfbc-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cfbc-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="4cfbc-124">-FollowNextPageLink</span></span>

<span data-ttu-id="4cfbc-125">Gibt an, dass das Cmdlet den Links der nächsten Seite folgen soll.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="4cfbc-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="4cfbc-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="4cfbc-127">Gibt an, wie oft links der nächsten Seite folgen soll, wenn FollowNextPageLink verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="4cfbc-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4cfbc-128">-Name</span></span>

<span data-ttu-id="4cfbc-129">Gibt den Namen einer Logik-App an, für die dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="4cfbc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cfbc-130">-ResourceGroupName</span></span>

<span data-ttu-id="4cfbc-131">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="4cfbc-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="4cfbc-132">-RunName</span></span>

<span data-ttu-id="4cfbc-133">Gibt den Namen einer Ausführung einer Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="4cfbc-134">Dieses Cmdlet ruft eine Aktion für die Ausführung ab, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cfbc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfbc-135">CommonParameters</span></span>

<span data-ttu-id="4cfbc-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfbc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfbc-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cfbc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfbc-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4cfbc-138">INPUTS</span></span>

### <span data-ttu-id="4cfbc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4cfbc-139">System.String</span></span>

## <span data-ttu-id="4cfbc-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4cfbc-140">OUTPUTS</span></span>

### <span data-ttu-id="4cfbc-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="4cfbc-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="4cfbc-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4cfbc-142">NOTES</span></span>

## <span data-ttu-id="4cfbc-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4cfbc-143">RELATED LINKS</span></span>

[<span data-ttu-id="4cfbc-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="4cfbc-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="4cfbc-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="4cfbc-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)

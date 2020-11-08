---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180370"
---
# <span data-ttu-id="46454-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="46454-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="46454-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46454-102">SYNOPSIS</span></span>
<span data-ttu-id="46454-103">Ruft eine Aktion aus einer Logik-App-Ausführung ab.</span><span class="sxs-lookup"><span data-stu-id="46454-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="46454-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46454-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46454-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46454-105">DESCRIPTION</span></span>
<span data-ttu-id="46454-106">Das Cmdlet " **Get-AzLogicAppRunAction** " Ruft eine Aktion aus einer Logik-App-Ausführung ab.</span><span class="sxs-lookup"><span data-stu-id="46454-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="46454-107">Dieses Cmdlet gibt ein **WorkflowRunAction** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="46454-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="46454-108">Geben Sie die Logik-APP, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="46454-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="46454-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="46454-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="46454-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="46454-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="46454-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="46454-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="46454-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="46454-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="46454-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46454-113">EXAMPLES</span></span>

### <span data-ttu-id="46454-114">Beispiel 1: Abrufen einer Aktion aus einer Logik-App-Ausführung</span><span class="sxs-lookup"><span data-stu-id="46454-114">Example 1: Get an action from a Logic App run</span></span>
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

<span data-ttu-id="46454-115">Dieser Befehl ruft eine bestimmte Logik-App-Aktion aus der Logik-App mit dem Namen LogicApp05 für den Run mit dem Namen LogicAppRun56 ab.</span><span class="sxs-lookup"><span data-stu-id="46454-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="46454-116">Beispiel 2: Abrufen aller Aktionen aus einer Logic-App-Ausführung</span><span class="sxs-lookup"><span data-stu-id="46454-116">Example 2: Get all the actions from a Logic App run</span></span>
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

<span data-ttu-id="46454-117">Dieser Befehl ruft alle Logik-App-Aktionen aus einem Run mit dem Namen LogicAppRun56 einer Logik-App mit dem Namen LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="46454-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="46454-118">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="46454-118">Example 3</span></span>

<span data-ttu-id="46454-119">Dieser Befehl ruft alle Logik-App-Aktionen aus einem Run mit dem Namen LogicAppRun56 einer Logik-App mit dem Namen LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="46454-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="46454-120">automatisch</span><span class="sxs-lookup"><span data-stu-id="46454-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="46454-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="46454-121">PARAMETERS</span></span>

### <span data-ttu-id="46454-122">-Aktionsname</span><span class="sxs-lookup"><span data-stu-id="46454-122">-ActionName</span></span>
<span data-ttu-id="46454-123">Gibt den Namen einer Aktion in einer Logic-APP an.</span><span class="sxs-lookup"><span data-stu-id="46454-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="46454-124">Dieses Cmdlet ruft die Aktion ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="46454-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="46454-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46454-125">-DefaultProfile</span></span>
<span data-ttu-id="46454-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="46454-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46454-127">-Name</span><span class="sxs-lookup"><span data-stu-id="46454-127">-Name</span></span>
<span data-ttu-id="46454-128">Gibt den Namen einer Logik-APP an, für die dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="46454-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="46454-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46454-129">-ResourceGroupName</span></span>
<span data-ttu-id="46454-130">Gibt den Namen einer Ressourcengruppe an, in der das Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="46454-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="46454-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="46454-131">-RunName</span></span>
<span data-ttu-id="46454-132">Gibt den Namen der Ausführung einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="46454-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="46454-133">Dieses Cmdlet ruft eine Aktion für die Ausführung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="46454-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="46454-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46454-134">CommonParameters</span></span>
<span data-ttu-id="46454-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46454-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46454-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46454-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46454-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46454-137">INPUTS</span></span>

### <span data-ttu-id="46454-138">System. String</span><span class="sxs-lookup"><span data-stu-id="46454-138">System.String</span></span>

## <span data-ttu-id="46454-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46454-139">OUTPUTS</span></span>

### <span data-ttu-id="46454-140">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="46454-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="46454-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="46454-141">NOTES</span></span>

## <span data-ttu-id="46454-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46454-142">RELATED LINKS</span></span>

[<span data-ttu-id="46454-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="46454-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="46454-144">Stopp-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="46454-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



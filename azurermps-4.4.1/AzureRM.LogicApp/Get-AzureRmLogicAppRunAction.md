---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 49968330f56fe0891adb9c5a62a1264700f53224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502694"
---
# <span data-ttu-id="e1601-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="e1601-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="e1601-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1601-102">SYNOPSIS</span></span>
<span data-ttu-id="e1601-103">Ruft eine Aktion aus einer Logik-App-Ausführung ab.</span><span class="sxs-lookup"><span data-stu-id="e1601-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1601-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1601-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1601-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1601-105">DESCRIPTION</span></span>
<span data-ttu-id="e1601-106">Das Cmdlet " **Get-AzureRmLogicAppRunAction** " Ruft eine Aktion aus einer Logik-App-Ausführung ab.</span><span class="sxs-lookup"><span data-stu-id="e1601-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="e1601-107">Dieses Cmdlet gibt ein **WorkflowRunAction** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="e1601-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="e1601-108">Geben Sie die Logik-APP, die Ressourcengruppe und die Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="e1601-108">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="e1601-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="e1601-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e1601-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="e1601-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e1601-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="e1601-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e1601-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="e1601-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e1601-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1601-113">EXAMPLES</span></span>

### <span data-ttu-id="e1601-114">Beispiel 1: Abrufen einer Aktion aus einer Logik-App-Ausführung</span><span class="sxs-lookup"><span data-stu-id="e1601-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="e1601-115">Dieser Befehl ruft eine bestimmte Logik-App-Aktion aus der Logik-App mit dem Namen LogicApp05 für den Run mit dem Namen LogicAppRun56 ab.</span><span class="sxs-lookup"><span data-stu-id="e1601-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="e1601-116">Beispiel 2: Abrufen aller Aktionen aus einer Logic-App-Ausführung</span><span class="sxs-lookup"><span data-stu-id="e1601-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="e1601-117">Dieser Befehl ruft alle Logik-App-Aktionen aus einem Run mit dem Namen LogicAppRun56 einer Logik-App mit dem Namen LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="e1601-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="e1601-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1601-118">PARAMETERS</span></span>

### <span data-ttu-id="e1601-119">-Aktionsname</span><span class="sxs-lookup"><span data-stu-id="e1601-119">-ActionName</span></span>
<span data-ttu-id="e1601-120">Gibt den Namen einer Aktion in einer Logic-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1601-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="e1601-121">Dieses Cmdlet ruft die Aktion ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e1601-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1601-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e1601-122">-Name</span></span>
<span data-ttu-id="e1601-123">Gibt den Namen einer Logik-APP an, für die dieses Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="e1601-123">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e1601-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1601-124">-ResourceGroupName</span></span>
<span data-ttu-id="e1601-125">Gibt den Namen einer Ressourcengruppe an, in der das Cmdlet eine Aktion erhält.</span><span class="sxs-lookup"><span data-stu-id="e1601-125">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="e1601-126">-RunName</span><span class="sxs-lookup"><span data-stu-id="e1601-126">-RunName</span></span>
<span data-ttu-id="e1601-127">Gibt den Namen der Ausführung einer Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="e1601-127">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="e1601-128">Dieses Cmdlet ruft eine Aktion für die Ausführung ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e1601-128">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="e1601-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1601-129">-DefaultProfile</span></span>
<span data-ttu-id="e1601-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1601-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1601-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1601-131">CommonParameters</span></span>
<span data-ttu-id="e1601-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1601-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1601-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1601-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1601-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1601-134">INPUTS</span></span>

## <span data-ttu-id="e1601-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1601-135">OUTPUTS</span></span>

### <span data-ttu-id="e1601-136">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="e1601-136">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="e1601-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1601-137">NOTES</span></span>

## <span data-ttu-id="e1601-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1601-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1601-139">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="e1601-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="e1601-140">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="e1601-140">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: d20d6ba980b424109e33fd4380eec9be4f7728ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004548"
---
# <span data-ttu-id="0dc9b-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="0dc9b-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="0dc9b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0dc9b-102">SYNOPSIS</span></span>
<span data-ttu-id="0dc9b-103">Ruft den Verlauf von Triggern in einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="0dc9b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dc9b-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dc9b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dc9b-105">DESCRIPTION</span></span>
<span data-ttu-id="0dc9b-106">Mit dem Cmdlet **Get-AzLogicAppTriggerHistory** wird der Verlauf der Trigger in einer Logik-App im Feature Logik-apps abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="0dc9b-107">Dieses Cmdlet gibt ein **WorkflowTriggerHistory** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="0dc9b-108">Geben Sie die Logik-APP, die Ressourcengruppe und den Trigger an.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="0dc9b-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0dc9b-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0dc9b-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0dc9b-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0dc9b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0dc9b-113">EXAMPLES</span></span>

### <span data-ttu-id="0dc9b-114">Beispiel 1: Abrufen eines Trigger-Verlaufs einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="0dc9b-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="0dc9b-115">Dieser Befehl ruft einen bestimmten Logik-App-Trigger-Verlauf für einen Trigger in der Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="0dc9b-116">Beispiel 2: Abrufen von Trigger-Verlaufsdaten einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="0dc9b-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="0dc9b-117">Dieser Befehl ruft die Workflow-Trigger-Historien für einen Trigger in der Logik-App mit dem Namen LogicApp07 ab.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="0dc9b-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dc9b-118">PARAMETERS</span></span>

### <span data-ttu-id="0dc9b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dc9b-119">-DefaultProfile</span></span>
<span data-ttu-id="0dc9b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0dc9b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0dc9b-121">-Verlaufsname</span><span class="sxs-lookup"><span data-stu-id="0dc9b-121">-HistoryName</span></span>
<span data-ttu-id="0dc9b-122">Gibt den Namen des Verlaufs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0dc9b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0dc9b-123">-Name</span></span>
<span data-ttu-id="0dc9b-124">Gibt den Namen der Logik-APP an, für die dieses Cmdlet das Trigger-Protokoll erhält.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="0dc9b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dc9b-125">-ResourceGroupName</span></span>
<span data-ttu-id="0dc9b-126">Gibt den Namen der Ressourcengruppe an, in der das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0dc9b-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="0dc9b-127">-TriggerName</span></span>
<span data-ttu-id="0dc9b-128">Gibt den Namen des Triggers an, für den das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0dc9b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dc9b-129">CommonParameters</span></span>
<span data-ttu-id="0dc9b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dc9b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dc9b-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dc9b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dc9b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0dc9b-132">INPUTS</span></span>

### <span data-ttu-id="0dc9b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0dc9b-133">System.String</span></span>

## <span data-ttu-id="0dc9b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0dc9b-134">OUTPUTS</span></span>

### <span data-ttu-id="0dc9b-135">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="0dc9b-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="0dc9b-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="0dc9b-136">NOTES</span></span>

## <span data-ttu-id="0dc9b-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0dc9b-137">RELATED LINKS</span></span>

[<span data-ttu-id="0dc9b-138">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0dc9b-138">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="0dc9b-139">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="0dc9b-139">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="0dc9b-140">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0dc9b-140">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



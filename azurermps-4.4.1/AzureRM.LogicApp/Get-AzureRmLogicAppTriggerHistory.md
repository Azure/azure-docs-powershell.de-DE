---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 23ccef6dedf1a0be0f7d7cf1b565c936e76a0309
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663926"
---
# <span data-ttu-id="3819c-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="3819c-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="3819c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3819c-102">SYNOPSIS</span></span>
<span data-ttu-id="3819c-103">Ruft den Verlauf von Triggern in einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="3819c-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3819c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3819c-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3819c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3819c-105">DESCRIPTION</span></span>
<span data-ttu-id="3819c-106">Mit dem Cmdlet **Get-AzureRmLogicAppTriggerHistory** wird der Verlauf der Trigger in einer Logik-App im Feature Logik-apps abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3819c-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="3819c-107">Dieses Cmdlet gibt ein **WorkflowTriggerHistory** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3819c-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="3819c-108">Geben Sie die Logik-APP, die Ressourcengruppe und den Trigger an.</span><span class="sxs-lookup"><span data-stu-id="3819c-108">Specify the logic app, resource group, and trigger.</span></span>

<span data-ttu-id="3819c-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="3819c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3819c-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="3819c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3819c-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="3819c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3819c-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="3819c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3819c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3819c-113">EXAMPLES</span></span>

### <span data-ttu-id="3819c-114">Beispiel 1: Abrufen eines Trigger-Verlaufs einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="3819c-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="3819c-115">Dieser Befehl ruft einen bestimmten Logik-App-Trigger-Verlauf für einen Trigger in der Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="3819c-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="3819c-116">Beispiel 2: Abrufen von Trigger-Verlaufsdaten einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="3819c-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="3819c-117">Dieser Befehl ruft die Workflow-Trigger-Historien für einen Trigger in der Logik-App mit dem Namen LogicApp07 ab.</span><span class="sxs-lookup"><span data-stu-id="3819c-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="3819c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3819c-118">PARAMETERS</span></span>

### <span data-ttu-id="3819c-119">-Verlaufsname</span><span class="sxs-lookup"><span data-stu-id="3819c-119">-HistoryName</span></span>
<span data-ttu-id="3819c-120">Gibt den Namen des Verlaufs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="3819c-120">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3819c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3819c-121">-Name</span></span>
<span data-ttu-id="3819c-122">Gibt den Namen der Logik-APP an, für die dieses Cmdlet das Trigger-Protokoll erhält.</span><span class="sxs-lookup"><span data-stu-id="3819c-122">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="3819c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3819c-123">-ResourceGroupName</span></span>
<span data-ttu-id="3819c-124">Gibt den Namen der Ressourcengruppe an, in der das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="3819c-124">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="3819c-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="3819c-125">-TriggerName</span></span>
<span data-ttu-id="3819c-126">Gibt den Namen des Triggers an, für den das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="3819c-126">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="3819c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3819c-127">-DefaultProfile</span></span>
<span data-ttu-id="3819c-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3819c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3819c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3819c-129">CommonParameters</span></span>
<span data-ttu-id="3819c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3819c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3819c-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3819c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3819c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3819c-132">INPUTS</span></span>

## <span data-ttu-id="3819c-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3819c-133">OUTPUTS</span></span>

### <span data-ttu-id="3819c-134">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="3819c-134">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="3819c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3819c-135">NOTES</span></span>

## <span data-ttu-id="3819c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3819c-136">RELATED LINKS</span></span>

[<span data-ttu-id="3819c-137">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3819c-137">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="3819c-138">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="3819c-138">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="3819c-139">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="3819c-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



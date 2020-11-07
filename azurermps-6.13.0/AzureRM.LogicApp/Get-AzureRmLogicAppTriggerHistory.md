---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 9c27fd1e46d17722f843a09babab31338e88e2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664576"
---
# <span data-ttu-id="5b4aa-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="5b4aa-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="5b4aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5b4aa-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4aa-103">Ruft den Verlauf von Triggern in einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b4aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b4aa-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b4aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b4aa-105">DESCRIPTION</span></span>
<span data-ttu-id="5b4aa-106">Mit dem Cmdlet **Get-AzureRmLogicAppTriggerHistory** wird der Verlauf der Trigger in einer Logik-App im Feature Logik-apps abgerufen.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="5b4aa-107">Dieses Cmdlet gibt ein **WorkflowTriggerHistory** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="5b4aa-108">Geben Sie die Logik-APP, die Ressourcengruppe und den Trigger an.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="5b4aa-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5b4aa-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5b4aa-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5b4aa-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5b4aa-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5b4aa-113">EXAMPLES</span></span>

### <span data-ttu-id="5b4aa-114">Beispiel 1: Abrufen eines Trigger-Verlaufs einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="5b4aa-114">Example 1: Get a trigger history of a logic app</span></span>
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

<span data-ttu-id="5b4aa-115">Dieser Befehl ruft einen bestimmten Logik-App-Trigger-Verlauf für einen Trigger in der Logik-App mit dem Namen LogicApp03 ab.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="5b4aa-116">Beispiel 2: Abrufen von Trigger-Verlaufsdaten einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="5b4aa-116">Example 2: Get trigger histories of a logic app</span></span>
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

<span data-ttu-id="5b4aa-117">Dieser Befehl ruft die Workflow-Trigger-Historien für einen Trigger in der Logik-App mit dem Namen LogicApp07 ab.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="5b4aa-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b4aa-118">PARAMETERS</span></span>

### <span data-ttu-id="5b4aa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4aa-119">-DefaultProfile</span></span>
<span data-ttu-id="5b4aa-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5b4aa-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b4aa-121">-Verlaufsname</span><span class="sxs-lookup"><span data-stu-id="5b4aa-121">-HistoryName</span></span>
<span data-ttu-id="5b4aa-122">Gibt den Namen des Verlaufs an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b4aa-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5b4aa-123">-Name</span></span>
<span data-ttu-id="5b4aa-124">Gibt den Namen der Logik-APP an, für die dieses Cmdlet das Trigger-Protokoll erhält.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="5b4aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b4aa-126">Gibt den Namen der Ressourcengruppe an, in der das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="5b4aa-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="5b4aa-127">-TriggerName</span></span>
<span data-ttu-id="5b4aa-128">Gibt den Namen des Triggers an, für den das Cmdlet das Protokoll abruft.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="5b4aa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4aa-129">CommonParameters</span></span>
<span data-ttu-id="5b4aa-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b4aa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4aa-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b4aa-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4aa-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5b4aa-132">INPUTS</span></span>

### <span data-ttu-id="5b4aa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5b4aa-133">System.String</span></span>

## <span data-ttu-id="5b4aa-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5b4aa-134">OUTPUTS</span></span>

### <span data-ttu-id="5b4aa-135">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="5b4aa-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="5b4aa-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5b4aa-136">NOTES</span></span>

## <span data-ttu-id="5b4aa-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5b4aa-137">RELATED LINKS</span></span>

[<span data-ttu-id="5b4aa-138">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="5b4aa-138">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="5b4aa-139">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="5b4aa-139">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="5b4aa-140">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5b4aa-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



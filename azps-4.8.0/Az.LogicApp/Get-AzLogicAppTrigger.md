---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 7061d70ca1f4bc38c9ac8cc12ad75f01a3fed8b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174694"
---
# <span data-ttu-id="0df22-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="0df22-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="0df22-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0df22-102">SYNOPSIS</span></span>
<span data-ttu-id="0df22-103">Ruft die Trigger einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="0df22-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="0df22-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0df22-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0df22-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0df22-105">DESCRIPTION</span></span>
<span data-ttu-id="0df22-106">Das Cmdlet " **Get-AzLogicAppTrigger** " ruft Trigger aus einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="0df22-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="0df22-107">Dieses Cmdlet gibt ein **WorkflowTrigger** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0df22-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="0df22-108">Geben Sie den Workflow, die Ressourcengruppe und den Trigger an.</span><span class="sxs-lookup"><span data-stu-id="0df22-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="0df22-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="0df22-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0df22-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="0df22-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0df22-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0df22-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0df22-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0df22-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0df22-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0df22-113">EXAMPLES</span></span>

### <span data-ttu-id="0df22-114">Beispiel 1: Abrufen eines Triggers einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="0df22-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="0df22-115">Dieser Befehl ruft den Trigger mit dem Namen Trigger01 aus der Logik-App mit dem Namen LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="0df22-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="0df22-116">Beispiel 2: Abrufen aller Trigger einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="0df22-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="0df22-117">Dieser Befehl ruft die Trigger der Logik-App mit dem Namen LogicApp07 ab.</span><span class="sxs-lookup"><span data-stu-id="0df22-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="0df22-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0df22-118">PARAMETERS</span></span>

### <span data-ttu-id="0df22-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df22-119">-DefaultProfile</span></span>
<span data-ttu-id="0df22-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0df22-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0df22-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0df22-121">-Name</span></span>
<span data-ttu-id="0df22-122">Gibt den Namen der Logik-APP an, aus der dieses Cmdlet einen Trigger erhält.</span><span class="sxs-lookup"><span data-stu-id="0df22-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="0df22-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0df22-123">-ResourceGroupName</span></span>
<span data-ttu-id="0df22-124">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet einen Trigger erhält.</span><span class="sxs-lookup"><span data-stu-id="0df22-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="0df22-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="0df22-125">-TriggerName</span></span>
<span data-ttu-id="0df22-126">Gibt den Namen des Triggers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0df22-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0df22-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df22-127">CommonParameters</span></span>
<span data-ttu-id="0df22-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df22-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df22-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0df22-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df22-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0df22-130">INPUTS</span></span>

### <span data-ttu-id="0df22-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0df22-131">System.String</span></span>

## <span data-ttu-id="0df22-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0df22-132">OUTPUTS</span></span>

### <span data-ttu-id="0df22-133">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="0df22-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="0df22-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="0df22-134">NOTES</span></span>

## <span data-ttu-id="0df22-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0df22-135">RELATED LINKS</span></span>

[<span data-ttu-id="0df22-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="0df22-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="0df22-137">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0df22-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



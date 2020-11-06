---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: f9f21689a894e46a9cd8d53d591d1cb17099fad8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479773"
---
# <span data-ttu-id="157d3-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="157d3-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="157d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="157d3-102">SYNOPSIS</span></span>
<span data-ttu-id="157d3-103">Ruft die Trigger einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="157d3-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="157d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="157d3-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="157d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="157d3-105">DESCRIPTION</span></span>
<span data-ttu-id="157d3-106">Das Cmdlet " **Get-AzureRmLogicAppTrigger** " ruft Trigger aus einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="157d3-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="157d3-107">Dieses Cmdlet gibt ein **WorkflowTrigger** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="157d3-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="157d3-108">Geben Sie den Workflow, die Ressourcengruppe und den Trigger an.</span><span class="sxs-lookup"><span data-stu-id="157d3-108">Specify the workflow, resource group, and trigger.</span></span>

<span data-ttu-id="157d3-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="157d3-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="157d3-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="157d3-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="157d3-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="157d3-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="157d3-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="157d3-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="157d3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="157d3-113">EXAMPLES</span></span>

### <span data-ttu-id="157d3-114">Beispiel 1: Abrufen eines Triggers einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="157d3-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="157d3-115">Dieser Befehl ruft den Trigger mit dem Namen Trigger01 aus der Logik-App mit dem Namen LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="157d3-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="157d3-116">Beispiel 2: Abrufen aller Trigger einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="157d3-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="157d3-117">Dieser Befehl ruft die Trigger der Logik-App mit dem Namen LogicApp07 ab.</span><span class="sxs-lookup"><span data-stu-id="157d3-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="157d3-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="157d3-118">PARAMETERS</span></span>

### <span data-ttu-id="157d3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157d3-119">-DefaultProfile</span></span>
<span data-ttu-id="157d3-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="157d3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="157d3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="157d3-121">-Name</span></span>
<span data-ttu-id="157d3-122">Gibt den Namen der Logik-APP an, aus der dieses Cmdlet einen Trigger erhält.</span><span class="sxs-lookup"><span data-stu-id="157d3-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="157d3-124">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet einen Trigger erhält.</span><span class="sxs-lookup"><span data-stu-id="157d3-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157d3-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="157d3-125">-TriggerName</span></span>
<span data-ttu-id="157d3-126">Gibt den Namen des Triggers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="157d3-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157d3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157d3-127">CommonParameters</span></span>
<span data-ttu-id="157d3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157d3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157d3-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157d3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157d3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="157d3-130">INPUTS</span></span>

### <span data-ttu-id="157d3-131">Keine</span><span class="sxs-lookup"><span data-stu-id="157d3-131">None</span></span>
<span data-ttu-id="157d3-132">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="157d3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="157d3-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="157d3-133">OUTPUTS</span></span>

### <span data-ttu-id="157d3-134">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="157d3-134">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="157d3-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="157d3-135">NOTES</span></span>

## <span data-ttu-id="157d3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="157d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="157d3-137">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="157d3-137">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="157d3-138">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="157d3-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



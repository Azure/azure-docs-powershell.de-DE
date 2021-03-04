---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 28a7cd76f03dd3b6d2fc79e5d0b8d4d963a7f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947080"
---
# <span data-ttu-id="73a8e-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="73a8e-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="73a8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="73a8e-103">Ruft die Trigger einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="73a8e-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="73a8e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73a8e-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73a8e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73a8e-105">DESCRIPTION</span></span>
<span data-ttu-id="73a8e-106">Das **Get-AzLogicAppTrigger-Cmdlet** ruft Trigger aus einer Logik-App ab.</span><span class="sxs-lookup"><span data-stu-id="73a8e-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="73a8e-107">Dieses Cmdlet gibt ein **WorkflowTrigger-Objekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="73a8e-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="73a8e-108">Geben Sie den Workflow, die Ressourcengruppe und den Trigger an.</span><span class="sxs-lookup"><span data-stu-id="73a8e-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="73a8e-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="73a8e-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="73a8e-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="73a8e-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="73a8e-111">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="73a8e-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="73a8e-112">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="73a8e-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="73a8e-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73a8e-113">EXAMPLES</span></span>

### <span data-ttu-id="73a8e-114">Beispiel 1: Herunterladen eines Triggers einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="73a8e-114">Example 1: Get a trigger of a logic app</span></span>
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

<span data-ttu-id="73a8e-115">Dieser Befehl ruft den Trigger mit dem Namen Trigger01 aus der Logik-App mit dem Namen LogicApp05 ab.</span><span class="sxs-lookup"><span data-stu-id="73a8e-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="73a8e-116">Beispiel 2: Alle Trigger einer Logik-App herunterladen</span><span class="sxs-lookup"><span data-stu-id="73a8e-116">Example 2: Get all triggers of a logic app</span></span>
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

<span data-ttu-id="73a8e-117">Dieser Befehl ruft die Trigger der Logik-App mit dem Namen LogicApp07 ab.</span><span class="sxs-lookup"><span data-stu-id="73a8e-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="73a8e-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="73a8e-118">PARAMETERS</span></span>

### <span data-ttu-id="73a8e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a8e-119">-DefaultProfile</span></span>
<span data-ttu-id="73a8e-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="73a8e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73a8e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="73a8e-121">-Name</span></span>
<span data-ttu-id="73a8e-122">Gibt den Namen der Logik-App an, aus der dieses Cmdlet einen Trigger erhält.</span><span class="sxs-lookup"><span data-stu-id="73a8e-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="73a8e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a8e-123">-ResourceGroupName</span></span>
<span data-ttu-id="73a8e-124">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet einen Trigger erhält.</span><span class="sxs-lookup"><span data-stu-id="73a8e-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

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

### <span data-ttu-id="73a8e-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="73a8e-125">-TriggerName</span></span>
<span data-ttu-id="73a8e-126">Gibt den Namen des Triggers an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="73a8e-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

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

### <span data-ttu-id="73a8e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a8e-127">CommonParameters</span></span>
<span data-ttu-id="73a8e-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a8e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a8e-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a8e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a8e-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73a8e-130">INPUTS</span></span>

### <span data-ttu-id="73a8e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="73a8e-131">System.String</span></span>

## <span data-ttu-id="73a8e-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73a8e-132">OUTPUTS</span></span>

### <span data-ttu-id="73a8e-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="73a8e-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="73a8e-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="73a8e-134">NOTES</span></span>

## <span data-ttu-id="73a8e-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="73a8e-135">RELATED LINKS</span></span>

[<span data-ttu-id="73a8e-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="73a8e-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="73a8e-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="73a8e-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: c109839692ea20f1fbbcced50df9c4167322b1b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918843"
---
# <span data-ttu-id="8efcd-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8efcd-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="8efcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8efcd-102">SYNOPSIS</span></span>
<span data-ttu-id="8efcd-103">Führt eine Logik-App in einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="8efcd-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="8efcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8efcd-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8efcd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8efcd-105">DESCRIPTION</span></span>
<span data-ttu-id="8efcd-106">Das **Cmdlet Start-AzLogicApp** führt mithilfe des Features Logik-Apps eine Logik-App aus.</span><span class="sxs-lookup"><span data-stu-id="8efcd-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="8efcd-107">Geben Sie einen Namen, eine Ressourcengruppe und einen Trigger an.</span><span class="sxs-lookup"><span data-stu-id="8efcd-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="8efcd-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="8efcd-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8efcd-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="8efcd-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8efcd-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="8efcd-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8efcd-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8efcd-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8efcd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8efcd-112">EXAMPLES</span></span>

### <span data-ttu-id="8efcd-113">Beispiel 1: Ausführen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="8efcd-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="8efcd-114">Mit diesem Befehl wird die Logik-App in der Ressourcengruppe "ResourceGroup11" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8efcd-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="8efcd-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8efcd-115">PARAMETERS</span></span>

### <span data-ttu-id="8efcd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8efcd-116">-DefaultProfile</span></span>
<span data-ttu-id="8efcd-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8efcd-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8efcd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8efcd-118">-Name</span></span>
<span data-ttu-id="8efcd-119">Gibt den Namen der Logik-App an, die dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="8efcd-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8efcd-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8efcd-120">-Parameters</span></span>
<span data-ttu-id="8efcd-121">Gibt ein Parametersammlungsobjekt der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="8efcd-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="8efcd-122">Geben Sie eine Hashtabelle, ein Wörterbuch \<string\> oder ein Wörterbuch \<string, WorkflowParameter\> an.</span><span class="sxs-lookup"><span data-stu-id="8efcd-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8efcd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8efcd-123">-ResourceGroupName</span></span>
<span data-ttu-id="8efcd-124">Gibt den Namen der Ressourcengruppe an, die die Logik-App enthält, die dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="8efcd-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8efcd-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="8efcd-125">-TriggerName</span></span>
<span data-ttu-id="8efcd-126">Gibt den Namen des Triggers der Logik-App an, die dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="8efcd-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="8efcd-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8efcd-127">-Confirm</span></span>
<span data-ttu-id="8efcd-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8efcd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8efcd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8efcd-129">-WhatIf</span></span>
<span data-ttu-id="8efcd-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8efcd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8efcd-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8efcd-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8efcd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efcd-132">CommonParameters</span></span>
<span data-ttu-id="8efcd-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efcd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efcd-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8efcd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efcd-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8efcd-135">INPUTS</span></span>

### <span data-ttu-id="8efcd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8efcd-136">System.String</span></span>

## <span data-ttu-id="8efcd-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8efcd-137">OUTPUTS</span></span>

### <span data-ttu-id="8efcd-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="8efcd-138">System.Void</span></span>

## <span data-ttu-id="8efcd-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8efcd-139">NOTES</span></span>

## <span data-ttu-id="8efcd-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8efcd-140">RELATED LINKS</span></span>

[<span data-ttu-id="8efcd-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8efcd-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="8efcd-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="8efcd-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="8efcd-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8efcd-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="8efcd-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8efcd-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="8efcd-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8efcd-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="8efcd-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="8efcd-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



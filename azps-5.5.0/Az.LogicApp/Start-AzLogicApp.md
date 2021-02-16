---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: e93efdaf8ec55c3b7c8fb0793a24e062553545ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161417"
---
# <span data-ttu-id="ba8ea-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba8ea-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="ba8ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8ea-103">Führt eine Logik-App in einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="ba8ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba8ea-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba8ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba8ea-105">DESCRIPTION</span></span>
<span data-ttu-id="ba8ea-106">Das **Cmdlet "Start-AzLogicApp"** führt eine Logik-App mithilfe des Features "Logik-Apps" aus.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="ba8ea-107">Geben Sie einen Namen, eine Ressourcengruppe und einen Trigger an.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="ba8ea-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba8ea-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba8ea-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie hinter dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba8ea-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba8ea-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba8ea-112">EXAMPLES</span></span>

### <span data-ttu-id="ba8ea-113">Beispiel 1: Ausführen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="ba8ea-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="ba8ea-114">Mit diesem Befehl wird die Logik-App in der Ressourcengruppe "ResourceGroup11" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ba8ea-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba8ea-115">PARAMETERS</span></span>

### <span data-ttu-id="ba8ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8ea-116">-DefaultProfile</span></span>
<span data-ttu-id="ba8ea-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ba8ea-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba8ea-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ba8ea-118">-Name</span></span>
<span data-ttu-id="ba8ea-119">Gibt den Namen der Logik-App an, die dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ba8ea-120">-Parameters</span><span class="sxs-lookup"><span data-stu-id="ba8ea-120">-Parameters</span></span>
<span data-ttu-id="ba8ea-121">Gibt ein Parametersammlungsobjekt der Logik-App an.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="ba8ea-122">Geben Sie eine Hashtabelle, ein Wörterbuch \<string\> oder ein Wörterbuch \<string, WorkflowParameter\> an.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="ba8ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba8ea-124">Gibt den Namen der Ressourcengruppe an, die die Logik-App enthält, die dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ba8ea-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ba8ea-125">-TriggerName</span></span>
<span data-ttu-id="ba8ea-126">Gibt den Namen des Triggers der Logik-App an, die dieses Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ba8ea-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba8ea-127">-Confirm</span></span>
<span data-ttu-id="ba8ea-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba8ea-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ba8ea-129">-WhatIf</span></span>
<span data-ttu-id="ba8ea-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba8ea-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba8ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8ea-132">CommonParameters</span></span>
<span data-ttu-id="ba8ea-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8ea-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8ea-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8ea-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba8ea-135">INPUTS</span></span>

### <span data-ttu-id="ba8ea-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ba8ea-136">System.String</span></span>

## <span data-ttu-id="ba8ea-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba8ea-137">OUTPUTS</span></span>

### <span data-ttu-id="ba8ea-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="ba8ea-138">System.Void</span></span>

## <span data-ttu-id="ba8ea-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ba8ea-139">NOTES</span></span>

## <span data-ttu-id="ba8ea-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ba8ea-140">RELATED LINKS</span></span>

[<span data-ttu-id="ba8ea-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba8ea-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="ba8ea-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="ba8ea-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="ba8ea-143">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba8ea-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="ba8ea-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba8ea-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="ba8ea-145">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba8ea-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="ba8ea-146">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="ba8ea-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



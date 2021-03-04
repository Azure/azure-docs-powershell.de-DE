---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: f9feca370a2672b14252691711810f5de241aa78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925536"
---
# <span data-ttu-id="2886f-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2886f-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="2886f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2886f-102">SYNOPSIS</span></span>
<span data-ttu-id="2886f-103">Entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2886f-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="2886f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2886f-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2886f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2886f-105">DESCRIPTION</span></span>
<span data-ttu-id="2886f-106">Das **Cmdlet Remove-AzLogicApp** entfernt eine Logik-App aus einer Ressourcengruppe mithilfe des Features Logik-Apps.</span><span class="sxs-lookup"><span data-stu-id="2886f-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="2886f-107">Geben Sie die Logik-App und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2886f-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="2886f-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="2886f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2886f-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="2886f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2886f-110">Um die Namen dynamischer Parameter zu ermitteln, geben Sie nach dem Namen des Cmdlets einen Bindestrich (-) ein, und drücken Sie dann wiederholt die TAB-TASTE, um die verfügbaren Parameter zu durchkreisen.</span><span class="sxs-lookup"><span data-stu-id="2886f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2886f-111">Wenn Sie einen erforderlichen Vorlagenparameter weglassen, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2886f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2886f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2886f-112">EXAMPLES</span></span>

### <span data-ttu-id="2886f-113">Beispiel 1: Entfernen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="2886f-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="2886f-114">Mit diesem Befehl wird eine Logik-App aus einer Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="2886f-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="2886f-115">Der Befehl enthält den *Parameter Erzwingen,* der verhindert, dass der Befehl Sie zur Bestätigung einfordert.</span><span class="sxs-lookup"><span data-stu-id="2886f-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="2886f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2886f-116">PARAMETERS</span></span>

### <span data-ttu-id="2886f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2886f-117">-DefaultProfile</span></span>
<span data-ttu-id="2886f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2886f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2886f-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="2886f-119">-Force</span></span>
<span data-ttu-id="2886f-120">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="2886f-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2886f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2886f-121">-Name</span></span>
<span data-ttu-id="2886f-122">Gibt den Namen der Logik-App an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2886f-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2886f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2886f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2886f-124">Gibt den Namen der Ressourcengruppe an, die die Logik-App enthält, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2886f-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2886f-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2886f-125">-Confirm</span></span>
<span data-ttu-id="2886f-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2886f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2886f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2886f-127">-WhatIf</span></span>
<span data-ttu-id="2886f-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2886f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2886f-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2886f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2886f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2886f-130">CommonParameters</span></span>
<span data-ttu-id="2886f-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2886f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2886f-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2886f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2886f-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2886f-133">INPUTS</span></span>

### <span data-ttu-id="2886f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="2886f-134">System.String</span></span>

## <span data-ttu-id="2886f-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2886f-135">OUTPUTS</span></span>

### <span data-ttu-id="2886f-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="2886f-136">System.Void</span></span>

## <span data-ttu-id="2886f-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2886f-137">NOTES</span></span>

## <span data-ttu-id="2886f-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2886f-138">RELATED LINKS</span></span>

[<span data-ttu-id="2886f-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2886f-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="2886f-140">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2886f-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="2886f-141">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2886f-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="2886f-142">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2886f-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



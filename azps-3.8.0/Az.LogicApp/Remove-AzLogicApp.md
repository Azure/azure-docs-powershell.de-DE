---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzLogicApp.md
ms.openlocfilehash: 573ebbef14eef64d0dc1dd5a6e193eaac2deec0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995137"
---
# <span data-ttu-id="6d270-101">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d270-101">Remove-AzLogicApp</span></span>

## <span data-ttu-id="6d270-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d270-102">SYNOPSIS</span></span>
<span data-ttu-id="6d270-103">Entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d270-103">Removes a logic app from a resource group.</span></span>

## <span data-ttu-id="6d270-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d270-104">SYNTAX</span></span>

```
Remove-AzLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d270-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d270-105">DESCRIPTION</span></span>
<span data-ttu-id="6d270-106">Das Cmdlet **Remove-AzLogicApp** entfernt eine Logik-App aus einer Ressourcengruppe mithilfe des Features Logik-apps.</span><span class="sxs-lookup"><span data-stu-id="6d270-106">The **Remove-AzLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="6d270-107">Geben Sie die Logik-APP und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6d270-107">Specify the logic app and resource group.</span></span>
<span data-ttu-id="6d270-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d270-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6d270-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="6d270-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6d270-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="6d270-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6d270-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6d270-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6d270-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d270-112">EXAMPLES</span></span>

### <span data-ttu-id="6d270-113">Beispiel 1: Entfernen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="6d270-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="6d270-114">Dieser Befehl entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6d270-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="6d270-115">Der Befehl enthält den Parameter *Force* , der verhindert, dass der Befehl Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="6d270-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="6d270-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d270-116">PARAMETERS</span></span>

### <span data-ttu-id="6d270-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d270-117">-DefaultProfile</span></span>
<span data-ttu-id="6d270-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6d270-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d270-119">-Force</span><span class="sxs-lookup"><span data-stu-id="6d270-119">-Force</span></span>
<span data-ttu-id="6d270-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="6d270-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d270-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6d270-121">-Name</span></span>
<span data-ttu-id="6d270-122">Gibt den Namen der Logik-APP an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6d270-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d270-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d270-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d270-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="6d270-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6d270-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6d270-125">-Confirm</span></span>
<span data-ttu-id="6d270-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6d270-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d270-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d270-127">-WhatIf</span></span>
<span data-ttu-id="6d270-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6d270-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d270-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d270-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d270-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d270-130">CommonParameters</span></span>
<span data-ttu-id="6d270-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d270-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d270-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d270-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d270-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d270-133">INPUTS</span></span>

### <span data-ttu-id="6d270-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6d270-134">System.String</span></span>

## <span data-ttu-id="6d270-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d270-135">OUTPUTS</span></span>

### <span data-ttu-id="6d270-136">System. void</span><span class="sxs-lookup"><span data-stu-id="6d270-136">System.Void</span></span>

## <span data-ttu-id="6d270-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d270-137">NOTES</span></span>

## <span data-ttu-id="6d270-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d270-138">RELATED LINKS</span></span>

[<span data-ttu-id="6d270-139">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d270-139">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="6d270-140">Neu – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d270-140">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="6d270-141">Satz-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d270-141">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="6d270-142">Anfang-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d270-142">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)



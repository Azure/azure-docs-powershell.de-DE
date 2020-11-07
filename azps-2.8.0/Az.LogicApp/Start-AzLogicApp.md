---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/start-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Start-AzLogicApp.md
ms.openlocfilehash: 1ec020aa93b1a7e6964e8f85eb8a02c6a9f895cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650697"
---
# <span data-ttu-id="d1d32-101">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1d32-101">Start-AzLogicApp</span></span>

## <span data-ttu-id="d1d32-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1d32-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d32-103">Führt eine Logik-app in einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="d1d32-103">Runs a logic app in a resource group.</span></span>

## <span data-ttu-id="d1d32-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1d32-104">SYNTAX</span></span>

```
Start-AzLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d32-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1d32-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d32-106">Das Cmdlet " **Start-AzLogicApp** " führt eine Logik-App mithilfe des Features "Logik-Apps" aus.</span><span class="sxs-lookup"><span data-stu-id="d1d32-106">The **Start-AzLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="d1d32-107">Geben Sie einen Namen, eine Ressourcengruppe und einen Trigger an.</span><span class="sxs-lookup"><span data-stu-id="d1d32-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="d1d32-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="d1d32-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d1d32-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="d1d32-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d1d32-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d1d32-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d1d32-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="d1d32-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d1d32-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1d32-112">EXAMPLES</span></span>

### <span data-ttu-id="d1d32-113">Beispiel 1: Ausführen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="d1d32-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="d1d32-114">Dieser Befehl führt die Logik-app in der Ressourcengruppe mit dem Namen ResourceGroup11 aus.</span><span class="sxs-lookup"><span data-stu-id="d1d32-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d1d32-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1d32-115">PARAMETERS</span></span>

### <span data-ttu-id="d1d32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d32-116">-DefaultProfile</span></span>
<span data-ttu-id="d1d32-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d1d32-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1d32-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d1d32-118">-Name</span></span>
<span data-ttu-id="d1d32-119">Gibt den Namen der Logik-APP an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d1d32-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d1d32-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d1d32-120">-Parameters</span></span>
<span data-ttu-id="d1d32-121">Gibt ein Parameter-Auflistungsobjekt der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="d1d32-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="d1d32-122">Geben Sie eine Hashtabelle, eine Wörterbuch \< Zeichenfolge \> oder eine Wörterbuch \< Zeichenfolge, Workflowparameter, an \> .</span><span class="sxs-lookup"><span data-stu-id="d1d32-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="d1d32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d32-123">-ResourceGroupName</span></span>
<span data-ttu-id="d1d32-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet gestartete Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="d1d32-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d1d32-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="d1d32-125">-TriggerName</span></span>
<span data-ttu-id="d1d32-126">Gibt den Namen des Triggers der Logik-APP an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d1d32-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="d1d32-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1d32-127">-Confirm</span></span>
<span data-ttu-id="d1d32-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1d32-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d32-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d32-129">-WhatIf</span></span>
<span data-ttu-id="d1d32-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d32-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d32-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1d32-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d32-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d32-132">CommonParameters</span></span>
<span data-ttu-id="d1d32-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d32-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d32-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1d32-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d32-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1d32-135">INPUTS</span></span>

### <span data-ttu-id="d1d32-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d1d32-136">System.String</span></span>

## <span data-ttu-id="d1d32-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1d32-137">OUTPUTS</span></span>

### <span data-ttu-id="d1d32-138">System. void</span><span class="sxs-lookup"><span data-stu-id="d1d32-138">System.Void</span></span>

## <span data-ttu-id="d1d32-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1d32-139">NOTES</span></span>

## <span data-ttu-id="d1d32-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1d32-140">RELATED LINKS</span></span>

[<span data-ttu-id="d1d32-141">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1d32-141">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="d1d32-142">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="d1d32-142">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="d1d32-143">Neu – AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1d32-143">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="d1d32-144">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1d32-144">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="d1d32-145">Satz-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="d1d32-145">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="d1d32-146">Stopp-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="d1d32-146">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)



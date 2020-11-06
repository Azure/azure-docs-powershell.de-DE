---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: ed8a8c198f626d569d47a9b06b6d9595517f2f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505910"
---
# <span data-ttu-id="62deb-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="62deb-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="62deb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62deb-102">SYNOPSIS</span></span>
<span data-ttu-id="62deb-103">Führt eine Logik-app in einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="62deb-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62deb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62deb-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62deb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62deb-105">DESCRIPTION</span></span>
<span data-ttu-id="62deb-106">Das Cmdlet " **Start-AzureRmLogicApp** " führt eine Logik-App mithilfe des Features "Logik-Apps" aus.</span><span class="sxs-lookup"><span data-stu-id="62deb-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="62deb-107">Geben Sie einen Namen, eine Ressourcengruppe und einen Trigger an.</span><span class="sxs-lookup"><span data-stu-id="62deb-107">Specify a name, resource group, and trigger.</span></span>

<span data-ttu-id="62deb-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="62deb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="62deb-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="62deb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="62deb-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="62deb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="62deb-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="62deb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="62deb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62deb-112">EXAMPLES</span></span>

### <span data-ttu-id="62deb-113">Beispiel 1: Ausführen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="62deb-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="62deb-114">Dieser Befehl führt die Logik-app in der Ressourcengruppe mit dem Namen ResourceGroup11 aus.</span><span class="sxs-lookup"><span data-stu-id="62deb-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="62deb-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="62deb-115">PARAMETERS</span></span>

### <span data-ttu-id="62deb-116">-Name</span><span class="sxs-lookup"><span data-stu-id="62deb-116">-Name</span></span>
<span data-ttu-id="62deb-117">Gibt den Namen der Logik-APP an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="62deb-117">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="62deb-118">-Parameter</span><span class="sxs-lookup"><span data-stu-id="62deb-118">-Parameters</span></span>
<span data-ttu-id="62deb-119">Gibt ein Parameter-Auflistungsobjekt der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="62deb-119">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="62deb-120">Angeben einer Hashtabelle, eines Wörterbuchs \<string\> oder eines Wörterbuchs \<string, WorkflowParameter\></span><span class="sxs-lookup"><span data-stu-id="62deb-120">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="62deb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62deb-121">-ResourceGroupName</span></span>
<span data-ttu-id="62deb-122">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet gestartete Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="62deb-122">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="62deb-123">-Triggername</span><span class="sxs-lookup"><span data-stu-id="62deb-123">-TriggerName</span></span>
<span data-ttu-id="62deb-124">Gibt den Namen des Triggers der Logik-APP an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="62deb-124">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="62deb-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62deb-125">-Confirm</span></span>
<span data-ttu-id="62deb-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62deb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62deb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62deb-127">-WhatIf</span></span>
<span data-ttu-id="62deb-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62deb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62deb-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62deb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62deb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62deb-130">-DefaultProfile</span></span>
<span data-ttu-id="62deb-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62deb-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62deb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62deb-132">CommonParameters</span></span>
<span data-ttu-id="62deb-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62deb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62deb-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62deb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62deb-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62deb-135">INPUTS</span></span>

## <span data-ttu-id="62deb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62deb-136">OUTPUTS</span></span>

### <span data-ttu-id="62deb-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="62deb-137">System.Object</span></span>

## <span data-ttu-id="62deb-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="62deb-138">NOTES</span></span>

## <span data-ttu-id="62deb-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62deb-139">RELATED LINKS</span></span>

[<span data-ttu-id="62deb-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="62deb-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="62deb-141">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="62deb-141">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="62deb-142">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="62deb-142">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="62deb-143">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="62deb-143">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="62deb-144">Satz-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="62deb-144">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="62deb-145">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="62deb-145">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)



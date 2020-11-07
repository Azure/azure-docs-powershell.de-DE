---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 50C359FC-D98C-4C2C-87EE-BE9A25C3EDC6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/start-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Start-AzureRmLogicApp.md
ms.openlocfilehash: 316df4d265b32fc87388b701f096df61df246d85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664567"
---
# <span data-ttu-id="a352c-101">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a352c-101">Start-AzureRmLogicApp</span></span>

## <span data-ttu-id="a352c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a352c-102">SYNOPSIS</span></span>
<span data-ttu-id="a352c-103">Führt eine Logik-app in einer Ressourcengruppe aus.</span><span class="sxs-lookup"><span data-stu-id="a352c-103">Runs a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a352c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a352c-104">SYNTAX</span></span>

```
Start-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Parameters <Object>] -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a352c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a352c-105">DESCRIPTION</span></span>
<span data-ttu-id="a352c-106">Das Cmdlet " **Start-AzureRmLogicApp** " führt eine Logik-App mithilfe des Features "Logik-Apps" aus.</span><span class="sxs-lookup"><span data-stu-id="a352c-106">The **Start-AzureRmLogicApp** cmdlet runs a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="a352c-107">Geben Sie einen Namen, eine Ressourcengruppe und einen Trigger an.</span><span class="sxs-lookup"><span data-stu-id="a352c-107">Specify a name, resource group, and trigger.</span></span>
<span data-ttu-id="a352c-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="a352c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a352c-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="a352c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a352c-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a352c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a352c-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a352c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a352c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a352c-112">EXAMPLES</span></span>

### <span data-ttu-id="a352c-113">Beispiel 1: Ausführen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="a352c-113">Example 1: Run a logic app</span></span>
```
PS C:\>Start-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -TriggerName "Trigger22"
```

<span data-ttu-id="a352c-114">Dieser Befehl führt die Logik-app in der Ressourcengruppe mit dem Namen ResourceGroup11 aus.</span><span class="sxs-lookup"><span data-stu-id="a352c-114">This command runs the logic app in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a352c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a352c-115">PARAMETERS</span></span>

### <span data-ttu-id="a352c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a352c-116">-DefaultProfile</span></span>
<span data-ttu-id="a352c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a352c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a352c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a352c-118">-Name</span></span>
<span data-ttu-id="a352c-119">Gibt den Namen der Logik-APP an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a352c-119">Specifies the name of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a352c-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a352c-120">-Parameters</span></span>
<span data-ttu-id="a352c-121">Gibt ein Parameter-Auflistungsobjekt der Logik-APP an.</span><span class="sxs-lookup"><span data-stu-id="a352c-121">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="a352c-122">Angeben einer Hashtabelle, eines Wörterbuchs \<string\> oder eines Wörterbuchs \<string, WorkflowParameter\></span><span class="sxs-lookup"><span data-stu-id="a352c-122">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="a352c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a352c-123">-ResourceGroupName</span></span>
<span data-ttu-id="a352c-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet gestartete Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="a352c-124">Specifies the name of the resource group that contains the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a352c-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="a352c-125">-TriggerName</span></span>
<span data-ttu-id="a352c-126">Gibt den Namen des Triggers der Logik-APP an, die von diesem Cmdlet gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="a352c-126">Specifies the name of the trigger of the logic app that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a352c-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a352c-127">-Confirm</span></span>
<span data-ttu-id="a352c-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a352c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a352c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a352c-129">-WhatIf</span></span>
<span data-ttu-id="a352c-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a352c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a352c-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a352c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a352c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a352c-132">CommonParameters</span></span>
<span data-ttu-id="a352c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a352c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a352c-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a352c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a352c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a352c-135">INPUTS</span></span>

### <span data-ttu-id="a352c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a352c-136">System.String</span></span>

## <span data-ttu-id="a352c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a352c-137">OUTPUTS</span></span>

### <span data-ttu-id="a352c-138">System. void</span><span class="sxs-lookup"><span data-stu-id="a352c-138">System.Void</span></span>

## <span data-ttu-id="a352c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a352c-139">NOTES</span></span>

## <span data-ttu-id="a352c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a352c-140">RELATED LINKS</span></span>

[<span data-ttu-id="a352c-141">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a352c-141">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="a352c-142">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a352c-142">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="a352c-143">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a352c-143">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="a352c-144">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a352c-144">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="a352c-145">Satz-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="a352c-145">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="a352c-146">Stopp-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a352c-146">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)



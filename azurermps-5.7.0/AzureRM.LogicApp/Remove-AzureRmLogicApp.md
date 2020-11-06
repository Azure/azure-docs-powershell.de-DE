---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 3650e04b8c6d254b396072c55d39cde38a1328f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498905"
---
# <span data-ttu-id="8bdeb-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8bdeb-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="8bdeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bdeb-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdeb-103">Entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8bdeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bdeb-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bdeb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bdeb-105">DESCRIPTION</span></span>
<span data-ttu-id="8bdeb-106">Das Cmdlet **Remove-AzureRmLogicApp** entfernt eine Logik-App aus einer Ressourcengruppe mithilfe des Features Logik-apps.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="8bdeb-107">Geben Sie die Logik-APP und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="8bdeb-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8bdeb-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8bdeb-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8bdeb-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8bdeb-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bdeb-112">EXAMPLES</span></span>

### <span data-ttu-id="8bdeb-113">Beispiel 1: Entfernen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="8bdeb-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="8bdeb-114">Dieser Befehl entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="8bdeb-115">Der Befehl enthält den Parameter *Force* , der verhindert, dass der Befehl Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="8bdeb-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bdeb-116">PARAMETERS</span></span>

### <span data-ttu-id="8bdeb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bdeb-117">-DefaultProfile</span></span>
<span data-ttu-id="8bdeb-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8bdeb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bdeb-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8bdeb-119">-Force</span></span>
<span data-ttu-id="8bdeb-120">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdeb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8bdeb-121">-Name</span></span>
<span data-ttu-id="8bdeb-122">Gibt den Namen der Logik-APP an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdeb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bdeb-123">-ResourceGroupName</span></span>
<span data-ttu-id="8bdeb-124">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8bdeb-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8bdeb-125">-Confirm</span></span>
<span data-ttu-id="8bdeb-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdeb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bdeb-127">-WhatIf</span></span>
<span data-ttu-id="8bdeb-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bdeb-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdeb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdeb-130">CommonParameters</span></span>
<span data-ttu-id="8bdeb-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdeb-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdeb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdeb-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bdeb-133">INPUTS</span></span>

### <span data-ttu-id="8bdeb-134">Keine</span><span class="sxs-lookup"><span data-stu-id="8bdeb-134">None</span></span>
<span data-ttu-id="8bdeb-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8bdeb-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8bdeb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bdeb-136">OUTPUTS</span></span>

### <span data-ttu-id="8bdeb-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="8bdeb-137">System.Object</span></span>

## <span data-ttu-id="8bdeb-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bdeb-138">NOTES</span></span>

## <span data-ttu-id="8bdeb-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bdeb-139">RELATED LINKS</span></span>

[<span data-ttu-id="8bdeb-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8bdeb-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="8bdeb-141">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8bdeb-141">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="8bdeb-142">Satz-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8bdeb-142">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="8bdeb-143">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8bdeb-143">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



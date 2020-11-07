---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 6b76440b2d9e61075ac19e5a6fa0846a95a77669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663917"
---
# <span data-ttu-id="dd8d5-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dd8d5-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="dd8d5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8d5-103">Entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd8d5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd8d5-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd8d5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd8d5-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8d5-106">Das Cmdlet **Remove-AzureRmLogicApp** entfernt eine Logik-App aus einer Ressourcengruppe mithilfe des Features Logik-apps.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="dd8d5-107">Geben Sie die Logik-APP und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="dd8d5-108">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="dd8d5-109">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="dd8d5-110">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="dd8d5-111">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="dd8d5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd8d5-112">EXAMPLES</span></span>

### <span data-ttu-id="dd8d5-113">Beispiel 1: Entfernen einer Logik-App</span><span class="sxs-lookup"><span data-stu-id="dd8d5-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="dd8d5-114">Dieser Befehl entfernt eine Logik-App aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="dd8d5-115">Der Befehl enthält den Parameter *Force* , der verhindert, dass der Befehl Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="dd8d5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd8d5-116">PARAMETERS</span></span>

### <span data-ttu-id="dd8d5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dd8d5-117">-Force</span></span>
<span data-ttu-id="dd8d5-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dd8d5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dd8d5-119">-Name</span></span>
<span data-ttu-id="dd8d5-120">Gibt den Namen der Logik-APP an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-120">Specifies the name of the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd8d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="dd8d5-122">Gibt den Namen der Ressourcengruppe an, die die von diesem Cmdlet entfernte Logik-app enthält.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-122">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dd8d5-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dd8d5-123">-Confirm</span></span>
<span data-ttu-id="dd8d5-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8d5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8d5-125">-WhatIf</span></span>
<span data-ttu-id="dd8d5-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8d5-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8d5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8d5-128">-DefaultProfile</span></span>
<span data-ttu-id="dd8d5-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd8d5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8d5-130">CommonParameters</span></span>
<span data-ttu-id="dd8d5-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8d5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8d5-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8d5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8d5-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd8d5-133">INPUTS</span></span>

## <span data-ttu-id="dd8d5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd8d5-134">OUTPUTS</span></span>

### <span data-ttu-id="dd8d5-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="dd8d5-135">System.Object</span></span>

## <span data-ttu-id="dd8d5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd8d5-136">NOTES</span></span>

## <span data-ttu-id="dd8d5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd8d5-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd8d5-138">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dd8d5-138">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="dd8d5-139">Neu – AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dd8d5-139">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="dd8d5-140">Satz-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dd8d5-140">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="dd8d5-141">Anfang-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="dd8d5-141">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: edb55424b16c0cdb6636f715ce6755a317e6f396
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373188"
---
# <span data-ttu-id="285d7-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="285d7-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="285d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="285d7-102">SYNOPSIS</span></span>
<span data-ttu-id="285d7-103">Entfernt eine Automatisierungsvariable.</span><span class="sxs-lookup"><span data-stu-id="285d7-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="285d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="285d7-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="285d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="285d7-105">DESCRIPTION</span></span>
<span data-ttu-id="285d7-106">Das **Cmdlet "Remove-AzAutomationVariable"** entfernt eine Variable aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="285d7-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="285d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="285d7-107">EXAMPLES</span></span>

### <span data-ttu-id="285d7-108">Beispiel 1: Entfernen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="285d7-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="285d7-109">Mit diesem Befehl wird eine Variable namens "StringVariable22" im Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="285d7-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="285d7-110">Dieser Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="285d7-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="285d7-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="285d7-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="285d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="285d7-112">PARAMETERS</span></span>

### <span data-ttu-id="285d7-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="285d7-113">-AutomationAccountName</span></span>
<span data-ttu-id="285d7-114">Gibt den Namen des Automatisierungskontos an, das die variable enthält, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="285d7-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="285d7-115">-DefaultProfile</span></span>
<span data-ttu-id="285d7-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="285d7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="285d7-117">-Name</span><span class="sxs-lookup"><span data-stu-id="285d7-117">-Name</span></span>
<span data-ttu-id="285d7-118">Gibt den Namen der Variablen an, die von diesem Cmdlet gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="285d7-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="285d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="285d7-120">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable löscht.</span><span class="sxs-lookup"><span data-stu-id="285d7-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="285d7-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="285d7-121">-Confirm</span></span>
<span data-ttu-id="285d7-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="285d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="285d7-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="285d7-123">-WhatIf</span></span>
<span data-ttu-id="285d7-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="285d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="285d7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="285d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="285d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="285d7-126">CommonParameters</span></span>
<span data-ttu-id="285d7-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="285d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="285d7-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="285d7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="285d7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="285d7-129">INPUTS</span></span>

### <span data-ttu-id="285d7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="285d7-130">System.String</span></span>

## <span data-ttu-id="285d7-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="285d7-131">OUTPUTS</span></span>

### <span data-ttu-id="285d7-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="285d7-132">System.Void</span></span>

## <span data-ttu-id="285d7-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="285d7-133">NOTES</span></span>

## <span data-ttu-id="285d7-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="285d7-134">RELATED LINKS</span></span>

[<span data-ttu-id="285d7-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="285d7-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="285d7-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="285d7-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="285d7-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="285d7-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)



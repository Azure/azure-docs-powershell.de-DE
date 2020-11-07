---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: cfb8aa96da85cbfe1e9c16277c5c1c3539e04ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657952"
---
# <span data-ttu-id="c0687-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0687-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="c0687-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0687-102">SYNOPSIS</span></span>
<span data-ttu-id="c0687-103">Entfernt eine Automatisierungs Variable.</span><span class="sxs-lookup"><span data-stu-id="c0687-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="c0687-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0687-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0687-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0687-105">DESCRIPTION</span></span>
<span data-ttu-id="c0687-106">Das Cmdlet **Remove-AzAutomationVariable** entfernt eine Variable aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="c0687-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="c0687-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0687-107">EXAMPLES</span></span>

### <span data-ttu-id="c0687-108">Beispiel 1: Entfernen einer Variablen</span><span class="sxs-lookup"><span data-stu-id="c0687-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0687-109">Dieser Befehl entfernt eine Variable mit dem Namen StringVariable22 im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0687-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="c0687-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="c0687-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c0687-111">Daher werden Sie nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c0687-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c0687-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0687-112">PARAMETERS</span></span>

### <span data-ttu-id="c0687-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0687-113">-AutomationAccountName</span></span>
<span data-ttu-id="c0687-114">Gibt den Namen des Automatisierungs Kontos an, das die vom Cmdlet gelöschte Variable enthält.</span><span class="sxs-lookup"><span data-stu-id="c0687-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c0687-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0687-115">-DefaultProfile</span></span>
<span data-ttu-id="c0687-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c0687-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0687-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c0687-117">-Name</span></span>
<span data-ttu-id="c0687-118">Gibt den Namen der vom Cmdlet gelöschten Variablen an.</span><span class="sxs-lookup"><span data-stu-id="c0687-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c0687-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0687-119">-ResourceGroupName</span></span>
<span data-ttu-id="c0687-120">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable löscht.</span><span class="sxs-lookup"><span data-stu-id="c0687-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="c0687-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0687-121">-Confirm</span></span>
<span data-ttu-id="c0687-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0687-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0687-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0687-123">-WhatIf</span></span>
<span data-ttu-id="c0687-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0687-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0687-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0687-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0687-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0687-126">CommonParameters</span></span>
<span data-ttu-id="c0687-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0687-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0687-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0687-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0687-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0687-129">INPUTS</span></span>

### <span data-ttu-id="c0687-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0687-130">System.String</span></span>

## <span data-ttu-id="c0687-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0687-131">OUTPUTS</span></span>

### <span data-ttu-id="c0687-132">System. void</span><span class="sxs-lookup"><span data-stu-id="c0687-132">System.Void</span></span>

## <span data-ttu-id="c0687-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0687-133">NOTES</span></span>

## <span data-ttu-id="c0687-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0687-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0687-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0687-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="c0687-136">Neu – AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0687-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="c0687-137">Satz-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="c0687-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)



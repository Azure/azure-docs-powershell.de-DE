---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 798e5f37fdeb53030d43f132eae59c94ea855fc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657966"
---
# <span data-ttu-id="d5a09-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d5a09-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="d5a09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5a09-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a09-103">Entfernt ein Modul aus Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="d5a09-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="d5a09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5a09-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5a09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5a09-105">DESCRIPTION</span></span>
<span data-ttu-id="d5a09-106">Das Cmdlet **Remove-AzAutomationModule** entfernt ein Modul aus einem Automatisierungs Konto in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d5a09-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="d5a09-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5a09-107">EXAMPLES</span></span>

### <span data-ttu-id="d5a09-108">Beispiel 1: Entfernen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="d5a09-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d5a09-109">Dieser Befehl entfernt ein Modul mit dem Namen ContosoModule aus dem Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d5a09-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d5a09-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5a09-110">PARAMETERS</span></span>

### <span data-ttu-id="d5a09-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d5a09-111">-AutomationAccountName</span></span>
<span data-ttu-id="d5a09-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5a09-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="d5a09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a09-113">-DefaultProfile</span></span>
<span data-ttu-id="d5a09-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d5a09-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5a09-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5a09-115">-Force</span></span>
<span data-ttu-id="d5a09-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d5a09-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a09-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d5a09-117">-Name</span></span>
<span data-ttu-id="d5a09-118">Gibt den Namen des Moduls an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d5a09-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d5a09-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a09-119">-ResourceGroupName</span></span>
<span data-ttu-id="d5a09-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="d5a09-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="d5a09-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5a09-121">-Confirm</span></span>
<span data-ttu-id="d5a09-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5a09-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5a09-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5a09-123">-WhatIf</span></span>
<span data-ttu-id="d5a09-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5a09-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5a09-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5a09-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5a09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a09-126">CommonParameters</span></span>
<span data-ttu-id="d5a09-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a09-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5a09-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a09-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5a09-129">INPUTS</span></span>

### <span data-ttu-id="d5a09-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d5a09-130">System.String</span></span>

## <span data-ttu-id="d5a09-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5a09-131">OUTPUTS</span></span>

### <span data-ttu-id="d5a09-132">System. void</span><span class="sxs-lookup"><span data-stu-id="d5a09-132">System.Void</span></span>

## <span data-ttu-id="d5a09-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5a09-133">NOTES</span></span>

## <span data-ttu-id="d5a09-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5a09-134">RELATED LINKS</span></span>

[<span data-ttu-id="d5a09-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d5a09-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="d5a09-136">Neu – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d5a09-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="d5a09-137">Satz-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d5a09-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)



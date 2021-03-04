---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 9fa84ffed6352dfb566ad02aa2393a7cba7f393b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947563"
---
# <span data-ttu-id="69431-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="69431-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="69431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69431-102">SYNOPSIS</span></span>
<span data-ttu-id="69431-103">Entfernt ein Modul aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="69431-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="69431-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69431-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="69431-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69431-105">DESCRIPTION</span></span>
<span data-ttu-id="69431-106">Das **Cmdlet Remove-AzAutomationModule** entfernt ein Modul aus einem Automatisierungskonto in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="69431-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="69431-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69431-107">EXAMPLES</span></span>

### <span data-ttu-id="69431-108">Beispiel 1: Entfernen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="69431-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="69431-109">Mit diesem Befehl wird ein Modul namens ContosoModule aus dem Automatisierungskonto namens Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="69431-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="69431-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="69431-110">PARAMETERS</span></span>

### <span data-ttu-id="69431-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="69431-111">-AutomationAccountName</span></span>
<span data-ttu-id="69431-112">Gibt den Namen des Automatisierungskontos an, aus dem dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="69431-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="69431-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69431-113">-DefaultProfile</span></span>
<span data-ttu-id="69431-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="69431-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69431-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="69431-115">-Force</span></span>
<span data-ttu-id="69431-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="69431-116">ps_force</span></span>

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

### <span data-ttu-id="69431-117">-Name</span><span class="sxs-lookup"><span data-stu-id="69431-117">-Name</span></span>
<span data-ttu-id="69431-118">Gibt den Namen des Moduls an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="69431-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="69431-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69431-119">-ResourceGroupName</span></span>
<span data-ttu-id="69431-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="69431-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="69431-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69431-121">-Confirm</span></span>
<span data-ttu-id="69431-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69431-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69431-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69431-123">-WhatIf</span></span>
<span data-ttu-id="69431-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69431-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69431-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69431-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69431-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69431-126">CommonParameters</span></span>
<span data-ttu-id="69431-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69431-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69431-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69431-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69431-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69431-129">INPUTS</span></span>

### <span data-ttu-id="69431-130">System.String</span><span class="sxs-lookup"><span data-stu-id="69431-130">System.String</span></span>

## <span data-ttu-id="69431-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69431-131">OUTPUTS</span></span>

### <span data-ttu-id="69431-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="69431-132">System.Void</span></span>

## <span data-ttu-id="69431-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="69431-133">NOTES</span></span>

## <span data-ttu-id="69431-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="69431-134">RELATED LINKS</span></span>

[<span data-ttu-id="69431-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="69431-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="69431-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="69431-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="69431-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="69431-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)



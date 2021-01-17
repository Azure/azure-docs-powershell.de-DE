---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471276"
---
# <span data-ttu-id="8f198-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f198-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="8f198-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f198-102">SYNOPSIS</span></span>
<span data-ttu-id="8f198-103">Entfernt ein Modul aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="8f198-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="8f198-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8f198-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8f198-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f198-105">DESCRIPTION</span></span>
<span data-ttu-id="8f198-106">Das **Cmdlet "Remove-AzAutomationModule"** entfernt ein Modul aus einem Automatisierungskonto in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="8f198-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="8f198-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8f198-107">EXAMPLES</span></span>

### <span data-ttu-id="8f198-108">Beispiel 1: Entfernen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="8f198-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f198-109">Mit diesem Befehl wird das Modul "ContosoModule" aus dem Automatisierungskonto namens "Contoso17" entfernt.</span><span class="sxs-lookup"><span data-stu-id="8f198-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8f198-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f198-110">PARAMETERS</span></span>

### <span data-ttu-id="8f198-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f198-111">-AutomationAccountName</span></span>
<span data-ttu-id="8f198-112">Gibt den Namen des Automatisierungskontos an, aus dem dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="8f198-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="8f198-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f198-113">-DefaultProfile</span></span>
<span data-ttu-id="8f198-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8f198-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f198-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8f198-115">-Force</span></span>
<span data-ttu-id="8f198-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="8f198-116">ps_force</span></span>

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

### <span data-ttu-id="8f198-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f198-117">-Name</span></span>
<span data-ttu-id="8f198-118">Gibt den Namen des Moduls an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8f198-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8f198-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f198-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f198-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="8f198-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="8f198-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f198-121">-Confirm</span></span>
<span data-ttu-id="8f198-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f198-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f198-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8f198-123">-WhatIf</span></span>
<span data-ttu-id="8f198-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f198-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f198-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f198-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f198-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f198-126">CommonParameters</span></span>
<span data-ttu-id="8f198-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f198-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f198-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f198-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f198-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8f198-129">INPUTS</span></span>

### <span data-ttu-id="8f198-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8f198-130">System.String</span></span>

## <span data-ttu-id="8f198-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8f198-131">OUTPUTS</span></span>

### <span data-ttu-id="8f198-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="8f198-132">System.Void</span></span>

## <span data-ttu-id="8f198-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8f198-133">NOTES</span></span>

## <span data-ttu-id="8f198-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8f198-134">RELATED LINKS</span></span>

[<span data-ttu-id="8f198-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f198-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="8f198-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f198-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="8f198-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8f198-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005130"
---
# <span data-ttu-id="2f53a-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2f53a-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="2f53a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2f53a-102">SYNOPSIS</span></span>
<span data-ttu-id="2f53a-103">Entfernt ein Modul aus Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="2f53a-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="2f53a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f53a-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f53a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2f53a-105">DESCRIPTION</span></span>
<span data-ttu-id="2f53a-106">Das Cmdlet **Remove-AzAutomationModule** entfernt ein Modul aus einem Automatisierungs Konto in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2f53a-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="2f53a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2f53a-107">EXAMPLES</span></span>

### <span data-ttu-id="2f53a-108">Beispiel 1: Entfernen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="2f53a-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2f53a-109">Dieser Befehl entfernt ein Modul mit dem Namen ContosoModule aus dem Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2f53a-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="2f53a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f53a-110">PARAMETERS</span></span>

### <span data-ttu-id="2f53a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2f53a-111">-AutomationAccountName</span></span>
<span data-ttu-id="2f53a-112">Gibt den Namen des Automatisierungs Kontos an, aus dem dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="2f53a-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="2f53a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f53a-113">-DefaultProfile</span></span>
<span data-ttu-id="2f53a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2f53a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f53a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2f53a-115">-Force</span></span>
<span data-ttu-id="2f53a-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="2f53a-116">ps_force</span></span>

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

### <span data-ttu-id="2f53a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="2f53a-117">-Name</span></span>
<span data-ttu-id="2f53a-118">Gibt den Namen des Moduls an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2f53a-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f53a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f53a-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f53a-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet ein Modul entfernt.</span><span class="sxs-lookup"><span data-stu-id="2f53a-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="2f53a-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2f53a-121">-Confirm</span></span>
<span data-ttu-id="2f53a-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2f53a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f53a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f53a-123">-WhatIf</span></span>
<span data-ttu-id="2f53a-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f53a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f53a-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f53a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f53a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f53a-126">CommonParameters</span></span>
<span data-ttu-id="2f53a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f53a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f53a-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f53a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f53a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2f53a-129">INPUTS</span></span>

### <span data-ttu-id="2f53a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2f53a-130">System.String</span></span>

## <span data-ttu-id="2f53a-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2f53a-131">OUTPUTS</span></span>

### <span data-ttu-id="2f53a-132">System. void</span><span class="sxs-lookup"><span data-stu-id="2f53a-132">System.Void</span></span>

## <span data-ttu-id="2f53a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="2f53a-133">NOTES</span></span>

## <span data-ttu-id="2f53a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2f53a-134">RELATED LINKS</span></span>

[<span data-ttu-id="2f53a-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2f53a-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="2f53a-136">Neu – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2f53a-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="2f53a-137">Satz-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="2f53a-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)



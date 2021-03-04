---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 35ef4a5629726b33a8d9099da78134e6a0bac8b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947584"
---
# <span data-ttu-id="596d0-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="596d0-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="596d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="596d0-102">SYNOPSIS</span></span>
<span data-ttu-id="596d0-103">Entfernt die Hybridarbeitergruppe aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="596d0-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="596d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="596d0-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="596d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="596d0-105">DESCRIPTION</span></span>
<span data-ttu-id="596d0-106">Das Remove-AzAutomationHybridWorkerGroup cmdlet entfernt eine Hybridarbeitergruppe aus der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="596d0-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="596d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="596d0-107">EXAMPLES</span></span>

### <span data-ttu-id="596d0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="596d0-108">Example 1</span></span>
<span data-ttu-id="596d0-109">Mit diesem Befehl wird ein Hybridarbeiter namens entfernt.</span><span class="sxs-lookup"><span data-stu-id="596d0-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="596d0-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="596d0-110">PARAMETERS</span></span>

### <span data-ttu-id="596d0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="596d0-111">-AutomationAccountName</span></span>
<span data-ttu-id="596d0-112">Der Name des Automatisierungskontos.</span><span class="sxs-lookup"><span data-stu-id="596d0-112">The automation account name.</span></span>

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

### <span data-ttu-id="596d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="596d0-113">-DefaultProfile</span></span>
<span data-ttu-id="596d0-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="596d0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="596d0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="596d0-115">-Name</span></span>
<span data-ttu-id="596d0-116">Der Name der Hybridarbeitergruppe.</span><span class="sxs-lookup"><span data-stu-id="596d0-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="596d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="596d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="596d0-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="596d0-118">The resource group name.</span></span>

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

### <span data-ttu-id="596d0-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="596d0-119">-Confirm</span></span>
<span data-ttu-id="596d0-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="596d0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596d0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="596d0-121">-WhatIf</span></span>
<span data-ttu-id="596d0-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="596d0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="596d0-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="596d0-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="596d0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="596d0-124">CommonParameters</span></span>
<span data-ttu-id="596d0-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="596d0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="596d0-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="596d0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="596d0-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="596d0-127">INPUTS</span></span>

### <span data-ttu-id="596d0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="596d0-128">System.String</span></span>

## <span data-ttu-id="596d0-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="596d0-129">OUTPUTS</span></span>

### <span data-ttu-id="596d0-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="596d0-130">System.Void</span></span>

## <span data-ttu-id="596d0-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="596d0-131">NOTES</span></span>

## <span data-ttu-id="596d0-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="596d0-132">RELATED LINKS</span></span>

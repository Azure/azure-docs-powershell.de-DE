---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100166884"
---
# <span data-ttu-id="42f0f-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="42f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="42f0f-103">Ruft ein Runbook ab.</span><span class="sxs-lookup"><span data-stu-id="42f0f-103">Gets a runbook.</span></span>

## <span data-ttu-id="42f0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42f0f-104">SYNTAX</span></span>

### <span data-ttu-id="42f0f-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="42f0f-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42f0f-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="42f0f-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42f0f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="42f0f-107">DESCRIPTION</span></span>
<span data-ttu-id="42f0f-108">Das **Cmdlet "Get-AzAutomationRunbook"** ruft Runbooks für die Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="42f0f-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="42f0f-109">Um ein bestimmtes Runbook zu erhalten, geben Sie dessen Namen an.</span><span class="sxs-lookup"><span data-stu-id="42f0f-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="42f0f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="42f0f-110">EXAMPLES</span></span>

### <span data-ttu-id="42f0f-111">Beispiel 1: Alle Runbooks erhalten</span><span class="sxs-lookup"><span data-stu-id="42f0f-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="42f0f-112">Dieser Befehl ruft alle Runbooks im Azure-Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="42f0f-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="42f0f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42f0f-113">PARAMETERS</span></span>

### <span data-ttu-id="42f0f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42f0f-114">-AutomationAccountName</span></span>
<span data-ttu-id="42f0f-115">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet Runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="42f0f-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="42f0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f0f-116">-DefaultProfile</span></span>
<span data-ttu-id="42f0f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="42f0f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42f0f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="42f0f-118">-Name</span></span>
<span data-ttu-id="42f0f-119">Gibt den Namen eines Runbooks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="42f0f-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42f0f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42f0f-120">-ResourceGroupName</span></span>
<span data-ttu-id="42f0f-121">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="42f0f-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="42f0f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f0f-122">CommonParameters</span></span>
<span data-ttu-id="42f0f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f0f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42f0f-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f0f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f0f-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="42f0f-125">INPUTS</span></span>

### <span data-ttu-id="42f0f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="42f0f-126">System.String</span></span>

## <span data-ttu-id="42f0f-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="42f0f-127">OUTPUTS</span></span>

### <span data-ttu-id="42f0f-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="42f0f-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="42f0f-129">NOTES</span></span>

## <span data-ttu-id="42f0f-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="42f0f-130">RELATED LINKS</span></span>

[<span data-ttu-id="42f0f-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="42f0f-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42f0f-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



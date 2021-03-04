---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 00d6908e244a54fb2dbd501f0d944fc9cfdbdff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949752"
---
# <span data-ttu-id="33b75-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="33b75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33b75-102">SYNOPSIS</span></span>
<span data-ttu-id="33b75-103">Ruft ein Runbook ab.</span><span class="sxs-lookup"><span data-stu-id="33b75-103">Gets a runbook.</span></span>

## <span data-ttu-id="33b75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33b75-104">SYNTAX</span></span>

### <span data-ttu-id="33b75-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="33b75-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33b75-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="33b75-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33b75-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33b75-107">DESCRIPTION</span></span>
<span data-ttu-id="33b75-108">Das **Get-AzAutomationRunbook-Cmdlet** ruft Azure Automation-Runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="33b75-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="33b75-109">Um ein bestimmtes Runbook zu erhalten, geben Sie dessen Namen an.</span><span class="sxs-lookup"><span data-stu-id="33b75-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="33b75-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="33b75-110">EXAMPLES</span></span>

### <span data-ttu-id="33b75-111">Beispiel 1: Alle Runbooks erhalten</span><span class="sxs-lookup"><span data-stu-id="33b75-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="33b75-112">Dieser Befehl ruft alle Runbooks im Azure Automation-Konto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="33b75-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="33b75-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="33b75-113">PARAMETERS</span></span>

### <span data-ttu-id="33b75-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="33b75-114">-AutomationAccountName</span></span>
<span data-ttu-id="33b75-115">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet Runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="33b75-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="33b75-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b75-116">-DefaultProfile</span></span>
<span data-ttu-id="33b75-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="33b75-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33b75-118">-Name</span><span class="sxs-lookup"><span data-stu-id="33b75-118">-Name</span></span>
<span data-ttu-id="33b75-119">Gibt den Namen eines Runbooks an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="33b75-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="33b75-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b75-120">-ResourceGroupName</span></span>
<span data-ttu-id="33b75-121">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet Runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="33b75-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="33b75-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b75-122">CommonParameters</span></span>
<span data-ttu-id="33b75-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b75-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b75-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b75-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b75-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="33b75-125">INPUTS</span></span>

### <span data-ttu-id="33b75-126">System.String</span><span class="sxs-lookup"><span data-stu-id="33b75-126">System.String</span></span>

## <span data-ttu-id="33b75-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="33b75-127">OUTPUTS</span></span>

### <span data-ttu-id="33b75-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="33b75-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="33b75-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="33b75-129">NOTES</span></span>

## <span data-ttu-id="33b75-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="33b75-130">RELATED LINKS</span></span>

[<span data-ttu-id="33b75-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="33b75-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="33b75-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



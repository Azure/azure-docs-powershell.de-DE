---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179920"
---
# <span data-ttu-id="ca6b5-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="ca6b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca6b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6b5-103">Ruft einen runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-103">Gets a runbook.</span></span>

## <span data-ttu-id="ca6b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca6b5-104">SYNTAX</span></span>

### <span data-ttu-id="ca6b5-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca6b5-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca6b5-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ca6b5-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca6b5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca6b5-107">DESCRIPTION</span></span>
<span data-ttu-id="ca6b5-108">Das Cmdlet " **Get-AzAutomationRunbook** " ruft Azure Automation runbooks.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="ca6b5-109">Um eine bestimmte runbooks zu erhalten, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="ca6b5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca6b5-110">EXAMPLES</span></span>

### <span data-ttu-id="ca6b5-111">Beispiel 1: Abrufen aller runbooks</span><span class="sxs-lookup"><span data-stu-id="ca6b5-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ca6b5-112">Dieser Befehl ruft alle runbooks im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ca6b5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca6b5-113">PARAMETERS</span></span>

### <span data-ttu-id="ca6b5-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca6b5-114">-AutomationAccountName</span></span>
<span data-ttu-id="ca6b5-115">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="ca6b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6b5-116">-DefaultProfile</span></span>
<span data-ttu-id="ca6b5-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ca6b5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca6b5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ca6b5-118">-Name</span></span>
<span data-ttu-id="ca6b5-119">Gibt den Namen einer runbooks an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ca6b5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca6b5-120">-ResourceGroupName</span></span>
<span data-ttu-id="ca6b5-121">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="ca6b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6b5-122">CommonParameters</span></span>
<span data-ttu-id="ca6b5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6b5-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca6b5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6b5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca6b5-125">INPUTS</span></span>

### <span data-ttu-id="ca6b5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ca6b5-126">System.String</span></span>

## <span data-ttu-id="ca6b5-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca6b5-127">OUTPUTS</span></span>

### <span data-ttu-id="ca6b5-128">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="ca6b5-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ca6b5-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca6b5-129">NOTES</span></span>

## <span data-ttu-id="ca6b5-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca6b5-130">RELATED LINKS</span></span>

[<span data-ttu-id="ca6b5-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-132">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-133">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-134">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-137">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="ca6b5-138">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca6b5-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



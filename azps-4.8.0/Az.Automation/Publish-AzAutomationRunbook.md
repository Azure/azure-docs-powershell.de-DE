---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008127"
---
# <span data-ttu-id="793e9-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="793e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="793e9-102">SYNOPSIS</span></span>
<span data-ttu-id="793e9-103">Veröffentlicht eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="793e9-103">Publishes a runbook.</span></span>

## <span data-ttu-id="793e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="793e9-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="793e9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="793e9-105">DESCRIPTION</span></span>
<span data-ttu-id="793e9-106">Das Cmdlet **Publish-AzAutomationRunbook** veröffentlicht einen runbooks zur Verwendung in der Produktionsumgebung von Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="793e9-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="793e9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="793e9-107">EXAMPLES</span></span>

### <span data-ttu-id="793e9-108">Beispiel 1: Veröffentlichen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="793e9-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="793e9-109">Dieser Befehl veröffentlicht die runbooks mit dem Namen Runbk01 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="793e9-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="793e9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="793e9-110">PARAMETERS</span></span>

### <span data-ttu-id="793e9-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="793e9-111">-AutomationAccountName</span></span>
<span data-ttu-id="793e9-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="793e9-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="793e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="793e9-113">-DefaultProfile</span></span>
<span data-ttu-id="793e9-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="793e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="793e9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="793e9-115">-Name</span></span>
<span data-ttu-id="793e9-116">Gibt den Namen der runbooks an, die dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="793e9-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="793e9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="793e9-117">-ResourceGroupName</span></span>
<span data-ttu-id="793e9-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="793e9-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="793e9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="793e9-119">CommonParameters</span></span>
<span data-ttu-id="793e9-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="793e9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="793e9-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="793e9-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="793e9-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="793e9-122">INPUTS</span></span>

### <span data-ttu-id="793e9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="793e9-123">System.String</span></span>

## <span data-ttu-id="793e9-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="793e9-124">OUTPUTS</span></span>

### <span data-ttu-id="793e9-125">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="793e9-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="793e9-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="793e9-126">NOTES</span></span>

## <span data-ttu-id="793e9-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="793e9-127">RELATED LINKS</span></span>

[<span data-ttu-id="793e9-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-130">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-131">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-132">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-134">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="793e9-135">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="793e9-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



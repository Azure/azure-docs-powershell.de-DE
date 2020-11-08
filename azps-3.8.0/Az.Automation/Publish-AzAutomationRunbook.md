---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005154"
---
# <span data-ttu-id="ca969-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="ca969-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca969-102">SYNOPSIS</span></span>
<span data-ttu-id="ca969-103">Veröffentlicht eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="ca969-103">Publishes a runbook.</span></span>

## <span data-ttu-id="ca969-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca969-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca969-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca969-105">DESCRIPTION</span></span>
<span data-ttu-id="ca969-106">Das Cmdlet **Publish-AzAutomationRunbook** veröffentlicht einen runbooks zur Verwendung in der Produktionsumgebung von Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ca969-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="ca969-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca969-107">EXAMPLES</span></span>

### <span data-ttu-id="ca969-108">Beispiel 1: Veröffentlichen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="ca969-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ca969-109">Dieser Befehl veröffentlicht die runbooks mit dem Namen Runbk01 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ca969-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ca969-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca969-110">PARAMETERS</span></span>

### <span data-ttu-id="ca969-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ca969-111">-AutomationAccountName</span></span>
<span data-ttu-id="ca969-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ca969-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="ca969-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca969-113">-DefaultProfile</span></span>
<span data-ttu-id="ca969-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ca969-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca969-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ca969-115">-Name</span></span>
<span data-ttu-id="ca969-116">Gibt den Namen der runbooks an, die dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ca969-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="ca969-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca969-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca969-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="ca969-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="ca969-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca969-119">CommonParameters</span></span>
<span data-ttu-id="ca969-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca969-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca969-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca969-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca969-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca969-122">INPUTS</span></span>

### <span data-ttu-id="ca969-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ca969-123">System.String</span></span>

## <span data-ttu-id="ca969-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca969-124">OUTPUTS</span></span>

### <span data-ttu-id="ca969-125">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="ca969-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ca969-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca969-126">NOTES</span></span>

## <span data-ttu-id="ca969-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca969-127">RELATED LINKS</span></span>

[<span data-ttu-id="ca969-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-130">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-131">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-132">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-134">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="ca969-135">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ca969-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



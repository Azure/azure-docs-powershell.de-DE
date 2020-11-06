---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: e3d60cf277402ac23764b538ba6492ef5c424219
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498485"
---
# <span data-ttu-id="30eea-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="30eea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30eea-102">SYNOPSIS</span></span>
<span data-ttu-id="30eea-103">Veröffentlicht eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="30eea-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30eea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30eea-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30eea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30eea-105">DESCRIPTION</span></span>
<span data-ttu-id="30eea-106">Das Cmdlet **Publish-AzureRmAutomationRunbook** veröffentlicht einen runbooks zur Verwendung in der Produktionsumgebung von Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="30eea-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="30eea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30eea-107">EXAMPLES</span></span>

### <span data-ttu-id="30eea-108">Beispiel 1: Veröffentlichen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="30eea-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="30eea-109">Dieser Befehl veröffentlicht die runbooks mit dem Namen Runbk01 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="30eea-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="30eea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30eea-110">PARAMETERS</span></span>

### <span data-ttu-id="30eea-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="30eea-111">-AutomationAccountName</span></span>
<span data-ttu-id="30eea-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="30eea-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="30eea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30eea-113">-DefaultProfile</span></span>
<span data-ttu-id="30eea-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="30eea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30eea-115">-Name</span><span class="sxs-lookup"><span data-stu-id="30eea-115">-Name</span></span>
<span data-ttu-id="30eea-116">Gibt den Namen der runbooks an, die dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="30eea-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="30eea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30eea-117">-ResourceGroupName</span></span>
<span data-ttu-id="30eea-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="30eea-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="30eea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30eea-119">CommonParameters</span></span>
<span data-ttu-id="30eea-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30eea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30eea-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30eea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30eea-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30eea-122">INPUTS</span></span>

### <span data-ttu-id="30eea-123">System. String</span><span class="sxs-lookup"><span data-stu-id="30eea-123">System.String</span></span>

## <span data-ttu-id="30eea-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30eea-124">OUTPUTS</span></span>

### <span data-ttu-id="30eea-125">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="30eea-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="30eea-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="30eea-126">NOTES</span></span>

## <span data-ttu-id="30eea-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30eea-127">RELATED LINKS</span></span>

[<span data-ttu-id="30eea-128">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-128">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-129">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-129">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-130">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-130">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-131">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-132">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-133">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-133">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-134">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-134">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="30eea-135">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="30eea-135">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



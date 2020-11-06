---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500953"
---
# <span data-ttu-id="cda88-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="cda88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cda88-102">SYNOPSIS</span></span>
<span data-ttu-id="cda88-103">Veröffentlicht eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="cda88-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cda88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cda88-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cda88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cda88-105">DESCRIPTION</span></span>
<span data-ttu-id="cda88-106">Das Cmdlet **Publish-AzureRmAutomationRunbook** veröffentlicht einen runbooks zur Verwendung in der Produktionsumgebung von Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="cda88-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="cda88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cda88-107">EXAMPLES</span></span>

### <span data-ttu-id="cda88-108">Beispiel 1: Veröffentlichen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="cda88-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cda88-109">Dieser Befehl veröffentlicht die runbooks mit dem Namen Runbk01 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cda88-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="cda88-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cda88-110">PARAMETERS</span></span>

### <span data-ttu-id="cda88-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cda88-111">-AutomationAccountName</span></span>
<span data-ttu-id="cda88-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cda88-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="cda88-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cda88-113">-Name</span></span>
<span data-ttu-id="cda88-114">Gibt den Namen der runbooks an, die dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cda88-114">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="cda88-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda88-115">-ResourceGroupName</span></span>
<span data-ttu-id="cda88-116">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="cda88-116">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="cda88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda88-117">-DefaultProfile</span></span>
<span data-ttu-id="cda88-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cda88-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cda88-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda88-119">CommonParameters</span></span>
<span data-ttu-id="cda88-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cda88-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda88-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cda88-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda88-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cda88-122">INPUTS</span></span>

## <span data-ttu-id="cda88-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cda88-123">OUTPUTS</span></span>

### <span data-ttu-id="cda88-124">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="cda88-124">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="cda88-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="cda88-125">NOTES</span></span>

## <span data-ttu-id="cda88-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cda88-126">RELATED LINKS</span></span>

[<span data-ttu-id="cda88-127">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-127">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-128">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-128">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-129">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-129">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-130">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-130">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-131">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-132">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-132">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-133">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-133">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="cda88-134">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="cda88-134">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



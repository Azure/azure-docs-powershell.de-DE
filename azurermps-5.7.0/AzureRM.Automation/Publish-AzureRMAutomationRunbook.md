---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/publish-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 1202ecbdaaf07b9ba5704a01449784172204bf73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478778"
---
# <span data-ttu-id="692c2-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="692c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="692c2-102">SYNOPSIS</span></span>
<span data-ttu-id="692c2-103">Veröffentlicht eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="692c2-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="692c2-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="692c2-105">DESCRIPTION</span></span>
<span data-ttu-id="692c2-106">Das Cmdlet **Publish-AzureRmAutomationRunbook** veröffentlicht einen runbooks zur Verwendung in der Produktionsumgebung von Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="692c2-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="692c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="692c2-107">EXAMPLES</span></span>

### <span data-ttu-id="692c2-108">Beispiel 1: Veröffentlichen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="692c2-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="692c2-109">Dieser Befehl veröffentlicht die runbooks mit dem Namen Runbk01 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="692c2-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="692c2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="692c2-110">PARAMETERS</span></span>

### <span data-ttu-id="692c2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="692c2-111">-AutomationAccountName</span></span>
<span data-ttu-id="692c2-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="692c2-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692c2-113">-DefaultProfile</span></span>
<span data-ttu-id="692c2-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="692c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="692c2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="692c2-115">-Name</span></span>
<span data-ttu-id="692c2-116">Gibt den Namen der runbooks an, die dieses Cmdlet veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="692c2-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="692c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="692c2-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="692c2-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692c2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692c2-119">CommonParameters</span></span>
<span data-ttu-id="692c2-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="692c2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692c2-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692c2-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692c2-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="692c2-122">INPUTS</span></span>

### <span data-ttu-id="692c2-123">Keine</span><span class="sxs-lookup"><span data-stu-id="692c2-123">None</span></span>
<span data-ttu-id="692c2-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="692c2-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="692c2-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="692c2-125">OUTPUTS</span></span>

### <span data-ttu-id="692c2-126">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="692c2-126">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="692c2-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="692c2-127">NOTES</span></span>

## <span data-ttu-id="692c2-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="692c2-128">RELATED LINKS</span></span>

[<span data-ttu-id="692c2-129">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-129">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-130">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-130">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-131">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-132">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-133">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-134">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-134">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-135">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-135">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="692c2-136">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="692c2-136">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



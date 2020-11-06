---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: e543a7da3ce5502e0f78619ca4fbb455b29b82d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479393"
---
# <span data-ttu-id="1801e-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="1801e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1801e-102">SYNOPSIS</span></span>
<span data-ttu-id="1801e-103">Ruft einen runbooks ab.</span><span class="sxs-lookup"><span data-stu-id="1801e-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1801e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1801e-104">SYNTAX</span></span>

### <span data-ttu-id="1801e-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="1801e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1801e-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="1801e-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1801e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1801e-107">DESCRIPTION</span></span>
<span data-ttu-id="1801e-108">Das Cmdlet " **Get-AzureRmAutomationRunbook** " ruft Azure Automation runbooks.</span><span class="sxs-lookup"><span data-stu-id="1801e-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="1801e-109">Um eine bestimmte runbooks zu erhalten, geben Sie den Namen an.</span><span class="sxs-lookup"><span data-stu-id="1801e-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="1801e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1801e-110">EXAMPLES</span></span>

### <span data-ttu-id="1801e-111">Beispiel 1: Abrufen aller runbooks</span><span class="sxs-lookup"><span data-stu-id="1801e-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1801e-112">Dieser Befehl ruft alle runbooks im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="1801e-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1801e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="1801e-113">PARAMETERS</span></span>

### <span data-ttu-id="1801e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1801e-114">-AutomationAccountName</span></span>
<span data-ttu-id="1801e-115">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="1801e-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="1801e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1801e-116">-Name</span></span>
<span data-ttu-id="1801e-117">Gibt den Namen einer runbooks an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1801e-117">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1801e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1801e-118">-ResourceGroupName</span></span>
<span data-ttu-id="1801e-119">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet runbooks erhält.</span><span class="sxs-lookup"><span data-stu-id="1801e-119">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="1801e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1801e-120">-DefaultProfile</span></span>
<span data-ttu-id="1801e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1801e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1801e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1801e-122">CommonParameters</span></span>
<span data-ttu-id="1801e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1801e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1801e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1801e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1801e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1801e-125">INPUTS</span></span>

## <span data-ttu-id="1801e-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1801e-126">OUTPUTS</span></span>

### <span data-ttu-id="1801e-127">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="1801e-127">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="1801e-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="1801e-128">NOTES</span></span>

## <span data-ttu-id="1801e-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1801e-129">RELATED LINKS</span></span>

[<span data-ttu-id="1801e-130">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-130">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-131">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-132">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-133">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-134">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-134">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-135">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-135">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-136">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-136">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="1801e-137">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="1801e-137">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



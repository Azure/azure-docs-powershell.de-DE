---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 69fe223a7b574e370ed58385ed21ab2462e4420f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479981"
---
# <span data-ttu-id="60865-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="60865-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60865-102">SYNOPSIS</span></span>
<span data-ttu-id="60865-103">Ändert eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="60865-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60865-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60865-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60865-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60865-105">DESCRIPTION</span></span>
<span data-ttu-id="60865-106">Das Cmdlet " **Satz-AzureRmAutomationRunbook** " ändert die Konfiguration eines Azure-Automatisierungs-runbooks in APS.</span><span class="sxs-lookup"><span data-stu-id="60865-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="60865-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60865-107">EXAMPLES</span></span>

### <span data-ttu-id="60865-108">Beispiel 1: Aktivieren der ausführlichen Protokollierung für ein runbooks</span><span class="sxs-lookup"><span data-stu-id="60865-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="60865-109">Dieser Befehl aktiviert die ausführliche Protokollierung für die Aufträge des angegebenen runbooks im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="60865-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="60865-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="60865-110">PARAMETERS</span></span>

### <span data-ttu-id="60865-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="60865-111">-AutomationAccountName</span></span>
<span data-ttu-id="60865-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="60865-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="60865-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60865-113">-Description</span></span>
<span data-ttu-id="60865-114">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="60865-114">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60865-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="60865-115">-LogProgress</span></span>
<span data-ttu-id="60865-116">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="60865-116">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60865-117">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="60865-117">-LogVerbose</span></span>
<span data-ttu-id="60865-118">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="60865-118">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60865-119">-Name</span><span class="sxs-lookup"><span data-stu-id="60865-119">-Name</span></span>
<span data-ttu-id="60865-120">Gibt den Namen der runbooks an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="60865-120">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="60865-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60865-121">-ResourceGroupName</span></span>
<span data-ttu-id="60865-122">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="60865-122">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="60865-123">-Tags</span><span class="sxs-lookup"><span data-stu-id="60865-123">-Tags</span></span>
<span data-ttu-id="60865-124">Gibt ein Wörterbuch mit Tags an, um die aktuellen Tags des geänderten runbooks zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="60865-124">Specifies a dictionary of tags to replace the current tags of the modified runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60865-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60865-125">-DefaultProfile</span></span>
<span data-ttu-id="60865-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60865-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60865-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60865-127">CommonParameters</span></span>
<span data-ttu-id="60865-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60865-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60865-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60865-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60865-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60865-130">INPUTS</span></span>

## <span data-ttu-id="60865-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60865-131">OUTPUTS</span></span>

### <span data-ttu-id="60865-132">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="60865-132">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="60865-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="60865-133">NOTES</span></span>

## <span data-ttu-id="60865-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60865-134">RELATED LINKS</span></span>

[<span data-ttu-id="60865-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-137">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-138">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-139">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-140">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-141">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-141">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="60865-142">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="60865-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



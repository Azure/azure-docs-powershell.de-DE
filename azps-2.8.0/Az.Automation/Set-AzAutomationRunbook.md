---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 4dd1eee278adcced1dbace9a30e88b5767037746
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93657939"
---
# <span data-ttu-id="fa662-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="fa662-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa662-102">SYNOPSIS</span></span>
<span data-ttu-id="fa662-103">Ändert eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="fa662-103">Modifies a runbook.</span></span>

## <span data-ttu-id="fa662-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa662-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa662-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa662-105">DESCRIPTION</span></span>
<span data-ttu-id="fa662-106">Das Cmdlet " **Satz-AzAutomationRunbook** " ändert die Konfiguration eines Azure-Automatisierungs-runbooks in APS.</span><span class="sxs-lookup"><span data-stu-id="fa662-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="fa662-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa662-107">EXAMPLES</span></span>

### <span data-ttu-id="fa662-108">Beispiel 1: Aktivieren der ausführlichen Protokollierung für ein runbooks</span><span class="sxs-lookup"><span data-stu-id="fa662-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fa662-109">Dieser Befehl aktiviert die ausführliche Protokollierung für die Aufträge des angegebenen runbooks im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fa662-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fa662-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa662-110">PARAMETERS</span></span>

### <span data-ttu-id="fa662-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fa662-111">-AutomationAccountName</span></span>
<span data-ttu-id="fa662-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="fa662-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="fa662-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa662-113">-DefaultProfile</span></span>
<span data-ttu-id="fa662-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fa662-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa662-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa662-115">-Description</span></span>
<span data-ttu-id="fa662-116">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="fa662-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="fa662-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="fa662-117">-LogProgress</span></span>
<span data-ttu-id="fa662-118">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="fa662-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="fa662-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="fa662-119">-LogVerbose</span></span>
<span data-ttu-id="fa662-120">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="fa662-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="fa662-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fa662-121">-Name</span></span>
<span data-ttu-id="fa662-122">Gibt den Namen der runbooks an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="fa662-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fa662-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa662-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa662-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="fa662-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="fa662-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="fa662-125">-Tag</span></span>
<span data-ttu-id="fa662-126">Die runbooks-Tags.</span><span class="sxs-lookup"><span data-stu-id="fa662-126">The runbook tags.</span></span>

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

### <span data-ttu-id="fa662-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa662-127">CommonParameters</span></span>
<span data-ttu-id="fa662-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa662-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa662-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa662-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa662-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa662-130">INPUTS</span></span>

### <span data-ttu-id="fa662-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fa662-131">System.String</span></span>

### <span data-ttu-id="fa662-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="fa662-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="fa662-133">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fa662-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fa662-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa662-134">OUTPUTS</span></span>

### <span data-ttu-id="fa662-135">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="fa662-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="fa662-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa662-136">NOTES</span></span>

## <span data-ttu-id="fa662-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa662-137">RELATED LINKS</span></span>

[<span data-ttu-id="fa662-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-140">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-141">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-142">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="fa662-145">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fa662-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



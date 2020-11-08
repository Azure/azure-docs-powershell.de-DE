---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 0f65d59a29b06959a9763d3900a8ef07dfa517b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008715"
---
# <span data-ttu-id="9e6f8-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="9e6f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6f8-103">Ändert eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-103">Modifies a runbook.</span></span>

## <span data-ttu-id="9e6f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e6f8-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e6f8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e6f8-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6f8-106">Das Cmdlet " **Satz-AzAutomationRunbook** " ändert die Konfiguration eines Azure-Automatisierungs-runbooks in APS.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="9e6f8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e6f8-107">EXAMPLES</span></span>

### <span data-ttu-id="9e6f8-108">Beispiel 1: Aktivieren der ausführlichen Protokollierung für ein runbooks</span><span class="sxs-lookup"><span data-stu-id="9e6f8-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9e6f8-109">Dieser Befehl aktiviert die ausführliche Protokollierung für die Aufträge des angegebenen runbooks im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9e6f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e6f8-110">PARAMETERS</span></span>

### <span data-ttu-id="9e6f8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e6f8-111">-AutomationAccountName</span></span>
<span data-ttu-id="9e6f8-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="9e6f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6f8-113">-DefaultProfile</span></span>
<span data-ttu-id="9e6f8-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9e6f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e6f8-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e6f8-115">-Description</span></span>
<span data-ttu-id="9e6f8-116">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="9e6f8-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="9e6f8-117">-LogProgress</span></span>
<span data-ttu-id="9e6f8-118">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="9e6f8-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="9e6f8-119">-LogVerbose</span></span>
<span data-ttu-id="9e6f8-120">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="9e6f8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9e6f8-121">-Name</span></span>
<span data-ttu-id="9e6f8-122">Gibt den Namen der runbooks an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="9e6f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e6f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e6f8-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="9e6f8-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e6f8-125">-Tag</span></span>
<span data-ttu-id="9e6f8-126">Die runbooks-Tags.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-126">The runbook tags.</span></span>

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

### <span data-ttu-id="9e6f8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6f8-127">CommonParameters</span></span>
<span data-ttu-id="9e6f8-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6f8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6f8-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6f8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6f8-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e6f8-130">INPUTS</span></span>

### <span data-ttu-id="9e6f8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9e6f8-131">System.String</span></span>

### <span data-ttu-id="9e6f8-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="9e6f8-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="9e6f8-133">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e6f8-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9e6f8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e6f8-134">OUTPUTS</span></span>

### <span data-ttu-id="9e6f8-135">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="9e6f8-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9e6f8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e6f8-136">NOTES</span></span>

## <span data-ttu-id="9e6f8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e6f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="9e6f8-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-140">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-141">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-142">Neu – AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="9e6f8-145">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9e6f8-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)



---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationRunbook.md
ms.openlocfilehash: 26f3214cf98e43a805aab99eb3ad1b92f289b2bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482570"
---
# <span data-ttu-id="7e035-101">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-101">Set-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="7e035-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e035-102">SYNOPSIS</span></span>
<span data-ttu-id="7e035-103">Ändert eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="7e035-103">Modifies a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e035-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e035-104">SYNTAX</span></span>

```
Set-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>]
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e035-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e035-105">DESCRIPTION</span></span>
<span data-ttu-id="7e035-106">Das Cmdlet " **Satz-AzureRmAutomationRunbook** " ändert die Konfiguration eines Azure-Automatisierungs-runbooks in APS.</span><span class="sxs-lookup"><span data-stu-id="7e035-106">The **Set-AzureRmAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="7e035-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e035-107">EXAMPLES</span></span>

### <span data-ttu-id="7e035-108">Beispiel 1: Aktivieren der ausführlichen Protokollierung für ein runbooks</span><span class="sxs-lookup"><span data-stu-id="7e035-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7e035-109">Dieser Befehl aktiviert die ausführliche Protokollierung für die Aufträge des angegebenen runbooks im Azure-Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7e035-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7e035-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e035-110">PARAMETERS</span></span>

### <span data-ttu-id="7e035-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7e035-111">-AutomationAccountName</span></span>
<span data-ttu-id="7e035-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7e035-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="7e035-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e035-113">-DefaultProfile</span></span>
<span data-ttu-id="7e035-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7e035-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e035-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e035-115">-Description</span></span>
<span data-ttu-id="7e035-116">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="7e035-116">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="7e035-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="7e035-117">-LogProgress</span></span>
<span data-ttu-id="7e035-118">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="7e035-118">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="7e035-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="7e035-119">-LogVerbose</span></span>
<span data-ttu-id="7e035-120">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7e035-120">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="7e035-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e035-121">-Name</span></span>
<span data-ttu-id="7e035-122">Gibt den Namen der runbooks an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="7e035-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7e035-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e035-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e035-124">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7e035-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="7e035-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="7e035-125">-Tag</span></span>
<span data-ttu-id="7e035-126">Die runbooks-Tags.</span><span class="sxs-lookup"><span data-stu-id="7e035-126">The runbook tags.</span></span>

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

### <span data-ttu-id="7e035-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e035-127">CommonParameters</span></span>
<span data-ttu-id="7e035-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e035-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e035-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e035-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e035-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e035-130">INPUTS</span></span>

### <span data-ttu-id="7e035-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7e035-131">System.String</span></span>

### <span data-ttu-id="7e035-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="7e035-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="7e035-133">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7e035-133">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7e035-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e035-134">OUTPUTS</span></span>

### <span data-ttu-id="7e035-135">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="7e035-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="7e035-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e035-136">NOTES</span></span>

## <span data-ttu-id="7e035-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e035-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e035-138">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-138">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-139">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-139">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-140">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-140">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-141">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-141">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-142">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-142">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-143">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-143">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-144">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-144">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="7e035-145">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7e035-145">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)



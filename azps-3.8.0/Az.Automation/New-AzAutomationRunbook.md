---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationRunbook.md
ms.openlocfilehash: 25690d1e125dbfe2a7588665ff4dbc71215e21d6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005173"
---
# <span data-ttu-id="2ea54-101">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-101">New-AzAutomationRunbook</span></span>

## <span data-ttu-id="2ea54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ea54-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea54-103">Erstellt ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="2ea54-103">Creates an Automation runbook.</span></span>

## <span data-ttu-id="2ea54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ea54-104">SYNTAX</span></span>

```
New-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ea54-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ea54-105">DESCRIPTION</span></span>
<span data-ttu-id="2ea54-106">Das Cmdlet **New-AzAutomationRunbook** erstellt mithilfe von APS eine leere Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="2ea54-106">The **New-AzAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="2ea54-107">Geben Sie einen Namen für die runbooks an.</span><span class="sxs-lookup"><span data-stu-id="2ea54-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="2ea54-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ea54-108">EXAMPLES</span></span>

### <span data-ttu-id="2ea54-109">Beispiel 1: Erstellen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="2ea54-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2ea54-110">Dieser Befehl erstellt eine runbooks mit dem Namen Runbook02 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2ea54-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2ea54-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ea54-111">PARAMETERS</span></span>

### <span data-ttu-id="2ea54-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2ea54-112">-AutomationAccountName</span></span>
<span data-ttu-id="2ea54-113">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ea54-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="2ea54-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea54-114">-DefaultProfile</span></span>
<span data-ttu-id="2ea54-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2ea54-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ea54-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ea54-116">-Description</span></span>
<span data-ttu-id="2ea54-117">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="2ea54-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="2ea54-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="2ea54-118">-LogProgress</span></span>
<span data-ttu-id="2ea54-119">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="2ea54-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="2ea54-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="2ea54-120">-LogVerbose</span></span>
<span data-ttu-id="2ea54-121">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="2ea54-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="2ea54-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2ea54-122">-Name</span></span>
<span data-ttu-id="2ea54-123">Gibt einen Namen für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="2ea54-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="2ea54-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea54-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ea54-125">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="2ea54-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="2ea54-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="2ea54-126">-Tags</span></span>
<span data-ttu-id="2ea54-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="2ea54-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2ea54-128">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="2ea54-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ea54-129">-Typ</span><span class="sxs-lookup"><span data-stu-id="2ea54-129">-Type</span></span>
<span data-ttu-id="2ea54-130">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="2ea54-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="2ea54-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="2ea54-131">Valid values are:</span></span>
- <span data-ttu-id="2ea54-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="2ea54-132">PowerShell</span></span>
- <span data-ttu-id="2ea54-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="2ea54-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="2ea54-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="2ea54-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="2ea54-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="2ea54-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="2ea54-136">Diagramm</span><span class="sxs-lookup"><span data-stu-id="2ea54-136">Graph</span></span>
- <span data-ttu-id="2ea54-137">Python2 der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="2ea54-137">Python2 The value Graph is obsolete.</span></span>
<span data-ttu-id="2ea54-138">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="2ea54-138">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph, Python2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ea54-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea54-139">CommonParameters</span></span>
<span data-ttu-id="2ea54-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea54-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea54-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ea54-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea54-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ea54-142">INPUTS</span></span>

### <span data-ttu-id="2ea54-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2ea54-143">System.String</span></span>

### <span data-ttu-id="2ea54-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="2ea54-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="2ea54-145">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ea54-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2ea54-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ea54-146">OUTPUTS</span></span>

### <span data-ttu-id="2ea54-147">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="2ea54-147">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="2ea54-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ea54-148">NOTES</span></span>

## <span data-ttu-id="2ea54-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ea54-149">RELATED LINKS</span></span>

[<span data-ttu-id="2ea54-150">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-150">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="2ea54-151">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-151">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2ea54-152">Importieren-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-152">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2ea54-153">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-153">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2ea54-154">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-154">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2ea54-155">Satz-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-155">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="2ea54-156">Anfang-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2ea54-156">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

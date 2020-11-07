---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 77c089e4ab46972892a7fe9ad3cc519dc7f20551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664396"
---
# <span data-ttu-id="214f1-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="214f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="214f1-102">SYNOPSIS</span></span>
<span data-ttu-id="214f1-103">Erstellt ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="214f1-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="214f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="214f1-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="214f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="214f1-105">DESCRIPTION</span></span>
<span data-ttu-id="214f1-106">Das Cmdlet **New-AzureRmAutomationRunbook** erstellt mithilfe von APS eine leere Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="214f1-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="214f1-107">Geben Sie einen Namen für die runbooks an.</span><span class="sxs-lookup"><span data-stu-id="214f1-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="214f1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="214f1-108">EXAMPLES</span></span>

### <span data-ttu-id="214f1-109">Beispiel 1: Erstellen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="214f1-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="214f1-110">Dieser Befehl erstellt eine runbooks mit dem Namen Runbook02 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="214f1-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="214f1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="214f1-111">PARAMETERS</span></span>

### <span data-ttu-id="214f1-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="214f1-112">-AutomationAccountName</span></span>
<span data-ttu-id="214f1-113">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="214f1-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="214f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214f1-114">-DefaultProfile</span></span>
<span data-ttu-id="214f1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="214f1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="214f1-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="214f1-116">-Description</span></span>
<span data-ttu-id="214f1-117">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="214f1-117">Specifies a description for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f1-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="214f1-118">-LogProgress</span></span>
<span data-ttu-id="214f1-119">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="214f1-119">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f1-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="214f1-120">-LogVerbose</span></span>
<span data-ttu-id="214f1-121">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="214f1-121">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="214f1-122">-Name</span></span>
<span data-ttu-id="214f1-123">Gibt einen Namen für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="214f1-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="214f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="214f1-125">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="214f1-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="214f1-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="214f1-126">-Tags</span></span>
<span data-ttu-id="214f1-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="214f1-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="214f1-128">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="214f1-128">For example:</span></span>

<span data-ttu-id="214f1-129">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="214f1-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214f1-130">-Typ</span><span class="sxs-lookup"><span data-stu-id="214f1-130">-Type</span></span>
<span data-ttu-id="214f1-131">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="214f1-131">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="214f1-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="214f1-132">Valid values are:</span></span>

- <span data-ttu-id="214f1-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="214f1-133">PowerShell</span></span>
- <span data-ttu-id="214f1-134">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="214f1-134">GraphicalPowerShell</span></span>
- <span data-ttu-id="214f1-135">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="214f1-135">PowerShellWorkflow</span></span>
- <span data-ttu-id="214f1-136">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="214f1-136">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="214f1-137">Diagramm</span><span class="sxs-lookup"><span data-stu-id="214f1-137">Graph</span></span>

<span data-ttu-id="214f1-138">Der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="214f1-138">The value Graph is obsolete.</span></span>
<span data-ttu-id="214f1-139">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="214f1-139">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214f1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214f1-140">CommonParameters</span></span>
<span data-ttu-id="214f1-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214f1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214f1-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214f1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214f1-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="214f1-143">INPUTS</span></span>

### <span data-ttu-id="214f1-144">Keine</span><span class="sxs-lookup"><span data-stu-id="214f1-144">None</span></span>
<span data-ttu-id="214f1-145">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="214f1-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="214f1-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="214f1-146">OUTPUTS</span></span>

### <span data-ttu-id="214f1-147">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="214f1-147">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="214f1-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="214f1-148">NOTES</span></span>

## <span data-ttu-id="214f1-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="214f1-149">RELATED LINKS</span></span>

[<span data-ttu-id="214f1-150">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-150">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="214f1-151">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-151">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="214f1-152">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-152">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="214f1-153">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-153">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="214f1-154">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-154">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="214f1-155">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-155">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="214f1-156">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="214f1-156">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

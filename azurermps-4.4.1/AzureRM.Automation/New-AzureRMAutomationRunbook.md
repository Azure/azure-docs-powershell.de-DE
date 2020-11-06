---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 664bfb83be4394c5aa50213177eda9f16f5ec6b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497961"
---
# <span data-ttu-id="24acf-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="24acf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24acf-102">SYNOPSIS</span></span>
<span data-ttu-id="24acf-103">Erstellt ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="24acf-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24acf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24acf-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24acf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24acf-105">DESCRIPTION</span></span>
<span data-ttu-id="24acf-106">Das Cmdlet **New-AzureRmAutomationRunbook** erstellt mithilfe von APS eine leere Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="24acf-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="24acf-107">Geben Sie einen Namen für die runbooks an.</span><span class="sxs-lookup"><span data-stu-id="24acf-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="24acf-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24acf-108">EXAMPLES</span></span>

### <span data-ttu-id="24acf-109">Beispiel 1: Erstellen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="24acf-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="24acf-110">Dieser Befehl erstellt eine runbooks mit dem Namen Runbook02 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="24acf-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="24acf-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="24acf-111">PARAMETERS</span></span>

### <span data-ttu-id="24acf-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24acf-112">-AutomationAccountName</span></span>
<span data-ttu-id="24acf-113">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="24acf-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="24acf-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24acf-114">-Description</span></span>
<span data-ttu-id="24acf-115">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="24acf-115">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="24acf-116">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="24acf-116">-LogProgress</span></span>
<span data-ttu-id="24acf-117">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="24acf-117">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="24acf-118">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="24acf-118">-LogVerbose</span></span>
<span data-ttu-id="24acf-119">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="24acf-119">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="24acf-120">-Name</span><span class="sxs-lookup"><span data-stu-id="24acf-120">-Name</span></span>
<span data-ttu-id="24acf-121">Gibt einen Namen für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="24acf-121">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="24acf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24acf-122">-ResourceGroupName</span></span>
<span data-ttu-id="24acf-123">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="24acf-123">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="24acf-124">-Tags</span><span class="sxs-lookup"><span data-stu-id="24acf-124">-Tags</span></span>
<span data-ttu-id="24acf-125">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="24acf-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24acf-126">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="24acf-126">For example:</span></span>

<span data-ttu-id="24acf-127">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="24acf-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="24acf-128">-Typ</span><span class="sxs-lookup"><span data-stu-id="24acf-128">-Type</span></span>
<span data-ttu-id="24acf-129">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="24acf-129">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="24acf-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="24acf-130">Valid values are:</span></span>

- <span data-ttu-id="24acf-131">PowerShell</span><span class="sxs-lookup"><span data-stu-id="24acf-131">PowerShell</span></span>
- <span data-ttu-id="24acf-132">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="24acf-132">GraphicalPowerShell</span></span>
- <span data-ttu-id="24acf-133">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="24acf-133">PowerShellWorkflow</span></span>
- <span data-ttu-id="24acf-134">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="24acf-134">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="24acf-135">Diagramm</span><span class="sxs-lookup"><span data-stu-id="24acf-135">Graph</span></span>

<span data-ttu-id="24acf-136">Der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="24acf-136">The value Graph is obsolete.</span></span>
<span data-ttu-id="24acf-137">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="24acf-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24acf-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24acf-138">-DefaultProfile</span></span>
<span data-ttu-id="24acf-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24acf-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24acf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24acf-140">CommonParameters</span></span>
<span data-ttu-id="24acf-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24acf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24acf-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24acf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24acf-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24acf-143">INPUTS</span></span>

## <span data-ttu-id="24acf-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24acf-144">OUTPUTS</span></span>

### <span data-ttu-id="24acf-145">Microsoft. Azure. Commands. Automation. Model. Job</span><span class="sxs-lookup"><span data-stu-id="24acf-145">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="24acf-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="24acf-146">NOTES</span></span>

## <span data-ttu-id="24acf-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24acf-147">RELATED LINKS</span></span>

[<span data-ttu-id="24acf-148">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-148">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="24acf-149">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-149">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="24acf-150">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-150">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="24acf-151">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="24acf-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="24acf-153">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="24acf-154">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="24acf-154">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

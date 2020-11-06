---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6E35D4D-B2C1-4527-94A6-E7E3488F510B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationRunbook.md
ms.openlocfilehash: 73945c02c5c5802e169e0868908874374080b344
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498505"
---
# <span data-ttu-id="38f09-101">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-101">New-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="38f09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="38f09-102">SYNOPSIS</span></span>
<span data-ttu-id="38f09-103">Erstellt ein Automatisierungs-runbooks.</span><span class="sxs-lookup"><span data-stu-id="38f09-103">Creates an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="38f09-104">SYNTAX</span></span>

```
New-AzureRmAutomationRunbook [-Name] <String> [-Description <String>] [-Tags <IDictionary>] -Type <String>
 [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f09-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38f09-105">DESCRIPTION</span></span>
<span data-ttu-id="38f09-106">Das Cmdlet **New-AzureRmAutomationRunbook** erstellt mithilfe von APS eine leere Azure Automation-runbooks.</span><span class="sxs-lookup"><span data-stu-id="38f09-106">The **New-AzureRmAutomationRunbook** cmdlet creates an empty Azure Automation runbook by using APS.</span></span>
<span data-ttu-id="38f09-107">Geben Sie einen Namen für die runbooks an.</span><span class="sxs-lookup"><span data-stu-id="38f09-107">Specify a name for the runbook.</span></span>

## <span data-ttu-id="38f09-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="38f09-108">EXAMPLES</span></span>

### <span data-ttu-id="38f09-109">Beispiel 1: Erstellen einer runbooks</span><span class="sxs-lookup"><span data-stu-id="38f09-109">Example 1: Create a runbook</span></span>
```
PS C:\>New-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="38f09-110">Dieser Befehl erstellt eine runbooks mit dem Namen Runbook02 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="38f09-110">This command creates a runbook named Runbook02 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="38f09-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="38f09-111">PARAMETERS</span></span>

### <span data-ttu-id="38f09-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38f09-112">-AutomationAccountName</span></span>
<span data-ttu-id="38f09-113">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="38f09-113">Specifies the name of the Automation account in which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="38f09-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f09-114">-DefaultProfile</span></span>
<span data-ttu-id="38f09-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="38f09-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38f09-116">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38f09-116">-Description</span></span>
<span data-ttu-id="38f09-117">Gibt eine Beschreibung für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="38f09-117">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="38f09-118">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="38f09-118">-LogProgress</span></span>
<span data-ttu-id="38f09-119">Gibt an, ob der runbooks-Protokollstatus protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="38f09-119">Specifies whether the runbook logs progress.</span></span>

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

### <span data-ttu-id="38f09-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="38f09-120">-LogVerbose</span></span>
<span data-ttu-id="38f09-121">Gibt an, ob die Protokollierung detaillierte Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="38f09-121">Specifies whether logging includes detailed information.</span></span>

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

### <span data-ttu-id="38f09-122">-Name</span><span class="sxs-lookup"><span data-stu-id="38f09-122">-Name</span></span>
<span data-ttu-id="38f09-123">Gibt einen Namen für den runbooks an.</span><span class="sxs-lookup"><span data-stu-id="38f09-123">Specifies a name for the runbook.</span></span>

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

### <span data-ttu-id="38f09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f09-124">-ResourceGroupName</span></span>
<span data-ttu-id="38f09-125">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks erstellt.</span><span class="sxs-lookup"><span data-stu-id="38f09-125">Specifies the name of the resource group for which this cmdlet creates a runbook.</span></span>

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

### <span data-ttu-id="38f09-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="38f09-126">-Tags</span></span>
<span data-ttu-id="38f09-127">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="38f09-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="38f09-128">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="38f09-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="38f09-129">-Typ</span><span class="sxs-lookup"><span data-stu-id="38f09-129">-Type</span></span>
<span data-ttu-id="38f09-130">Gibt den Typ der runbooks an, die von diesem Cmdlet erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="38f09-130">Specifies the type of runbook that this cmdlet creates.</span></span>
<span data-ttu-id="38f09-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="38f09-131">Valid values are:</span></span>
- <span data-ttu-id="38f09-132">PowerShell</span><span class="sxs-lookup"><span data-stu-id="38f09-132">PowerShell</span></span>
- <span data-ttu-id="38f09-133">GraphicalPowerShell</span><span class="sxs-lookup"><span data-stu-id="38f09-133">GraphicalPowerShell</span></span>
- <span data-ttu-id="38f09-134">PowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="38f09-134">PowerShellWorkflow</span></span>
- <span data-ttu-id="38f09-135">GraphicalPowerShellWorkflow</span><span class="sxs-lookup"><span data-stu-id="38f09-135">GraphicalPowerShellWorkflow</span></span>
- <span data-ttu-id="38f09-136">Diagramm der Wert Graph ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="38f09-136">Graph The value Graph is obsolete.</span></span>
<span data-ttu-id="38f09-137">Sie entspricht GraphicalPowerShellWorkflow.</span><span class="sxs-lookup"><span data-stu-id="38f09-137">It is equivalent to GraphicalPowerShellWorkflow.</span></span>

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

### <span data-ttu-id="38f09-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f09-138">CommonParameters</span></span>
<span data-ttu-id="38f09-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f09-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f09-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f09-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f09-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="38f09-141">INPUTS</span></span>

### <span data-ttu-id="38f09-142">System. String</span><span class="sxs-lookup"><span data-stu-id="38f09-142">System.String</span></span>

### <span data-ttu-id="38f09-143">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="38f09-143">System.Collections.IDictionary</span></span>

### <span data-ttu-id="38f09-144">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="38f09-144">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="38f09-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="38f09-145">OUTPUTS</span></span>

### <span data-ttu-id="38f09-146">Microsoft. Azure. Commands. Automation. Model. runbooks</span><span class="sxs-lookup"><span data-stu-id="38f09-146">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="38f09-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="38f09-147">NOTES</span></span>

## <span data-ttu-id="38f09-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="38f09-148">RELATED LINKS</span></span>

[<span data-ttu-id="38f09-149">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-149">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38f09-150">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-150">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38f09-151">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-151">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38f09-152">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-152">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38f09-153">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-153">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38f09-154">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-154">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="38f09-155">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="38f09-155">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)

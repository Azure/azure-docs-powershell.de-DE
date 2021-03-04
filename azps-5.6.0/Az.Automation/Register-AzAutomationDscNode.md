---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947616"
---
# <span data-ttu-id="cc31c-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc31c-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="cc31c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc31c-102">SYNOPSIS</span></span>
<span data-ttu-id="cc31c-103">Registriert einen virtuellen Azure-Computer mit Windows OS als DSC-Knoten für ein Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="cc31c-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="cc31c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc31c-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc31c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc31c-105">DESCRIPTION</span></span>
<span data-ttu-id="cc31c-106">Das **Cmdlet Register-AzAutomationDscNode** registriert einen virtuellen Azure-Computer als APS Desired State Configuration (DSC)-Knoten in einem Azure Automation-Konto.</span><span class="sxs-lookup"><span data-stu-id="cc31c-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="cc31c-107">Dieses Cmdlet registriert nur VMs mit Windows OS als Automatisierungs-DSC-Knoten für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="cc31c-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="cc31c-108">Wenn Sie einen Knoten bei einem Automatisierungskonto in einem anderen Abonnement registrieren müssen, müssen Sie anstelle von Cmdlets eine ARM verwenden.</span><span class="sxs-lookup"><span data-stu-id="cc31c-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="cc31c-109">Weitere Details finden Sie in [der](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) Dokumentation zur Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="cc31c-109">See the Azure Automation [documentation](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="cc31c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc31c-110">EXAMPLES</span></span>

### <span data-ttu-id="cc31c-111">Beispiel 1: Registrieren eines virtuellen Azure-Computers als Azure DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="cc31c-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="cc31c-112">Mit diesem Befehl wird der virtuelle Azure-Computer mit dem Namen VirtualMachine01 als DSC-Knoten im Automatisierungskonto namens Contoso17 registriert.</span><span class="sxs-lookup"><span data-stu-id="cc31c-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="cc31c-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="cc31c-113">PARAMETERS</span></span>

### <span data-ttu-id="cc31c-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="cc31c-114">-ActionAfterReboot</span></span>
<span data-ttu-id="cc31c-115">Gibt die Aktion an, die der virtuelle Computer nach dem Neustart ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="cc31c-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="cc31c-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cc31c-116">Valid values are:</span></span> 
- <span data-ttu-id="cc31c-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc31c-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="cc31c-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc31c-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="cc31c-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="cc31c-120">Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation DSC-Pullserver herunterlädet, die vorhandenen Module ersetzen, die sich bereits auf dem Zielknoten befinden.</span><span class="sxs-lookup"><span data-stu-id="cc31c-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cc31c-121">-AutomationAccountName</span></span>
<span data-ttu-id="cc31c-122">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="cc31c-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="cc31c-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="cc31c-123">-AzureVMLocation</span></span>
<span data-ttu-id="cc31c-124">Der Azure VM-Speicherort.</span><span class="sxs-lookup"><span data-stu-id="cc31c-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="cc31c-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="cc31c-125">-AzureVMName</span></span>
<span data-ttu-id="cc31c-126">Der Name des virtuellen Azure-Computers, der für die Verwaltung bei Azure Automation DSC registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc31c-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cc31c-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="cc31c-128">Der Name der Azure VM-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc31c-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="cc31c-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="cc31c-129">-ConfigurationMode</span></span>
<span data-ttu-id="cc31c-130">Gibt den DSC-Konfigurationsmodus an.</span><span class="sxs-lookup"><span data-stu-id="cc31c-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="cc31c-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="cc31c-131">Valid values are:</span></span> 
- <span data-ttu-id="cc31c-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="cc31c-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="cc31c-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="cc31c-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="cc31c-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="cc31c-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="cc31c-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="cc31c-136">Gibt die Häufigkeit in Minuten an, mit der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration auf dem Zielknoten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="cc31c-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc31c-137">-DefaultProfile</span></span>
<span data-ttu-id="cc31c-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cc31c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc31c-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="cc31c-139">-NodeConfigurationName</span></span>
<span data-ttu-id="cc31c-140">Gibt den Namen der Knotenkonfiguration an, die von diesem Cmdlet so konfiguriert wird, dass der virtuelle Computer von Azure Automation DSC abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cc31c-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="cc31c-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="cc31c-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="cc31c-142">Gibt an, ob der virtuelle Computer bei Bedarf neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc31c-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="cc31c-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="cc31c-144">Gibt die Häufigkeit in Minuten an, mit der sich der lokale Configuration Manager an den Azure Automation DSC-Pullserver wendet, um die neueste Knotenkonfiguration herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="cc31c-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc31c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc31c-145">-ResourceGroupName</span></span>
<span data-ttu-id="cc31c-146">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="cc31c-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cc31c-147">Das Automatisierungskonto, mit dem dieses Cmdlet einen virtuellen Computer registriert, gehört zu der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cc31c-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc31c-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc31c-148">CommonParameters</span></span>
<span data-ttu-id="cc31c-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc31c-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc31c-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc31c-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc31c-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc31c-151">INPUTS</span></span>

### <span data-ttu-id="cc31c-152">System.String</span><span class="sxs-lookup"><span data-stu-id="cc31c-152">System.String</span></span>

### <span data-ttu-id="cc31c-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="cc31c-153">System.Int32</span></span>

### <span data-ttu-id="cc31c-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc31c-154">System.Boolean</span></span>

## <span data-ttu-id="cc31c-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc31c-155">OUTPUTS</span></span>

### <span data-ttu-id="cc31c-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="cc31c-156">System.Void</span></span>

## <span data-ttu-id="cc31c-157">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="cc31c-157">NOTES</span></span>

## <span data-ttu-id="cc31c-158">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="cc31c-158">RELATED LINKS</span></span>

[<span data-ttu-id="cc31c-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc31c-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="cc31c-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc31c-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="cc31c-161">Aufheben der Registrierung-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="cc31c-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



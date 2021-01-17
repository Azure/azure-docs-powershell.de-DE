---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471294"
---
# <span data-ttu-id="ddfbc-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ddfbc-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="ddfbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddfbc-102">SYNOPSIS</span></span>
<span data-ttu-id="ddfbc-103">Registriert einen virtuellen Azure-Computer, auf dem das Windows-Betriebssystem ausgeführt wird, als DSC-Knoten für ein Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="ddfbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddfbc-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddfbc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddfbc-105">DESCRIPTION</span></span>
<span data-ttu-id="ddfbc-106">Das **Cmdlet "Register-AzAutomationDscNode"** registriert einen virtuellen Azure-Computer als APS Desired State Configuration (DSC)-Knoten in einem Azure-Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="ddfbc-107">Mit diesem Cmdlet werden nur VMs, auf deren Betriebssystem Windows ausgeführt wird, als Automatisierungs-DSC-Knoten für ein Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="ddfbc-108">Wenn Sie einen Knoten für ein Automatisierungskonto in einem anderen Abonnement registrieren müssen, müssen Sie eine ARM anstelle von Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="ddfbc-109">Weitere Details finden Sie in [der Dokumentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) zur Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="ddfbc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ddfbc-110">EXAMPLES</span></span>

### <span data-ttu-id="ddfbc-111">Beispiel 1: Registrieren eines virtuellen Azure-Computers als Azure -DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="ddfbc-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="ddfbc-112">Dieser Befehl registriert den virtuellen Azure-Computer "VirtualMachine01" als DSC-Knoten im Automatisierungskonto namens "Contoso17".</span><span class="sxs-lookup"><span data-stu-id="ddfbc-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="ddfbc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddfbc-113">PARAMETERS</span></span>

### <span data-ttu-id="ddfbc-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="ddfbc-114">-ActionAfterReboot</span></span>
<span data-ttu-id="ddfbc-115">Gibt die Aktion an, die der virtuelle Computer nach dem Neustart ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="ddfbc-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-116">Valid values are:</span></span> 
- <span data-ttu-id="ddfbc-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddfbc-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="ddfbc-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="ddfbc-118">StopConfiguration</span></span>

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

### <span data-ttu-id="ddfbc-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="ddfbc-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="ddfbc-120">Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation -DSC-Pullserver herunterlädt, die vorhandenen Module ersetzen, die sich bereits auf dem Zielknoten befinden.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="ddfbc-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ddfbc-121">-AutomationAccountName</span></span>
<span data-ttu-id="ddfbc-122">Gibt den Namen eines Automatisierungskontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="ddfbc-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="ddfbc-123">-AzureVMLocation</span></span>
<span data-ttu-id="ddfbc-124">Der Azure VM-Standort.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="ddfbc-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="ddfbc-125">-AzureVMName</span></span>
<span data-ttu-id="ddfbc-126">Der Name des virtuellen Azure-Computers, der für die Verwaltung bei Azure Automation DSC registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="ddfbc-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddfbc-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="ddfbc-128">Der Name der Azure VM-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="ddfbc-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="ddfbc-129">-ConfigurationMode</span></span>
<span data-ttu-id="ddfbc-130">Gibt den DSC-Konfigurationsmodus an.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="ddfbc-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ddfbc-131">Valid values are:</span></span> 
- <span data-ttu-id="ddfbc-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="ddfbc-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="ddfbc-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="ddfbc-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="ddfbc-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="ddfbc-134">ApplyOnly</span></span>

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

### <span data-ttu-id="ddfbc-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="ddfbc-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="ddfbc-136">Gibt die Häufigkeit in Minuten an, mit der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration für den Zielknoten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="ddfbc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddfbc-137">-DefaultProfile</span></span>
<span data-ttu-id="ddfbc-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ddfbc-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddfbc-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ddfbc-139">-NodeConfigurationName</span></span>
<span data-ttu-id="ddfbc-140">Gibt den Namen der Knotenkonfiguration an, die dieses Cmdlet für die Pull des virtuellen Computers aus Azure Automation DSC konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="ddfbc-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="ddfbc-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="ddfbc-142">Gibt an, ob der virtuelle Computer bei Bedarf neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="ddfbc-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="ddfbc-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="ddfbc-144">Gibt die Häufigkeit in Minuten an, mit der der lokale Configuration Manager kontaktiert den Azure Automation -DSC-Pullserver, um die neueste Knotenkonfiguration herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="ddfbc-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddfbc-145">-ResourceGroupName</span></span>
<span data-ttu-id="ddfbc-146">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="ddfbc-147">Das Automatisierungskonto, für das dieses Cmdlet einen virtuellen Computer registriert, gehört zu der Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ddfbc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddfbc-148">CommonParameters</span></span>
<span data-ttu-id="ddfbc-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddfbc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddfbc-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddfbc-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddfbc-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ddfbc-151">INPUTS</span></span>

### <span data-ttu-id="ddfbc-152">System.String</span><span class="sxs-lookup"><span data-stu-id="ddfbc-152">System.String</span></span>

### <span data-ttu-id="ddfbc-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ddfbc-153">System.Int32</span></span>

### <span data-ttu-id="ddfbc-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ddfbc-154">System.Boolean</span></span>

## <span data-ttu-id="ddfbc-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ddfbc-155">OUTPUTS</span></span>

### <span data-ttu-id="ddfbc-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="ddfbc-156">System.Void</span></span>

## <span data-ttu-id="ddfbc-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ddfbc-157">NOTES</span></span>

## <span data-ttu-id="ddfbc-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ddfbc-158">RELATED LINKS</span></span>

[<span data-ttu-id="ddfbc-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ddfbc-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="ddfbc-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ddfbc-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="ddfbc-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="ddfbc-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



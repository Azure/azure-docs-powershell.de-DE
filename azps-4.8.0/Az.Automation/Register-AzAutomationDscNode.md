---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: e8367d4e291f3cd08cdb1020375cce1741a679c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009422"
---
# <span data-ttu-id="da2fd-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="da2fd-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="da2fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da2fd-102">SYNOPSIS</span></span>
<span data-ttu-id="da2fd-103">Registriert einen virtuellen Azure-Computer, auf dem Windows OS ausgeführt wird, als DSC-Knoten für ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="da2fd-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="da2fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da2fd-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da2fd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da2fd-105">DESCRIPTION</span></span>
<span data-ttu-id="da2fd-106">Mit dem Cmdlet " **Register-AzAutomationDscNode** " wird ein Azure Virtual Machine als APS-Knoten (Desired State Configuration, DSC) in einem Azure Automation-Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="da2fd-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="da2fd-107">Dieses Cmdlet registriert nur VMS, auf denen Windows OS ausgeführt wird, als Automatisierungs-DSC-Knoten für ein Konto.</span><span class="sxs-lookup"><span data-stu-id="da2fd-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="da2fd-108">Wenn Sie einen Knoten für ein Automatisierungs Konto in einem anderen Abonnement registrieren müssen, müssen Sie anstelle von Cmdlets eine Arm-Vorlage verwenden.</span><span class="sxs-lookup"><span data-stu-id="da2fd-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="da2fd-109">Weitere Informationen finden Sie in der [Dokumentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) zur Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="da2fd-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="da2fd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da2fd-110">EXAMPLES</span></span>

### <span data-ttu-id="da2fd-111">Beispiel 1: Registrieren eines Azure Virtual Machine als Azure DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="da2fd-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="da2fd-112">Dieser Befehl registriert den Azure Virtual Machine mit dem Namen VirtualMachine01 als DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="da2fd-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="da2fd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="da2fd-113">PARAMETERS</span></span>

### <span data-ttu-id="da2fd-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="da2fd-114">-ActionAfterReboot</span></span>
<span data-ttu-id="da2fd-115">Gibt die Aktion an, die der virtuelle Computer ausführt, nachdem er neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="da2fd-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="da2fd-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="da2fd-116">Valid values are:</span></span> 
- <span data-ttu-id="da2fd-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="da2fd-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="da2fd-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="da2fd-118">StopConfiguration</span></span>

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

### <span data-ttu-id="da2fd-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="da2fd-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="da2fd-120">Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation DSC-Pull-Server herunterlädt, die vorhandenen Module ersetzen, die bereits auf dem Zielknoten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="da2fd-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="da2fd-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da2fd-121">-AutomationAccountName</span></span>
<span data-ttu-id="da2fd-122">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="da2fd-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="da2fd-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="da2fd-123">-AzureVMLocation</span></span>
<span data-ttu-id="da2fd-124">Die Azure VM-Position.</span><span class="sxs-lookup"><span data-stu-id="da2fd-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="da2fd-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="da2fd-125">-AzureVMName</span></span>
<span data-ttu-id="da2fd-126">Der Name des virtuellen Azure-Computers, der für die Verwaltung mit Azure Automation DSC registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="da2fd-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="da2fd-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="da2fd-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="da2fd-128">Der Name der Azure VM-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="da2fd-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="da2fd-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="da2fd-129">-ConfigurationMode</span></span>
<span data-ttu-id="da2fd-130">Gibt den DSC-Konfigurationsmodus an.</span><span class="sxs-lookup"><span data-stu-id="da2fd-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="da2fd-131">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="da2fd-131">Valid values are:</span></span> 
- <span data-ttu-id="da2fd-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="da2fd-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="da2fd-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="da2fd-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="da2fd-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="da2fd-134">ApplyOnly</span></span>

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

### <span data-ttu-id="da2fd-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="da2fd-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="da2fd-136">Gibt die Häufigkeit in Minuten an, bei der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration auf dem Zielknoten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="da2fd-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="da2fd-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da2fd-137">-DefaultProfile</span></span>
<span data-ttu-id="da2fd-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="da2fd-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da2fd-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="da2fd-139">-NodeConfigurationName</span></span>
<span data-ttu-id="da2fd-140">Gibt den Namen der Knoten Konfiguration an, die von diesem Cmdlet für den virtuellen Computer konfiguriert wird, um von Azure Automation DSC zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="da2fd-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="da2fd-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="da2fd-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="da2fd-142">Gibt an, ob der virtuelle Computer bei Bedarf neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da2fd-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="da2fd-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="da2fd-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="da2fd-144">Gibt die Häufigkeit in Minuten an, mit der der lokale Konfigurations-Manager den Azure Automation DSC-Pull-Server kontaktiert, um die neueste Knoten Konfiguration herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="da2fd-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="da2fd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da2fd-145">-ResourceGroupName</span></span>
<span data-ttu-id="da2fd-146">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="da2fd-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="da2fd-147">Das Automatisierungs Konto, mit dem dieses Cmdlet einen virtuellen Computer registriert, gehört zur Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="da2fd-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="da2fd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da2fd-148">CommonParameters</span></span>
<span data-ttu-id="da2fd-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da2fd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da2fd-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da2fd-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da2fd-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da2fd-151">INPUTS</span></span>

### <span data-ttu-id="da2fd-152">System. String</span><span class="sxs-lookup"><span data-stu-id="da2fd-152">System.String</span></span>

### <span data-ttu-id="da2fd-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="da2fd-153">System.Int32</span></span>

### <span data-ttu-id="da2fd-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da2fd-154">System.Boolean</span></span>

## <span data-ttu-id="da2fd-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da2fd-155">OUTPUTS</span></span>

### <span data-ttu-id="da2fd-156">System. void</span><span class="sxs-lookup"><span data-stu-id="da2fd-156">System.Void</span></span>

## <span data-ttu-id="da2fd-157">Notizen</span><span class="sxs-lookup"><span data-stu-id="da2fd-157">NOTES</span></span>

## <span data-ttu-id="da2fd-158">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da2fd-158">RELATED LINKS</span></span>

[<span data-ttu-id="da2fd-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="da2fd-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="da2fd-160">Satz-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="da2fd-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="da2fd-161">Registrierung aufheben-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="da2fd-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



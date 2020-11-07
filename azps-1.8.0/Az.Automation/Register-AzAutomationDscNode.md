---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661754"
---
# <span data-ttu-id="529c6-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="529c6-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="529c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="529c6-102">SYNOPSIS</span></span>
<span data-ttu-id="529c6-103">Registriert einen virtuellen Azure-Computer als DSC-Knoten für ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="529c6-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="529c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="529c6-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="529c6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="529c6-105">DESCRIPTION</span></span>
<span data-ttu-id="529c6-106">Mit dem Cmdlet " **Register-AzAutomationDscNode** " wird ein Azure Virtual Machine als APS-Knoten (Desired State Configuration, DSC) in einem Azure Automation-Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="529c6-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="529c6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="529c6-107">EXAMPLES</span></span>

### <span data-ttu-id="529c6-108">Beispiel 1: Registrieren eines Azure Virtual Machine als Azure DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="529c6-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="529c6-109">Dieser Befehl registriert den Azure Virtual Machine mit dem Namen VirtualMachine01 als DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="529c6-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="529c6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="529c6-110">PARAMETERS</span></span>

### <span data-ttu-id="529c6-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="529c6-111">-ActionAfterReboot</span></span>
<span data-ttu-id="529c6-112">Gibt die Aktion an, die der virtuelle Computer ausführt, nachdem er neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="529c6-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="529c6-113">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="529c6-113">Valid values are:</span></span> 
- <span data-ttu-id="529c6-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="529c6-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="529c6-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="529c6-115">StopConfiguration</span></span>

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

### <span data-ttu-id="529c6-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="529c6-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="529c6-117">Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation DSC-Pull-Server herunterlädt, die vorhandenen Module ersetzen, die bereits auf dem Zielknoten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="529c6-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="529c6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="529c6-118">-AutomationAccountName</span></span>
<span data-ttu-id="529c6-119">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="529c6-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="529c6-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="529c6-120">-AzureVMLocation</span></span>
<span data-ttu-id="529c6-121">Die Azure VM-Position.</span><span class="sxs-lookup"><span data-stu-id="529c6-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="529c6-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="529c6-122">-AzureVMName</span></span>
<span data-ttu-id="529c6-123">Der Name des virtuellen Azure-Computers, der für die Verwaltung mit Azure Automation DSC registriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="529c6-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="529c6-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="529c6-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="529c6-125">Der Name der Azure VM-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="529c6-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="529c6-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="529c6-126">-ConfigurationMode</span></span>
<span data-ttu-id="529c6-127">Gibt den DSC-Konfigurationsmodus an.</span><span class="sxs-lookup"><span data-stu-id="529c6-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="529c6-128">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="529c6-128">Valid values are:</span></span> 
- <span data-ttu-id="529c6-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="529c6-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="529c6-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="529c6-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="529c6-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="529c6-131">ApplyOnly</span></span>

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

### <span data-ttu-id="529c6-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="529c6-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="529c6-133">Gibt die Häufigkeit in Minuten an, bei der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration auf dem Zielknoten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="529c6-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="529c6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529c6-134">-DefaultProfile</span></span>
<span data-ttu-id="529c6-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="529c6-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="529c6-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="529c6-136">-NodeConfigurationName</span></span>
<span data-ttu-id="529c6-137">Gibt den Namen der Knoten Konfiguration an, die von diesem Cmdlet für den virtuellen Computer konfiguriert wird, um von Azure Automation DSC zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="529c6-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="529c6-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="529c6-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="529c6-139">Gibt an, ob der virtuelle Computer bei Bedarf neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="529c6-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="529c6-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="529c6-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="529c6-141">Gibt die Häufigkeit in Minuten an, mit der der lokale Konfigurations-Manager den Azure Automation DSC-Pull-Server kontaktiert, um die neueste Knoten Konfiguration herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="529c6-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="529c6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="529c6-142">-ResourceGroupName</span></span>
<span data-ttu-id="529c6-143">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="529c6-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="529c6-144">Das Automatisierungs Konto, mit dem dieses Cmdlet einen virtuellen Computer registriert, gehört zur Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="529c6-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="529c6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529c6-145">CommonParameters</span></span>
<span data-ttu-id="529c6-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="529c6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529c6-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="529c6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529c6-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="529c6-148">INPUTS</span></span>

### <span data-ttu-id="529c6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="529c6-149">System.String</span></span>

### <span data-ttu-id="529c6-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="529c6-150">System.Int32</span></span>

### <span data-ttu-id="529c6-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="529c6-151">System.Boolean</span></span>

## <span data-ttu-id="529c6-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="529c6-152">OUTPUTS</span></span>

### <span data-ttu-id="529c6-153">System. void</span><span class="sxs-lookup"><span data-stu-id="529c6-153">System.Void</span></span>

## <span data-ttu-id="529c6-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="529c6-154">NOTES</span></span>

## <span data-ttu-id="529c6-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="529c6-155">RELATED LINKS</span></span>

[<span data-ttu-id="529c6-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="529c6-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="529c6-157">Satz-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="529c6-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="529c6-158">Registrierung aufheben-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="529c6-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)



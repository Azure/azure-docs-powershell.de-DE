---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 567ac6012465508fbaf03d603a79d2abb04ed6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498482"
---
# <span data-ttu-id="4381a-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4381a-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="4381a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4381a-102">SYNOPSIS</span></span>
<span data-ttu-id="4381a-103">Registriert einen virtuellen Azure-Computer als DSC-Knoten für ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="4381a-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4381a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4381a-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4381a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4381a-105">DESCRIPTION</span></span>
<span data-ttu-id="4381a-106">Mit dem Cmdlet " **Register-AzureRmAutomationDscNode** " wird ein Azure Virtual Machine als APS-Knoten (Desired State Configuration, DSC) in einem Azure Automation-Konto registriert.</span><span class="sxs-lookup"><span data-stu-id="4381a-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="4381a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4381a-107">EXAMPLES</span></span>

### <span data-ttu-id="4381a-108">Beispiel 1: Registrieren eines Azure Virtual Machine als Azure DSC-Knoten</span><span class="sxs-lookup"><span data-stu-id="4381a-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="4381a-109">Dieser Befehl registriert den Azure Virtual Machine mit dem Namen VirtualMachine01 als DSC-Knoten im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4381a-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4381a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4381a-110">PARAMETERS</span></span>

### <span data-ttu-id="4381a-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="4381a-111">-ActionAfterReboot</span></span>
<span data-ttu-id="4381a-112">Gibt die Aktion an, die der virtuelle Computer ausführt, nachdem er neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="4381a-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="4381a-113">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4381a-113">Valid values are:</span></span> 
- <span data-ttu-id="4381a-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="4381a-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="4381a-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="4381a-115">StopConfiguration</span></span>

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

### <span data-ttu-id="4381a-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="4381a-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="4381a-117">Gibt an, ob neue Konfigurationen, die dieser DSC-Knoten vom Azure Automation DSC-Pull-Server herunterlädt, die vorhandenen Module ersetzen, die bereits auf dem Zielknoten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4381a-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="4381a-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4381a-118">-AutomationAccountName</span></span>
<span data-ttu-id="4381a-119">Gibt den Namen eines Automatisierungs Kontos an, in dem dieses Cmdlet einen virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="4381a-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="4381a-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="4381a-120">-AzureVMLocation</span></span>
<span data-ttu-id="4381a-121">Gibt den Speicherort an, an dem dieses Cmdlet einen virtuellen Computer registriert.</span><span class="sxs-lookup"><span data-stu-id="4381a-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="4381a-122">Verwenden Sie das Get-AzureRMLocation-Cmdlet, um gültige Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4381a-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="4381a-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="4381a-123">-AzureVMName</span></span>
<span data-ttu-id="4381a-124">Gibt den Namen des Azure Virtual Machine an, den dieses Cmdlet für die Verwaltung registriert.</span><span class="sxs-lookup"><span data-stu-id="4381a-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="4381a-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4381a-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="4381a-126">Gibt den Namen der Ressourcengruppe des Azure Virtual Machine an, die dieses Cmdlet registriert.</span><span class="sxs-lookup"><span data-stu-id="4381a-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="4381a-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="4381a-127">-ConfigurationMode</span></span>
<span data-ttu-id="4381a-128">Gibt den DSC-Konfigurationsmodus an.</span><span class="sxs-lookup"><span data-stu-id="4381a-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="4381a-129">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4381a-129">Valid values are:</span></span> 
- <span data-ttu-id="4381a-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="4381a-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="4381a-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="4381a-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="4381a-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="4381a-132">ApplyOnly</span></span>

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

### <span data-ttu-id="4381a-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="4381a-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="4381a-134">Gibt die Häufigkeit in Minuten an, bei der die Hintergrundanwendung von DSC versucht, die aktuelle Konfiguration auf dem Zielknoten zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4381a-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="4381a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4381a-135">-DefaultProfile</span></span>
<span data-ttu-id="4381a-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4381a-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4381a-137">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4381a-137">-NodeConfigurationName</span></span>
<span data-ttu-id="4381a-138">Gibt den Namen der Knoten Konfiguration an, die von diesem Cmdlet für den virtuellen Computer konfiguriert wird, um von Azure Automation DSC zu ziehen.</span><span class="sxs-lookup"><span data-stu-id="4381a-138">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="4381a-139">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="4381a-139">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="4381a-140">Gibt an, ob der virtuelle Computer bei Bedarf neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4381a-140">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="4381a-141">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="4381a-141">-RefreshFrequencyMins</span></span>
<span data-ttu-id="4381a-142">Gibt die Häufigkeit in Minuten an, mit der der lokale Konfigurations-Manager den Azure Automation DSC-Pull-Server kontaktiert, um die neueste Knoten Konfiguration herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="4381a-142">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="4381a-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4381a-143">-ResourceGroupName</span></span>
<span data-ttu-id="4381a-144">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4381a-144">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4381a-145">Das Automatisierungs Konto, mit dem dieses Cmdlet einen virtuellen Computer registriert, gehört zur Ressourcengruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="4381a-145">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4381a-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4381a-146">CommonParameters</span></span>
<span data-ttu-id="4381a-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4381a-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4381a-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4381a-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4381a-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4381a-149">INPUTS</span></span>

### <span data-ttu-id="4381a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4381a-150">System.String</span></span>

### <span data-ttu-id="4381a-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4381a-151">System.Int32</span></span>

### <span data-ttu-id="4381a-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4381a-152">System.Boolean</span></span>

## <span data-ttu-id="4381a-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4381a-153">OUTPUTS</span></span>

### <span data-ttu-id="4381a-154">System. void</span><span class="sxs-lookup"><span data-stu-id="4381a-154">System.Void</span></span>

## <span data-ttu-id="4381a-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="4381a-155">NOTES</span></span>

## <span data-ttu-id="4381a-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4381a-156">RELATED LINKS</span></span>

[<span data-ttu-id="4381a-157">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4381a-157">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="4381a-158">Satz-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4381a-158">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="4381a-159">Registrierung aufheben-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4381a-159">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)



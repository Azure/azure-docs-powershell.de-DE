---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "94007557"
---
# <span data-ttu-id="6a41b-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a41b-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="6a41b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a41b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a41b-103">Konfiguriert die DSC-Erweiterung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="6a41b-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="6a41b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a41b-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a41b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a41b-105">DESCRIPTION</span></span>
<span data-ttu-id="6a41b-106">Das Cmdlet " **festlegen-AzureVMDscExtension** " konfiguriert die Erweiterung der gewünschten Zustands Konfiguration (DSC) auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="6a41b-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="6a41b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a41b-107">EXAMPLES</span></span>

### <span data-ttu-id="6a41b-108">Beispiel 1: Konfigurieren der DSC-Erweiterung auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6a41b-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="6a41b-109">Mit diesem Befehl wird die DSC-Erweiterung auf einem virtuellen Computer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="6a41b-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="6a41b-110">Das MyConfiguration.ps1.zip-Paket muss zuvor mit dem Befehl **Publish-AzureVMDscConfiguration** in den Azure-Speicher hochgeladen worden sein und enthält das MyConfiguration.ps1-Skript und die Module, von denen es abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="6a41b-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="6a41b-111">Das myconfiguration-Argument gibt die spezifische DSC-Konfiguration innerhalb des Skripts an, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a41b-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="6a41b-112">Der Parameter- *ConfigurationArgument* gibt eine Hashtable mit den Argumenten an, die an die Konfigurationsfunktion übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="6a41b-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="6a41b-113">Beispiel 2: Konfigurieren der DSC-Erweiterung auf einem virtuellen Computer mithilfe eines Pfads zu den Konfigurationsdaten</span><span class="sxs-lookup"><span data-stu-id="6a41b-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="6a41b-114">Dieser Befehl konfiguriert die DSC-Erweiterung auf einem virtuellen Computer mithilfe eines Pfads zu den Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="6a41b-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="6a41b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a41b-115">PARAMETERS</span></span>

### <span data-ttu-id="6a41b-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="6a41b-116">-ConfigurationArchive</span></span>
<span data-ttu-id="6a41b-117">Gibt den Namen des Konfigurationspakets (ZIP-Datei) an, das zuvor von Publish-AzureVMDscConfiguration hochgeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="6a41b-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="6a41b-118">Dieser Parameter muss nur den Namen der Datei ohne Pfad angeben.</span><span class="sxs-lookup"><span data-stu-id="6a41b-118">This parameter must specify only the name of the file, without any path.</span></span>

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

### <span data-ttu-id="6a41b-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="6a41b-119">-ConfigurationArgument</span></span>
<span data-ttu-id="6a41b-120">Gibt eine Hashtable an, die die Argumente für die Konfigurationsfunktion angibt.</span><span class="sxs-lookup"><span data-stu-id="6a41b-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="6a41b-121">Die Schlüssel entsprechen den Parameternamen und den Werten für die Parameterwerte.</span><span class="sxs-lookup"><span data-stu-id="6a41b-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="6a41b-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6a41b-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a41b-123">Primitive Typen</span><span class="sxs-lookup"><span data-stu-id="6a41b-123">primitive types</span></span>
- <span data-ttu-id="6a41b-124">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6a41b-124">string</span></span>
- <span data-ttu-id="6a41b-125">Matrix</span><span class="sxs-lookup"><span data-stu-id="6a41b-125">array</span></span>
- <span data-ttu-id="6a41b-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="6a41b-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="6a41b-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="6a41b-128">Gibt den Pfad einer psd1-Datei an, die die Daten für die Konfigurationsfunktion angibt.</span><span class="sxs-lookup"><span data-stu-id="6a41b-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="6a41b-129">Diese Datei muss eine Hashtable enthalten, wie unter Trennen von Konfigurations-und Umgebungsdaten beschrieben https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="6a41b-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

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

### <span data-ttu-id="6a41b-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6a41b-130">-ConfigurationName</span></span>
<span data-ttu-id="6a41b-131">Gibt den Namen des Konfigurationsskripts oder Moduls an, das von der DSC-Erweiterung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6a41b-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="6a41b-132">Der Wert dieses Parameters muss der Name einer der Konfigurationsfunktionen sein, die in den Skripts oder Modulen enthalten sind, die in *ConfigurationArchive* verpackt sind.</span><span class="sxs-lookup"><span data-stu-id="6a41b-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="6a41b-133">Dieses Cmdlet ist standardmäßig mit dem Namen der Datei versehen, die vom *ConfigurationArchive* -Parameter angegeben wird, wenn Sie diesen Parameter ohne Erweiterung auslassen.</span><span class="sxs-lookup"><span data-stu-id="6a41b-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="6a41b-134">Wenn *ConfigurationArchive* beispielsweise "SalesWebSite.ps1.zip" ist, lautet der Standardwert für *ConfigurationName* "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="6a41b-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

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

### <span data-ttu-id="6a41b-135">-Containername</span><span class="sxs-lookup"><span data-stu-id="6a41b-135">-ContainerName</span></span>
<span data-ttu-id="6a41b-136">Gibt den Namen des Azure-Speichercontainers an, in dem sich der *ConfigurationArchive* befindet.</span><span class="sxs-lookup"><span data-stu-id="6a41b-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

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

### <span data-ttu-id="6a41b-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="6a41b-137">-DataCollection</span></span>
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

### <span data-ttu-id="6a41b-138">-Force</span><span class="sxs-lookup"><span data-stu-id="6a41b-138">-Force</span></span>
<span data-ttu-id="6a41b-139">Gibt an, dass mit diesem Cmdlet vorhandene BLOBs überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6a41b-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-140">-Information</span><span class="sxs-lookup"><span data-stu-id="6a41b-140">-InformationAction</span></span>
<span data-ttu-id="6a41b-141">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="6a41b-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6a41b-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6a41b-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a41b-143">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="6a41b-143">Continue</span></span>
- <span data-ttu-id="6a41b-144">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="6a41b-144">Ignore</span></span>
- <span data-ttu-id="6a41b-145">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="6a41b-145">Inquire</span></span>
- <span data-ttu-id="6a41b-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6a41b-146">SilentlyContinue</span></span>
- <span data-ttu-id="6a41b-147">Beenden</span><span class="sxs-lookup"><span data-stu-id="6a41b-147">Stop</span></span>
- <span data-ttu-id="6a41b-148">Anhalten</span><span class="sxs-lookup"><span data-stu-id="6a41b-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6a41b-149">-InformationVariable</span></span>
<span data-ttu-id="6a41b-150">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="6a41b-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-151">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a41b-151">-Profile</span></span>
<span data-ttu-id="6a41b-152">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="6a41b-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6a41b-153">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="6a41b-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="6a41b-154">-ReferenceName</span></span>
<span data-ttu-id="6a41b-155">Gibt eine benutzerdefinierte Zeichenfolge an, die verwendet werden kann, um auf eine Erweiterung zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="6a41b-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="6a41b-156">Dieser Parameter wird angegeben, wenn die Erweiterung zum ersten Mal dem virtuellen Computer hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6a41b-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="6a41b-157">Bei nachfolgenden Updates sollten Sie den zuvor verwendeten Verweisnamen angeben, während Sie die Erweiterung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6a41b-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="6a41b-158">Der *Verweisname* , der einer Erweiterung zugewiesen ist, wird mit dem Cmdlet **Get-AzureVM** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a41b-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="6a41b-159">-Storagecontext</span><span class="sxs-lookup"><span data-stu-id="6a41b-159">-StorageContext</span></span>
<span data-ttu-id="6a41b-160">Gibt den Azure-Speicherkontext an, in dem die Sicherheitseinstellungen für den Zugriff auf das Konfigurationsskript bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6a41b-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="6a41b-161">Dieser Kontext bietet Lesezugriff auf den Container, der durch den *Containername* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a41b-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6a41b-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="6a41b-163">Gibt das DNS-Endpunkt Suffix für alle Speicherdienste an, beispielsweise "Core.contoso.net".</span><span class="sxs-lookup"><span data-stu-id="6a41b-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

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

### <span data-ttu-id="6a41b-164">-Version</span><span class="sxs-lookup"><span data-stu-id="6a41b-164">-Version</span></span>
<span data-ttu-id="6a41b-165">Gibt die spezifische Version der zu verwendenden DSC-Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="6a41b-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="6a41b-166">Der Standardwert ist auf "1. \*" festgelegt, wenn dieser Parameter nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="6a41b-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

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

### <span data-ttu-id="6a41b-167">-VM</span><span class="sxs-lookup"><span data-stu-id="6a41b-167">-VM</span></span>
<span data-ttu-id="6a41b-168">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="6a41b-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="6a41b-169">-WmfVersion</span></span>
<span data-ttu-id="6a41b-170">Gibt die Version des Windows Management Framework (WMF) an, die auf dem virtuellen Computer installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a41b-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="6a41b-171">Die DSC-Erweiterung hängt von den DSC-Funktionen ab, die nur in den WMF-Updates zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="6a41b-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="6a41b-172">Dieser Parameter gibt an, welche Version des Updates auf dem virtuellen Computer installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a41b-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="6a41b-173">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6a41b-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6a41b-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="6a41b-174">4.0.</span></span>
<span data-ttu-id="6a41b-175">Installiert WMF 4,0, es sei denn, eine neuere Version ist bereits installiert.</span><span class="sxs-lookup"><span data-stu-id="6a41b-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="6a41b-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="6a41b-176">5.0.</span></span>
<span data-ttu-id="6a41b-177">Installiert die neueste Version von WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="6a41b-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="6a41b-178">neueste.</span><span class="sxs-lookup"><span data-stu-id="6a41b-178">latest.</span></span>
<span data-ttu-id="6a41b-179">Installiert die aktuelle WMF, derzeit WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="6a41b-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="6a41b-180">Der Standardwert ist aktuell.</span><span class="sxs-lookup"><span data-stu-id="6a41b-180">The default value is latest.</span></span>

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

### <span data-ttu-id="6a41b-181">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a41b-181">-Confirm</span></span>
<span data-ttu-id="6a41b-182">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a41b-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a41b-183">-WhatIf</span></span>
<span data-ttu-id="6a41b-184">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a41b-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a41b-185">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a41b-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a41b-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a41b-186">CommonParameters</span></span>
<span data-ttu-id="6a41b-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a41b-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a41b-188">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a41b-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a41b-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a41b-189">INPUTS</span></span>

## <span data-ttu-id="6a41b-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a41b-190">OUTPUTS</span></span>

## <span data-ttu-id="6a41b-191">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a41b-191">NOTES</span></span>

## <span data-ttu-id="6a41b-192">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a41b-192">RELATED LINKS</span></span>

[<span data-ttu-id="6a41b-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a41b-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="6a41b-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a41b-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="6a41b-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6a41b-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="6a41b-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="6a41b-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="6a41b-197">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a41b-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)



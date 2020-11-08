---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008599"
---
# <span data-ttu-id="a1cb0-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="a1cb0-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="a1cb0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="a1cb0-103">Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="a1cb0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1cb0-104">SYNTAX</span></span>

### <span data-ttu-id="a1cb0-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1cb0-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1cb0-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="a1cb0-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1cb0-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="a1cb0-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a1cb0-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="a1cb0-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1cb0-109">Linux</span><span class="sxs-lookup"><span data-stu-id="a1cb0-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1cb0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1cb0-110">DESCRIPTION</span></span>
<span data-ttu-id="a1cb0-111">Das Cmdlet " **Set-AzVMOperatingSystem** " legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="a1cb0-112">Sie können Anmeldeinformationen, Computername und Typ des Betriebssystems angeben.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="a1cb0-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1cb0-113">EXAMPLES</span></span>

### <span data-ttu-id="a1cb0-114">Beispiel 1: Einrichten von Betriebssystemeigenschaften für eine neue virtuelle Maschine</span><span class="sxs-lookup"><span data-stu-id="a1cb0-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="a1cb0-115">Der erste Befehl wandelt ein Kennwort in eine sichere Zeichenfolge um und speichert es dann in der $SecurePassword-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="a1cb0-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="a1cb0-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="a1cb0-117">Mit dem zweiten Befehl werden die Anmeldeinformationen für den Benutzer FullerP und das in $SecurePassword gespeicherte Kennwort erstellt, und die Anmeldeinformationen werden dann in der $Credential Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="a1cb0-118">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="a1cb0-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="a1cb0-119">Der dritte Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailabilitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="a1cb0-120">Der vierte Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a1cb0-121">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="a1cb0-122">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="a1cb0-123">In den nächsten vier Befehlen werden Variablenwerte zugewiesen, die Sie im folgenden Befehl verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="a1cb0-124">Da Sie diese Zeichenfolgen direkt im Befehl " **Satz-AzVMOperatingSystem** " angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="a1cb0-125">Sie können jedoch einen solchen Ansatz in Skripten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="a1cb0-126">Mit dem letzten Befehl werden die Betriebssystemeigenschaften für den virtuellen Computer festgelegt, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="a1cb0-127">Der Befehl verwendet die in $Credential gespeicherten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="a1cb0-128">Der Befehl verwendet für einige Parameter in vorherigen Befehlen zugewiesene Variablen.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="a1cb0-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1cb0-129">PARAMETERS</span></span>

### <span data-ttu-id="a1cb0-130">-Computername</span><span class="sxs-lookup"><span data-stu-id="a1cb0-130">-ComputerName</span></span>
<span data-ttu-id="a1cb0-131">Gibt den Namen des Computers an.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-131">Specifies the name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-132">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a1cb0-132">-Credential</span></span>
<span data-ttu-id="a1cb0-133">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="a1cb0-134">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a1cb0-135">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a1cb0-135">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="a1cb0-136">-CustomData</span></span>
<span data-ttu-id="a1cb0-137">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="a1cb0-138">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="a1cb0-139">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-139">The maximum length of the binary array is 65535 bytes.</span></span><br>
<span data-ttu-id="a1cb0-140">**Hinweis: übergeben Sie keine Geheimnisse oder Kennwörter in der CustomData-Eigenschaft.**</span><span class="sxs-lookup"><span data-stu-id="a1cb0-140">**Note: Do not pass any secrets or passwords in customData property**</span></span><br>
<span data-ttu-id="a1cb0-141">Diese Eigenschaft kann nicht aktualisiert werden, nachdem die VM erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-141">This property cannot be updated after the VM is created.</span></span> <br>
<span data-ttu-id="a1cb0-142">CustomData wird an den virtuellen Computer übergeben, der als Datei gespeichert werden soll, weitere Informationen finden Sie unter [benutzerdefinierte Daten auf Azure VMS](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span><span class="sxs-lookup"><span data-stu-id="a1cb0-142">customData is passed to the VM to be saved as a file, for more information see [Custom Data on Azure VMs](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/)</span></span> <br>
<span data-ttu-id="a1cb0-143">Informationen zum Verwenden von Cloud-init für Ihre Linux-VM finden Sie unter [Verwenden von Cloud-init zum Anpassen einer Linux-VM während der Erstellung](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) .</span><span class="sxs-lookup"><span data-stu-id="a1cb0-143">For using cloud-init for your Linux VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1cb0-144">-DefaultProfile</span></span>
<span data-ttu-id="a1cb0-145">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1cb0-146">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="a1cb0-146">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="a1cb0-147">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-147">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-148">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="a1cb0-148">-DisableVMAgent</span></span>
<span data-ttu-id="a1cb0-149">Bereitstellen des VM-Agents deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-149">Disable Provision VM Agent.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-150">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="a1cb0-150">-EnableAutoUpdate</span></span>
<span data-ttu-id="a1cb0-151">Gibt an, dass dieses Cmdlet die automatische Aktualisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-151">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-152">-Linux</span><span class="sxs-lookup"><span data-stu-id="a1cb0-152">-Linux</span></span>
<span data-ttu-id="a1cb0-153">Gibt an, dass der Typ des Betriebssystems Linux ist.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-153">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-154">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="a1cb0-154">-PatchMode</span></span>
<span data-ttu-id="a1cb0-155">Gibt den Modus des in-Guest-Patches für IaaS Virtual Machine an.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-155">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="a1cb0-156">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="a1cb0-156">Possible values are:</span></span><br>
<span data-ttu-id="a1cb0-157">**Manuell** : Sie steuern die Anwendung von Patches auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-157">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="a1cb0-158">Dazu können Sie Patches manuell innerhalb des VM anwenden.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-158">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="a1cb0-159">In diesem Modus sind automatische Updates deaktiviert; die Eigenschaft WindowsConfiguration. enableAutomaticUpdates muss "falsch" sein.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-159">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="a1cb0-160">**AutomaticByOS** – die virtuelle Maschine wird automatisch vom Betriebssystem aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-160">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="a1cb0-161">Die Eigenschaft WindowsConfiguration. enableAutomaticUpdates muss true sein.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-161">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="a1cb0-162">**AutomaticByPlatform** – die virtuelle Maschine wird automatisch vom Betriebssystem aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-162">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="a1cb0-163">Die Eigenschaften provisionVMAgent und WindowsConfiguration. enableAutomaticUpdates müssen wahr sein.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-163">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-164">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="a1cb0-164">-ProvisionVMAgent</span></span>
<span data-ttu-id="a1cb0-165">Gibt an, dass für die Einstellungen der Virtual Machine-Agent auf dem virtuellen Computer installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-165">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-166">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="a1cb0-166">-TimeZone</span></span>
<span data-ttu-id="a1cb0-167">Gibt die Zeitzone des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-167">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="a1cb0-168">z.b. \" Pacific Normalzeit \" .</span><span class="sxs-lookup"><span data-stu-id="a1cb0-168">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="a1cb0-169">Mögliche Werte können [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) -Wert aus Zeitzonen sein, die von [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-169">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-170">-VM</span><span class="sxs-lookup"><span data-stu-id="a1cb0-170">-VM</span></span>
<span data-ttu-id="a1cb0-171">Gibt das Objekt des lokalen virtuellen Computers an, auf dem Betriebssystemeigenschaften festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-171">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="a1cb0-172">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-172">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="a1cb0-173">Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des New-AzVMConfig-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-173">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-174">-Windows</span><span class="sxs-lookup"><span data-stu-id="a1cb0-174">-Windows</span></span>
<span data-ttu-id="a1cb0-175">Gibt an, dass der Typ des Betriebssystems Windows ist.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-175">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-176">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a1cb0-176">-WinRMCertificateUrl</span></span>
<span data-ttu-id="a1cb0-177">Gibt den URI eines WinRM-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-177">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="a1cb0-178">Dieser muss in einem schlüsseltresor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-178">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-179">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="a1cb0-179">-WinRMHttp</span></span>
<span data-ttu-id="a1cb0-180">Gibt an, dass dieses Betriebssystem http WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-180">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-181">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="a1cb0-181">-WinRMHttps</span></span>
<span data-ttu-id="a1cb0-182">Gibt an, dass dieses Betriebssystem HTTPS WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-182">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1cb0-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1cb0-183">CommonParameters</span></span>
<span data-ttu-id="a1cb0-184">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1cb0-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1cb0-185">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1cb0-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1cb0-186">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1cb0-186">INPUTS</span></span>

### <span data-ttu-id="a1cb0-187">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a1cb0-187">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a1cb0-188">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a1cb0-188">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a1cb0-189">System. String</span><span class="sxs-lookup"><span data-stu-id="a1cb0-189">System.String</span></span>

### <span data-ttu-id="a1cb0-190">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="a1cb0-190">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="a1cb0-191">System. Uri</span><span class="sxs-lookup"><span data-stu-id="a1cb0-191">System.Uri</span></span>

## <span data-ttu-id="a1cb0-192">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1cb0-192">OUTPUTS</span></span>

### <span data-ttu-id="a1cb0-193">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a1cb0-193">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a1cb0-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1cb0-194">NOTES</span></span>

## <span data-ttu-id="a1cb0-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1cb0-195">RELATED LINKS</span></span>

[<span data-ttu-id="a1cb0-196">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a1cb0-196">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a1cb0-197">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a1cb0-197">New-AzVMConfig</span></span>](./New-AzVMConfig.md)



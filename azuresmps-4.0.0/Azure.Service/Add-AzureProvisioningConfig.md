---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006588"
---
# <span data-ttu-id="0f170-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="0f170-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="0f170-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f170-102">SYNOPSIS</span></span>
<span data-ttu-id="0f170-103">Fügt die Bereitstellungskonfiguration für einen virtuellen Azure-Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f170-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="0f170-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f170-104">SYNTAX</span></span>

### <span data-ttu-id="0f170-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f170-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f170-106">Linux</span><span class="sxs-lookup"><span data-stu-id="0f170-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0f170-107">Windows Domain</span><span class="sxs-lookup"><span data-stu-id="0f170-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0f170-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f170-108">DESCRIPTION</span></span>
<span data-ttu-id="0f170-109">Das **Add-AzureProvisioningConfig-** Cmdlet fügt einer Azure Virtual Machine-Konfiguration Bereitstellungs Konfigurationsinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f170-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="0f170-110">Sie können das Configuration-Objekt zum Erstellen eines virtuellen Computers verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f170-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="0f170-111">Dieses Cmdlet unterstützt verschiedene Bereitstellungskonfigurationen, einschließlich eigenständiger Windows-Server, Windows-Server, die einer Active Directory-Domäne beigetreten sind, und Linux-basierten Servern.</span><span class="sxs-lookup"><span data-stu-id="0f170-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="0f170-112">Wenn Sie einen Active Directory-Domänen beigetretenen Server erstellen möchten, geben Sie den vollqualifizierten Domänennamen der Active Directory-Domäne und die Domänenanmeldeinformationen eines Benutzers an, der die Berechtigung hat, dem virtuellen Computer mit der Domäne beizutreten.</span><span class="sxs-lookup"><span data-stu-id="0f170-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="0f170-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f170-113">EXAMPLES</span></span>

### <span data-ttu-id="0f170-114">Beispiel 1: Erstellen eines eigenständigen virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="0f170-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="0f170-115">Mit diesem Befehl wird ein Virtual Machine-Konfigurationsobjekt mithilfe des Cmdlets **New-AzureVMConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="0f170-116">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f170-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0f170-117">Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration für einen virtuellen Computer hinzu, auf dem das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f170-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="0f170-118">Die Konfiguration umfasst den Benutzernamen und das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="0f170-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="0f170-119">Der Befehl übergibt die Konfiguration an das Cmdlet **New-AzureVM** , das den virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="0f170-120">Beispiel 2: Erstellen einer Domäne, die einem virtuellen Computer beigetreten ist</span><span class="sxs-lookup"><span data-stu-id="0f170-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="0f170-121">Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="0f170-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="0f170-122">Das aktuelle Cmdlet fügt eine Bereitstellungskonfiguration für einen virtuellen Computer hinzu, der mit der Contoso-Domäne verbunden werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f170-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="0f170-123">Der Befehl enthält den Benutzernamen und das Kennwort, die erforderlich sind, um den virtuellen Computer zur Domäne hinzufügen zu können.</span><span class="sxs-lookup"><span data-stu-id="0f170-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="0f170-124">Bei der Konfiguration muss der Benutzer das Benutzerkennwort bei der ersten Anmeldung ändern.</span><span class="sxs-lookup"><span data-stu-id="0f170-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="0f170-125">Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f170-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="0f170-126">Beispiel 3: Erstellen eines Linux-basierten virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="0f170-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="0f170-127">Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="0f170-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="0f170-128">Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration für einen virtuellen Computer hinzu, auf dem das Linux-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f170-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="0f170-129">Die Konfiguration umfasst den Stammbenutzer Namen und das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="0f170-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="0f170-130">Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f170-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="0f170-131">Beispiel 4: Erstellen eines virtuellen Computers, der Zertifikate für WinRM enthält</span><span class="sxs-lookup"><span data-stu-id="0f170-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="0f170-132">Der erste Befehl ruft Zertifikate aus einem Zertifikatspeicher ab und speichert Sie dann in der $certs-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="0f170-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="0f170-133">Der zweite Befehl erstellt ein Konfigurationsobjekt für einen virtuellen Computer und übergibt es an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f170-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="0f170-134">Das aktuelle Cmdlet fügt eine Bereitstellungskonfiguration mit Zertifikaten für WinRM hinzu.</span><span class="sxs-lookup"><span data-stu-id="0f170-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="0f170-135">Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f170-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="0f170-136">Beispiel 5: Erstellen eines virtuellen Computers, auf dem WinRM über HTTP aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="0f170-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="0f170-137">Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="0f170-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="0f170-138">Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration hinzu, bei der WinRM über HTTP aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0f170-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="0f170-139">Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f170-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="0f170-140">Beispiel 6: Erstellen eines virtuellen Computers, auf dem WinRM über HTTPS deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="0f170-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="0f170-141">Mit diesem Befehl wird ein Konfigurationsobjekt für einen virtuellen Computer erstellt und an das aktuelle Cmdlet weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="0f170-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="0f170-142">Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration hinzu, die WinRM über HTTPS deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="0f170-143">Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f170-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="0f170-144">Beispiel 7: Erstellen einer virtuellen Maschine ohne Schlüsselexport</span><span class="sxs-lookup"><span data-stu-id="0f170-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="0f170-145">Der erste Befehl ruft Zertifikate aus einem Zertifikatspeicher ab und speichert Sie dann in der $certs-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="0f170-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="0f170-146">Der zweite Befehl erstellt ein Konfigurationsobjekt für einen virtuellen Computer und übergibt es an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f170-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="0f170-147">Das aktuelle Cmdlet fügt die Bereitstellungskonfiguration für einen virtuellen Computer hinzu, der Zertifikate enthält, und exportiert keine privaten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0f170-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="0f170-148">Der Befehl erstellt den virtuellen Computer basierend auf dem Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="0f170-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="0f170-149">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f170-149">PARAMETERS</span></span>

### <span data-ttu-id="0f170-150">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="0f170-150">-AdminUsername</span></span>
<span data-ttu-id="0f170-151">Gibt den Benutzernamen des Administrator Kontos an, das von dieser Konfiguration auf dem virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f170-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-152">-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="0f170-152">-Certificates</span></span>
<span data-ttu-id="0f170-153">Gibt eine Reihe von Zertifikaten an, die von dieser Konfiguration auf dem virtuellen Computer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0f170-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="0f170-154">-CustomDataFile</span></span>
<span data-ttu-id="0f170-155">Gibt eine Datendatei für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="0f170-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="0f170-156">Dieses Cmdlet codiert den Inhalt der Datei als Base64.</span><span class="sxs-lookup"><span data-stu-id="0f170-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="0f170-157">Die Datei muss weniger als 64 KB lang sein.</span><span class="sxs-lookup"><span data-stu-id="0f170-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="0f170-158">Wenn es sich bei dem Gastbetriebssystem um das Windows-Betriebssystem handelt, speichert diese Konfiguration diese Daten als Binärdatei mit dem Namen%SystemDrive%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="0f170-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="0f170-159">Wenn es sich bei dem Gastbetriebssystem um Linux handelt, übergibt diese Konfiguration die Daten mithilfe der ovf-env.xml-Datei.</span><span class="sxs-lookup"><span data-stu-id="0f170-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="0f170-160">Die Konfiguration kopiert diese Datei in das/var/lib/waagent-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="0f170-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="0f170-161">Der Agent speichert auch die Base64-codierten Daten in/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="0f170-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="0f170-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="0f170-163">Gibt an, dass diese Konfiguration automatische Updates deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="0f170-164">-DisableGuestAgent</span></span>
<span data-ttu-id="0f170-165">Gibt an, dass diese Konfiguration den Gast-Agent "Infrastructure as a Service (IaaS)" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="0f170-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="0f170-166">-DisableSSH</span></span>
<span data-ttu-id="0f170-167">Gibt an, dass diese Konfiguration SSH deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="0f170-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="0f170-169">Gibt an, dass diese Konfiguration die Windows-Remote Verwaltung (WinRM) auf HTTPS deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="0f170-170">Standardmäßig ist WinRM über HTTPS aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-171">-Domäne</span><span class="sxs-lookup"><span data-stu-id="0f170-171">-Domain</span></span>
<span data-ttu-id="0f170-172">Gibt den Namen der Domäne des Kontos an, das über die Berechtigung zum Hinzufügen des Computers zu einer Domäne verfügt.</span><span class="sxs-lookup"><span data-stu-id="0f170-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="0f170-173">-DomainPassword</span></span>
<span data-ttu-id="0f170-174">Gibt das Kennwort des Benutzerkontos an, das über die Berechtigung zum Hinzufügen des Computers zu einer Domäne verfügt.</span><span class="sxs-lookup"><span data-stu-id="0f170-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-175">-Domain User Name</span><span class="sxs-lookup"><span data-stu-id="0f170-175">-DomainUserName</span></span>
<span data-ttu-id="0f170-176">Gibt den Namen des Benutzerkontos an, das über die Berechtigung zum Hinzufügen des Computers zu einer Domäne verfügt.</span><span class="sxs-lookup"><span data-stu-id="0f170-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="0f170-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="0f170-178">Gibt an, dass diese Konfiguration WinRM über HTTP aktiviert.</span><span class="sxs-lookup"><span data-stu-id="0f170-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-179">-Information</span><span class="sxs-lookup"><span data-stu-id="0f170-179">-InformationAction</span></span>
<span data-ttu-id="0f170-180">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="0f170-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0f170-181">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0f170-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f170-182">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="0f170-182">Continue</span></span>
- <span data-ttu-id="0f170-183">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0f170-183">Ignore</span></span>
- <span data-ttu-id="0f170-184">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="0f170-184">Inquire</span></span>
- <span data-ttu-id="0f170-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0f170-185">SilentlyContinue</span></span>
- <span data-ttu-id="0f170-186">Beenden</span><span class="sxs-lookup"><span data-stu-id="0f170-186">Stop</span></span>
- <span data-ttu-id="0f170-187">Anhalten</span><span class="sxs-lookup"><span data-stu-id="0f170-187">Suspend</span></span>

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

### <span data-ttu-id="0f170-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0f170-188">-InformationVariable</span></span>
<span data-ttu-id="0f170-189">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="0f170-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0f170-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="0f170-190">-JoinDomain</span></span>
<span data-ttu-id="0f170-191">Gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) der Domäne an, der Sie beitreten möchten.</span><span class="sxs-lookup"><span data-stu-id="0f170-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="0f170-192">-Linux</span></span>
<span data-ttu-id="0f170-193">Gibt an, dass diese Konfiguration eine Linux-Konfiguration erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-193">Indicates that this configuration creates a Linux configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="0f170-194">-LinuxUser</span></span>
<span data-ttu-id="0f170-195">Gibt den Benutzernamen des Linux-Administratorkontos an, das von dieser Konfiguration auf dem virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0f170-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="0f170-196">-MachineObjectOU</span></span>
<span data-ttu-id="0f170-197">Gibt den vollqualifizierten Namen der Organisationseinheit an, in der die Konfiguration das Computerkonto erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="0f170-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="0f170-199">Gibt an, dass diese Konfiguration den privaten Schlüssel nicht hochlädt.</span><span class="sxs-lookup"><span data-stu-id="0f170-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f170-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="0f170-201">Gibt an, dass diese Konfiguration einen virtuellen Computer ohne einen Remote Desktop Endpunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f170-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="0f170-203">Gibt an, dass diese Konfiguration einen virtuellen Computer ohne einen SSH-Endpunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="0f170-204">-NoSSHPassword</span></span>
<span data-ttu-id="0f170-205">Gibt an, dass diese Konfiguration einen virtuellen Computer ohne ein SSH-Kennwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f170-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="0f170-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="0f170-207">Gibt an, dass diese Konfiguration keinen WinRM-Endpunkt für den virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="0f170-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-208">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="0f170-208">-Password</span></span>
<span data-ttu-id="0f170-209">Gibt das Kennwort für das Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="0f170-209">Specifies the password of the administrator account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-210">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f170-210">-Profile</span></span>
<span data-ttu-id="0f170-211">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0f170-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f170-212">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0f170-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f170-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="0f170-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="0f170-214">Gibt an, dass der Benutzer das Kennwort bei der ersten Anmeldung vom virtuellen Computer ändern muss.</span><span class="sxs-lookup"><span data-stu-id="0f170-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="0f170-215">-SSHKeyPairs</span></span>
<span data-ttu-id="0f170-216">Gibt SSH-Schlüsselpaare an.</span><span class="sxs-lookup"><span data-stu-id="0f170-216">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="0f170-217">-SSHPublicKeys</span></span>
<span data-ttu-id="0f170-218">Gibt die öffentlichen SSH-Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="0f170-218">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-219">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="0f170-219">-TimeZone</span></span>
<span data-ttu-id="0f170-220">Gibt die Zeitzone für den virtuellen Computer an, beispielsweise Pacific Standard Time oder Kanada Central Normalzeit.</span><span class="sxs-lookup"><span data-stu-id="0f170-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-221">-VM</span><span class="sxs-lookup"><span data-stu-id="0f170-221">-VM</span></span>
<span data-ttu-id="0f170-222">Gibt ein Objekt eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="0f170-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="0f170-223">-Windows</span></span>
<span data-ttu-id="0f170-224">Gibt an, dass diese Konfiguration einen eigenständigen virtuellen Computer erstellt, auf dem das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f170-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-225">-Windows Domain</span><span class="sxs-lookup"><span data-stu-id="0f170-225">-WindowsDomain</span></span>
<span data-ttu-id="0f170-226">Gibt an, dass diese Konfiguration Windows Server erstellt, der einer Active Directory-Domäne beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0f170-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="0f170-227">-WinRMCertificate</span></span>
<span data-ttu-id="0f170-228">Gibt ein Zertifikat an, das diese Konfiguration einem WinRM-Endpunkt zuordnet.</span><span class="sxs-lookup"><span data-stu-id="0f170-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="0f170-229">-X509Certificates</span></span>
<span data-ttu-id="0f170-230">Gibt ein Array von X509-Zertifikaten an, die für einen gehosteten Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0f170-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f170-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f170-231">CommonParameters</span></span>
<span data-ttu-id="0f170-232">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f170-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f170-233">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f170-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f170-234">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f170-234">INPUTS</span></span>

## <span data-ttu-id="0f170-235">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f170-235">OUTPUTS</span></span>

## <span data-ttu-id="0f170-236">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f170-236">NOTES</span></span>

## <span data-ttu-id="0f170-237">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f170-237">RELATED LINKS</span></span>

[<span data-ttu-id="0f170-238">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="0f170-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="0f170-239">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="0f170-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)



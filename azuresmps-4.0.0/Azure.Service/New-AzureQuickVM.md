---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006115"
---
# <span data-ttu-id="eece5-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="eece5-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="eece5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eece5-102">SYNOPSIS</span></span>
<span data-ttu-id="eece5-103">Konfiguriert und erstellt einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="eece5-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="eece5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eece5-104">SYNTAX</span></span>

### <span data-ttu-id="eece5-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="eece5-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="eece5-106">Linux</span><span class="sxs-lookup"><span data-stu-id="eece5-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="eece5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eece5-107">DESCRIPTION</span></span>
<span data-ttu-id="eece5-108">Das Cmdlet **New-AzureQuickVM** konfiguriert und erstellt einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="eece5-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="eece5-109">Dieses Cmdlet kann einen virtuellen Computer in einem vorhandenen Azure-Dienst bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eece5-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="eece5-110">Dieses Cmdlet kann alternativ einen Azure-Dienst erstellen, der den neuen virtuellen Computer hostet.</span><span class="sxs-lookup"><span data-stu-id="eece5-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="eece5-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eece5-111">EXAMPLES</span></span>

### <span data-ttu-id="eece5-112">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="eece5-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="eece5-113">Dieser Befehl erstellt einen virtuellen Computer, auf dem das Windows-Betriebssystem in einem vorhandenen Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eece5-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="eece5-114">Das Cmdlet basiert auf dem angegebenen Bild auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="eece5-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="eece5-115">Der Befehl gibt den *WaitForBoot* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="eece5-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="eece5-116">Daher wartet das Cmdlet auf den Start des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="eece5-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="eece5-117">Beispiel 2: Erstellen eines virtuellen Computers mit Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="eece5-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="eece5-118">Der erste Befehl ruft Zertifikate aus einem Store ab und speichert Sie in der $certs-Variablen.</span><span class="sxs-lookup"><span data-stu-id="eece5-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="eece5-119">Der zweite Befehl erstellt einen virtuellen Computer, der das Windows-Betriebssystem in einem vorhandenen Dienst aus einem Bild ausführt.</span><span class="sxs-lookup"><span data-stu-id="eece5-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="eece5-120">Standardmäßig ist WinRM HTTPS-Listener auf dem virtuellen Computer aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eece5-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="eece5-121">Der Befehl gibt den *WaitForBoot* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="eece5-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="eece5-122">Daher wartet das Cmdlet auf den Start des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="eece5-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="eece5-123">Der Befehl lädt ein WinRM-Zertifikat und-X509Certificates in den gehosteten Dienst hoch.</span><span class="sxs-lookup"><span data-stu-id="eece5-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="eece5-124">Beispiel 3: Erstellen eines virtuellen Computers, auf dem das Linux-Betriebssystem ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="eece5-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="eece5-125">Dieser Befehl erstellt einen virtuellen Computer, auf dem das Linux-Betriebssystem aus einem Bild ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="eece5-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="eece5-126">Dieser Befehl erstellt einen Dienst zum Hosten des neuen virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="eece5-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="eece5-127">Der Befehl gibt einen Speicherort für den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="eece5-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="eece5-128">Beispiel 4: Erstellen eines virtuellen Computers und Erstellen eines Diensts zum Hosten des neuen virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="eece5-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="eece5-129">Der erste Befehl ruft Speicherorte mit dem Cmdlet **Get-AzureLocation** ab und speichert Sie dann in der $Locations-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="eece5-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="eece5-130">Der zweite Befehl ruft verfügbare Bilder mit dem Cmdlet **Get-AzureVMImage** ab und speichert Sie dann in der $Images-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="eece5-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="eece5-131">Der endgültige Befehl erstellt einen umfangreichen virtuellen Computer mit dem Namen VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="eece5-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="eece5-132">Auf dem virtuellen Computer wird das Betriebssystem Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eece5-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="eece5-133">Sie basiert auf einem der Bilder in $Images.</span><span class="sxs-lookup"><span data-stu-id="eece5-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="eece5-134">Der Befehl erstellt einen Dienst mit dem Namen ContosoService03 für den neuen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="eece5-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="eece5-135">Der Dienst befindet sich an einem Speicherort in $Locations.</span><span class="sxs-lookup"><span data-stu-id="eece5-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="eece5-136">Beispiel 5: Erstellen eines virtuellen Computers mit einem reservierten IP-Namen</span><span class="sxs-lookup"><span data-stu-id="eece5-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="eece5-137">Der erste Befehl ruft Speicherorte ab und speichert Sie dann in der $Locations-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="eece5-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="eece5-138">Der zweite Befehl ruft verfügbare Bilder ab und speichert Sie dann in der $Images-Arrayvariablen.</span><span class="sxs-lookup"><span data-stu-id="eece5-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="eece5-139">Der endgültige Befehl erstellt einen virtuellen Computer mit dem Namen VirtualMachine27, der auf einem der Bilder in $Images basiert.</span><span class="sxs-lookup"><span data-stu-id="eece5-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="eece5-140">Der Befehl erstellt einen Dienst an einem Speicherort in $Locations.</span><span class="sxs-lookup"><span data-stu-id="eece5-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="eece5-141">Der virtuelle Computer verfügt über einen reservierten IP-Namen, der zuvor in der $ipName-Variablen gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="eece5-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="eece5-142">Parameter</span><span class="sxs-lookup"><span data-stu-id="eece5-142">PARAMETERS</span></span>

### <span data-ttu-id="eece5-143">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="eece5-143">-AdminUsername</span></span>
<span data-ttu-id="eece5-144">Gibt den Benutzernamen des Administrator Kontos an, das dieses Cmdlet auf dem virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="eece5-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

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

### <span data-ttu-id="eece5-145">-Affinitygroup</span><span class="sxs-lookup"><span data-stu-id="eece5-145">-AffinityGroup</span></span>
<span data-ttu-id="eece5-146">Gibt die affinitätsgruppe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="eece5-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="eece5-147">Geben Sie diesen Parameter oder den *Location* -Parameter nur an, wenn mit diesem Cmdlet ein Azure-Dienst für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eece5-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="eece5-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="eece5-148">-AvailabilitySetName</span></span>
<span data-ttu-id="eece5-149">Gibt den Namen des Verfügbarkeits Satzes an, in dem dieses Cmdlet den virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="eece5-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="eece5-150">-Zertifikate</span><span class="sxs-lookup"><span data-stu-id="eece5-150">-Certificates</span></span>
<span data-ttu-id="eece5-151">Gibt eine Liste der Zertifikate an, die dieses Cmdlet zum Erstellen des Diensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="eece5-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="eece5-152">-CustomDataFile</span></span>
<span data-ttu-id="eece5-153">Gibt eine Datendatei für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="eece5-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="eece5-154">Dieses Cmdlet codiert den Inhalt der Datei als Base64.</span><span class="sxs-lookup"><span data-stu-id="eece5-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="eece5-155">Die Datei muss weniger als 64 KB lang sein.</span><span class="sxs-lookup"><span data-stu-id="eece5-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="eece5-156">Wenn es sich bei dem Gastbetriebssystem um das Windows-Betriebssystem handelt, speichert dieses Cmdlet diese Daten als Binärdatei mit dem Namen%SystemDrive%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="eece5-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="eece5-157">Wenn es sich bei dem Gastbetriebssystem um Linux handelt, übergibt dieses Cmdlet die Daten mithilfe der ovf-env.xml-Datei.</span><span class="sxs-lookup"><span data-stu-id="eece5-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="eece5-158">Bei der Installation wird die Datei in das/var/lib/waagent-Verzeichnis kopiert.</span><span class="sxs-lookup"><span data-stu-id="eece5-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="eece5-159">Der Agent speichert auch die Base64-codierten Daten in/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="eece5-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="eece5-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="eece5-160">-DisableGuestAgent</span></span>
<span data-ttu-id="eece5-161">Gibt an, dass dieses Cmdlet den Guest-Agent "Infrastructure as a Service (IaaS)" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eece5-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="eece5-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="eece5-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="eece5-163">Gibt an, dass dieses Cmdlet die Windows-Remote Verwaltung (WinRM) auf HTTPS deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="eece5-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="eece5-164">Standardmäßig ist WinRM über HTTPS aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eece5-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="eece5-165">-DnsSettings</span></span>
<span data-ttu-id="eece5-166">Gibt ein Array von DNS-Server Objekten an, die die DNS-Einstellungen für die neue Bereitstellung definieren.</span><span class="sxs-lookup"><span data-stu-id="eece5-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="eece5-167">Verwenden Sie zum Erstellen eines **DnsServer** -Objekts das Cmdlet **New-AzureDns** .</span><span class="sxs-lookup"><span data-stu-id="eece5-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="eece5-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="eece5-169">Gibt an, dass das Cmdlet WinRM über HTTP aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eece5-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="eece5-170">-HostCaching</span></span>
<span data-ttu-id="eece5-171">Gibt den Host Zwischenspeicherungsmodus für den Datenträger des Betriebssystems an.</span><span class="sxs-lookup"><span data-stu-id="eece5-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="eece5-172">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="eece5-172">Valid values are:</span></span> 

- <span data-ttu-id="eece5-173">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="eece5-173">ReadOnly</span></span>
- <span data-ttu-id="eece5-174">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eece5-174">ReadWrite</span></span>

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

### <span data-ttu-id="eece5-175">-Bildname</span><span class="sxs-lookup"><span data-stu-id="eece5-175">-ImageName</span></span>
<span data-ttu-id="eece5-176">Gibt den Namen der Datenträgerabbildung an, die dieses Cmdlet zum Erstellen des Betriebssystemdatenträgers verwendet.</span><span class="sxs-lookup"><span data-stu-id="eece5-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-177">-Information</span><span class="sxs-lookup"><span data-stu-id="eece5-177">-InformationAction</span></span>
<span data-ttu-id="eece5-178">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="eece5-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="eece5-179">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="eece5-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="eece5-180">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="eece5-180">Continue</span></span>
- <span data-ttu-id="eece5-181">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="eece5-181">Ignore</span></span>
- <span data-ttu-id="eece5-182">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="eece5-182">Inquire</span></span>
- <span data-ttu-id="eece5-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eece5-183">SilentlyContinue</span></span>
- <span data-ttu-id="eece5-184">Beenden</span><span class="sxs-lookup"><span data-stu-id="eece5-184">Stop</span></span>
- <span data-ttu-id="eece5-185">Anhalten</span><span class="sxs-lookup"><span data-stu-id="eece5-185">Suspend</span></span>

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

### <span data-ttu-id="eece5-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eece5-186">-InformationVariable</span></span>
<span data-ttu-id="eece5-187">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="eece5-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eece5-188">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="eece5-188">-InstanceSize</span></span>
<span data-ttu-id="eece5-189">Gibt die Größe der Instanz an.</span><span class="sxs-lookup"><span data-stu-id="eece5-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="eece5-190">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="eece5-190">Valid values are:</span></span> 

- <span data-ttu-id="eece5-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="eece5-191">ExtraSmall</span></span>
- <span data-ttu-id="eece5-192">Kleine</span><span class="sxs-lookup"><span data-stu-id="eece5-192">Small</span></span>
- <span data-ttu-id="eece5-193">Mittel</span><span class="sxs-lookup"><span data-stu-id="eece5-193">Medium</span></span>
- <span data-ttu-id="eece5-194">Große</span><span class="sxs-lookup"><span data-stu-id="eece5-194">Large</span></span>
- <span data-ttu-id="eece5-195">Extra Large</span><span class="sxs-lookup"><span data-stu-id="eece5-195">ExtraLarge</span></span>
- <span data-ttu-id="eece5-196">A5</span><span class="sxs-lookup"><span data-stu-id="eece5-196">A5</span></span>
- <span data-ttu-id="eece5-197">A6</span><span class="sxs-lookup"><span data-stu-id="eece5-197">A6</span></span>
- <span data-ttu-id="eece5-198">A7</span><span class="sxs-lookup"><span data-stu-id="eece5-198">A7</span></span>
- <span data-ttu-id="eece5-199">A8</span><span class="sxs-lookup"><span data-stu-id="eece5-199">A8</span></span>
- <span data-ttu-id="eece5-200">A9</span><span class="sxs-lookup"><span data-stu-id="eece5-200">A9</span></span>
- <span data-ttu-id="eece5-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="eece5-201">Basic_A0</span></span>
- <span data-ttu-id="eece5-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="eece5-202">Basic_A1</span></span>
- <span data-ttu-id="eece5-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="eece5-203">Basic_A2</span></span>
- <span data-ttu-id="eece5-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="eece5-204">Basic_A3</span></span>
- <span data-ttu-id="eece5-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="eece5-205">Basic_A4</span></span>
- <span data-ttu-id="eece5-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="eece5-206">Standard_D1</span></span>
- <span data-ttu-id="eece5-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="eece5-207">Standard_D2</span></span>
- <span data-ttu-id="eece5-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="eece5-208">Standard_D3</span></span>
- <span data-ttu-id="eece5-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="eece5-209">Standard_D4</span></span>
- <span data-ttu-id="eece5-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="eece5-210">Standard_D11</span></span>
- <span data-ttu-id="eece5-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="eece5-211">Standard_D12</span></span>
- <span data-ttu-id="eece5-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="eece5-212">Standard_D13</span></span>
- <span data-ttu-id="eece5-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="eece5-213">Standard_D14</span></span>

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

### <span data-ttu-id="eece5-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="eece5-214">-Linux</span></span>
<span data-ttu-id="eece5-215">Gibt an, dass mit diesem Cmdlet ein Linux-basierter virtueller Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eece5-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

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

### <span data-ttu-id="eece5-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="eece5-216">-LinuxUser</span></span>
<span data-ttu-id="eece5-217">Gibt den Benutzernamen des Linux-Administratorkontos an, das dieses Cmdlet auf dem virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="eece5-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

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

### <span data-ttu-id="eece5-218">-Standort</span><span class="sxs-lookup"><span data-stu-id="eece5-218">-Location</span></span>
<span data-ttu-id="eece5-219">Gibt das Azure Datacenter an, das den virtuellen Computer hostet.</span><span class="sxs-lookup"><span data-stu-id="eece5-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="eece5-220">Wenn Sie diesen Parameter angeben, erstellt das Cmdlet einen Azure-Dienst an der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="eece5-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="eece5-221">Geben Sie diesen Parameter oder den *affinitygroup* -Parameter nur an, wenn mit diesem Cmdlet ein Azure-Dienst für den virtuellen Computer erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eece5-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="eece5-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="eece5-222">-MediaLocation</span></span>
<span data-ttu-id="eece5-223">Gibt den Azure-Speicherort an, an dem mit diesem Cmdlet die virtuellen Computer Datenträger erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eece5-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="eece5-224">-Name</span><span class="sxs-lookup"><span data-stu-id="eece5-224">-Name</span></span>
<span data-ttu-id="eece5-225">Gibt den Namen des virtuellen Computers an, der vom Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eece5-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="eece5-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="eece5-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="eece5-227">Gibt an, dass diese Konfiguration den privaten Schlüssel nicht hochlädt.</span><span class="sxs-lookup"><span data-stu-id="eece5-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="eece5-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="eece5-229">Gibt an, dass dieses Cmdlet keinen WinRM-Endpunkt für den virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="eece5-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-230">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="eece5-230">-Password</span></span>
<span data-ttu-id="eece5-231">Gibt das Kennwort für das Administratorkonto an.</span><span class="sxs-lookup"><span data-stu-id="eece5-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="eece5-232">-Profil</span><span class="sxs-lookup"><span data-stu-id="eece5-232">-Profile</span></span>
<span data-ttu-id="eece5-233">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="eece5-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eece5-234">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="eece5-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eece5-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="eece5-235">-ReservedIPName</span></span>
<span data-ttu-id="eece5-236">Gibt den reservierten IP-Namen an.</span><span class="sxs-lookup"><span data-stu-id="eece5-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="eece5-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="eece5-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="eece5-238">Gibt den vollqualifizierten Domänennamen für die Reverse-DNS-Suche an.</span><span class="sxs-lookup"><span data-stu-id="eece5-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="eece5-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="eece5-239">-ServiceName</span></span>
<span data-ttu-id="eece5-240">Gibt den Namen eines neuen oder vorhandenen Azure-Diensts an, dem dieses Cmdlet den neuen virtuellen Computer hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="eece5-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="eece5-241">Wenn Sie einen neuen Dienst angeben, wird er von diesen Cmdlets erstellt.</span><span class="sxs-lookup"><span data-stu-id="eece5-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="eece5-242">Wenn Sie einen neuen Dienst erstellen möchten, müssen Sie den Parameter *Location* oder *affinitygroup* angeben.</span><span class="sxs-lookup"><span data-stu-id="eece5-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="eece5-243">Wenn Sie einen vorhandenen Dienst angeben, geben Sie *Location* oder *affinitygroup* nicht an.</span><span class="sxs-lookup"><span data-stu-id="eece5-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="eece5-244">-SSHKeyPairs</span></span>
<span data-ttu-id="eece5-245">Gibt SSH-Schlüsselpaare an.</span><span class="sxs-lookup"><span data-stu-id="eece5-245">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="eece5-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="eece5-246">-SSHPublicKeys</span></span>
<span data-ttu-id="eece5-247">Gibt die öffentlichen SSH-Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="eece5-247">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="eece5-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="eece5-248">-SubnetNames</span></span>
<span data-ttu-id="eece5-249">Gibt ein Array von Namen des Subnets für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="eece5-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="eece5-250">-VNetName</span></span>
<span data-ttu-id="eece5-251">Gibt den Namen eines virtuellen Netzwerks für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="eece5-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="eece5-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="eece5-252">-WaitForBoot</span></span>
<span data-ttu-id="eece5-253">Gibt an, dass dieses Cmdlet auf den virtuellen Computer wartet, um den Zustand ReadyRole zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="eece5-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="eece5-254">Wenn der virtuelle Computer einen der folgenden Zustände erreicht, schlägt das Cmdlet fehl: FailedStartingVM, ProvisioningFailed oder ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="eece5-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="eece5-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="eece5-255">-Windows</span></span>
<span data-ttu-id="eece5-256">Gibt an, dass dieses Cmdlet einen virtuellen Windows-Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="eece5-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

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

### <span data-ttu-id="eece5-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="eece5-257">-WinRMCertificate</span></span>
<span data-ttu-id="eece5-258">Gibt ein Zertifikat an, das dieses Cmdlet einem WinRM-Endpunkt zuordnet.</span><span class="sxs-lookup"><span data-stu-id="eece5-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="eece5-259">-X509Certificates</span></span>
<span data-ttu-id="eece5-260">Gibt ein Array von X509-Zertifikaten an, die für einen gehosteten Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="eece5-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eece5-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eece5-261">CommonParameters</span></span>
<span data-ttu-id="eece5-262">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eece5-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eece5-263">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eece5-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eece5-264">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eece5-264">INPUTS</span></span>

## <span data-ttu-id="eece5-265">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eece5-265">OUTPUTS</span></span>

## <span data-ttu-id="eece5-266">Notizen</span><span class="sxs-lookup"><span data-stu-id="eece5-266">NOTES</span></span>

## <span data-ttu-id="eece5-267">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eece5-267">RELATED LINKS</span></span>

[<span data-ttu-id="eece5-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="eece5-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="eece5-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="eece5-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="eece5-270">Neu – AzureDns</span><span class="sxs-lookup"><span data-stu-id="eece5-270">New-AzureDns</span></span>](./New-AzureDns.md)



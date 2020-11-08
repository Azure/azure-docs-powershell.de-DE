---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006406"
---
# <span data-ttu-id="fbac2-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="fbac2-101">New-AzureVM</span></span>

## <span data-ttu-id="fbac2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbac2-102">SYNOPSIS</span></span>
<span data-ttu-id="fbac2-103">Erstellt einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="fbac2-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="fbac2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbac2-104">SYNTAX</span></span>

### <span data-ttu-id="fbac2-105">ExistingService (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbac2-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="fbac2-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="fbac2-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="fbac2-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbac2-107">DESCRIPTION</span></span>
<span data-ttu-id="fbac2-108">Das Cmdlet **New-AzureVM** fügt einen neuen virtuellen Computer zu einem vorhandenen Azure-Dienst hinzu oder erstellt einen virtuellen Computer und einen Dienst im aktuellen Abonnement, wenn entweder der *Standort* oder die *Affinitäts* Leiste angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fbac2-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="fbac2-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbac2-109">EXAMPLES</span></span>

### <span data-ttu-id="fbac2-110">Beispiel 1: Erstellen eines virtuellen Computers für eine Windows-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fbac2-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="fbac2-111">Mit diesem Befehl wird eine Bereitstellungskonfiguration basierend auf einer virtuellen Computerkonfiguration für das Windows-Betriebssystem erstellt und zum Erstellen eines virtuellen Computers in einer bestimmten affinitätsgruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="fbac2-112">Beispiel 2: Erstellen eines virtuellen Computers für eine Linux-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fbac2-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="fbac2-113">Mit diesem Befehl wird eine Bereitstellungskonfiguration basierend auf einer virtuellen Computerkonfiguration für Linux erstellt und zum Erstellen eines virtuellen Computers in einer bestimmten affinitätsgruppe verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="fbac2-114">Beispiel 3: Erstellen eines virtuellen Computers und Hinzufügen eines Datenlaufwerks</span><span class="sxs-lookup"><span data-stu-id="fbac2-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="fbac2-115">Die ersten beiden Befehle erhalten verfügbare Bilder mit dem Cmdlet **Get-AzureVMImage** und speichert eines davon in der $Image-Variablen.</span><span class="sxs-lookup"><span data-stu-id="fbac2-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="fbac2-116">Mit diesem Befehl wird eine Bereitstellungskonfiguration basierend auf einer virtuellen Computerkonfiguration für das Windows-Betriebssystem erstellt und zum Erstellen eines virtuellen Computers mit einem Azure-Daten Datenträger verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="fbac2-117">Beispiel 4: Erstellen eines virtuellen Computers mit einer reservierten IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="fbac2-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="fbac2-118">Mit diesem Befehl wird eine Bereitstellungskonfiguration basierend auf einer virtuellen Computerkonfiguration für das Windows-Betriebssystem erstellt und zum Erstellen eines virtuellen Computers mit einer reservierten IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="fbac2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbac2-119">PARAMETERS</span></span>

### <span data-ttu-id="fbac2-120">-Affinitygroup</span><span class="sxs-lookup"><span data-stu-id="fbac2-120">-AffinityGroup</span></span>
<span data-ttu-id="fbac2-121">Gibt die Azure-affinitätsgruppe an, in der sich der clouddienst befindet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="fbac2-122">Dieser Parameter ist nur erforderlich, wenn mit diesem Cmdlet ein clouddienst erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="fbac2-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="fbac2-123">-DeploymentLabel</span></span>
<span data-ttu-id="fbac2-124">Gibt eine Bezeichnung für die Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-124">Specifies a label for the deployment.</span></span>

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

### <span data-ttu-id="fbac2-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="fbac2-125">-DeploymentName</span></span>
<span data-ttu-id="fbac2-126">Gibt einen Bereitstellungsnamen an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-126">Specifies a deployment name.</span></span>
<span data-ttu-id="fbac2-127">Wenn Sie nicht angegeben wird, verwendet dieses Cmdlet den Dienstnamen als Bereitstellungsnamen.</span><span class="sxs-lookup"><span data-stu-id="fbac2-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

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

### <span data-ttu-id="fbac2-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="fbac2-128">-DnsSettings</span></span>
<span data-ttu-id="fbac2-129">Gibt ein DNS-Server Objekt an, das die DNS-Einstellungen für die neue Bereitstellung definiert.</span><span class="sxs-lookup"><span data-stu-id="fbac2-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-130">-Information</span><span class="sxs-lookup"><span data-stu-id="fbac2-130">-InformationAction</span></span>
<span data-ttu-id="fbac2-131">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="fbac2-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fbac2-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="fbac2-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fbac2-133">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="fbac2-133">Continue</span></span>
- <span data-ttu-id="fbac2-134">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="fbac2-134">Ignore</span></span>
- <span data-ttu-id="fbac2-135">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="fbac2-135">Inquire</span></span>
- <span data-ttu-id="fbac2-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fbac2-136">SilentlyContinue</span></span>
- <span data-ttu-id="fbac2-137">Beenden</span><span class="sxs-lookup"><span data-stu-id="fbac2-137">Stop</span></span>
- <span data-ttu-id="fbac2-138">Anhalten</span><span class="sxs-lookup"><span data-stu-id="fbac2-138">Suspend</span></span>

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

### <span data-ttu-id="fbac2-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fbac2-139">-InformationVariable</span></span>
<span data-ttu-id="fbac2-140">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fbac2-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="fbac2-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="fbac2-142">Gibt ein internes Lastenausgleichsmodul an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="fbac2-143">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-144">-Standort</span><span class="sxs-lookup"><span data-stu-id="fbac2-144">-Location</span></span>
<span data-ttu-id="fbac2-145">Gibt den Speicherort an, der den neuen Dienst hostet.</span><span class="sxs-lookup"><span data-stu-id="fbac2-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="fbac2-146">Wenn der Dienst bereits vorhanden ist, geben Sie diesen Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-147">-Profil</span><span class="sxs-lookup"><span data-stu-id="fbac2-147">-Profile</span></span>
<span data-ttu-id="fbac2-148">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="fbac2-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fbac2-149">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="fbac2-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fbac2-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="fbac2-150">-ReservedIPName</span></span>
<span data-ttu-id="fbac2-151">Gibt den Namen der reservierten IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-151">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="fbac2-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="fbac2-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="fbac2-153">Gibt den vollqualifizierten Domänennamen für Reverse-DNS an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="fbac2-154">-ServiceDescription</span></span>
<span data-ttu-id="fbac2-155">Gibt eine Beschreibung für den neuen Dienst an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="fbac2-156">-ServiceLabel</span></span>
<span data-ttu-id="fbac2-157">Gibt eine Bezeichnung für den neuen Dienst an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fbac2-158">-ServiceName</span></span>
<span data-ttu-id="fbac2-159">Gibt den neuen oder vorhandenen Dienstnamen an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="fbac2-160">Wenn der Dienst nicht vorhanden ist, wird dieser vom Cmdlet für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="fbac2-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="fbac2-161">Verwenden Sie den Parameter *Location* oder *affinitygroup* , um anzugeben, wo der Dienst erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fbac2-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="fbac2-162">Wenn der Dienst vorhanden ist, wird der *Location* -oder *affinitygroup* -Parameter nicht benötigt.</span><span class="sxs-lookup"><span data-stu-id="fbac2-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-163">-VMS</span><span class="sxs-lookup"><span data-stu-id="fbac2-163">-VMs</span></span>
<span data-ttu-id="fbac2-164">Gibt eine Liste der zu erstellende virtuellen Computerobjekte an.</span><span class="sxs-lookup"><span data-stu-id="fbac2-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbac2-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="fbac2-165">-VNetName</span></span>
<span data-ttu-id="fbac2-166">Gibt den Namen des virtuellen Netzwerks an, in dem dieses Cmdlet den virtuellen Computer bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="fbac2-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

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

### <span data-ttu-id="fbac2-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="fbac2-167">-WaitForBoot</span></span>
<span data-ttu-id="fbac2-168">Gibt an, dass dieses Cmdlet auf den virtuellen Computer wartet, um den **ReadyRole** -Zustand zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="fbac2-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="fbac2-169">Dieses Cmdlet schlägt fehl, wenn der virtuelle Computer während des Wartens in einen der folgenden Zustände fällt: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="fbac2-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="fbac2-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbac2-170">CommonParameters</span></span>
<span data-ttu-id="fbac2-171">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbac2-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbac2-172">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbac2-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbac2-173">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbac2-173">INPUTS</span></span>

## <span data-ttu-id="fbac2-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbac2-174">OUTPUTS</span></span>

## <span data-ttu-id="fbac2-175">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbac2-175">NOTES</span></span>

## <span data-ttu-id="fbac2-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbac2-176">RELATED LINKS</span></span>

[<span data-ttu-id="fbac2-177">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="fbac2-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="fbac2-178">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="fbac2-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="fbac2-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="fbac2-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="fbac2-180">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="fbac2-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)



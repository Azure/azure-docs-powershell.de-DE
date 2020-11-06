---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505173"
---
# <span data-ttu-id="67393-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-101">New-AzureRmVM</span></span>

## <span data-ttu-id="67393-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67393-102">SYNOPSIS</span></span>
<span data-ttu-id="67393-103">Erstellt einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="67393-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67393-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67393-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67393-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67393-105">DESCRIPTION</span></span>
<span data-ttu-id="67393-106">Das Cmdlet **New-AzureRmVM** erstellt einen virtuellen Computer in Azure.</span><span class="sxs-lookup"><span data-stu-id="67393-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="67393-107">Dieses Cmdlet akzeptiert ein Objekt eines virtuellen Computers als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="67393-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="67393-108">Verwenden Sie das New-AzureRmVMConfig-Cmdlet zum Erstellen eines virtuellen Computerobjekts.</span><span class="sxs-lookup"><span data-stu-id="67393-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="67393-109">Andere Cmdlets können verwendet werden, um den virtuellen Computer wie "AzureRmVMOperatingSystem", "AzureRmVMSourceImage", "Add-AzureRmVMNetworkInterface" und "Satz-AzureRmVMOSDisk" zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="67393-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="67393-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67393-110">EXAMPLES</span></span>

### <span data-ttu-id="67393-111">Beispiel 1: Erstellen eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="67393-111">Example 1: Create a virtual machine</span></span>
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

<span data-ttu-id="67393-112">Dieses Beispielskript zeigt, wie Sie einen virtuellen Computer erstellen.</span><span class="sxs-lookup"><span data-stu-id="67393-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="67393-113">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="67393-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="67393-114">Beispiel 2: Erstellen eines virtuellen Computers aus einem benutzerdefinierten Benutzerbild</span><span class="sxs-lookup"><span data-stu-id="67393-114">Example 2: Create a virtual machine from a custom user image</span></span>
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force 
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account. 
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance. 
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3" 
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="67393-115">In diesem Beispiel wird ein vorhandenes, von sys vorbereitetes, generalisiertes benutzerdefiniertes Betriebssystemabbild verwendet und ein Daten Datenträger an ihn angefügt, ein neues Netzwerk bereitgestellt, die VHD bereitgestellt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67393-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="67393-116">Dieses Skript kann für die automatische Bereitstellung verwendet werden, da es die Administratoranmeldeinformationen des lokalen virtuellen Computers Inline verwendet, anstatt **Get-Credential** aufzurufen, für die Benutzerinteraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="67393-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="67393-117">Bei diesem Skript wird davon ausgegangen, dass Sie bereits bei Ihrem Azure-Konto angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="67393-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="67393-118">Mit dem Cmdlet **Get-AzureSubscription** können Sie Ihren Anmeldestatus bestätigen.</span><span class="sxs-lookup"><span data-stu-id="67393-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="67393-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="67393-119">PARAMETERS</span></span>

### <span data-ttu-id="67393-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67393-120">-DefaultProfile</span></span>
<span data-ttu-id="67393-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67393-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67393-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="67393-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="67393-123">Gibt an, dass dieses Cmdlet die **BG-Informations** Erweiterung auf dem virtuellen Computer nicht installiert.</span><span class="sxs-lookup"><span data-stu-id="67393-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67393-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="67393-124">-LicenseType</span></span>
<span data-ttu-id="67393-125">Gibt einen Lizenztyp an, der angibt, dass das Bild oder der Datenträger für den virtuellen Computer lokal genehmigt wurde.</span><span class="sxs-lookup"><span data-stu-id="67393-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="67393-126">Dieser Wert wird nur für Bilder verwendet, die das Betriebssystem Windows Server enthalten.</span><span class="sxs-lookup"><span data-stu-id="67393-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="67393-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="67393-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="67393-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="67393-128">Windows_Client</span></span> 
- <span data-ttu-id="67393-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="67393-129">Windows_Server</span></span>

<span data-ttu-id="67393-130">Dieser Wert kann nicht aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="67393-130">This value cannot be updated.</span></span>
<span data-ttu-id="67393-131">Wenn Sie diesen Parameter für eine Aktualisierung angeben, muss der Wert dem Anfangswert für den virtuellen Computer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="67393-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67393-132">-Standort</span><span class="sxs-lookup"><span data-stu-id="67393-132">-Location</span></span>
<span data-ttu-id="67393-133">Gibt einen Speicherort für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="67393-133">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="67393-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67393-134">-ResourceGroupName</span></span>
<span data-ttu-id="67393-135">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="67393-135">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="67393-136">-Tags</span><span class="sxs-lookup"><span data-stu-id="67393-136">-Tags</span></span>
<span data-ttu-id="67393-137">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="67393-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="67393-138">Durch das Hinzufügen von Kategorien zu Ressourcen können Sie Ressourcengruppen übergreifend gruppieren und eigene Ansichten erstellen.</span><span class="sxs-lookup"><span data-stu-id="67393-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="67393-139">Für jede Ressource oder jede Ressourcengruppe können maximal 15 Tags vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="67393-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67393-140">-VM</span><span class="sxs-lookup"><span data-stu-id="67393-140">-VM</span></span>
<span data-ttu-id="67393-141">Gibt einen lokalen virtuellen Computer an, den Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="67393-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="67393-142">Verwenden Sie das New-AzureRmVMConfig-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="67393-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="67393-143">Andere Cmdlets können zum Konfigurieren des virtuellen Computers verwendet werden, beispielsweise "AzureRmVMOperatingSystem", "AzureRmVMSourceImage" und "Add-AzureRmVMNetworkInterface".</span><span class="sxs-lookup"><span data-stu-id="67393-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67393-144">-Zone</span><span class="sxs-lookup"><span data-stu-id="67393-144">-Zone</span></span>
<span data-ttu-id="67393-145">Gibt die Zonenliste der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="67393-145">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67393-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67393-146">-Confirm</span></span>
<span data-ttu-id="67393-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67393-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67393-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67393-148">-WhatIf</span></span>
<span data-ttu-id="67393-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67393-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="67393-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67393-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67393-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67393-151">CommonParameters</span></span>
<span data-ttu-id="67393-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67393-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67393-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67393-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67393-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67393-154">INPUTS</span></span>

## <span data-ttu-id="67393-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67393-155">OUTPUTS</span></span>

## <span data-ttu-id="67393-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="67393-156">NOTES</span></span>

## <span data-ttu-id="67393-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67393-157">RELATED LINKS</span></span>

[<span data-ttu-id="67393-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="67393-159">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="67393-160">Neustart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="67393-161">Anfang-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="67393-162">Stopp-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="67393-163">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="67393-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="67393-164">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="67393-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="67393-165">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="67393-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="67393-166">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="67393-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="67393-167">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="67393-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="67393-168">Satz-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="67393-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="67393-169">Satz-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="67393-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)



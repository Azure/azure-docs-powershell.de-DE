---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938272"
---
# <span data-ttu-id="4c9b7-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4c9b7-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="4c9b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9b7-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9b7-103">Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="4c9b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c9b7-104">SYNTAX</span></span>

### <span data-ttu-id="4c9b7-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c9b7-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9b7-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="4c9b7-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9b7-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="4c9b7-107">WindowsDisableVMAgent</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9b7-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="4c9b7-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9b7-109">Linux</span><span class="sxs-lookup"><span data-stu-id="4c9b7-109">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c9b7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4c9b7-110">DESCRIPTION</span></span>
<span data-ttu-id="4c9b7-111">Das **Cmdlet Set-AzVMOperatingSystem** legt Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-111">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="4c9b7-112">Sie können Anmeldeinformationen, Computername und Betriebssystemtyp angeben.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="4c9b7-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4c9b7-113">EXAMPLES</span></span>

### <span data-ttu-id="4c9b7-114">Beispiel 1: Festlegen von Betriebssystemeigenschaften für einen neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4c9b7-114">Example 1: Set operating system properties for a new virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="4c9b7-115">Mit dem ersten Befehl wird ein Kennwort in eine sichere Zeichenfolge konvertiert und dann in der $SecurePassword gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="4c9b7-116">Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="4c9b7-117">Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer FullerP und das kennwort, das in $SecurePassword gespeichert ist, und speichert dann die Anmeldeinformationen in der $Credential Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="4c9b7-118">Weitere Informationen finden Sie unter `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="4c9b7-119">Der dritte Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-119">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4c9b7-120">Mit dem vierten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4c9b7-121">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4c9b7-122">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4c9b7-123">Die nächsten vier Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="4c9b7-124">Da Sie diese Zeichenfolgen direkt im **Befehl Set-AzVMOperatingSystem** angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-124">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="4c9b7-125">Sie können jedoch einen ansatz wie diesen in Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="4c9b7-126">Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der auf der $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4c9b7-127">Der Befehl verwendet die in der Datei $Credential.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="4c9b7-128">Der Befehl verwendet Variablen, die in früheren Befehlen für einige Parameter zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-128">The command uses variables assigned in previous commands for some parameters.</span></span>

### <span data-ttu-id="4c9b7-129">Beispiel 2: Festlegen von Betriebssystemeigenschaften für einen neuen virtuellen Computer mit aktivierter hot patching</span><span class="sxs-lookup"><span data-stu-id="4c9b7-129">Example 2: Set operating system properties for a new virtual machine with hot patching enabled</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

<span data-ttu-id="4c9b7-130">Mit dem ersten Befehl wird ein Kennwort in eine sichere Zeichenfolge konvertiert und dann in der $SecurePassword gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-130">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="4c9b7-131">Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-131">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="4c9b7-132">Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer FullerP und das kennwort, das in $SecurePassword gespeichert ist, und speichert dann die Anmeldeinformationen in der $Credential Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-132">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="4c9b7-133">Weitere Informationen finden Sie unter `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-133">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="4c9b7-134">Der dritte Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-134">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4c9b7-135">Mit dem vierten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-135">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4c9b7-136">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-136">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4c9b7-137">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-137">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4c9b7-138">Die nächsten vier Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-138">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="4c9b7-139">Da Sie diese Zeichenfolgen direkt im **Befehl Set-AzVMOperatingSystem** angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-139">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="4c9b7-140">Sie können jedoch einen ansatz wie diesen in Skripts verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-140">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="4c9b7-141">Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der auf der $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-141">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4c9b7-142">Der Befehl verwendet die in der Datei $Credential.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-142">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="4c9b7-143">Der Befehl verwendet Variablen, die in früheren Befehlen für einige Parameter zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-143">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="4c9b7-144">Der Befehl aktiviert hotpatching auf dem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-144">The command enables Hotpatching on the virtual machine.</span></span>

### <span data-ttu-id="4c9b7-145">Beispiel 3: Festlegen von Betriebssystemeigenschaften für einen neuen virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="4c9b7-145">Example 3: Set operating system properties for a new Linux virtual machine</span></span>
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

<span data-ttu-id="4c9b7-146">Mit dem ersten Befehl wird ein Kennwort in eine sichere Zeichenfolge konvertiert und dann in der $SecurePassword gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-146">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="4c9b7-147">Weitere Informationen finden Sie unter `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-147">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="4c9b7-148">Der zweite Befehl erstellt eine Anmeldeinformationen für den Benutzer FullerP und das kennwort, das in $SecurePassword gespeichert ist, und speichert dann die Anmeldeinformationen in der $Credential Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-148">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="4c9b7-149">Weitere Informationen finden Sie unter `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-149">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="4c9b7-150">Der dritte Befehl ruft den Verfügbarkeitssatz "AvailabilitySet03" in der Ressourcengruppe "ResourceGroup11" ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-150">The third command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4c9b7-151">Mit dem vierten Befehl wird ein Objekt eines virtuellen Computers erstellt und dann in der $VirtualMachine gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-151">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4c9b7-152">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-152">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4c9b7-153">Der virtuelle Computer gehört zu dem Verfügbarkeitssatz, der auf der $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-153">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4c9b7-154">Die nächsten beiden Befehle weisen Variablen Werte zu, die im folgenden Befehl verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-154">The next two commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="4c9b7-155">Der letzte Befehl legt die Betriebssystemeigenschaften für den virtuellen Computer fest, der auf der $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-155">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4c9b7-156">Der Befehl verwendet die in der Datei $Credential.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-156">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="4c9b7-157">Der Befehl verwendet Variablen, die in früheren Befehlen für einige Parameter zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-157">The command uses variables assigned in previous commands for some parameters.</span></span>
<span data-ttu-id="4c9b7-158">Der Befehl legt den Patchmoduswert auf dem virtuellen Computer auf "AutomaticByPlatform" fest.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-158">The command sets the patch mode value on the virtual machine to "AutomaticByPlatform".</span></span>

## <span data-ttu-id="4c9b7-159">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4c9b7-159">PARAMETERS</span></span>

### <span data-ttu-id="4c9b7-160">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="4c9b7-160">-ComputerName</span></span>
<span data-ttu-id="4c9b7-161">Gibt den Namen des Computers an.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-161">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="4c9b7-162">-Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4c9b7-162">-Credential</span></span>
<span data-ttu-id="4c9b7-163">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-163">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="4c9b7-164">Verwenden Sie das cmdlet Get-Credential, um eine Anmeldeinformationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-164">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="4c9b7-165">Weitere Informationen finden Sie unter `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-165">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="4c9b7-166">-CustomData</span><span class="sxs-lookup"><span data-stu-id="4c9b7-166">-CustomData</span></span>
<span data-ttu-id="4c9b7-167">Gibt eine Zeichenfolge an, die an den virtuellen Computer übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-167">Specifies a string to be passed to the virtual machine.</span></span> <span data-ttu-id="4c9b7-168">Weitere Informationen finden Sie unter [Benutzerdefinierte Daten auf Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span><span class="sxs-lookup"><span data-stu-id="4c9b7-168">For more information see [Custom Data on Azure VMs](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data).</span></span>
<span data-ttu-id="4c9b7-169">**Hinweis: Es wird nicht empfohlen, vertrauliche Informationen in benutzerdefinierten Daten zu speichern.**</span><span class="sxs-lookup"><span data-stu-id="4c9b7-169">**Note: It is not recommended to store sensitive information in custom data.**</span></span>


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

### <span data-ttu-id="4c9b7-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9b7-170">-DefaultProfile</span></span>
<span data-ttu-id="4c9b7-171">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c9b7-172">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="4c9b7-172">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="4c9b7-173">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-173">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="4c9b7-174">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="4c9b7-174">-DisableVMAgent</span></span>
<span data-ttu-id="4c9b7-175">Deaktivieren Sie den Bereitstellungs-VM-Agent.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-175">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="4c9b7-176">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4c9b7-176">-EnableAutoUpdate</span></span>
<span data-ttu-id="4c9b7-177">Gibt an, dass dieses Cmdlet die automatische Aktualisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-177">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="4c9b7-178">-EnableHotpatching</span><span class="sxs-lookup"><span data-stu-id="4c9b7-178">-EnableHotpatching</span></span>
<span data-ttu-id="4c9b7-179">Ermöglicht Kunden das Patchen ihrer Azure VMs, ohne dass ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-179">Enables customers to patch their Azure VMs without requiring a reboot.</span></span> <span data-ttu-id="4c9b7-180">Für enableHotpatching muss der Wert "provisionVMAgent" auf "true" und "patchMode" auf "AutomaticByPlatform" festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-180">For enableHotpatching, the 'provisionVMAgent' must be set to true and 'patchMode' must be set to 'AutomaticByPlatform'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9b7-181">-Linux</span><span class="sxs-lookup"><span data-stu-id="4c9b7-181">-Linux</span></span>
<span data-ttu-id="4c9b7-182">Gibt an, dass der Typ des Betriebssystems Linux ist.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-182">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="4c9b7-183">-PatchMode</span><span class="sxs-lookup"><span data-stu-id="4c9b7-183">-PatchMode</span></span>
<span data-ttu-id="4c9b7-184">Gibt den Modus des In-Guest-Patchings auf den virtuellen IaaS-Computer an.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-184">Specifies the mode of in-guest patching to IaaS virtual machine.</span></span><br><br>
<span data-ttu-id="4c9b7-185">Mögliche Werte sind:</span><span class="sxs-lookup"><span data-stu-id="4c9b7-185">Possible values are:</span></span><br>
<span data-ttu-id="4c9b7-186">**Manuell** – Sie steuern die Anwendung von Patches auf einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-186">**Manual** - You  control the application of patches to a virtual machine.</span></span> <span data-ttu-id="4c9b7-187">Dazu müssen Sie Patches manuell innerhalb der VM anwenden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-187">You do this by applying patches manually inside the VM.</span></span> <span data-ttu-id="4c9b7-188">In diesem Modus werden automatische Updates deaktiviert. die -Eigenschaft WindowsConfiguration.enableAutomaticUpdates muss false sein.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-188">In this mode, automatic updates are disabled; the property WindowsConfiguration.enableAutomaticUpdates must be false</span></span><br>
<span data-ttu-id="4c9b7-189">**AutomaticByOS** – Der virtuelle Computer wird automatisch vom Betriebssystem aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-189">**AutomaticByOS** - The virtual machine will automatically be updated by the OS.</span></span> <span data-ttu-id="4c9b7-190">Die -Eigenschaft WindowsConfiguration.enableAutomaticUpdates muss true sein.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-190">The property WindowsConfiguration.enableAutomaticUpdates must be true.</span></span> <br >
<span data-ttu-id="4c9b7-191">**AutomaticByPlatform** – Der virtuelle Computer wird automatisch vom Betriebssystem aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-191">**AutomaticByPlatform** - the virtual machine will automatically updated by the OS.</span></span> <span data-ttu-id="4c9b7-192">Die Eigenschaften provisionVMAgent und WindowsConfiguration.enableAutomaticUpdates müssen true sein.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-192">The properties provisionVMAgent and WindowsConfiguration.enableAutomaticUpdates must be true</span></span>

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

### <span data-ttu-id="4c9b7-193">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="4c9b7-193">-ProvisionVMAgent</span></span>
<span data-ttu-id="4c9b7-194">Gibt an, dass für die Einstellungen die Installation des virtuellen Computer-Agents auf dem virtuellen Computer erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-194">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="4c9b7-195">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="4c9b7-195">-TimeZone</span></span>
<span data-ttu-id="4c9b7-196">Gibt die Zeitzone des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-196">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="4c9b7-197">z. B. \" Pacific Standard Time \" .</span><span class="sxs-lookup"><span data-stu-id="4c9b7-197">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="4c9b7-198">Mögliche Werte können [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) aus Zeitzonen angezeigt werden, die von [TimeZoneInfo.GetSystemTimeZones zurückgegeben werden.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="4c9b7-198">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="4c9b7-199">-VM</span><span class="sxs-lookup"><span data-stu-id="4c9b7-199">-VM</span></span>
<span data-ttu-id="4c9b7-200">Gibt das Objekt des lokalen virtuellen Computers an, für das Betriebssystemeigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-200">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="4c9b7-201">Zum Abrufen eines Virtuellen Computerobjekts verwenden Sie das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-201">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="4c9b7-202">Erstellen Sie ein Virtuelles Computerobjekt mithilfe des New-AzVMConfig-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-202">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="4c9b7-203">-Windows</span><span class="sxs-lookup"><span data-stu-id="4c9b7-203">-Windows</span></span>
<span data-ttu-id="4c9b7-204">Gibt an, dass der Typ des Betriebssystems Windows ist.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-204">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="4c9b7-205">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="4c9b7-205">-WinRMCertificateUrl</span></span>
<span data-ttu-id="4c9b7-206">Gibt den URI eines WinRM-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-206">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="4c9b7-207">Dies muss in einem Schlüsseltresor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-207">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="4c9b7-208">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="4c9b7-208">-WinRMHttp</span></span>
<span data-ttu-id="4c9b7-209">Gibt an, dass dieses Betriebssystem HTTP WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-209">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="4c9b7-210">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="4c9b7-210">-WinRMHttps</span></span>
<span data-ttu-id="4c9b7-211">Gibt an, dass dieses Betriebssystem HTTPS WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-211">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="4c9b7-212">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9b7-212">CommonParameters</span></span>
<span data-ttu-id="4c9b7-213">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9b7-213">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9b7-214">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c9b7-214">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9b7-215">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4c9b7-215">INPUTS</span></span>

### <span data-ttu-id="4c9b7-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4c9b7-216">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4c9b7-217">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c9b7-217">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4c9b7-218">System.String</span><span class="sxs-lookup"><span data-stu-id="4c9b7-218">System.String</span></span>

### <span data-ttu-id="4c9b7-219">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="4c9b7-219">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4c9b7-220">System.Uri</span><span class="sxs-lookup"><span data-stu-id="4c9b7-220">System.Uri</span></span>

## <span data-ttu-id="4c9b7-221">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4c9b7-221">OUTPUTS</span></span>

### <span data-ttu-id="4c9b7-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4c9b7-222">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4c9b7-223">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4c9b7-223">NOTES</span></span>

## <span data-ttu-id="4c9b7-224">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4c9b7-224">RELATED LINKS</span></span>

[<span data-ttu-id="4c9b7-225">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="4c9b7-225">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="4c9b7-226">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="4c9b7-226">New-AzVMConfig</span></span>](./New-AzVMConfig.md)



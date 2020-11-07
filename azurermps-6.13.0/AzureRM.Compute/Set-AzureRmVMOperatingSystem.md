---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMOperatingSystem.md
ms.openlocfilehash: 804606f854ab3375d7a40d364d5af9c9179e8952
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662829"
---
# <span data-ttu-id="4db47-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4db47-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="4db47-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4db47-102">SYNOPSIS</span></span>
<span data-ttu-id="4db47-103">Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="4db47-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4db47-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4db47-104">SYNTAX</span></span>

### <span data-ttu-id="4db47-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="4db47-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db47-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="4db47-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db47-107">WindowsDisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="4db47-107">WindowsDisableVMAgent</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db47-108">WindowsDisableVMAgentWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="4db47-108">WindowsDisableVMAgentWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4db47-109">Linux</span><span class="sxs-lookup"><span data-stu-id="4db47-109">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4db47-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4db47-110">DESCRIPTION</span></span>
<span data-ttu-id="4db47-111">Das Cmdlet " **Set-AzureRmVMOperatingSystem** " legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="4db47-111">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="4db47-112">Sie können Anmeldeinformationen, Computername und Typ des Betriebssystems angeben.</span><span class="sxs-lookup"><span data-stu-id="4db47-112">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="4db47-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4db47-113">EXAMPLES</span></span>

### <span data-ttu-id="4db47-114">Beispiel 1: Einrichten von Betriebssystemeigenschaften für eine neue virtuelle Maschine</span><span class="sxs-lookup"><span data-stu-id="4db47-114">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="4db47-115">Der erste Befehl wandelt ein Kennwort in eine sichere Zeichenfolge um und speichert es dann in der $SecurePassword-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4db47-115">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="4db47-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="4db47-116">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>
<span data-ttu-id="4db47-117">Mit dem zweiten Befehl werden die Anmeldeinformationen für den Benutzer FullerP und das in $SecurePassword gespeicherte Kennwort erstellt, und die Anmeldeinformationen werden dann in der $Credential Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4db47-117">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="4db47-118">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="4db47-118">For more information, type `Get-Help New-Object`.</span></span>
<span data-ttu-id="4db47-119">Der dritte Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="4db47-119">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="4db47-120">Der vierte Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="4db47-120">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="4db47-121">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="4db47-121">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="4db47-122">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4db47-122">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="4db47-123">In den nächsten vier Befehlen werden Variablenwerte zugewiesen, die Sie im folgenden Befehl verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4db47-123">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="4db47-124">Da Sie diese Zeichenfolgen direkt im Befehl " **Satz-AzureRmVMOperatingSystem** " angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="4db47-124">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="4db47-125">Sie können jedoch einen solchen Ansatz in Skripten verwenden.</span><span class="sxs-lookup"><span data-stu-id="4db47-125">However, you might use an approach such as this in scripts.</span></span>
<span data-ttu-id="4db47-126">Mit dem letzten Befehl werden die Betriebssystemeigenschaften für den virtuellen Computer festgelegt, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4db47-126">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="4db47-127">Der Befehl verwendet die in $Credential gespeicherten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4db47-127">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="4db47-128">Der Befehl verwendet für einige Parameter in vorherigen Befehlen zugewiesene Variablen.</span><span class="sxs-lookup"><span data-stu-id="4db47-128">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="4db47-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="4db47-129">PARAMETERS</span></span>

### <span data-ttu-id="4db47-130">-Computername</span><span class="sxs-lookup"><span data-stu-id="4db47-130">-ComputerName</span></span>
<span data-ttu-id="4db47-131">Gibt den Namen des Computers an.</span><span class="sxs-lookup"><span data-stu-id="4db47-131">Specifies the name of the computer.</span></span>

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

### <span data-ttu-id="4db47-132">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="4db47-132">-Credential</span></span>
<span data-ttu-id="4db47-133">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4db47-133">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="4db47-134">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4db47-134">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="4db47-135">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="4db47-135">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="4db47-136">-CustomData</span><span class="sxs-lookup"><span data-stu-id="4db47-136">-CustomData</span></span>
<span data-ttu-id="4db47-137">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="4db47-137">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="4db47-138">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="4db47-138">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="4db47-139">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="4db47-139">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="4db47-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db47-140">-DefaultProfile</span></span>
<span data-ttu-id="4db47-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4db47-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4db47-142">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="4db47-142">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="4db47-143">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4db47-143">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="4db47-144">-DisableVMAgent</span><span class="sxs-lookup"><span data-stu-id="4db47-144">-DisableVMAgent</span></span>
<span data-ttu-id="4db47-145">Bereitstellen des VM-Agents deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4db47-145">Disable Provision VM Agent.</span></span>

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

### <span data-ttu-id="4db47-146">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="4db47-146">-EnableAutoUpdate</span></span>
<span data-ttu-id="4db47-147">Gibt an, dass dieses Cmdlet die automatische Aktualisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4db47-147">Indicates that this cmdlet enables auto update.</span></span>

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

### <span data-ttu-id="4db47-148">-Linux</span><span class="sxs-lookup"><span data-stu-id="4db47-148">-Linux</span></span>
<span data-ttu-id="4db47-149">Gibt an, dass der Typ des Betriebssystems Linux ist.</span><span class="sxs-lookup"><span data-stu-id="4db47-149">Indicates that the type of operating system is Linux.</span></span>

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

### <span data-ttu-id="4db47-150">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="4db47-150">-ProvisionVMAgent</span></span>
<span data-ttu-id="4db47-151">Gibt an, dass für die Einstellungen der Virtual Machine-Agent auf dem virtuellen Computer installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4db47-151">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

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

### <span data-ttu-id="4db47-152">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="4db47-152">-TimeZone</span></span>
<span data-ttu-id="4db47-153">Gibt die Zeitzone für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="4db47-153">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="4db47-154">-VM</span><span class="sxs-lookup"><span data-stu-id="4db47-154">-VM</span></span>
<span data-ttu-id="4db47-155">Gibt das Objekt des lokalen virtuellen Computers an, auf dem Betriebssystemeigenschaften festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4db47-155">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="4db47-156">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4db47-156">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="4db47-157">Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des New-AzureRmVMConfig-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4db47-157">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

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

### <span data-ttu-id="4db47-158">-Windows</span><span class="sxs-lookup"><span data-stu-id="4db47-158">-Windows</span></span>
<span data-ttu-id="4db47-159">Gibt an, dass der Typ des Betriebssystems Windows ist.</span><span class="sxs-lookup"><span data-stu-id="4db47-159">Indicates that the type of operating system is Windows.</span></span>

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

### <span data-ttu-id="4db47-160">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="4db47-160">-WinRMCertificateUrl</span></span>
<span data-ttu-id="4db47-161">Gibt den URI eines WinRM-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="4db47-161">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="4db47-162">Dieser muss in einem schlüsseltresor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4db47-162">This needs to be stored in a Key Vault.</span></span>

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

### <span data-ttu-id="4db47-163">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="4db47-163">-WinRMHttp</span></span>
<span data-ttu-id="4db47-164">Gibt an, dass dieses Betriebssystem http WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="4db47-164">Indicates that this operating system uses HTTP WinRM.</span></span>

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

### <span data-ttu-id="4db47-165">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="4db47-165">-WinRMHttps</span></span>
<span data-ttu-id="4db47-166">Gibt an, dass dieses Betriebssystem HTTPS WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="4db47-166">Indicates that this operating system uses HTTPS WinRM.</span></span>

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

### <span data-ttu-id="4db47-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db47-167">CommonParameters</span></span>
<span data-ttu-id="4db47-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4db47-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db47-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4db47-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db47-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4db47-170">INPUTS</span></span>

### <span data-ttu-id="4db47-171">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4db47-171">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="4db47-172">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="4db47-172">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4db47-173">System. String</span><span class="sxs-lookup"><span data-stu-id="4db47-173">System.String</span></span>

### <span data-ttu-id="4db47-174">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4db47-174">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="4db47-175">System. Uri</span><span class="sxs-lookup"><span data-stu-id="4db47-175">System.Uri</span></span>

## <span data-ttu-id="4db47-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4db47-176">OUTPUTS</span></span>

### <span data-ttu-id="4db47-177">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4db47-177">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4db47-178">Notizen</span><span class="sxs-lookup"><span data-stu-id="4db47-178">NOTES</span></span>

## <span data-ttu-id="4db47-179">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4db47-179">RELATED LINKS</span></span>

[<span data-ttu-id="4db47-180">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4db47-180">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4db47-181">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="4db47-181">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)



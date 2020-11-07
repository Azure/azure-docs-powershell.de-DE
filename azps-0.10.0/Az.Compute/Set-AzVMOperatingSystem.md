---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 874045a510c8ab87143e25994fd5f15d5be7e741
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844204"
---
# <span data-ttu-id="ff096-101">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ff096-101">Set-AzVMOperatingSystem</span></span>

## <span data-ttu-id="ff096-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ff096-102">SYNOPSIS</span></span>
<span data-ttu-id="ff096-103">Legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ff096-103">Sets operating system properties for a virtual machine.</span></span>

## <span data-ttu-id="ff096-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff096-104">SYNTAX</span></span>

### <span data-ttu-id="ff096-105">Windows (Standard)</span><span class="sxs-lookup"><span data-stu-id="ff096-105">Windows (Default)</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff096-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ff096-106">WindowsWinRmHttps</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff096-107">Linux</span><span class="sxs-lookup"><span data-stu-id="ff096-107">Linux</span></span>
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff096-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff096-108">DESCRIPTION</span></span>
<span data-ttu-id="ff096-109">Das Cmdlet " **Set-AzVMOperatingSystem** " legt die Betriebssystemeigenschaften für einen virtuellen Computer fest.</span><span class="sxs-lookup"><span data-stu-id="ff096-109">The **Set-AzVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="ff096-110">Sie können Anmeldeinformationen, Computername und Typ des Betriebssystems angeben.</span><span class="sxs-lookup"><span data-stu-id="ff096-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="ff096-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ff096-111">EXAMPLES</span></span>

### <span data-ttu-id="ff096-112">Beispiel 1: Einrichten von Betriebssystemeigenschaften für eine neue virtuelle Maschine</span><span class="sxs-lookup"><span data-stu-id="ff096-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="ff096-113">Der erste Befehl wandelt ein Kennwort in eine sichere Zeichenfolge um und speichert es dann in der $SecurePassword-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff096-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="ff096-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ff096-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="ff096-115">Mit dem zweiten Befehl werden die Anmeldeinformationen für den Benutzer FullerP und das in $SecurePassword gespeicherte Kennwort erstellt, und die Anmeldeinformationen werden dann in der $Credential Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ff096-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="ff096-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="ff096-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="ff096-117">Der dritte Befehl ruft den Verfügbarkeits Satz mit dem Namen AvailablitySet03 in der Ressourcengruppe mit dem Namen ResourceGroup11 ab und speichert dieses Objekt dann in der $AvailabilitySet Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff096-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="ff096-118">Der vierte Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff096-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ff096-119">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="ff096-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ff096-120">Der virtuelle Computer gehört zum verfügbaren Verfügbarkeits Satz, der in $AvailabilitySet gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ff096-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="ff096-121">In den nächsten vier Befehlen werden Variablenwerte zugewiesen, die Sie im folgenden Befehl verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ff096-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="ff096-122">Da Sie diese Zeichenfolgen direkt im Befehl " **Satz-AzVMOperatingSystem** " angeben können, wird dieser Ansatz nur zur Lesbarkeit verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff096-122">Because you could specify these strings directly in the **Set-AzVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="ff096-123">Sie können jedoch einen solchen Ansatz in Skripten verwenden.</span><span class="sxs-lookup"><span data-stu-id="ff096-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="ff096-124">Mit dem letzten Befehl werden die Betriebssystemeigenschaften für den virtuellen Computer festgelegt, der in $VirtualMachine gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ff096-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ff096-125">Der Befehl verwendet die in $Credential gespeicherten Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="ff096-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="ff096-126">Der Befehl verwendet für einige Parameter in vorherigen Befehlen zugewiesene Variablen.</span><span class="sxs-lookup"><span data-stu-id="ff096-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="ff096-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff096-127">PARAMETERS</span></span>

### <span data-ttu-id="ff096-128">-Computername</span><span class="sxs-lookup"><span data-stu-id="ff096-128">-ComputerName</span></span>
<span data-ttu-id="ff096-129">Gibt den Namen des Computers an.</span><span class="sxs-lookup"><span data-stu-id="ff096-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-130">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="ff096-130">-Credential</span></span>
<span data-ttu-id="ff096-131">Gibt den Benutzernamen und das Kennwort für den virtuellen Computer als **PSCredential** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ff096-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ff096-132">Verwenden Sie zum Abrufen von Anmeldeinformationen das Get-Credential-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff096-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ff096-133">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ff096-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ff096-134">-CustomData</span></span>
<span data-ttu-id="ff096-135">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="ff096-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ff096-136">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ff096-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ff096-137">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="ff096-137">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff096-138">-DefaultProfile</span></span>
<span data-ttu-id="ff096-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ff096-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff096-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ff096-141">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ff096-141">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ff096-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="ff096-143">Gibt an, dass dieses Cmdlet die automatische Aktualisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ff096-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="ff096-144">-Linux</span></span>
<span data-ttu-id="ff096-145">Gibt an, dass der Typ des Betriebssystems Linux ist.</span><span class="sxs-lookup"><span data-stu-id="ff096-145">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ff096-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="ff096-147">Gibt an, dass für die Einstellungen der Virtual Machine-Agent auf dem virtuellen Computer installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="ff096-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ff096-148">-TimeZone</span></span>
<span data-ttu-id="ff096-149">Gibt die Zeitzone für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ff096-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-150">-VM</span><span class="sxs-lookup"><span data-stu-id="ff096-150">-VM</span></span>
<span data-ttu-id="ff096-151">Gibt das Objekt des lokalen virtuellen Computers an, auf dem Betriebssystemeigenschaften festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ff096-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="ff096-152">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ff096-152">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ff096-153">Erstellen Sie ein Objekt für einen virtuellen Computer mithilfe des New-AzVMConfig-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ff096-153">Create a virtual machine object by using the New-AzVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="ff096-154">-Windows</span></span>
<span data-ttu-id="ff096-155">Gibt an, dass der Typ des Betriebssystems Windows ist.</span><span class="sxs-lookup"><span data-stu-id="ff096-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ff096-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="ff096-157">Gibt den URI eines WinRM-Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="ff096-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="ff096-158">Dieser muss in einem schlüsseltresor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="ff096-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ff096-159">-WinRMHttp</span></span>
<span data-ttu-id="ff096-160">Gibt an, dass dieses Betriebssystem http WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff096-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ff096-161">-WinRMHttps</span></span>
<span data-ttu-id="ff096-162">Gibt an, dass dieses Betriebssystem HTTPS WinRM verwendet.</span><span class="sxs-lookup"><span data-stu-id="ff096-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff096-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff096-163">CommonParameters</span></span>
<span data-ttu-id="ff096-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff096-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff096-165">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff096-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff096-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ff096-166">INPUTS</span></span>

### <span data-ttu-id="ff096-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ff096-167">PSVirtualMachine</span></span>
<span data-ttu-id="ff096-168">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ff096-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ff096-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ff096-169">OUTPUTS</span></span>

### <span data-ttu-id="ff096-170">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ff096-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ff096-171">Notizen</span><span class="sxs-lookup"><span data-stu-id="ff096-171">NOTES</span></span>

## <span data-ttu-id="ff096-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ff096-172">RELATED LINKS</span></span>

[<span data-ttu-id="ff096-173">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff096-173">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ff096-174">Neu – AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ff096-174">New-AzVMConfig</span></span>](./New-AzVMConfig.md)



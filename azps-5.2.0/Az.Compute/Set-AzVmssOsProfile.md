---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366987"
---
# <span data-ttu-id="7e4d5-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="7e4d5-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="7e4d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e4d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4d5-103">Legt die Profileigenschaften des Betriebssystems VMSS fest.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="7e4d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e4d5-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4d5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e4d5-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4d5-106">Das **Cmdlet "Set-AzVmssOsProfile"** legt die Profileigenschaften des Betriebssystems "Virtual Machine Scale Set" fest.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="7e4d5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7e4d5-107">EXAMPLES</span></span>

### <span data-ttu-id="7e4d5-108">Beispiel 1: Festlegen der Betriebssystemprofileigenschaften für eine VMSS</span><span class="sxs-lookup"><span data-stu-id="7e4d5-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="7e4d5-109">Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zu den VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="7e4d5-110">Der Befehl legt das Computernamenpräfix für alle Instanzen des virtuellen Computers in VMSS auf "Test" fest und stellt den Benutzernamen und das Kennwort des Administrators zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="7e4d5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e4d5-111">PARAMETERS</span></span>

### <span data-ttu-id="7e4d5-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="7e4d5-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="7e4d5-113">Gibt ein unbeaufsichtigtes Inhaltsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="7e4d5-114">Sie können die Add-AzVMAdditionalUnattendContent zum Erstellen des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="7e4d5-115">-AdminPassword</span></span>
<span data-ttu-id="7e4d5-116">Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in vmSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="7e4d5-117">-AdminUsername</span></span>
<span data-ttu-id="7e4d5-118">Gibt den Administratorkontonamen an, der für alle Instanzen des virtuellen Computers in vmSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="7e4d5-119">**Einschränkung nur für Windows:** Kann nicht enden mit \" .\"</span><span class="sxs-lookup"><span data-stu-id="7e4d5-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="7e4d5-120">**Unzulässige Werte:** \" \"Administrator, \" \" \" \" Administrator, Benutzer, \" \" \" Benutzer1, \" Test, \" \" Benutzer2, \" \" Test1, \" \" Benutzer3, \" \" Administrator1, \" \" 1, \" 123 \" , a , \" \" \" Actuser, \" \" \" Adm, \" \" \" Admin2, \" Aspnet, \" \" Sicherung, \" \" Konsole, \" \" David, \" \" Gast, \" \" John, \" \" Besitzer, \" \" Stamm, \" \" Server, \" \" SQL, \" \" Support, \" support_388945a0 , sys \" , \" \" \" \" Test2, \" \" Test3, \" \" Benutzer4, \" \" Benutzer5.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="7e4d5-121">**Mindestlänge (Linux):** 1 Zeichen</span><span class="sxs-lookup"><span data-stu-id="7e4d5-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="7e4d5-122">**Maximale Länge (Linux):** 64 Zeichen</span><span class="sxs-lookup"><span data-stu-id="7e4d5-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="7e4d5-123">**Max. Länge (Windows):** 20 Zeichen</span><span class="sxs-lookup"><span data-stu-id="7e4d5-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="7e4d5-124">Informationen zum Stammzugriff auf die Linux VM finden Sie unter "Verwenden von Stammberechtigungen [auf virtuellen Linux-Computern in Azure".](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="7e4d5-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="7e4d5-125">Eine Liste der integrierten Systembenutzer unter Linux, die in diesem Feld nicht verwendet werden sollten, finden Sie unter Auswählen von Benutzernamen für [Linux in Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="7e4d5-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="7e4d5-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="7e4d5-127">Gibt das Computernamenpräfix für alle Instanzen virtueller Computer in der VMSS an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="7e4d5-128">Computernamen müssen 1 bis 15 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-128">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="7e4d5-129">-CustomData</span></span>
<span data-ttu-id="7e4d5-130">Gibt eine base-64-codierte Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="7e4d5-131">Dies wird in ein Binärarray decodiert, das als Datei auf dem virtuellen Computer gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="7e4d5-132">Die maximale Länge des Binärarrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="7e4d5-133">Informationen zur Verwendung von cloud-init für Ihre VM finden Sie unter "Verwenden von [cloud-init zum Anpassen einer Linux-VM während der Erstellung".](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="7e4d5-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="7e4d5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4d5-134">-DefaultProfile</span></span>
<span data-ttu-id="7e4d5-135">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e4d5-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="7e4d5-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="7e4d5-137">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-137">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="7e4d5-138">-Listener</span></span>
<span data-ttu-id="7e4d5-139">Gibt die Windows Remote Management (WinRM)-Listener an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="7e4d5-140">Dies ermöglicht Remote-Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="7e4d5-141">Sie können das cmdlet Add-AzVmssWinRMListener zum Erstellen des Listeners verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="7e4d5-142">-PublicKey</span></span>
<span data-ttu-id="7e4d5-143">Gibt das öffentliche Schlüsselobjekt der Secure Shell (SSH) an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="7e4d5-144">Sie können das cmdlet Add-AzVMSshPublicKey zum Erstellen des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="7e4d5-145">-Secret</span></span>
<span data-ttu-id="7e4d5-146">Gibt das geheime Objekt an, das die Zertifikatverweise enthält, die auf dem virtuellen Computer platzieren werden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="7e4d5-147">Sie können das cmdlet Add-AzVmssSecret zum Erstellen des geheimen Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="7e4d5-148">-TimeZone</span></span>
<span data-ttu-id="7e4d5-149">Gibt die Zeitzone des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="7e4d5-150">z. B. \" Pacific Standard \" Time.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="7e4d5-151">Mögliche Werte können als [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) zeitzonen verwendet werden, die von ["TimeZoneInfo.GetSystemTimeZones" zurückgegeben werden.](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)</span><span class="sxs-lookup"><span data-stu-id="7e4d5-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7e4d5-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7e4d5-153">Gibt das "VMSS"-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="7e4d5-154">Sie können das cmdlet New-AzVmssConfig zum Erstellen des Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="7e4d5-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="7e4d5-156">Gibt an, ob die virtuellen Computer in VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="7e4d5-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="7e4d5-158">Gibt an, ob der Agent für virtuelle Computer auf den virtuellen Computern auf der VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e4d5-159">-Confirm</span></span>
<span data-ttu-id="7e4d5-160">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-161">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7e4d5-161">-WhatIf</span></span>
<span data-ttu-id="7e4d5-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e4d5-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e4d5-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4d5-164">CommonParameters</span></span>
<span data-ttu-id="7e4d5-165">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e4d5-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4d5-166">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e4d5-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4d5-167">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7e4d5-167">INPUTS</span></span>

### <span data-ttu-id="7e4d5-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7e4d5-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7e4d5-169">System.String</span><span class="sxs-lookup"><span data-stu-id="7e4d5-169">System.String</span></span>

### <span data-ttu-id="7e4d5-170">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="7e4d5-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7e4d5-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span><span class="sxs-lookup"><span data-stu-id="7e4d5-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="7e4d5-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span><span class="sxs-lookup"><span data-stu-id="7e4d5-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="7e4d5-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span><span class="sxs-lookup"><span data-stu-id="7e4d5-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="7e4d5-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span><span class="sxs-lookup"><span data-stu-id="7e4d5-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="7e4d5-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7e4d5-175">OUTPUTS</span></span>

### <span data-ttu-id="7e4d5-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7e4d5-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7e4d5-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7e4d5-177">NOTES</span></span>

## <span data-ttu-id="7e4d5-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7e4d5-178">RELATED LINKS</span></span>

[<span data-ttu-id="7e4d5-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="7e4d5-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="7e4d5-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="7e4d5-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="7e4d5-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="7e4d5-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="7e4d5-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="7e4d5-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="7e4d5-183">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7e4d5-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



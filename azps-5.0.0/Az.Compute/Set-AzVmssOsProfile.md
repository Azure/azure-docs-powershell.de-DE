---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296470"
---
# <span data-ttu-id="f0f54-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="f0f54-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="f0f54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0f54-102">SYNOPSIS</span></span>
<span data-ttu-id="f0f54-103">Legt die Profileigenschaften des VMSS-Betriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="f0f54-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="f0f54-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0f54-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0f54-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0f54-105">DESCRIPTION</span></span>
<span data-ttu-id="f0f54-106">Mit dem Cmdlet **Set-AzVmssOsProfile** werden die Eigenschaften des virtuellen Computers für das Betriebssystem festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f0f54-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="f0f54-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0f54-107">EXAMPLES</span></span>

### <span data-ttu-id="f0f54-108">Beispiel 1: Einrichten der Profileigenschaften des Betriebssystems für ein VMSS</span><span class="sxs-lookup"><span data-stu-id="f0f54-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="f0f54-109">Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="f0f54-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="f0f54-110">Der Befehl legt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS fest, um den Benutzernamen und das Kennwort des Administrators zu testen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="f0f54-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0f54-111">PARAMETERS</span></span>

### <span data-ttu-id="f0f54-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="f0f54-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="f0f54-113">Gibt ein unbeaufsichtigtes Inhaltsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="f0f54-114">Sie können die Add-AzVMAdditionalUnattendContent verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="f0f54-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="f0f54-115">-AdminPassword</span></span>
<span data-ttu-id="f0f54-116">Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in der VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0f54-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="f0f54-117">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="f0f54-117">-AdminUsername</span></span>
<span data-ttu-id="f0f54-118">Gibt den Namen des Administratorkontos an, das für alle Instanzen des virtuellen Computers in VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0f54-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="f0f54-119">**Nur Windows-Einschränkungen:** Kann nicht beendet werden \" .\"</span><span class="sxs-lookup"><span data-stu-id="f0f54-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="f0f54-120">Nicht **zulässige Werte:** \" Administrator, Administrator \" \" \" , \" Benutzer \" , \" Benutzer1 \" , \" Test \" , \" User2 \" , \" test1 \" , \" user3 \" , \" Admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" ACTUser \" , \" adm \" , \" admin2 \" , \" ASPNET \" , \" Backup \" , \" Console \" , \" David \" , \" Guest \" , \" John \" , \" Owner \" , \" root \" , \" Server \" , \" SQL \" , \" Support \" , \" Support_388945a0 \" , \" sys \" , \" test2 \" , \" test3 \" , \" benutzer4 \" , \" user5 \" .</span><span class="sxs-lookup"><span data-stu-id="f0f54-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="f0f54-121">**Minimale Länge (Linux):** 1 Zeichen</span><span class="sxs-lookup"><span data-stu-id="f0f54-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="f0f54-122">**Max-length (Linux):** 64 Zeichen</span><span class="sxs-lookup"><span data-stu-id="f0f54-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="f0f54-123">**Max-length (Windows):** 20 Zeichen</span><span class="sxs-lookup"><span data-stu-id="f0f54-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="f0f54-124">Informationen zum root-Zugriff auf die Linux-VM finden Sie unter [Verwenden von root-Privilegien auf virtuellen Linux-Computern in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="f0f54-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="f0f54-125">Eine Liste der integrierten Systembenutzer unter Linux, die nicht in diesem Feld verwendet werden sollten, finden Sie unter [Auswählen von Benutzernamen für Linux auf Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="f0f54-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="f0f54-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="f0f54-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="f0f54-127">Gibt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="f0f54-128">Computer Namen müssen 1 bis 15 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f0f54-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="f0f54-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="f0f54-129">-CustomData</span></span>
<span data-ttu-id="f0f54-130">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="f0f54-131">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="f0f54-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="f0f54-132">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="f0f54-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="f0f54-133">Informationen zum Verwenden von Cloud-init für Ihre VM finden Sie unter [Verwenden von Cloud-init zum Anpassen einer Linux-VM während der Erstellung](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="f0f54-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="f0f54-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0f54-134">-DefaultProfile</span></span>
<span data-ttu-id="f0f54-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0f54-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0f54-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="f0f54-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="f0f54-137">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f0f54-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="f0f54-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="f0f54-138">-Listener</span></span>
<span data-ttu-id="f0f54-139">Gibt die Windows-Remote Verwaltung (WinRM)-Listener an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="f0f54-140">Dies ermöglicht die Remote-Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f0f54-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="f0f54-141">Sie können das Add-AzVmssWinRMListener-Cmdlet verwenden, um den Listener zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="f0f54-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="f0f54-142">-PublicKey</span></span>
<span data-ttu-id="f0f54-143">Gibt das Secure Shell (SSH)-Objekt für öffentliche Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="f0f54-144">Sie können das Add-AzVMSshPublicKey-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="f0f54-145">-Secret</span><span class="sxs-lookup"><span data-stu-id="f0f54-145">-Secret</span></span>
<span data-ttu-id="f0f54-146">Gibt das Secrets-Objekt an, das die Zertifikat Verweise enthält, die auf dem virtuellen Computer platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="f0f54-147">Sie können das Add-AzVmssSecret-Cmdlet verwenden, um das Secrets-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="f0f54-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="f0f54-148">-TimeZone</span></span>
<span data-ttu-id="f0f54-149">Gibt die Zeitzone des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="f0f54-150">z.b. \" Pacific Normalzeit \" .</span><span class="sxs-lookup"><span data-stu-id="f0f54-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="f0f54-151">Mögliche Werte können [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) -Wert aus Zeitzonen sein, die von [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0f54-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="f0f54-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0f54-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f0f54-153">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f0f54-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="f0f54-154">Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="f0f54-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="f0f54-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="f0f54-156">Gibt an, ob die virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="f0f54-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="f0f54-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="f0f54-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="f0f54-158">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f0f54-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="f0f54-159">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f0f54-159">-Confirm</span></span>
<span data-ttu-id="f0f54-160">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0f54-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0f54-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0f54-161">-WhatIf</span></span>
<span data-ttu-id="f0f54-162">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f0f54-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0f54-163">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0f54-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0f54-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0f54-164">CommonParameters</span></span>
<span data-ttu-id="f0f54-165">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0f54-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0f54-166">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0f54-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0f54-167">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0f54-167">INPUTS</span></span>

### <span data-ttu-id="f0f54-168">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0f54-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f0f54-169">System. String</span><span class="sxs-lookup"><span data-stu-id="f0f54-169">System.String</span></span>

### <span data-ttu-id="f0f54-170">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0f54-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f0f54-171">Microsoft. Azure. Management. Compute. Models. AdditionalUnattendContent []</span><span class="sxs-lookup"><span data-stu-id="f0f54-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="f0f54-172">Microsoft. Azure. Management. Compute. Models. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="f0f54-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="f0f54-173">Microsoft. Azure. Management. Compute. Models. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="f0f54-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="f0f54-174">Microsoft. Azure. Management. Compute. Models. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="f0f54-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="f0f54-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0f54-175">OUTPUTS</span></span>

### <span data-ttu-id="f0f54-176">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0f54-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f0f54-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0f54-177">NOTES</span></span>

## <span data-ttu-id="f0f54-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0f54-178">RELATED LINKS</span></span>

[<span data-ttu-id="f0f54-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="f0f54-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="f0f54-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="f0f54-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="f0f54-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="f0f54-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="f0f54-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="f0f54-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="f0f54-183">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f0f54-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



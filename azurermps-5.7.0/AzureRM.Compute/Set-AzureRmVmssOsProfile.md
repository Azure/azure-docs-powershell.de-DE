---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664673"
---
# <span data-ttu-id="0883e-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="0883e-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="0883e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0883e-102">SYNOPSIS</span></span>
<span data-ttu-id="0883e-103">Legt die Profileigenschaften des VMSS-Betriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="0883e-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0883e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0883e-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0883e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0883e-105">DESCRIPTION</span></span>
<span data-ttu-id="0883e-106">Mit dem Cmdlet **Set-AzureRmVmssOsProfile** werden die Eigenschaften des virtuellen Computers für das Betriebssystem festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0883e-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="0883e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0883e-107">EXAMPLES</span></span>

### <span data-ttu-id="0883e-108">Beispiel 1: Einrichten der Profileigenschaften des Betriebssystems für ein VMSS</span><span class="sxs-lookup"><span data-stu-id="0883e-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="0883e-109">Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="0883e-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="0883e-110">Der Befehl legt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS fest, um den Benutzernamen und das Kennwort des Administrators zu testen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0883e-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="0883e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0883e-111">PARAMETERS</span></span>

### <span data-ttu-id="0883e-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="0883e-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="0883e-113">Gibt ein unbeaufsichtigtes Inhaltsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="0883e-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="0883e-114">Sie können die Add-AzureRmVMAdditionalUnattendContent verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0883e-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="0883e-115">-AdminPassword</span></span>
<span data-ttu-id="0883e-116">Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in der VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0883e-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-117">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="0883e-117">-AdminUsername</span></span>
<span data-ttu-id="0883e-118">Gibt den Namen des Administratorkontos an, das für alle Instanzen des virtuellen Computers in VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0883e-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0883e-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="0883e-120">Gibt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="0883e-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="0883e-121">Computer Namen müssen 1 bis 15 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="0883e-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="0883e-122">-CustomData</span></span>
<span data-ttu-id="0883e-123">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="0883e-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="0883e-124">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0883e-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="0883e-125">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="0883e-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="0883e-126">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="0883e-126">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="0883e-127">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0883e-127">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-128">-Listener</span><span class="sxs-lookup"><span data-stu-id="0883e-128">-Listener</span></span>
<span data-ttu-id="0883e-129">Gibt die Windows-Remote Verwaltung (WinRM)-Listener an.</span><span class="sxs-lookup"><span data-stu-id="0883e-129">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="0883e-130">Dies ermöglicht die Remote-Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0883e-130">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="0883e-131">Sie können das Add-AzureRmVmssWinRMListener-Cmdlet verwenden, um den Listener zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0883e-131">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-132">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="0883e-132">-PublicKey</span></span>
<span data-ttu-id="0883e-133">Gibt das Secure Shell (SSH)-Objekt für öffentliche Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="0883e-133">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="0883e-134">Sie können das Add-AzureRmVMSshPublicKey-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0883e-134">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-135">-Secret</span><span class="sxs-lookup"><span data-stu-id="0883e-135">-Secret</span></span>
<span data-ttu-id="0883e-136">Gibt das Secrets-Objekt an, das die Zertifikat Verweise enthält, die auf dem virtuellen Computer platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0883e-136">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="0883e-137">Sie können das Add-AzureRmVmssSecret-Cmdlet verwenden, um das Secrets-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0883e-137">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-138">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="0883e-138">-TimeZone</span></span>
<span data-ttu-id="0883e-139">Gibt die Zeitzone für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="0883e-139">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-140">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0883e-140">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0883e-141">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0883e-141">Specifies the VMSS object.</span></span>
<span data-ttu-id="0883e-142">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0883e-142">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-143">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="0883e-143">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="0883e-144">Gibt an, ob die virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="0883e-144">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-145">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="0883e-145">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="0883e-146">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0883e-146">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0883e-147">-Confirm</span></span>
<span data-ttu-id="0883e-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0883e-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0883e-149">-WhatIf</span></span>
<span data-ttu-id="0883e-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0883e-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0883e-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0883e-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0883e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0883e-152">CommonParameters</span></span>
<span data-ttu-id="0883e-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0883e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0883e-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0883e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0883e-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0883e-155">INPUTS</span></span>

### <span data-ttu-id="0883e-156">Keine</span><span class="sxs-lookup"><span data-stu-id="0883e-156">None</span></span>
<span data-ttu-id="0883e-157">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0883e-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0883e-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0883e-158">OUTPUTS</span></span>

### <span data-ttu-id="0883e-159">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0883e-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0883e-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="0883e-160">NOTES</span></span>

## <span data-ttu-id="0883e-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0883e-161">RELATED LINKS</span></span>

[<span data-ttu-id="0883e-162">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="0883e-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="0883e-163">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="0883e-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="0883e-164">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0883e-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="0883e-165">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="0883e-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="0883e-166">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0883e-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



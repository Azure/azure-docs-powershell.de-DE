---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844172"
---
# <span data-ttu-id="ab4e7-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="ab4e7-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="ab4e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ab4e7-103">Legt die Profileigenschaften des VMSS-Betriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="ab4e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab4e7-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab4e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab4e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ab4e7-106">Mit dem Cmdlet **Set-AzVmssOsProfile** werden die Eigenschaften des virtuellen Computers für das Betriebssystem festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="ab4e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab4e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ab4e7-108">Beispiel 1: Einrichten der Profileigenschaften des Betriebssystems für ein VMSS</span><span class="sxs-lookup"><span data-stu-id="ab4e7-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="ab4e7-109">Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="ab4e7-110">Der Befehl legt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS fest, um den Benutzernamen und das Kennwort des Administrators zu testen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="ab4e7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab4e7-111">PARAMETERS</span></span>

### <span data-ttu-id="ab4e7-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ab4e7-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="ab4e7-113">Gibt ein unbeaufsichtigtes Inhaltsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="ab4e7-114">Sie können die Add-AzVMAdditionalUnattendContent verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="ab4e7-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="ab4e7-115">-AdminPassword</span></span>
<span data-ttu-id="ab4e7-116">Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in der VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="ab4e7-117">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="ab4e7-117">-AdminUsername</span></span>
<span data-ttu-id="ab4e7-118">Gibt den Namen des Administratorkontos an, das für alle Instanzen des virtuellen Computers in VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="ab4e7-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ab4e7-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="ab4e7-120">Gibt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="ab4e7-121">Computer Namen müssen 1 bis 15 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="ab4e7-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ab4e7-122">-CustomData</span></span>
<span data-ttu-id="ab4e7-123">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ab4e7-124">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ab4e7-125">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ab4e7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab4e7-126">-DefaultProfile</span></span>
<span data-ttu-id="ab4e7-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab4e7-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ab4e7-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="ab4e7-129">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="ab4e7-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="ab4e7-130">-Listener</span></span>
<span data-ttu-id="ab4e7-131">Gibt die Windows-Remote Verwaltung (WinRM)-Listener an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="ab4e7-132">Dies ermöglicht die Remote-Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="ab4e7-133">Sie können das Add-AzVmssWinRMListener-Cmdlet verwenden, um den Listener zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="ab4e7-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="ab4e7-134">-PublicKey</span></span>
<span data-ttu-id="ab4e7-135">Gibt das Secure Shell (SSH)-Objekt für öffentliche Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="ab4e7-136">Sie können das Add-AzVMSshPublicKey-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="ab4e7-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="ab4e7-137">-Secret</span></span>
<span data-ttu-id="ab4e7-138">Gibt das Secrets-Objekt an, das die Zertifikat Verweise enthält, die auf dem virtuellen Computer platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="ab4e7-139">Sie können das Add-AzVmssSecret-Cmdlet verwenden, um das Secrets-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="ab4e7-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ab4e7-140">-TimeZone</span></span>
<span data-ttu-id="ab4e7-141">Gibt die Zeitzone für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="ab4e7-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ab4e7-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ab4e7-143">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="ab4e7-144">Sie können das New-AzVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab4e7-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="ab4e7-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="ab4e7-146">Gibt an, ob die virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="ab4e7-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ab4e7-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="ab4e7-148">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="ab4e7-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab4e7-149">-Confirm</span></span>
<span data-ttu-id="ab4e7-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab4e7-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab4e7-151">-WhatIf</span></span>
<span data-ttu-id="ab4e7-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab4e7-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab4e7-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab4e7-154">CommonParameters</span></span>
<span data-ttu-id="ab4e7-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab4e7-156">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab4e7-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab4e7-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab4e7-157">INPUTS</span></span>

### <span data-ttu-id="ab4e7-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ab4e7-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="ab4e7-159">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="ab4e7-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab4e7-160">OUTPUTS</span></span>

### <span data-ttu-id="ab4e7-161">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="ab4e7-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ab4e7-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab4e7-162">NOTES</span></span>

## <span data-ttu-id="ab4e7-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab4e7-163">RELATED LINKS</span></span>

[<span data-ttu-id="ab4e7-164">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="ab4e7-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="ab4e7-165">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="ab4e7-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="ab4e7-166">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ab4e7-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="ab4e7-167">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="ab4e7-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="ab4e7-168">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ab4e7-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)



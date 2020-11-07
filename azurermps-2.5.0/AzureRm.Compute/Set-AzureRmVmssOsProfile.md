---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssosprofile
schema: 2.0.0
ms.openlocfilehash: ff2b46c661640221326d50aa71c2659bd5672ab1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849363"
---
# <span data-ttu-id="0d2ce-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="0d2ce-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="0d2ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2ce-103">Legt die Profileigenschaften des VMSS-Betriebssystems fest.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d2ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d2ce-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d2ce-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="0d2ce-106">Mit dem Cmdlet **Set-AzureRmVmssOsProfile** werden die Eigenschaften des virtuellen Computers für das Betriebssystem festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="0d2ce-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="0d2ce-108">Beispiel 1: Einrichten der Profileigenschaften des Betriebssystems für ein VMSS</span><span class="sxs-lookup"><span data-stu-id="0d2ce-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="0d2ce-109">Mit diesem Befehl werden die Profileigenschaften des Betriebssystems für die virtuellen Computer festgelegt, die zum VMSS mit dem Namen ContosoVMSS gehören.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="0d2ce-110">Der Befehl legt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS fest, um den Benutzernamen und das Kennwort des Administrators zu testen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="0d2ce-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d2ce-111">PARAMETERS</span></span>

### <span data-ttu-id="0d2ce-112">-AdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="0d2ce-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="0d2ce-113">Gibt ein unbeaufsichtigtes Inhaltsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="0d2ce-114">Sie können die Add-AzureRmVMAdditionalUnattendContent verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="0d2ce-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="0d2ce-115">-AdminPassword</span></span>
<span data-ttu-id="0d2ce-116">Gibt das Administratorkennwort an, das für alle Instanzen des virtuellen Computers in der VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="0d2ce-117">-Nation aus AdminUsername</span><span class="sxs-lookup"><span data-stu-id="0d2ce-117">-AdminUsername</span></span>
<span data-ttu-id="0d2ce-118">Gibt den Namen des Administratorkontos an, das für alle Instanzen des virtuellen Computers in VMSS verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="0d2ce-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="0d2ce-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="0d2ce-120">Gibt das Präfix für den Computernamen für alle Instanzen des virtuellen Computers im VMSS an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="0d2ce-121">Computer Namen müssen 1 bis 15 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="0d2ce-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="0d2ce-122">-CustomData</span></span>
<span data-ttu-id="0d2ce-123">Gibt eine codierte Base-64-Zeichenfolge mit benutzerdefinierten Daten an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="0d2ce-124">Dies wird in einem binären Array dekodiert, das als Datei auf dem virtuellen Computer gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="0d2ce-125">Die maximale Länge des binären Arrays beträgt 65535 Bytes.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="0d2ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2ce-126">-DefaultProfile</span></span>
<span data-ttu-id="0d2ce-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d2ce-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="0d2ce-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="0d2ce-129">Gibt an, dass dieses Cmdlet die Kennwortauthentifizierung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="0d2ce-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="0d2ce-130">-Listener</span></span>
<span data-ttu-id="0d2ce-131">Gibt die Windows-Remote Verwaltung (WinRM)-Listener an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="0d2ce-132">Dies ermöglicht die Remote-Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="0d2ce-133">Sie können das Add-AzureRmVmssWinRMListener-Cmdlet verwenden, um den Listener zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="0d2ce-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="0d2ce-134">-PublicKey</span></span>
<span data-ttu-id="0d2ce-135">Gibt das Secure Shell (SSH)-Objekt für öffentliche Schlüssel an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="0d2ce-136">Sie können das Add-AzureRmVMSshPublicKey-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0d2ce-137">-Secret</span><span class="sxs-lookup"><span data-stu-id="0d2ce-137">-Secret</span></span>
<span data-ttu-id="0d2ce-138">Gibt das Secrets-Objekt an, das die Zertifikat Verweise enthält, die auf dem virtuellen Computer platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="0d2ce-139">Sie können das Add-AzureRmVmssSecret-Cmdlet verwenden, um das Secrets-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="0d2ce-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="0d2ce-140">-TimeZone</span></span>
<span data-ttu-id="0d2ce-141">Gibt die Zeitzone für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="0d2ce-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0d2ce-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0d2ce-143">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="0d2ce-144">Sie können das New-AzureRmVmssConfig-Cmdlet verwenden, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0d2ce-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="0d2ce-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="0d2ce-146">Gibt an, ob die virtuellen Computer im VMSS für automatische Updates aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="0d2ce-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="0d2ce-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="0d2ce-148">Gibt an, ob der Virtual Machine-Agent auf den virtuellen Computern im VMSS bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="0d2ce-149">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d2ce-149">-Confirm</span></span>
<span data-ttu-id="0d2ce-150">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d2ce-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d2ce-151">-WhatIf</span></span>
<span data-ttu-id="0d2ce-152">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d2ce-153">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d2ce-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2ce-154">CommonParameters</span></span>
<span data-ttu-id="0d2ce-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2ce-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2ce-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2ce-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d2ce-157">INPUTS</span></span>

### <span data-ttu-id="0d2ce-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0d2ce-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="0d2ce-159">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="0d2ce-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d2ce-160">OUTPUTS</span></span>

### <span data-ttu-id="0d2ce-161">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0d2ce-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0d2ce-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d2ce-162">NOTES</span></span>

## <span data-ttu-id="0d2ce-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d2ce-163">RELATED LINKS</span></span>

[<span data-ttu-id="0d2ce-164">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="0d2ce-164">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="0d2ce-165">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="0d2ce-165">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="0d2ce-166">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0d2ce-166">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="0d2ce-167">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="0d2ce-167">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="0d2ce-168">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0d2ce-168">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)



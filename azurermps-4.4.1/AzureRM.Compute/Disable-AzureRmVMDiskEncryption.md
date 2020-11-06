---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 2227193923b014f69da0ddb60ae9ee00bdc14b6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505197"
---
# <span data-ttu-id="f95ed-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f95ed-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="f95ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f95ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f95ed-103">Deaktiviert die Verschlüsselung auf einem virtuellen IaaS-Computer.</span><span class="sxs-lookup"><span data-stu-id="f95ed-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f95ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f95ed-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f95ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f95ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f95ed-106">Das Cmdlet **Disable-AzureRmVMDiskEncryption** deaktiviert die Verschlüsselung auf einem virtuellen Computer mit einem Dienst (Infrastructure as a Service, IaaS).</span><span class="sxs-lookup"><span data-stu-id="f95ed-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="f95ed-107">Dieses Cmdlet wird nur auf virtuellen Windows-Computern und nicht auf virtuellen Linux-Computern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f95ed-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="f95ed-108">Dieses Cmdlet installiert eine Erweiterung auf dem virtuellen Computer, um die Verschlüsselung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="f95ed-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="f95ed-109">Wenn der Parameter *Name* nicht angegeben ist, wird eine Erweiterung mit dem Standardnamen "AzureDiskEncryption für Windows VMS" erstellt.</span><span class="sxs-lookup"><span data-stu-id="f95ed-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="f95ed-110">Vorsicht: Dieses Cmdlet startet den virtuellen Computer neu.</span><span class="sxs-lookup"><span data-stu-id="f95ed-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="f95ed-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f95ed-111">EXAMPLES</span></span>

### <span data-ttu-id="f95ed-112">Beispiel 1: Deaktivieren der Verschlüsselung für alle Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="f95ed-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="f95ed-113">Mit diesem Befehl wird die Verschlüsselung für Volumes des Typs alle für den virtuellen Computer mit dem Namen VM002 deaktiviert, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="f95ed-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="f95ed-114">Da der Parameter *volumetype* nicht angegeben ist, legt das Cmdlet den Wert auf alle fest.</span><span class="sxs-lookup"><span data-stu-id="f95ed-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="f95ed-115">Beispiel 2: Deaktivieren der Verschlüsselung für Daten-Volumes auf einem virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="f95ed-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="f95ed-116">Mit diesem Befehl wird die Verschlüsselung für Volumes vom Typ Data für den virtuellen Computer mit dem Namen VM004 deaktiviert, der zur Ressourcengruppe mit dem Namen Group002 gehört.</span><span class="sxs-lookup"><span data-stu-id="f95ed-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="f95ed-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="f95ed-117">PARAMETERS</span></span>

### <span data-ttu-id="f95ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95ed-118">-DefaultProfile</span></span>
<span data-ttu-id="f95ed-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f95ed-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f95ed-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f95ed-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f95ed-121">Gibt an, dass dieses Cmdlet die automatische Aktualisierung der Nebenversion der Erweiterung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f95ed-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f95ed-122">-Force</span></span>
<span data-ttu-id="f95ed-123">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f95ed-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f95ed-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f95ed-124">-Name</span></span>
<span data-ttu-id="f95ed-125">Gibt an der Name der Azure Resource Manager (Arm)-Ressource, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="f95ed-125">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="f95ed-126">Wenn dieser Parameter nicht angegeben wird, ist dieses Cmdlet standardmäßig auf "AzureDiskEncryption für Windows-VMS" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f95ed-126">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95ed-127">-ResourceGroupName</span></span>
<span data-ttu-id="f95ed-128">Gibt den Ressourcengruppennamen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f95ed-128">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="f95ed-129">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f95ed-129">-TypeHandlerVersion</span></span>
<span data-ttu-id="f95ed-130">Gibt die Version der Verschlüsselungs Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="f95ed-130">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="f95ed-131">Wenn Sie keinen Wert für diesen Parameter angeben, wird die neueste Version der Erweiterung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f95ed-131">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="f95ed-132">-VMName</span></span>
<span data-ttu-id="f95ed-133">Gibt den Namen des virtuellen Computers an, auf dem dieses Cmdlet die Verschlüsselung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="f95ed-133">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-134">-Volumetype</span><span class="sxs-lookup"><span data-stu-id="f95ed-134">-VolumeType</span></span>
<span data-ttu-id="f95ed-135">Gibt den Typ der virtuellen Maschinen-Volumes an, um den Verschlüsselungsvorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f95ed-135">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="f95ed-136">Bei Windows-virtuellen Computern sind gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="f95ed-136">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="f95ed-137">Alle</span><span class="sxs-lookup"><span data-stu-id="f95ed-137">All</span></span>
- <span data-ttu-id="f95ed-138">OS</span><span class="sxs-lookup"><span data-stu-id="f95ed-138">OS</span></span>
- <span data-ttu-id="f95ed-139">Daten.</span><span class="sxs-lookup"><span data-stu-id="f95ed-139">Data.</span></span>
<span data-ttu-id="f95ed-140">Wenn Sie keinen Wert für diesen Parameter angeben, lautet der Standardwert alle.</span><span class="sxs-lookup"><span data-stu-id="f95ed-140">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="f95ed-141">Die Option "Verschlüsselung deaktivieren" wird derzeit für Linux nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f95ed-141">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95ed-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f95ed-142">-Confirm</span></span>
<span data-ttu-id="f95ed-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f95ed-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f95ed-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f95ed-144">-WhatIf</span></span>
<span data-ttu-id="f95ed-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f95ed-145">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f95ed-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f95ed-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f95ed-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95ed-147">CommonParameters</span></span>
<span data-ttu-id="f95ed-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95ed-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95ed-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f95ed-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95ed-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f95ed-150">INPUTS</span></span>

## <span data-ttu-id="f95ed-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f95ed-151">OUTPUTS</span></span>

### <span data-ttu-id="f95ed-152">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f95ed-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f95ed-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="f95ed-153">NOTES</span></span>

## <span data-ttu-id="f95ed-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f95ed-154">RELATED LINKS</span></span>

[<span data-ttu-id="f95ed-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f95ed-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="f95ed-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f95ed-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="f95ed-157">Satz-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f95ed-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)



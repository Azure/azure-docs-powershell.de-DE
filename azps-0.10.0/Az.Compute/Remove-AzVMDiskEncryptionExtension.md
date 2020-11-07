---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 51b1273e5c44756df56177878dbe4fbc9563ec2a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844372"
---
# <span data-ttu-id="2b821-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2b821-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="2b821-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2b821-102">SYNOPSIS</span></span>
<span data-ttu-id="2b821-103">Entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2b821-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="2b821-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b821-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b821-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b821-105">DESCRIPTION</span></span>
<span data-ttu-id="2b821-106">Das Cmdlet **Remove-AzVMDiskEncryptionExtension** entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2b821-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="2b821-107">Wenn kein Erweiterungsname angegeben wird, entfernt dieses Cmdlet die Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer, die das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-basierte virtuelle Maschinen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b821-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="2b821-108">Dieses Cmdlet deaktiviert die Verschlüsselung auf dem virtuellen Computer nicht.</span><span class="sxs-lookup"><span data-stu-id="2b821-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="2b821-109">Sie entfernt die Erweiterung und die zugehörige Erweiterungskonfiguration vom virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2b821-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="2b821-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2b821-110">EXAMPLES</span></span>

### <span data-ttu-id="2b821-111">Beispiel 1: Entfernen Sie die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="2b821-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="2b821-112">Dieser Befehl entfernt die Erweiterung mit dem Standardnamen AzureDiskEncryption für einen virtuellen Computer, auf dem das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux basierter virtueller Computer mit dem Namen MyTestVM ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b821-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="2b821-113">Beispiel 2: Entfernen einer bestimmten Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="2b821-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="2b821-114">Dieser Befehl entfernt die Verschlüsselungs Erweiterung mit dem Namen MyDiskEncryptionExtension vom virtuellen Computer mit dem Namen MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="2b821-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="2b821-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b821-115">PARAMETERS</span></span>

### <span data-ttu-id="2b821-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b821-116">-DefaultProfile</span></span>
<span data-ttu-id="2b821-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2b821-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b821-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2b821-118">-Force</span></span>
<span data-ttu-id="2b821-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2b821-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b821-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2b821-120">-Name</span></span>
<span data-ttu-id="2b821-121">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="2b821-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="2b821-122">Mit dem Set-AzVMDiskEncryptionExtension-Cmdlet wird dieser Name auf AzureDiskEncryption für virtuelle Computer festgelegt, auf denen das Windows-Betriebssystem und AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2b821-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="2b821-123">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzVMDiskEncryptionExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="2b821-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b821-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b821-124">-ResourceGroupName</span></span>
<span data-ttu-id="2b821-125">Gibt den Namen der Ressourcengruppe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="2b821-125">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b821-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="2b821-126">-VMName</span></span>
<span data-ttu-id="2b821-127">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="2b821-127">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b821-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b821-128">-Confirm</span></span>
<span data-ttu-id="2b821-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b821-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b821-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b821-130">-WhatIf</span></span>
<span data-ttu-id="2b821-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b821-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2b821-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b821-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b821-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b821-133">CommonParameters</span></span>
<span data-ttu-id="2b821-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b821-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b821-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b821-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b821-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2b821-136">INPUTS</span></span>

### <span data-ttu-id="2b821-137">Keine</span><span class="sxs-lookup"><span data-stu-id="2b821-137">None</span></span>
<span data-ttu-id="2b821-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2b821-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2b821-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2b821-139">OUTPUTS</span></span>

### <span data-ttu-id="2b821-140">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2b821-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2b821-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="2b821-141">NOTES</span></span>

## <span data-ttu-id="2b821-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2b821-142">RELATED LINKS</span></span>

[<span data-ttu-id="2b821-143">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="2b821-143">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="2b821-144">Satz-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="2b821-144">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)



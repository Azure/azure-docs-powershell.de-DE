---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008607"
---
# <span data-ttu-id="48ea6-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="48ea6-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="48ea6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="48ea6-103">Entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="48ea6-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="48ea6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="48ea6-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48ea6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48ea6-105">DESCRIPTION</span></span>
<span data-ttu-id="48ea6-106">Das Cmdlet **Remove-AzVMDiskEncryptionExtension** entfernt die Datenträger Verschlüsselungs Erweiterung und die zugehörige Erweiterungskonfiguration von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="48ea6-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="48ea6-107">Wenn kein Erweiterungsname angegeben wird, entfernt dieses Cmdlet die Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer, die das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-basierte virtuelle Maschinen ausführen.</span><span class="sxs-lookup"><span data-stu-id="48ea6-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="48ea6-108">Bei diesem Cmdlet tritt ein Fehler auf, wenn die Verschlüsselung auf dem virtuellen Computer nicht zuerst deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="48ea6-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="48ea6-109">Wenn Sie die Verschlüsselung auf einem virtuellen Computer deaktivieren möchten, verwenden Sie [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span><span class="sxs-lookup"><span data-stu-id="48ea6-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="48ea6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48ea6-110">EXAMPLES</span></span>

### <span data-ttu-id="48ea6-111">Beispiel 1: Entfernen Sie die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="48ea6-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="48ea6-112">Dieser Befehl entfernt die Erweiterung mit dem Standardnamen AzureDiskEncryption für einen virtuellen Computer, auf dem das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux basierter virtueller Computer mit dem Namen MyTestVM ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48ea6-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="48ea6-113">Beispiel 2: Entfernen einer bestimmten Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="48ea6-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="48ea6-114">Dieser Befehl entfernt die Verschlüsselungs Erweiterung mit dem Namen MyDiskEncryptionExtension vom virtuellen Computer mit dem Namen MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="48ea6-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="48ea6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="48ea6-115">PARAMETERS</span></span>

### <span data-ttu-id="48ea6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48ea6-116">-DefaultProfile</span></span>
<span data-ttu-id="48ea6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="48ea6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48ea6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="48ea6-118">-Force</span></span>
<span data-ttu-id="48ea6-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="48ea6-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="48ea6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="48ea6-120">-Name</span></span>
<span data-ttu-id="48ea6-121">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="48ea6-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="48ea6-122">Mit dem Set-AzVMDiskEncryptionExtension-Cmdlet wird dieser Name auf AzureDiskEncryption für virtuelle Computer festgelegt, auf denen das Windows-Betriebssystem und AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="48ea6-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="48ea6-123">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzVMDiskEncryptionExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="48ea6-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48ea6-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="48ea6-124">-NoWait</span></span>
<span data-ttu-id="48ea6-125">Startet den Vorgang und gibt unmittelbar vor dem Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="48ea6-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="48ea6-126">Verwenden Sie einen anderen Mechanismus, um festzustellen, ob der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="48ea6-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="48ea6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48ea6-127">-ResourceGroupName</span></span>
<span data-ttu-id="48ea6-128">Gibt den Namen der Ressourcengruppe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="48ea6-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="48ea6-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="48ea6-129">-VMName</span></span>
<span data-ttu-id="48ea6-130">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="48ea6-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="48ea6-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="48ea6-131">-Confirm</span></span>
<span data-ttu-id="48ea6-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48ea6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48ea6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48ea6-133">-WhatIf</span></span>
<span data-ttu-id="48ea6-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48ea6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48ea6-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48ea6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48ea6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48ea6-136">CommonParameters</span></span>
<span data-ttu-id="48ea6-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48ea6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48ea6-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48ea6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48ea6-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48ea6-139">INPUTS</span></span>

### <span data-ttu-id="48ea6-140">System. String</span><span class="sxs-lookup"><span data-stu-id="48ea6-140">System.String</span></span>

## <span data-ttu-id="48ea6-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48ea6-141">OUTPUTS</span></span>

### <span data-ttu-id="48ea6-142">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="48ea6-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="48ea6-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="48ea6-143">NOTES</span></span>

## <span data-ttu-id="48ea6-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48ea6-144">RELATED LINKS</span></span>

[<span data-ttu-id="48ea6-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="48ea6-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="48ea6-146">Satz-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="48ea6-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)



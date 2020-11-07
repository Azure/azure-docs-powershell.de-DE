---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 3fc1424fe2cde9b2137ca6925a8788fa5c8a8139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662276"
---
# <span data-ttu-id="9e548-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9e548-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="9e548-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9e548-102">SYNOPSIS</span></span>
<span data-ttu-id="9e548-103">Entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9e548-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e548-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e548-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e548-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e548-105">DESCRIPTION</span></span>
<span data-ttu-id="9e548-106">Das Cmdlet **Remove-AzureRmVMDiskEncryptionExtension** entfernt die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9e548-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="9e548-107">Wenn kein Erweiterungsname angegeben wird, entfernt dieses Cmdlet die Erweiterung mit dem Standardnamen AzureDiskEncryption für virtuelle Computer, die das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux-basierte virtuelle Maschinen ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e548-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="9e548-108">Dieses Cmdlet deaktiviert die Verschlüsselung auf dem virtuellen Computer nicht.</span><span class="sxs-lookup"><span data-stu-id="9e548-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="9e548-109">Sie entfernt die Erweiterung und die zugehörige Erweiterungskonfiguration vom virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9e548-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="9e548-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e548-110">EXAMPLES</span></span>

### <span data-ttu-id="9e548-111">Beispiel 1: Entfernen Sie die Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="9e548-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="9e548-112">Dieser Befehl entfernt die Erweiterung mit dem Standardnamen AzureDiskEncryption für einen virtuellen Computer, auf dem das Windows-Betriebssystem oder AzureDiskEncryptionForLinux für Linux basierter virtueller Computer mit dem Namen MyTestVM ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e548-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="9e548-113">Beispiel 2: Entfernen einer bestimmten Datenträger Verschlüsselungs Erweiterung von einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="9e548-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="9e548-114">Dieser Befehl entfernt die Verschlüsselungs Erweiterung mit dem Namen MyDiskEncryptionExtension vom virtuellen Computer mit dem Namen MyTestVM.</span><span class="sxs-lookup"><span data-stu-id="9e548-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="9e548-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e548-115">PARAMETERS</span></span>

### <span data-ttu-id="9e548-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e548-116">-DefaultProfile</span></span>
<span data-ttu-id="9e548-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9e548-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e548-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9e548-118">-Force</span></span>
<span data-ttu-id="9e548-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9e548-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e548-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9e548-120">-Name</span></span>
<span data-ttu-id="9e548-121">Gibt den Namen der Azure Resource Manager-Ressource an, die die Erweiterung darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e548-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9e548-122">Mit dem Set-AzureRmVMDiskEncryptionExtension-Cmdlet wird dieser Name auf AzureDiskEncryption für virtuelle Computer festgelegt, auf denen das Windows-Betriebssystem und AzureDiskEncryptionForLinux für Linux-virtuelle Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9e548-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="9e548-123">Geben Sie diesen Parameter nur an, wenn Sie den Standardnamen im Cmdlet " **Satz-AzureRmVMDiskEncryptionExtension** " geändert oder einen anderen Ressourcennamen in einer Ressourcen-Manager-Vorlage verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="9e548-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="9e548-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e548-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e548-125">Gibt den Namen der Ressourcengruppe für den virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="9e548-125">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="9e548-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e548-126">-VMName</span></span>
<span data-ttu-id="9e548-127">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="9e548-127">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9e548-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e548-128">-Confirm</span></span>
<span data-ttu-id="9e548-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e548-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e548-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e548-130">-WhatIf</span></span>
<span data-ttu-id="9e548-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e548-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9e548-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e548-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e548-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e548-133">CommonParameters</span></span>
<span data-ttu-id="9e548-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e548-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e548-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e548-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e548-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9e548-136">INPUTS</span></span>

## <span data-ttu-id="9e548-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9e548-137">OUTPUTS</span></span>

## <span data-ttu-id="9e548-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="9e548-138">NOTES</span></span>

## <span data-ttu-id="9e548-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9e548-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e548-140">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="9e548-140">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="9e548-141">Satz-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9e548-141">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: a697ead2f971191d108d4fb348a213e35b363d63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940579"
---
# <span data-ttu-id="26e35-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="26e35-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="26e35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e35-102">SYNOPSIS</span></span>
<span data-ttu-id="26e35-103">Zeigt den Datenträgerverschlüsselungsstatus von VMs in einem VM-Skalierungssatz an.</span><span class="sxs-lookup"><span data-stu-id="26e35-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="26e35-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26e35-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26e35-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26e35-105">DESCRIPTION</span></span>
<span data-ttu-id="26e35-106">Zeigt den Datenträgerverschlüsselungsstatus des VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="26e35-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="26e35-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26e35-107">EXAMPLES</span></span>

### <span data-ttu-id="26e35-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="26e35-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="26e35-109">Zeigt den Datenträgerverschlüsselungsstatus der VM-Instanz 1 im VM-Skalierungssatz "VMSS001" an, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="26e35-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="26e35-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="26e35-110">PARAMETERS</span></span>

### <span data-ttu-id="26e35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e35-111">-DefaultProfile</span></span>
<span data-ttu-id="26e35-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26e35-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26e35-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="26e35-113">-ExtensionName</span></span>
<span data-ttu-id="26e35-114">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="26e35-114">The extension name.</span></span>
<span data-ttu-id="26e35-115">Wenn dieser Parameter nicht angegeben ist, werden Standardwerte verwendet: AzureDiskEncryption für Windows-VMs und AzureDiskEncryptionForLinux für Linux-VMs.</span><span class="sxs-lookup"><span data-stu-id="26e35-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="26e35-116">-InstanceId</span></span>
<span data-ttu-id="26e35-117">Gibt die Instanz-ID an.</span><span class="sxs-lookup"><span data-stu-id="26e35-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="26e35-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e35-118">-ResourceGroupName</span></span>
<span data-ttu-id="26e35-119">Ressourcengruppenname des Skalierungssatzs für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="26e35-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="26e35-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="26e35-120">-VMScaleSetName</span></span>
<span data-ttu-id="26e35-121">Der Name des Skalierungssatzs für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="26e35-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26e35-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e35-122">CommonParameters</span></span>
<span data-ttu-id="26e35-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e35-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e35-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26e35-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e35-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26e35-125">INPUTS</span></span>

### <span data-ttu-id="26e35-126">System.String</span><span class="sxs-lookup"><span data-stu-id="26e35-126">System.String</span></span>

## <span data-ttu-id="26e35-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26e35-127">OUTPUTS</span></span>

### <span data-ttu-id="26e35-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="26e35-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="26e35-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="26e35-129">NOTES</span></span>

## <span data-ttu-id="26e35-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="26e35-130">RELATED LINKS</span></span>

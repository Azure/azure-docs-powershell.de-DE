---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470886"
---
# <span data-ttu-id="05597-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="05597-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="05597-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05597-102">SYNOPSIS</span></span>
<span data-ttu-id="05597-103">Zeigt den Datenträgerverschlüsselungsstatus von VMs in einem VM-Skalierungssatz an.</span><span class="sxs-lookup"><span data-stu-id="05597-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="05597-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05597-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05597-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05597-105">DESCRIPTION</span></span>
<span data-ttu-id="05597-106">Zeigt den Datenträgerverschlüsselungsstatus des festgelegten VM-Maßstabs an.</span><span class="sxs-lookup"><span data-stu-id="05597-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="05597-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="05597-107">EXAMPLES</span></span>

### <span data-ttu-id="05597-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="05597-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="05597-109">Zeigt den Datenträgerverschlüsselungsstatus der VM-Instanz 1 im VM-Skalierungssatz namens VMSS001 an, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="05597-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="05597-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05597-110">PARAMETERS</span></span>

### <span data-ttu-id="05597-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05597-111">-DefaultProfile</span></span>
<span data-ttu-id="05597-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05597-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05597-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="05597-113">-ExtensionName</span></span>
<span data-ttu-id="05597-114">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="05597-114">The extension name.</span></span>
<span data-ttu-id="05597-115">Wenn dieser Parameter nicht angegeben wird, werden die Standardwerte "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux für Linux-VMs" verwendet.</span><span class="sxs-lookup"><span data-stu-id="05597-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="05597-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="05597-116">-InstanceId</span></span>
<span data-ttu-id="05597-117">Gibt die Instanz-ID an.</span><span class="sxs-lookup"><span data-stu-id="05597-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="05597-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05597-118">-ResourceGroupName</span></span>
<span data-ttu-id="05597-119">Ressourcengruppenname des Skalierungssatzs für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="05597-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="05597-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="05597-120">-VMScaleSetName</span></span>
<span data-ttu-id="05597-121">Der Name des Skalierungssatz für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="05597-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="05597-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05597-122">CommonParameters</span></span>
<span data-ttu-id="05597-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05597-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05597-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05597-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05597-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="05597-125">INPUTS</span></span>

### <span data-ttu-id="05597-126">System.String</span><span class="sxs-lookup"><span data-stu-id="05597-126">System.String</span></span>

## <span data-ttu-id="05597-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="05597-127">OUTPUTS</span></span>

### <span data-ttu-id="05597-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="05597-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="05597-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="05597-129">NOTES</span></span>

## <span data-ttu-id="05597-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="05597-130">RELATED LINKS</span></span>

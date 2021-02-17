---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175996"
---
# <span data-ttu-id="a9ec1-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a9ec1-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="a9ec1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ec1-103">Zeigt den Datenträgerverschlüsselungsstatus von VMs in einem VM-Skalierungssatz an.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="a9ec1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9ec1-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ec1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="a9ec1-106">Zeigt den Datenträgerverschlüsselungsstatus des festgelegten VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="a9ec1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a9ec1-107">EXAMPLES</span></span>

### <span data-ttu-id="a9ec1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9ec1-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="a9ec1-109">Zeigt den Datenträgerverschlüsselungsstatus der VM-Instanz 1 im VM-Skalierungssatz namens VMSS001 an, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="a9ec1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9ec1-110">PARAMETERS</span></span>

### <span data-ttu-id="a9ec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ec1-111">-DefaultProfile</span></span>
<span data-ttu-id="a9ec1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9ec1-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="a9ec1-113">-ExtensionName</span></span>
<span data-ttu-id="a9ec1-114">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-114">The extension name.</span></span>
<span data-ttu-id="a9ec1-115">Wenn dieser Parameter nicht angegeben wird, werden die Standardwerte "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux für Linux-VMs" verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="a9ec1-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a9ec1-116">-InstanceId</span></span>
<span data-ttu-id="a9ec1-117">Gibt die Instanz-ID an.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="a9ec1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ec1-118">-ResourceGroupName</span></span>
<span data-ttu-id="a9ec1-119">Ressourcengruppenname des Skalierungssatzs für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="a9ec1-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a9ec1-120">-VMScaleSetName</span></span>
<span data-ttu-id="a9ec1-121">Der Name des Skalierungssatz für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="a9ec1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ec1-122">CommonParameters</span></span>
<span data-ttu-id="a9ec1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9ec1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ec1-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9ec1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ec1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a9ec1-125">INPUTS</span></span>

### <span data-ttu-id="a9ec1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a9ec1-126">System.String</span></span>

## <span data-ttu-id="a9ec1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a9ec1-127">OUTPUTS</span></span>

### <span data-ttu-id="a9ec1-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="a9ec1-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="a9ec1-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a9ec1-129">NOTES</span></span>

## <span data-ttu-id="a9ec1-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a9ec1-130">RELATED LINKS</span></span>

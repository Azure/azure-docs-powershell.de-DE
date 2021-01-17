---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470893"
---
# <span data-ttu-id="0f325-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="0f325-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="0f325-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f325-102">SYNOPSIS</span></span>
<span data-ttu-id="0f325-103">Zeigt den Datenträgerverschlüsselungsstatus eines VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="0f325-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="0f325-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f325-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f325-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f325-105">DESCRIPTION</span></span>
<span data-ttu-id="0f325-106">Zeigt den Datenträgerverschlüsselungsstatus eines VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="0f325-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="0f325-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f325-107">EXAMPLES</span></span>

### <span data-ttu-id="0f325-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f325-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="0f325-109">Zeigt den Datenträgerverschlüsselungsstatus des VM-Skalierungssets namens VMSS001 an, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="0f325-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="0f325-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f325-110">PARAMETERS</span></span>

### <span data-ttu-id="0f325-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f325-111">-DefaultProfile</span></span>
<span data-ttu-id="0f325-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f325-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f325-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="0f325-113">-ExtensionName</span></span>
<span data-ttu-id="0f325-114">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="0f325-114">The extension name.</span></span>
<span data-ttu-id="0f325-115">Wenn dieser Parameter nicht angegeben wird, werden die Standardwerte "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux für Linux-VMs" verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f325-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="0f325-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f325-116">-ResourceGroupName</span></span>
<span data-ttu-id="0f325-117">Ressourcengruppenname des Skalierungssets für den virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="0f325-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f325-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0f325-118">-VMScaleSetName</span></span>
<span data-ttu-id="0f325-119">Der Name des Skalierungssatz für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="0f325-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f325-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f325-120">CommonParameters</span></span>
<span data-ttu-id="0f325-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f325-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f325-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f325-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f325-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f325-123">INPUTS</span></span>

### <span data-ttu-id="0f325-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0f325-124">System.String</span></span>

## <span data-ttu-id="0f325-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f325-125">OUTPUTS</span></span>

### <span data-ttu-id="0f325-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="0f325-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="0f325-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f325-127">NOTES</span></span>

## <span data-ttu-id="0f325-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f325-128">RELATED LINKS</span></span>

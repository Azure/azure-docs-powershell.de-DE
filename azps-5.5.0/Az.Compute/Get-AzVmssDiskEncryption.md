---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171234"
---
# <span data-ttu-id="4ae75-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4ae75-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="4ae75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae75-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae75-103">Zeigt den Datenträgerverschlüsselungsstatus eines VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="4ae75-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4ae75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ae75-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae75-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ae75-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae75-106">Zeigt den Datenträgerverschlüsselungsstatus eines VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="4ae75-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4ae75-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ae75-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae75-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ae75-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4ae75-109">Zeigt den Datenträgerverschlüsselungsstatus des VM-Skalierungssets namens VMSS001 an, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="4ae75-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4ae75-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ae75-110">PARAMETERS</span></span>

### <span data-ttu-id="4ae75-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae75-111">-DefaultProfile</span></span>
<span data-ttu-id="4ae75-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ae75-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae75-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4ae75-113">-ExtensionName</span></span>
<span data-ttu-id="4ae75-114">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="4ae75-114">The extension name.</span></span>
<span data-ttu-id="4ae75-115">Wenn dieser Parameter nicht angegeben wird, werden die Standardwerte "AzureDiskEncryption" für Windows-VMs und "AzureDiskEncryptionForLinux für Linux-VMs" verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ae75-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4ae75-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae75-116">-ResourceGroupName</span></span>
<span data-ttu-id="4ae75-117">Ressourcengruppenname des Skalierungssets für den virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4ae75-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="4ae75-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4ae75-118">-VMScaleSetName</span></span>
<span data-ttu-id="4ae75-119">Der Name des Skalierungssatz für den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4ae75-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="4ae75-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae75-120">CommonParameters</span></span>
<span data-ttu-id="4ae75-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ae75-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae75-122">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ae75-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae75-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ae75-123">INPUTS</span></span>

### <span data-ttu-id="4ae75-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4ae75-124">System.String</span></span>

## <span data-ttu-id="4ae75-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ae75-125">OUTPUTS</span></span>

### <span data-ttu-id="4ae75-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="4ae75-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="4ae75-127">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ae75-127">NOTES</span></span>

## <span data-ttu-id="4ae75-128">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ae75-128">RELATED LINKS</span></span>

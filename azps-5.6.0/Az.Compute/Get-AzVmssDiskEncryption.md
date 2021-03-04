---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 56fcbadbcdbd874df3fea74918381eb24b2fa1f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933067"
---
# <span data-ttu-id="4562a-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4562a-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="4562a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4562a-102">SYNOPSIS</span></span>
<span data-ttu-id="4562a-103">Zeigt den Datenträgerverschlüsselungsstatus eines VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="4562a-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4562a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4562a-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4562a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4562a-105">DESCRIPTION</span></span>
<span data-ttu-id="4562a-106">Zeigt den Datenträgerverschlüsselungsstatus eines VM-Skalierungssets an.</span><span class="sxs-lookup"><span data-stu-id="4562a-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="4562a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4562a-107">EXAMPLES</span></span>

### <span data-ttu-id="4562a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4562a-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4562a-109">Zeigt den Datenträgerverschlüsselungsstatus des VM-Skalierungssatzs mit dem Namen VMSS001 an, der zur Ressourcengruppe "Group001" gehört.</span><span class="sxs-lookup"><span data-stu-id="4562a-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4562a-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4562a-110">PARAMETERS</span></span>

### <span data-ttu-id="4562a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4562a-111">-DefaultProfile</span></span>
<span data-ttu-id="4562a-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4562a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4562a-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="4562a-113">-ExtensionName</span></span>
<span data-ttu-id="4562a-114">Der Erweiterungsname.</span><span class="sxs-lookup"><span data-stu-id="4562a-114">The extension name.</span></span>
<span data-ttu-id="4562a-115">Wenn dieser Parameter nicht angegeben ist, werden Standardwerte verwendet: AzureDiskEncryption für Windows-VMs und AzureDiskEncryptionForLinux für Linux-VMs.</span><span class="sxs-lookup"><span data-stu-id="4562a-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="4562a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4562a-116">-ResourceGroupName</span></span>
<span data-ttu-id="4562a-117">Ressourcengruppenname des Skalierungssatzs für virtuelle Computer</span><span class="sxs-lookup"><span data-stu-id="4562a-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="4562a-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4562a-118">-VMScaleSetName</span></span>
<span data-ttu-id="4562a-119">Der Name des Skalierungssatzs für virtuelle Computer.</span><span class="sxs-lookup"><span data-stu-id="4562a-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="4562a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4562a-120">CommonParameters</span></span>
<span data-ttu-id="4562a-121">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4562a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4562a-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4562a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4562a-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4562a-123">INPUTS</span></span>

### <span data-ttu-id="4562a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4562a-124">System.String</span></span>

## <span data-ttu-id="4562a-125">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4562a-125">OUTPUTS</span></span>

### <span data-ttu-id="4562a-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="4562a-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="4562a-127">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4562a-127">NOTES</span></span>

## <span data-ttu-id="4562a-128">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4562a-128">RELATED LINKS</span></span>

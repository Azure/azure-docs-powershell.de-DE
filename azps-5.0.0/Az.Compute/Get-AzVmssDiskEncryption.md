---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302797"
---
# <span data-ttu-id="b07b8-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="b07b8-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="b07b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b07b8-102">SYNOPSIS</span></span>
<span data-ttu-id="b07b8-103">Zeigt den Datenträger Verschlüsselungsstatus eines VM-Skalierungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="b07b8-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="b07b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b07b8-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b07b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b07b8-105">DESCRIPTION</span></span>
<span data-ttu-id="b07b8-106">Zeigt den Datenträger Verschlüsselungsstatus eines VM-Skalierungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="b07b8-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="b07b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b07b8-107">EXAMPLES</span></span>

### <span data-ttu-id="b07b8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b07b8-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b07b8-109">Zeigt den Datenträger Verschlüsselungsstatus des VM-Skalierungs Satzes mit dem Namen "VMSS001" an, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="b07b8-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b07b8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b07b8-110">PARAMETERS</span></span>

### <span data-ttu-id="b07b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b07b8-111">-DefaultProfile</span></span>
<span data-ttu-id="b07b8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b07b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b07b8-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="b07b8-113">-ExtensionName</span></span>
<span data-ttu-id="b07b8-114">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="b07b8-114">The extension name.</span></span>
<span data-ttu-id="b07b8-115">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="b07b8-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="b07b8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b07b8-116">-ResourceGroupName</span></span>
<span data-ttu-id="b07b8-117">Ressourcengruppenname des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="b07b8-117">Resource group name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="b07b8-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b07b8-118">-VMScaleSetName</span></span>
<span data-ttu-id="b07b8-119">Der Skalierungs Satz Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="b07b8-119">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="b07b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b07b8-120">CommonParameters</span></span>
<span data-ttu-id="b07b8-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b07b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b07b8-122">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b07b8-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b07b8-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b07b8-123">INPUTS</span></span>

### <span data-ttu-id="b07b8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b07b8-124">System.String</span></span>

## <span data-ttu-id="b07b8-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b07b8-125">OUTPUTS</span></span>

### <span data-ttu-id="b07b8-126">Microsoft. Azure. Commands. Compute. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="b07b8-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="b07b8-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="b07b8-127">NOTES</span></span>

## <span data-ttu-id="b07b8-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b07b8-128">RELATED LINKS</span></span>

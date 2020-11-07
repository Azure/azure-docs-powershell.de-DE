---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 84f8abc6c298d7c82bef2494086deef3e4130842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662957"
---
# <span data-ttu-id="3909a-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="3909a-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="3909a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3909a-102">SYNOPSIS</span></span>
<span data-ttu-id="3909a-103">Entfernt (a) Secret (s) aus einem virtuellen Computerobjekt</span><span class="sxs-lookup"><span data-stu-id="3909a-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3909a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3909a-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3909a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3909a-105">DESCRIPTION</span></span>
<span data-ttu-id="3909a-106">Das Remove-AzureRmVMSecret-Cmdlet entfernt (a) Secret (s) aus einem virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="3909a-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="3909a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3909a-107">EXAMPLES</span></span>

### <span data-ttu-id="3909a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3909a-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="3909a-109">Entfernt alle Geheimnisse von einem virtuellen Computer "VM1" in der Ressourcengruppe "RG1" und aktualisiert die VM.</span><span class="sxs-lookup"><span data-stu-id="3909a-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="3909a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3909a-110">PARAMETERS</span></span>

### <span data-ttu-id="3909a-111">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3909a-111">-SourceVaultId</span></span>
<span data-ttu-id="3909a-112">Gibt ein Array von Quell Vault-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="3909a-112">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3909a-113">-VM</span><span class="sxs-lookup"><span data-stu-id="3909a-113">-VM</span></span>
<span data-ttu-id="3909a-114">Gibt den virtuellen Computer an, von dem dieses Cmdlet (a) Secret (s) entfernt.</span><span class="sxs-lookup"><span data-stu-id="3909a-114">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="3909a-115">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3909a-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3909a-116">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3909a-116">-Confirm</span></span>
<span data-ttu-id="3909a-117">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3909a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3909a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3909a-118">-WhatIf</span></span>
<span data-ttu-id="3909a-119">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3909a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3909a-120">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3909a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3909a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3909a-121">CommonParameters</span></span>
<span data-ttu-id="3909a-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3909a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3909a-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3909a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3909a-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3909a-124">INPUTS</span></span>

### <span data-ttu-id="3909a-125">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3909a-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3909a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3909a-126">OUTPUTS</span></span>

### <span data-ttu-id="3909a-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="3909a-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="3909a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3909a-128">NOTES</span></span>

## <span data-ttu-id="3909a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3909a-129">RELATED LINKS</span></span>


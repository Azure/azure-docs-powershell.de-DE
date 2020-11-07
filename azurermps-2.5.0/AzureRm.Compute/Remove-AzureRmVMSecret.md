---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 8d3c10be9d4a3f165932271838f6af8fdbf18e4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849736"
---
# <span data-ttu-id="d3d18-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="d3d18-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="d3d18-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3d18-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d18-103">Entfernt (a) Secret (s) aus einem virtuellen Computerobjekt</span><span class="sxs-lookup"><span data-stu-id="d3d18-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3d18-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3d18-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d18-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3d18-105">DESCRIPTION</span></span>
<span data-ttu-id="d3d18-106">Das Remove-AzureRmVMSecret-Cmdlet entfernt (a) Secret (s) aus einem virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="d3d18-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="d3d18-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3d18-107">EXAMPLES</span></span>

### <span data-ttu-id="d3d18-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3d18-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="d3d18-109">Entfernt alle Geheimnisse von einem virtuellen Computer "VM1" in der Ressourcengruppe "RG1" und aktualisiert die VM.</span><span class="sxs-lookup"><span data-stu-id="d3d18-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="d3d18-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3d18-110">PARAMETERS</span></span>

### <span data-ttu-id="d3d18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d18-111">-DefaultProfile</span></span>
<span data-ttu-id="d3d18-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3d18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d18-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="d3d18-113">-SourceVaultId</span></span>
<span data-ttu-id="d3d18-114">Gibt ein Array von Quell Vault-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d3d18-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d3d18-115">-VM</span><span class="sxs-lookup"><span data-stu-id="d3d18-115">-VM</span></span>
<span data-ttu-id="d3d18-116">Gibt den virtuellen Computer an, von dem dieses Cmdlet (a) Secret (s) entfernt.</span><span class="sxs-lookup"><span data-stu-id="d3d18-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="d3d18-117">Verwenden Sie das Get-AzureRmVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d3d18-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="d3d18-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3d18-118">-Confirm</span></span>
<span data-ttu-id="d3d18-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3d18-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d18-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d18-120">-WhatIf</span></span>
<span data-ttu-id="d3d18-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3d18-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d18-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3d18-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d18-123">CommonParameters</span></span>
<span data-ttu-id="d3d18-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d18-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3d18-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d18-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3d18-126">INPUTS</span></span>

### <span data-ttu-id="d3d18-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3d18-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d3d18-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3d18-128">OUTPUTS</span></span>

### <span data-ttu-id="d3d18-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d3d18-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d3d18-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3d18-130">NOTES</span></span>

## <span data-ttu-id="d3d18-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3d18-131">RELATED LINKS</span></span>


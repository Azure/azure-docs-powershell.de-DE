---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003875"
---
# <span data-ttu-id="64694-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="64694-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="64694-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64694-102">SYNOPSIS</span></span>
<span data-ttu-id="64694-103">Entfernt (a) Secret (s) aus einem virtuellen Computerobjekt</span><span class="sxs-lookup"><span data-stu-id="64694-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="64694-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64694-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64694-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64694-105">DESCRIPTION</span></span>
<span data-ttu-id="64694-106">Das Remove-AzVMSecret-Cmdlet entfernt (a) Secret (s) aus einem virtuellen Computerobjekt.</span><span class="sxs-lookup"><span data-stu-id="64694-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="64694-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64694-107">EXAMPLES</span></span>

### <span data-ttu-id="64694-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="64694-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="64694-109">Entfernt alle Geheimnisse von einem virtuellen Computer "VM1" in der Ressourcengruppe "RG1" und aktualisiert die VM.</span><span class="sxs-lookup"><span data-stu-id="64694-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="64694-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="64694-110">PARAMETERS</span></span>

### <span data-ttu-id="64694-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64694-111">-DefaultProfile</span></span>
<span data-ttu-id="64694-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="64694-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64694-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="64694-113">-SourceVaultId</span></span>
<span data-ttu-id="64694-114">Gibt ein Array von Quell Vault-IDs an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="64694-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64694-115">-VM</span><span class="sxs-lookup"><span data-stu-id="64694-115">-VM</span></span>
<span data-ttu-id="64694-116">Gibt den virtuellen Computer an, von dem dieses Cmdlet (a) Secret (s) entfernt.</span><span class="sxs-lookup"><span data-stu-id="64694-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="64694-117">Verwenden Sie das Get-AzVM-Cmdlet, um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="64694-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64694-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="64694-118">-Confirm</span></span>
<span data-ttu-id="64694-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="64694-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64694-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64694-120">-WhatIf</span></span>
<span data-ttu-id="64694-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="64694-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64694-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="64694-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64694-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64694-123">CommonParameters</span></span>
<span data-ttu-id="64694-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64694-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64694-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64694-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64694-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64694-126">INPUTS</span></span>

### <span data-ttu-id="64694-127">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="64694-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="64694-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64694-128">OUTPUTS</span></span>

### <span data-ttu-id="64694-129">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="64694-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="64694-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="64694-130">NOTES</span></span>

## <span data-ttu-id="64694-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64694-131">RELATED LINKS</span></span>

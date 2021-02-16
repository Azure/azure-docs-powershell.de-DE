---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171192"
---
# <span data-ttu-id="93063-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="93063-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="93063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93063-102">SYNOPSIS</span></span>
<span data-ttu-id="93063-103">Entfernt (a) geheime(n) Schlüssel aus einem Objekt des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="93063-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="93063-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="93063-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93063-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="93063-105">DESCRIPTION</span></span>
<span data-ttu-id="93063-106">Das Remove-AzVMSecret cmdlet entfernt (a) geheime(n) Schlüssel aus einem Objekt des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="93063-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="93063-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="93063-107">EXAMPLES</span></span>

### <span data-ttu-id="93063-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93063-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="93063-109">Entfernt alle Geheimen von einem virtuellen Computer "vm1" in der Ressourcengruppe "rg1" und aktualisiert die VM</span><span class="sxs-lookup"><span data-stu-id="93063-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="93063-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93063-110">PARAMETERS</span></span>

### <span data-ttu-id="93063-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93063-111">-DefaultProfile</span></span>
<span data-ttu-id="93063-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93063-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93063-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="93063-113">-SourceVaultId</span></span>
<span data-ttu-id="93063-114">Gibt ein Array mit Quelltresor-IDs an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="93063-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="93063-115">-VM</span><span class="sxs-lookup"><span data-stu-id="93063-115">-VM</span></span>
<span data-ttu-id="93063-116">Gibt den virtuellen Computer an, von dem dieses Cmdlet (a) geheime(n) Schlüssel entfernt.</span><span class="sxs-lookup"><span data-stu-id="93063-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="93063-117">Verwenden Sie zum Abrufen eines Objekts für einen virtuellen Computer das Get-AzVM Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93063-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="93063-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93063-118">-Confirm</span></span>
<span data-ttu-id="93063-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="93063-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93063-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="93063-120">-WhatIf</span></span>
<span data-ttu-id="93063-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="93063-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93063-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93063-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93063-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93063-123">CommonParameters</span></span>
<span data-ttu-id="93063-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93063-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93063-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93063-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93063-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="93063-126">INPUTS</span></span>

### <span data-ttu-id="93063-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="93063-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="93063-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="93063-128">OUTPUTS</span></span>

### <span data-ttu-id="93063-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="93063-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="93063-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="93063-130">NOTES</span></span>

## <span data-ttu-id="93063-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="93063-131">RELATED LINKS</span></span>

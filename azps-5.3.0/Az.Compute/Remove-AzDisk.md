---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDisk.md
ms.openlocfilehash: d48946b39c27a203e7d119c69e965633de8c6d6d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473049"
---
# <span data-ttu-id="e7f91-101">Remove-AzDisk</span><span class="sxs-lookup"><span data-stu-id="e7f91-101">Remove-AzDisk</span></span>

## <span data-ttu-id="e7f91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f91-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f91-103">Entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e7f91-103">Removes a disk.</span></span>

## <span data-ttu-id="e7f91-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7f91-104">SYNTAX</span></span>

```
Remove-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f91-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7f91-105">DESCRIPTION</span></span>
<span data-ttu-id="e7f91-106">Das **Cmdlet "Remove-AzDisk"** entfernt einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e7f91-106">The **Remove-AzDisk** cmdlet removes a disk.</span></span>

## <span data-ttu-id="e7f91-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e7f91-107">EXAMPLES</span></span>

### <span data-ttu-id="e7f91-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e7f91-108">Example 1</span></span>
```
PS C:\> Remove-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Force;
```

<span data-ttu-id="e7f91-109">Mit diesem Befehl wird der Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="e7f91-109">This command removes the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e7f91-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7f91-110">PARAMETERS</span></span>

### <span data-ttu-id="e7f91-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7f91-111">-AsJob</span></span>
<span data-ttu-id="e7f91-112">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="e7f91-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f91-113">-DefaultProfile</span></span>
<span data-ttu-id="e7f91-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e7f91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7f91-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e7f91-115">-DiskName</span></span>
<span data-ttu-id="e7f91-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e7f91-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e7f91-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e7f91-117">-Force</span></span>
<span data-ttu-id="e7f91-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="e7f91-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f91-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f91-119">-ResourceGroupName</span></span>
<span data-ttu-id="e7f91-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e7f91-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e7f91-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7f91-121">-Confirm</span></span>
<span data-ttu-id="e7f91-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7f91-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f91-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e7f91-123">-WhatIf</span></span>
<span data-ttu-id="e7f91-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7f91-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7f91-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7f91-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f91-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f91-126">CommonParameters</span></span>
<span data-ttu-id="e7f91-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f91-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f91-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7f91-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f91-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e7f91-129">INPUTS</span></span>

### <span data-ttu-id="e7f91-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e7f91-130">System.String</span></span>

## <span data-ttu-id="e7f91-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e7f91-131">OUTPUTS</span></span>

### <span data-ttu-id="e7f91-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e7f91-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e7f91-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e7f91-133">NOTES</span></span>

## <span data-ttu-id="e7f91-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e7f91-134">RELATED LINKS</span></span>

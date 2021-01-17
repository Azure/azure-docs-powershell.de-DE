---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 76fb2e7483bb510d5eceb92b51f7e5e538c3b22b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472980"
---
# <span data-ttu-id="82477-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="82477-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="82477-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82477-102">SYNOPSIS</span></span>
<span data-ttu-id="82477-103">Widerruft den Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="82477-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="82477-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82477-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82477-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82477-105">DESCRIPTION</span></span>
<span data-ttu-id="82477-106">Das **Cmdlet Revoke-AzDiskAccess** widerruft den Zugriff auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="82477-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="82477-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82477-107">EXAMPLES</span></span>

### <span data-ttu-id="82477-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82477-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="82477-109">Widerrufen des Zugriffs auf den Datenträger mit dem Namen "Disk01" in der Ressourcengruppe mit dem Namen 'ResourceGroup01'</span><span class="sxs-lookup"><span data-stu-id="82477-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="82477-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82477-110">PARAMETERS</span></span>

### <span data-ttu-id="82477-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82477-111">-AsJob</span></span>
<span data-ttu-id="82477-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="82477-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82477-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82477-113">-DefaultProfile</span></span>
<span data-ttu-id="82477-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82477-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82477-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="82477-115">-DiskName</span></span>
<span data-ttu-id="82477-116">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="82477-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="82477-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82477-117">-ResourceGroupName</span></span>
<span data-ttu-id="82477-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="82477-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="82477-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82477-119">-Confirm</span></span>
<span data-ttu-id="82477-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82477-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82477-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82477-121">-WhatIf</span></span>
<span data-ttu-id="82477-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82477-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82477-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82477-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82477-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82477-124">CommonParameters</span></span>
<span data-ttu-id="82477-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82477-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82477-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82477-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82477-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82477-127">INPUTS</span></span>

### <span data-ttu-id="82477-128">System.String</span><span class="sxs-lookup"><span data-stu-id="82477-128">System.String</span></span>

## <span data-ttu-id="82477-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82477-129">OUTPUTS</span></span>

### <span data-ttu-id="82477-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="82477-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="82477-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82477-131">NOTES</span></span>

## <span data-ttu-id="82477-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82477-132">RELATED LINKS</span></span>

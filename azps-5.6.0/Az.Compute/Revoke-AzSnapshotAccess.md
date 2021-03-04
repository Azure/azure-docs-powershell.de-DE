---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/revoke-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Revoke-AzSnapshotAccess.md
ms.openlocfilehash: b18db3b4e8448212b413dc13887ea68b35f22422
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919011"
---
# <span data-ttu-id="9e220-101">Revoke-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="9e220-101">Revoke-AzSnapshotAccess</span></span>

## <span data-ttu-id="9e220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e220-102">SYNOPSIS</span></span>
<span data-ttu-id="9e220-103">Widerruft den Zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="9e220-103">Revokes an access to a snapshot.</span></span>

## <span data-ttu-id="9e220-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e220-104">SYNTAX</span></span>

```
Revoke-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e220-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e220-105">DESCRIPTION</span></span>
<span data-ttu-id="9e220-106">Das **Cmdlet Revoke-AzSnapshotAccess** widerruft den Zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="9e220-106">The **Revoke-AzSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="9e220-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e220-107">EXAMPLES</span></span>

### <span data-ttu-id="9e220-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e220-108">Example 1</span></span>
```
PS C:\> Revoke-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="9e220-109">Widerrufen des Zugriffs auf die Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="9e220-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="9e220-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9e220-110">PARAMETERS</span></span>

### <span data-ttu-id="9e220-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e220-111">-AsJob</span></span>
<span data-ttu-id="9e220-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9e220-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9e220-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e220-113">-DefaultProfile</span></span>
<span data-ttu-id="9e220-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e220-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e220-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e220-115">-ResourceGroupName</span></span>
<span data-ttu-id="9e220-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="9e220-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9e220-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="9e220-117">-SnapshotName</span></span>
<span data-ttu-id="9e220-118">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="9e220-118">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="9e220-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9e220-119">-Confirm</span></span>
<span data-ttu-id="9e220-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e220-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e220-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e220-121">-WhatIf</span></span>
<span data-ttu-id="9e220-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e220-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e220-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e220-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e220-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e220-124">CommonParameters</span></span>
<span data-ttu-id="9e220-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e220-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e220-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e220-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e220-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e220-127">INPUTS</span></span>

### <span data-ttu-id="9e220-128">System.String</span><span class="sxs-lookup"><span data-stu-id="9e220-128">System.String</span></span>

## <span data-ttu-id="9e220-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e220-129">OUTPUTS</span></span>

### <span data-ttu-id="9e220-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9e220-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9e220-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9e220-131">NOTES</span></span>

## <span data-ttu-id="9e220-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9e220-132">RELATED LINKS</span></span>

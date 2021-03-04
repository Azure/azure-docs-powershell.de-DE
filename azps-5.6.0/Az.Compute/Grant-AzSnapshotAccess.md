---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: 215ae1149cdfd939db242907a00b82b1e9fd82a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944243"
---
# <span data-ttu-id="1d769-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="1d769-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="1d769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d769-102">SYNOPSIS</span></span>
<span data-ttu-id="1d769-103">Gewährt einen Zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="1d769-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="1d769-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d769-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1d769-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d769-105">DESCRIPTION</span></span>
<span data-ttu-id="1d769-106">Das **Grant-AzSnapshotAccess-Cmdlet** gewährt zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="1d769-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="1d769-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d769-107">EXAMPLES</span></span>

### <span data-ttu-id="1d769-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1d769-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="1d769-109">Gewähren Sie 60 Sekunden lang "Lesezugriff" auf die Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1d769-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="1d769-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1d769-110">PARAMETERS</span></span>

### <span data-ttu-id="1d769-111">-Access</span><span class="sxs-lookup"><span data-stu-id="1d769-111">-Access</span></span>
<span data-ttu-id="1d769-112">Gibt die Access-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="1d769-112">Specifies Access level.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d769-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d769-113">-AsJob</span></span>
<span data-ttu-id="1d769-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1d769-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d769-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d769-115">-DefaultProfile</span></span>
<span data-ttu-id="1d769-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d769-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d769-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="1d769-117">-DurationInSecond</span></span>
<span data-ttu-id="1d769-118">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="1d769-118">Specifies access duration in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d769-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d769-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d769-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1d769-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1d769-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1d769-121">-SnapshotName</span></span>
<span data-ttu-id="1d769-122">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="1d769-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1d769-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1d769-123">-Confirm</span></span>
<span data-ttu-id="1d769-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1d769-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d769-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d769-125">-WhatIf</span></span>
<span data-ttu-id="1d769-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d769-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d769-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1d769-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d769-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d769-128">CommonParameters</span></span>
<span data-ttu-id="1d769-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d769-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d769-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d769-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d769-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d769-131">INPUTS</span></span>

### <span data-ttu-id="1d769-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1d769-132">System.String</span></span>

## <span data-ttu-id="1d769-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d769-133">OUTPUTS</span></span>

### <span data-ttu-id="1d769-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="1d769-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="1d769-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1d769-135">NOTES</span></span>

## <span data-ttu-id="1d769-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1d769-136">RELATED LINKS</span></span>

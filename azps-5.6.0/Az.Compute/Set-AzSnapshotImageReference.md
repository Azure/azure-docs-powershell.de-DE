---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: 6746bc96f7c1a14d617f3147676556be7402b71c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946624"
---
# <span data-ttu-id="37f5e-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="37f5e-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="37f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="37f5e-103">Legt die Bildreferenzeigenschaften für ein Snapshotobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="37f5e-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="37f5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37f5e-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37f5e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37f5e-105">DESCRIPTION</span></span>
<span data-ttu-id="37f5e-106">Das **Cmdlet Set-AzSnapshotImageReference** legt die Bildreferenzeigenschaften für ein Snapshotobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="37f5e-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="37f5e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37f5e-107">EXAMPLES</span></span>

### <span data-ttu-id="37f5e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37f5e-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="37f5e-109">Mit dem ersten Befehl wird ein lokales Snapshotobjekt mit der Größe 10 GB in Premium_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="37f5e-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="37f5e-110">Außerdem wird der Windows OS-Typ bestimmt.</span><span class="sxs-lookup"><span data-stu-id="37f5e-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="37f5e-111">Mit dem zweiten Befehl werden die Bild-ID und die logische Einheitennummer 0 für das Snapshotobjekt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="37f5e-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="37f5e-112">Der letzte Befehl übernimmt das Snapshotobjekt und erstellt eine Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="37f5e-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="37f5e-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="37f5e-113">PARAMETERS</span></span>

### <span data-ttu-id="37f5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37f5e-114">-DefaultProfile</span></span>
<span data-ttu-id="37f5e-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37f5e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37f5e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="37f5e-116">-Id</span></span>
<span data-ttu-id="37f5e-117">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="37f5e-117">Specifies the ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37f5e-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="37f5e-118">-Lun</span></span>
<span data-ttu-id="37f5e-119">Gibt die Logische Einheitennummer (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="37f5e-119">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37f5e-120">-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="37f5e-120">-Snapshot</span></span>
<span data-ttu-id="37f5e-121">Gibt ein lokales Snapshotobjekt an.</span><span class="sxs-lookup"><span data-stu-id="37f5e-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37f5e-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37f5e-122">-Confirm</span></span>
<span data-ttu-id="37f5e-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37f5e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37f5e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37f5e-124">-WhatIf</span></span>
<span data-ttu-id="37f5e-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37f5e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37f5e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37f5e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37f5e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37f5e-127">CommonParameters</span></span>
<span data-ttu-id="37f5e-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37f5e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37f5e-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37f5e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37f5e-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37f5e-130">INPUTS</span></span>

### <span data-ttu-id="37f5e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="37f5e-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="37f5e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="37f5e-132">System.String</span></span>

### <span data-ttu-id="37f5e-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="37f5e-133">System.Int32</span></span>

## <span data-ttu-id="37f5e-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37f5e-134">OUTPUTS</span></span>

### <span data-ttu-id="37f5e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="37f5e-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="37f5e-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="37f5e-136">NOTES</span></span>

## <span data-ttu-id="37f5e-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="37f5e-137">RELATED LINKS</span></span>

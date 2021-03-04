---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: aed0113b229d41665effd7904d2de2357b4b5d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938851"
---
# <span data-ttu-id="f1e30-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="f1e30-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="f1e30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e30-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e30-103">Legt die Bildreferenzeigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="f1e30-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="f1e30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f1e30-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e30-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f1e30-105">DESCRIPTION</span></span>
<span data-ttu-id="f1e30-106">Das **Cmdlet Set-AzDiskImageReference** legt die Bildreferenzeigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="f1e30-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="f1e30-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f1e30-107">EXAMPLES</span></span>

### <span data-ttu-id="f1e30-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f1e30-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="f1e30-109">Mit dem ersten Befehl wird ein lokales Datenträgerobjekt mit der Größe 10 GB in Premium_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1e30-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f1e30-110">Außerdem wird der Windows OS-Typ bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f1e30-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="f1e30-111">Mit dem zweiten Befehl werden die Bild-ID und die logische Einheitennummer 0 für das Datenträgerobjekt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f1e30-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="f1e30-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f1e30-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f1e30-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f1e30-113">PARAMETERS</span></span>

### <span data-ttu-id="f1e30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e30-114">-DefaultProfile</span></span>
<span data-ttu-id="f1e30-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1e30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e30-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="f1e30-116">-Disk</span></span>
<span data-ttu-id="f1e30-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f1e30-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e30-118">-ID</span><span class="sxs-lookup"><span data-stu-id="f1e30-118">-Id</span></span>
<span data-ttu-id="f1e30-119">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="f1e30-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="f1e30-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="f1e30-120">-Lun</span></span>
<span data-ttu-id="f1e30-121">Gibt die Logische Einheitennummer (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="f1e30-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="f1e30-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f1e30-122">-Confirm</span></span>
<span data-ttu-id="f1e30-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f1e30-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e30-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e30-124">-WhatIf</span></span>
<span data-ttu-id="f1e30-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f1e30-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1e30-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f1e30-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e30-127">CommonParameters</span></span>
<span data-ttu-id="f1e30-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1e30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e30-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1e30-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e30-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f1e30-130">INPUTS</span></span>

### <span data-ttu-id="f1e30-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="f1e30-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="f1e30-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f1e30-132">System.String</span></span>

### <span data-ttu-id="f1e30-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f1e30-133">System.Int32</span></span>

## <span data-ttu-id="f1e30-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f1e30-134">OUTPUTS</span></span>

### <span data-ttu-id="f1e30-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="f1e30-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="f1e30-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f1e30-136">NOTES</span></span>

## <span data-ttu-id="f1e30-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f1e30-137">RELATED LINKS</span></span>

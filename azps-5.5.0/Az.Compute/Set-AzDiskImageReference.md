---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171143"
---
# <span data-ttu-id="d5b05-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="d5b05-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="d5b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5b05-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b05-103">Legt die Bildverweiseigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="d5b05-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="d5b05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5b05-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5b05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5b05-105">DESCRIPTION</span></span>
<span data-ttu-id="d5b05-106">Das **Cmdlet Set-AzDiskImageReference** legt die Bildverweiseigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="d5b05-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="d5b05-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d5b05-107">EXAMPLES</span></span>

### <span data-ttu-id="d5b05-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5b05-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="d5b05-109">Der erste Befehl erstellt ein lokales Datenträgerobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="d5b05-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="d5b05-110">Außerdem wird der Typ des Windows-Betriebssystems bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d5b05-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="d5b05-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="d5b05-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="d5b05-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen 'Disk01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="d5b05-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d5b05-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5b05-113">PARAMETERS</span></span>

### <span data-ttu-id="d5b05-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b05-114">-DefaultProfile</span></span>
<span data-ttu-id="d5b05-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5b05-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5b05-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="d5b05-116">-Disk</span></span>
<span data-ttu-id="d5b05-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="d5b05-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="d5b05-118">-ID</span><span class="sxs-lookup"><span data-stu-id="d5b05-118">-Id</span></span>
<span data-ttu-id="d5b05-119">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="d5b05-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="d5b05-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="d5b05-120">-Lun</span></span>
<span data-ttu-id="d5b05-121">Gibt die Wahrheitsnummer der Einheit (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="d5b05-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="d5b05-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5b05-122">-Confirm</span></span>
<span data-ttu-id="d5b05-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5b05-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b05-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d5b05-124">-WhatIf</span></span>
<span data-ttu-id="d5b05-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b05-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5b05-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5b05-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b05-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b05-127">CommonParameters</span></span>
<span data-ttu-id="d5b05-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b05-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b05-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5b05-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b05-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d5b05-130">INPUTS</span></span>

### <span data-ttu-id="d5b05-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="d5b05-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="d5b05-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d5b05-132">System.String</span></span>

### <span data-ttu-id="d5b05-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d5b05-133">System.Int32</span></span>

## <span data-ttu-id="d5b05-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d5b05-134">OUTPUTS</span></span>

### <span data-ttu-id="d5b05-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="d5b05-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="d5b05-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d5b05-136">NOTES</span></span>

## <span data-ttu-id="d5b05-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d5b05-137">RELATED LINKS</span></span>

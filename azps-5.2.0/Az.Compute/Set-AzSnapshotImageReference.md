---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370388"
---
# <span data-ttu-id="5cbea-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="5cbea-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="5cbea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cbea-102">SYNOPSIS</span></span>
<span data-ttu-id="5cbea-103">Legt die Bildverweiseigenschaften für ein Momentaufnahmeobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="5cbea-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="5cbea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5cbea-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cbea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5cbea-105">DESCRIPTION</span></span>
<span data-ttu-id="5cbea-106">Das **Cmdlet "Set-AzSnapshotImageReference"** legt die Bildverweiseigenschaften für ein Momentaufnahmeobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="5cbea-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="5cbea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5cbea-107">EXAMPLES</span></span>

### <span data-ttu-id="5cbea-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5cbea-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="5cbea-109">Der erste Befehl erstellt ein lokales Momentaufnahmeobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="5cbea-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="5cbea-110">Außerdem wird der Typ des Windows-Betriebssystems bestimmt.</span><span class="sxs-lookup"><span data-stu-id="5cbea-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="5cbea-111">Der zweite Befehl legt die Bild-ID und die logische Einheitsnummer 0 für das Momentaufnahmeobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="5cbea-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="5cbea-112">Der letzte Befehl erstellt das Momentaufnahmeobjekt und erstellt eine Momentaufnahme mit dem Namen 'Snapshot01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="5cbea-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="5cbea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cbea-113">PARAMETERS</span></span>

### <span data-ttu-id="5cbea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cbea-114">-DefaultProfile</span></span>
<span data-ttu-id="5cbea-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cbea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cbea-116">-ID</span><span class="sxs-lookup"><span data-stu-id="5cbea-116">-Id</span></span>
<span data-ttu-id="5cbea-117">Gibt die ID an.</span><span class="sxs-lookup"><span data-stu-id="5cbea-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="5cbea-118">-Lun</span><span class="sxs-lookup"><span data-stu-id="5cbea-118">-Lun</span></span>
<span data-ttu-id="5cbea-119">Gibt die Wahrheitsnummer der Einheit (LUN) an.</span><span class="sxs-lookup"><span data-stu-id="5cbea-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="5cbea-120">-Snapshot</span><span class="sxs-lookup"><span data-stu-id="5cbea-120">-Snapshot</span></span>
<span data-ttu-id="5cbea-121">Gibt ein lokales Momentaufnahmeobjekt an.</span><span class="sxs-lookup"><span data-stu-id="5cbea-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="5cbea-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cbea-122">-Confirm</span></span>
<span data-ttu-id="5cbea-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cbea-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cbea-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5cbea-124">-WhatIf</span></span>
<span data-ttu-id="5cbea-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cbea-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cbea-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cbea-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cbea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cbea-127">CommonParameters</span></span>
<span data-ttu-id="5cbea-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cbea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cbea-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cbea-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cbea-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5cbea-130">INPUTS</span></span>

### <span data-ttu-id="5cbea-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="5cbea-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="5cbea-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5cbea-132">System.String</span></span>

### <span data-ttu-id="5cbea-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5cbea-133">System.Int32</span></span>

## <span data-ttu-id="5cbea-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5cbea-134">OUTPUTS</span></span>

### <span data-ttu-id="5cbea-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="5cbea-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="5cbea-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5cbea-136">NOTES</span></span>

## <span data-ttu-id="5cbea-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5cbea-137">RELATED LINKS</span></span>

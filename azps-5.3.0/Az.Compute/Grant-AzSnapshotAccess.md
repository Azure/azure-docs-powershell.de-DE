---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/grant-azsnapshotaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Grant-AzSnapshotAccess.md
ms.openlocfilehash: a431428c670dba7e0bfb152bde0cae22f47d8099
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470885"
---
# <span data-ttu-id="da5fc-101">Grant-AzSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="da5fc-101">Grant-AzSnapshotAccess</span></span>

## <span data-ttu-id="da5fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da5fc-102">SYNOPSIS</span></span>
<span data-ttu-id="da5fc-103">Gewährt zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="da5fc-103">Grants an access to a snapshot.</span></span>

## <span data-ttu-id="da5fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da5fc-104">SYNTAX</span></span>

```
Grant-AzSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-Access] <String>
 [[-DurationInSecond] <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da5fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da5fc-105">DESCRIPTION</span></span>
<span data-ttu-id="da5fc-106">Das **Cmdlet Grant-AzSnapshotAccess** gewährt zugriff auf eine Momentaufnahme.</span><span class="sxs-lookup"><span data-stu-id="da5fc-106">The **Grant-AzSnapshotAccess** cmdlet grants an access to a snapshot.</span></span>

## <span data-ttu-id="da5fc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="da5fc-107">EXAMPLES</span></span>

### <span data-ttu-id="da5fc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da5fc-108">Example 1</span></span>
```
PS C:\> Grant-AzSnapshotAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Access 'Read' -DurationInSecond 60;
```

<span data-ttu-id="da5fc-109">Gewähren Sie Lesezugriff auf die Momentaufnahme mit dem Namen "Snapshot01" in der Ressourcengruppe mit dem Namen "ResourceGroup01" 60 Sekunden lang.</span><span class="sxs-lookup"><span data-stu-id="da5fc-109">Grant 'Read' access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01' for 60 seconds.</span></span>

## <span data-ttu-id="da5fc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da5fc-110">PARAMETERS</span></span>

### <span data-ttu-id="da5fc-111">-Access</span><span class="sxs-lookup"><span data-stu-id="da5fc-111">-Access</span></span>
<span data-ttu-id="da5fc-112">Gibt die Zugriffsebene an.</span><span class="sxs-lookup"><span data-stu-id="da5fc-112">Specifies Access level.</span></span>

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

### <span data-ttu-id="da5fc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da5fc-113">-AsJob</span></span>
<span data-ttu-id="da5fc-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="da5fc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da5fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5fc-115">-DefaultProfile</span></span>
<span data-ttu-id="da5fc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da5fc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da5fc-117">-DurationInSecond</span><span class="sxs-lookup"><span data-stu-id="da5fc-117">-DurationInSecond</span></span>
<span data-ttu-id="da5fc-118">Gibt die Zugriffsdauer in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="da5fc-118">Specifies access duration in seconds.</span></span>

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

### <span data-ttu-id="da5fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da5fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="da5fc-120">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="da5fc-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="da5fc-121">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="da5fc-121">-SnapshotName</span></span>
<span data-ttu-id="da5fc-122">Gibt den Namen einer Momentaufnahme an.</span><span class="sxs-lookup"><span data-stu-id="da5fc-122">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="da5fc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da5fc-123">-Confirm</span></span>
<span data-ttu-id="da5fc-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da5fc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da5fc-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="da5fc-125">-WhatIf</span></span>
<span data-ttu-id="da5fc-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da5fc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da5fc-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da5fc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da5fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5fc-128">CommonParameters</span></span>
<span data-ttu-id="da5fc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5fc-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da5fc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5fc-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="da5fc-131">INPUTS</span></span>

### <span data-ttu-id="da5fc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="da5fc-132">System.String</span></span>

## <span data-ttu-id="da5fc-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="da5fc-133">OUTPUTS</span></span>

### <span data-ttu-id="da5fc-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span><span class="sxs-lookup"><span data-stu-id="da5fc-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSAccessUri</span></span>

## <span data-ttu-id="da5fc-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="da5fc-135">NOTES</span></span>

## <span data-ttu-id="da5fc-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="da5fc-136">RELATED LINKS</span></span>

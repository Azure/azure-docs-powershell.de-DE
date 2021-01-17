---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458931"
---
# <span data-ttu-id="5fe82-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="5fe82-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="5fe82-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fe82-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe82-103">Den Status der Replikation erhalten</span><span class="sxs-lookup"><span data-stu-id="5fe82-103">Get the status of the replication</span></span>

## <span data-ttu-id="5fe82-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fe82-104">SYNTAX</span></span>

### <span data-ttu-id="5fe82-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fe82-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fe82-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fe82-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5fe82-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fe82-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fe82-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fe82-108">DESCRIPTION</span></span>
<span data-ttu-id="5fe82-109">Den Status der Replikation erhalten</span><span class="sxs-lookup"><span data-stu-id="5fe82-109">Get the status of the replication</span></span>

## <span data-ttu-id="5fe82-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fe82-110">EXAMPLES</span></span>

### <span data-ttu-id="5fe82-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5fe82-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="5fe82-112">Dieser Befehl ruft den Status der Replikation für MyVol ab.</span><span class="sxs-lookup"><span data-stu-id="5fe82-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="5fe82-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fe82-113">PARAMETERS</span></span>

### <span data-ttu-id="5fe82-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5fe82-114">-AccountName</span></span>
<span data-ttu-id="5fe82-115">Der Name des ANF-Kontos des Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5fe82-115">The name of the ANF account of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe82-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe82-116">-DefaultProfile</span></span>
<span data-ttu-id="5fe82-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fe82-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fe82-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fe82-118">-InputObject</span></span>
<span data-ttu-id="5fe82-119">Das Zielvolumeobjekt für die ANF-Replikation, um den Replikationsstatus zu erhalten</span><span class="sxs-lookup"><span data-stu-id="5fe82-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5fe82-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5fe82-120">-Name</span></span>
<span data-ttu-id="5fe82-121">Der Name des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5fe82-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe82-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="5fe82-122">-PoolName</span></span>
<span data-ttu-id="5fe82-123">Der Name des ANF-Pools des Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5fe82-123">The name of the ANF pool of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe82-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe82-124">-ResourceGroupName</span></span>
<span data-ttu-id="5fe82-125">Die Ressourcengruppe des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5fe82-125">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fe82-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fe82-126">-ResourceId</span></span>
<span data-ttu-id="5fe82-127">Die Ressourcen-ID des ANF-Replikationszielvolumes</span><span class="sxs-lookup"><span data-stu-id="5fe82-127">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fe82-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe82-128">CommonParameters</span></span>
<span data-ttu-id="5fe82-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe82-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe82-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fe82-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe82-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fe82-131">INPUTS</span></span>

### <span data-ttu-id="5fe82-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5fe82-132">System.String</span></span>

### <span data-ttu-id="5fe82-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5fe82-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5fe82-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fe82-134">OUTPUTS</span></span>

### <span data-ttu-id="5fe82-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="5fe82-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="5fe82-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5fe82-136">NOTES</span></span>

## <span data-ttu-id="5fe82-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5fe82-137">RELATED LINKS</span></span>

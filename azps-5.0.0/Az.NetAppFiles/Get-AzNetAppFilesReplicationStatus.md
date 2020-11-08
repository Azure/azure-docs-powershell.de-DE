---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177816"
---
# <span data-ttu-id="100a6-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="100a6-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="100a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="100a6-102">SYNOPSIS</span></span>
<span data-ttu-id="100a6-103">Abrufen des Replikationsstatus</span><span class="sxs-lookup"><span data-stu-id="100a6-103">Get the status of the replication</span></span>

## <span data-ttu-id="100a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="100a6-104">SYNTAX</span></span>

### <span data-ttu-id="100a6-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="100a6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="100a6-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="100a6-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="100a6-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="100a6-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="100a6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="100a6-108">DESCRIPTION</span></span>
<span data-ttu-id="100a6-109">Abrufen des Replikationsstatus</span><span class="sxs-lookup"><span data-stu-id="100a6-109">Get the status of the replication</span></span>

## <span data-ttu-id="100a6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="100a6-110">EXAMPLES</span></span>

### <span data-ttu-id="100a6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="100a6-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="100a6-112">Dieser Befehl ruft den Replikationsstatus auf MyVol</span><span class="sxs-lookup"><span data-stu-id="100a6-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="100a6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="100a6-113">PARAMETERS</span></span>

### <span data-ttu-id="100a6-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="100a6-114">-AccountName</span></span>
<span data-ttu-id="100a6-115">Der Name des ANF-Kontos des Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="100a6-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="100a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100a6-116">-DefaultProfile</span></span>
<span data-ttu-id="100a6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="100a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="100a6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="100a6-118">-InputObject</span></span>
<span data-ttu-id="100a6-119">Das ANF-Replikationsziel Volumen Objekt zum Abrufen des Replikationsstatus</span><span class="sxs-lookup"><span data-stu-id="100a6-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="100a6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="100a6-120">-Name</span></span>
<span data-ttu-id="100a6-121">Der Name des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="100a6-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="100a6-122">-Poolname</span><span class="sxs-lookup"><span data-stu-id="100a6-122">-PoolName</span></span>
<span data-ttu-id="100a6-123">Der Name des ANF-Pools des Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="100a6-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="100a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="100a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="100a6-125">Die Ressourcengruppe des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="100a6-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="100a6-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="100a6-126">-ResourceId</span></span>
<span data-ttu-id="100a6-127">Die Ressourcen-ID des ANF-Replikationsziel Datenträgers</span><span class="sxs-lookup"><span data-stu-id="100a6-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="100a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100a6-128">CommonParameters</span></span>
<span data-ttu-id="100a6-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="100a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100a6-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="100a6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100a6-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="100a6-131">INPUTS</span></span>

### <span data-ttu-id="100a6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="100a6-132">System.String</span></span>

## <span data-ttu-id="100a6-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="100a6-133">OUTPUTS</span></span>

### <span data-ttu-id="100a6-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="100a6-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="100a6-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="100a6-135">NOTES</span></span>

## <span data-ttu-id="100a6-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="100a6-136">RELATED LINKS</span></span>

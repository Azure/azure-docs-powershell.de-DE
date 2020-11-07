---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: b41acc1d10a09febec04b60c397496b97606fb18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845063"
---
# <span data-ttu-id="5f4c4-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="5f4c4-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="5f4c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5f4c4-103">Ruft Details zu einem Azure NetApp-Dateien (ANF)-Snapshot ab.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="5f4c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f4c4-104">SYNTAX</span></span>

### <span data-ttu-id="5f4c4-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5f4c4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f4c4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f4c4-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5f4c4-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f4c4-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f4c4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f4c4-108">DESCRIPTION</span></span>
<span data-ttu-id="5f4c4-109">Das Cmdlet " **Get-AzNetAppFilesSnapshot** " ruft Details zu einem ANF-Snapshot ab.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="5f4c4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f4c4-110">EXAMPLES</span></span>

### <span data-ttu-id="5f4c4-111">Beispiel 1: Abrufen eines ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="5f4c4-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="5f4c4-112">Dieser Befehl ruft den Snapshot mit dem Namen MyAnfSnapshot aus dem Volume "MyAnfVolume" ab.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="5f4c4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f4c4-113">PARAMETERS</span></span>

### <span data-ttu-id="5f4c4-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5f4c4-114">-AccountName</span></span>
<span data-ttu-id="5f4c4-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="5f4c4-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f4c4-116">-DefaultProfile</span></span>
<span data-ttu-id="5f4c4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5f4c4-118">-Name</span></span>
<span data-ttu-id="5f4c4-119">Der Name des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="5f4c4-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-120">-Poolname</span><span class="sxs-lookup"><span data-stu-id="5f4c4-120">-PoolName</span></span>
<span data-ttu-id="5f4c4-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="5f4c4-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f4c4-122">-ResourceGroupName</span></span>
<span data-ttu-id="5f4c4-123">Die Ressourcengruppe des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="5f4c4-123">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5f4c4-124">-ResourceId</span></span>
<span data-ttu-id="5f4c4-125">Die Ressourcen-ID des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="5f4c4-125">The resource id of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-126">-Volumename</span><span class="sxs-lookup"><span data-stu-id="5f4c4-126">-VolumeName</span></span>
<span data-ttu-id="5f4c4-127">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="5f4c4-127">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-128">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="5f4c4-128">-VolumeObject</span></span>
<span data-ttu-id="5f4c4-129">Das Volume-Objekt, das den zurückzugebenden Snapshot enthält</span><span class="sxs-lookup"><span data-stu-id="5f4c4-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f4c4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f4c4-130">CommonParameters</span></span>
<span data-ttu-id="5f4c4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f4c4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5f4c4-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f4c4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f4c4-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f4c4-133">INPUTS</span></span>

### <span data-ttu-id="5f4c4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5f4c4-134">System.String</span></span>

### <span data-ttu-id="5f4c4-135">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="5f4c4-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="5f4c4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f4c4-136">OUTPUTS</span></span>

### <span data-ttu-id="5f4c4-137">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="5f4c4-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="5f4c4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f4c4-138">NOTES</span></span>

## <span data-ttu-id="5f4c4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f4c4-139">RELATED LINKS</span></span>

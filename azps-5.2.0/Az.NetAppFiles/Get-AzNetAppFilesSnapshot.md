---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360043"
---
# <span data-ttu-id="de1b0-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="de1b0-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="de1b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="de1b0-103">Ruft Details einer Azure NetApp Files (ANF)-Momentaufnahme ab.</span><span class="sxs-lookup"><span data-stu-id="de1b0-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="de1b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de1b0-104">SYNTAX</span></span>

### <span data-ttu-id="de1b0-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="de1b0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de1b0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de1b0-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de1b0-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de1b0-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de1b0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de1b0-108">DESCRIPTION</span></span>
<span data-ttu-id="de1b0-109">Das **Cmdlet "Get-AzNetAppFilesSnapshot"** ruft Details zu einer ANF-Momentaufnahme ab.</span><span class="sxs-lookup"><span data-stu-id="de1b0-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="de1b0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de1b0-110">EXAMPLES</span></span>

### <span data-ttu-id="de1b0-111">Beispiel 1: Erhalten einer ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="de1b0-111">Example 1: Get an ANF snapshot</span></span>
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

<span data-ttu-id="de1b0-112">Dieser Befehl ruft die Momentaufnahme namens "MyAnfSnapshot" aus dem Volumen "MyAnfVolume" ab.</span><span class="sxs-lookup"><span data-stu-id="de1b0-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="de1b0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de1b0-113">PARAMETERS</span></span>

### <span data-ttu-id="de1b0-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="de1b0-114">-AccountName</span></span>
<span data-ttu-id="de1b0-115">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="de1b0-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="de1b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1b0-116">-DefaultProfile</span></span>
<span data-ttu-id="de1b0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de1b0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de1b0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="de1b0-118">-Name</span></span>
<span data-ttu-id="de1b0-119">Der Name der ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="de1b0-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de1b0-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="de1b0-120">-PoolName</span></span>
<span data-ttu-id="de1b0-121">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="de1b0-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="de1b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de1b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="de1b0-123">Die Ressourcengruppe des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="de1b0-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="de1b0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de1b0-124">-ResourceId</span></span>
<span data-ttu-id="de1b0-125">Die Ressourcen-ID der ANF-Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="de1b0-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="de1b0-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="de1b0-126">-VolumeName</span></span>
<span data-ttu-id="de1b0-127">Der Name des ANF-Volumens</span><span class="sxs-lookup"><span data-stu-id="de1b0-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="de1b0-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="de1b0-128">-VolumeObject</span></span>
<span data-ttu-id="de1b0-129">Das Volumenobjekt mit der zurückzukehrenden Momentaufnahme</span><span class="sxs-lookup"><span data-stu-id="de1b0-129">The volume object containing the snapshot to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de1b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1b0-130">CommonParameters</span></span>
<span data-ttu-id="de1b0-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de1b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1b0-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="de1b0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1b0-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de1b0-133">INPUTS</span></span>

### <span data-ttu-id="de1b0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="de1b0-134">System.String</span></span>

### <span data-ttu-id="de1b0-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="de1b0-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="de1b0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de1b0-136">OUTPUTS</span></span>

### <span data-ttu-id="de1b0-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="de1b0-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="de1b0-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="de1b0-138">NOTES</span></span>

## <span data-ttu-id="de1b0-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="de1b0-139">RELATED LINKS</span></span>

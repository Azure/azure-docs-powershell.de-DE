---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 47383ee57d527f6348781e57ed965e1ed8d36ef2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845056"
---
# <span data-ttu-id="f183e-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f183e-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="f183e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f183e-102">SYNOPSIS</span></span>
<span data-ttu-id="f183e-103">Erstellt einen neuen Azure NetApp-Dateien (ANF)-Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="f183e-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="f183e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f183e-104">SYNTAX</span></span>

### <span data-ttu-id="f183e-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f183e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f183e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f183e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f183e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f183e-107">DESCRIPTION</span></span>
<span data-ttu-id="f183e-108">Das Cmdlet **New-AzNetAppFilesSnapshot** erstellt einen ANF-Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="f183e-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="f183e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f183e-109">EXAMPLES</span></span>

### <span data-ttu-id="f183e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f183e-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="f183e-111">Dieser Befehl erstellt den neuen ANF-Schnappschuss "MyAnfSnapshot" innerhalb des Volumes "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="f183e-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="f183e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f183e-112">PARAMETERS</span></span>

### <span data-ttu-id="f183e-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="f183e-113">-AccountName</span></span>
<span data-ttu-id="f183e-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="f183e-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="f183e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f183e-115">-DefaultProfile</span></span>
<span data-ttu-id="f183e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f183e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f183e-117">-Dateisystem-Nr</span><span class="sxs-lookup"><span data-stu-id="f183e-117">-FileSystemId</span></span>
<span data-ttu-id="f183e-118">Die Dateisystem-ID</span><span class="sxs-lookup"><span data-stu-id="f183e-118">The file system id</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="f183e-119">-Location</span></span>
<span data-ttu-id="f183e-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="f183e-120">The location of the resource</span></span>

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

### <span data-ttu-id="f183e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f183e-121">-Name</span></span>
<span data-ttu-id="f183e-122">Der Name des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="f183e-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-123">-Poolname</span><span class="sxs-lookup"><span data-stu-id="f183e-123">-PoolName</span></span>
<span data-ttu-id="f183e-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="f183e-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="f183e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f183e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f183e-126">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="f183e-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="f183e-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f183e-127">-Tag</span></span>
<span data-ttu-id="f183e-128">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="f183e-128">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-129">-Volumename</span><span class="sxs-lookup"><span data-stu-id="f183e-129">-VolumeName</span></span>
<span data-ttu-id="f183e-130">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="f183e-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="f183e-131">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="f183e-131">-VolumeObject</span></span>
<span data-ttu-id="f183e-132">Die Lautstärke des neuen Snapshot-Objekts</span><span class="sxs-lookup"><span data-stu-id="f183e-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="f183e-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f183e-133">-Confirm</span></span>
<span data-ttu-id="f183e-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f183e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f183e-135">-WhatIf</span></span>
<span data-ttu-id="f183e-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f183e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f183e-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f183e-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f183e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f183e-138">CommonParameters</span></span>
<span data-ttu-id="f183e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f183e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f183e-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f183e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f183e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f183e-141">INPUTS</span></span>

### <span data-ttu-id="f183e-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="f183e-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="f183e-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f183e-143">OUTPUTS</span></span>

### <span data-ttu-id="f183e-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="f183e-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="f183e-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="f183e-145">NOTES</span></span>

## <span data-ttu-id="f183e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f183e-146">RELATED LINKS</span></span>

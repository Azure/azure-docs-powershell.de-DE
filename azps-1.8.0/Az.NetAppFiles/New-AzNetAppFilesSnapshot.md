---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: bad4c1dfc2317bcc4d03414980cafa73c78949d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660977"
---
# <span data-ttu-id="18e9d-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="18e9d-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="18e9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="18e9d-102">SYNOPSIS</span></span>
<span data-ttu-id="18e9d-103">Erstellt einen neuen Azure NetApp-Dateien (ANF)-Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="18e9d-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="18e9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="18e9d-104">SYNTAX</span></span>

### <span data-ttu-id="18e9d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="18e9d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> -FileSystemId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e9d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="18e9d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18e9d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18e9d-107">DESCRIPTION</span></span>
<span data-ttu-id="18e9d-108">Das Cmdlet **New-AzNetAppFilesSnapshot** erstellt einen ANF-Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="18e9d-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="18e9d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="18e9d-109">EXAMPLES</span></span>

### <span data-ttu-id="18e9d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="18e9d-110">Example 1</span></span>
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
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="18e9d-111">Dieser Befehl erstellt den neuen ANF-Schnappschuss "MyAnfSnapshot" innerhalb des Volumes "MyAnfVolume".</span><span class="sxs-lookup"><span data-stu-id="18e9d-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="18e9d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="18e9d-112">PARAMETERS</span></span>

### <span data-ttu-id="18e9d-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="18e9d-113">-AccountName</span></span>
<span data-ttu-id="18e9d-114">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="18e9d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="18e9d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e9d-115">-DefaultProfile</span></span>
<span data-ttu-id="18e9d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="18e9d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18e9d-117">-Dateisystem-Nr</span><span class="sxs-lookup"><span data-stu-id="18e9d-117">-FileSystemId</span></span>
<span data-ttu-id="18e9d-118">Die Dateisystem-ID</span><span class="sxs-lookup"><span data-stu-id="18e9d-118">The file system id</span></span>

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

### <span data-ttu-id="18e9d-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="18e9d-119">-Location</span></span>
<span data-ttu-id="18e9d-120">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="18e9d-120">The location of the resource</span></span>

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

### <span data-ttu-id="18e9d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="18e9d-121">-Name</span></span>
<span data-ttu-id="18e9d-122">Der Name des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="18e9d-122">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="18e9d-123">-Poolname</span><span class="sxs-lookup"><span data-stu-id="18e9d-123">-PoolName</span></span>
<span data-ttu-id="18e9d-124">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="18e9d-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="18e9d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e9d-125">-ResourceGroupName</span></span>
<span data-ttu-id="18e9d-126">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="18e9d-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="18e9d-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="18e9d-127">-Tag</span></span>
<span data-ttu-id="18e9d-128">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="18e9d-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="18e9d-129">-Volumename</span><span class="sxs-lookup"><span data-stu-id="18e9d-129">-VolumeName</span></span>
<span data-ttu-id="18e9d-130">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="18e9d-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="18e9d-131">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="18e9d-131">-VolumeObject</span></span>
<span data-ttu-id="18e9d-132">Die Lautstärke des neuen Snapshot-Objekts</span><span class="sxs-lookup"><span data-stu-id="18e9d-132">The volume for the new snapshot object</span></span>

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

### <span data-ttu-id="18e9d-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="18e9d-133">-Confirm</span></span>
<span data-ttu-id="18e9d-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="18e9d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e9d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e9d-135">-WhatIf</span></span>
<span data-ttu-id="18e9d-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="18e9d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18e9d-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="18e9d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e9d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e9d-138">CommonParameters</span></span>
<span data-ttu-id="18e9d-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e9d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="18e9d-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e9d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e9d-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="18e9d-141">INPUTS</span></span>

### <span data-ttu-id="18e9d-142">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="18e9d-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="18e9d-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="18e9d-143">OUTPUTS</span></span>

### <span data-ttu-id="18e9d-144">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="18e9d-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="18e9d-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="18e9d-145">NOTES</span></span>

## <span data-ttu-id="18e9d-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="18e9d-146">RELATED LINKS</span></span>

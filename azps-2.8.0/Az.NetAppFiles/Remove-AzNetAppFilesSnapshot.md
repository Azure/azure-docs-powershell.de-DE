---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 16eb962245502338c7b12f6e5abf20a9bc04b83f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822583"
---
# <span data-ttu-id="8b6cc-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8b6cc-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="8b6cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8b6cc-103">Löscht einen Azure NetApp-Dateien (ANF)-Schnappschuss.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="8b6cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b6cc-104">SYNTAX</span></span>

### <span data-ttu-id="8b6cc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b6cc-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6cc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b6cc-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6cc-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b6cc-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b6cc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b6cc-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b6cc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b6cc-109">DESCRIPTION</span></span>
<span data-ttu-id="8b6cc-110">Das Cmdlet **Remove-AzNetAppFilesSnapshot** löscht einen ANF-Snapshot.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="8b6cc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b6cc-111">EXAMPLES</span></span>

### <span data-ttu-id="8b6cc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b6cc-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="8b6cc-113">Mit diesem Befehl wird der Anf-Schnappschuss "MyAnfSnapshot" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="8b6cc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b6cc-114">PARAMETERS</span></span>

### <span data-ttu-id="8b6cc-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="8b6cc-115">-AccountName</span></span>
<span data-ttu-id="8b6cc-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="8b6cc-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="8b6cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b6cc-117">-DefaultProfile</span></span>
<span data-ttu-id="8b6cc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b6cc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b6cc-119">-InputObject</span></span>
<span data-ttu-id="8b6cc-120">Das zu entfernende Snapshot-Objekt</span><span class="sxs-lookup"><span data-stu-id="8b6cc-120">The snapshot object to remove</span></span>

```yaml
Type: PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b6cc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b6cc-121">-Name</span></span>
<span data-ttu-id="8b6cc-122">Der Name des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="8b6cc-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6cc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b6cc-123">-PassThru</span></span>
<span data-ttu-id="8b6cc-124">Zurückgeben, ob das angegebene Volume erfolgreich entfernt wurde</span><span class="sxs-lookup"><span data-stu-id="8b6cc-124">Return whether the specified volume was successfully removed</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b6cc-125">-Poolname</span><span class="sxs-lookup"><span data-stu-id="8b6cc-125">-PoolName</span></span>
<span data-ttu-id="8b6cc-126">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="8b6cc-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="8b6cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b6cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="8b6cc-128">Die Ressourcengruppe des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="8b6cc-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="8b6cc-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8b6cc-129">-ResourceId</span></span>
<span data-ttu-id="8b6cc-130">Die Ressourcen-ID des ANF-Snapshots</span><span class="sxs-lookup"><span data-stu-id="8b6cc-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="8b6cc-131">-Volumename</span><span class="sxs-lookup"><span data-stu-id="8b6cc-131">-VolumeName</span></span>
<span data-ttu-id="8b6cc-132">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="8b6cc-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="8b6cc-133">-Volumeobject</span><span class="sxs-lookup"><span data-stu-id="8b6cc-133">-VolumeObject</span></span>
<span data-ttu-id="8b6cc-134">Das Volume-Objekt, das den zu entfernenden Snapshot enthält</span><span class="sxs-lookup"><span data-stu-id="8b6cc-134">The volume object containing the snapshot to remove</span></span>

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

### <span data-ttu-id="8b6cc-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b6cc-135">-Confirm</span></span>
<span data-ttu-id="8b6cc-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b6cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b6cc-137">-WhatIf</span></span>
<span data-ttu-id="8b6cc-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b6cc-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b6cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b6cc-140">CommonParameters</span></span>
<span data-ttu-id="8b6cc-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b6cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8b6cc-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b6cc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b6cc-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b6cc-143">INPUTS</span></span>

### <span data-ttu-id="8b6cc-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8b6cc-144">System.String</span></span>

### <span data-ttu-id="8b6cc-145">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="8b6cc-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="8b6cc-146">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="8b6cc-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="8b6cc-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b6cc-147">OUTPUTS</span></span>

### <span data-ttu-id="8b6cc-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b6cc-148">System.Boolean</span></span>

## <span data-ttu-id="8b6cc-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b6cc-149">NOTES</span></span>

## <span data-ttu-id="8b6cc-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b6cc-150">RELATED LINKS</span></span>

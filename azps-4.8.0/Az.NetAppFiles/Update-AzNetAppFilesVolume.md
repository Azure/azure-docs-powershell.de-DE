---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007933"
---
# <span data-ttu-id="ad24d-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ad24d-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="ad24d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad24d-102">SYNOPSIS</span></span>
<span data-ttu-id="ad24d-103">Aktualisiert ein Azure NetApp-Dateien (ANF)-Volume entsprechend den bereitgestellten optionalen Modifizierer.</span><span class="sxs-lookup"><span data-stu-id="ad24d-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="ad24d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad24d-104">SYNTAX</span></span>

### <span data-ttu-id="ad24d-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad24d-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad24d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad24d-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad24d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad24d-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad24d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad24d-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad24d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad24d-109">DESCRIPTION</span></span>
<span data-ttu-id="ad24d-110">Das Cmdlet **Update-AzNetAppFilesVolume** aktualisiert ein ANF-Volume.</span><span class="sxs-lookup"><span data-stu-id="ad24d-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="ad24d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad24d-111">EXAMPLES</span></span>

### <span data-ttu-id="ad24d-112">Beispiel 1: Aktualisieren eines ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="ad24d-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="ad24d-113">Mit diesem Befehl wird das ANF-Volumen "MyAnfVolume" mit der neuen UsageThreshold-Größe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ad24d-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="ad24d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad24d-114">PARAMETERS</span></span>

### <span data-ttu-id="ad24d-115">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ad24d-115">-AccountName</span></span>
<span data-ttu-id="ad24d-116">Der Name des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="ad24d-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="ad24d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad24d-117">-DefaultProfile</span></span>
<span data-ttu-id="ad24d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad24d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad24d-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="ad24d-119">-ExportPolicy</span></span>
<span data-ttu-id="ad24d-120">Ein Hashtable-Array, das die Export Richtlinie darstellt</span><span class="sxs-lookup"><span data-stu-id="ad24d-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad24d-121">-InputObject</span></span>
<span data-ttu-id="ad24d-122">Das zu aktualisierbare Volume-Objekt</span><span class="sxs-lookup"><span data-stu-id="ad24d-122">The volume object to update</span></span>

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

### <span data-ttu-id="ad24d-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="ad24d-123">-Location</span></span>
<span data-ttu-id="ad24d-124">Der Speicherort der Ressource</span><span class="sxs-lookup"><span data-stu-id="ad24d-124">The location of the resource</span></span>

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

### <span data-ttu-id="ad24d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ad24d-125">-Name</span></span>
<span data-ttu-id="ad24d-126">Der Name des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="ad24d-126">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24d-127">-Poolname</span><span class="sxs-lookup"><span data-stu-id="ad24d-127">-PoolName</span></span>
<span data-ttu-id="ad24d-128">Der Name des ANF-Pools</span><span class="sxs-lookup"><span data-stu-id="ad24d-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ad24d-129">-Poolobject</span><span class="sxs-lookup"><span data-stu-id="ad24d-129">-PoolObject</span></span>
<span data-ttu-id="ad24d-130">Das Pool-Objekt, das das zu aktualisierbare Volume enthält</span><span class="sxs-lookup"><span data-stu-id="ad24d-130">The pool object containing the volume to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad24d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad24d-131">-ResourceGroupName</span></span>
<span data-ttu-id="ad24d-132">Die Ressourcengruppe des ANF-Kontos</span><span class="sxs-lookup"><span data-stu-id="ad24d-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="ad24d-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ad24d-133">-ResourceId</span></span>
<span data-ttu-id="ad24d-134">Die Ressourcen-ID des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="ad24d-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="ad24d-135">-Service Level</span><span class="sxs-lookup"><span data-stu-id="ad24d-135">-ServiceLevel</span></span>
<span data-ttu-id="ad24d-136">Die Dienstebene des ANF-Volumes</span><span class="sxs-lookup"><span data-stu-id="ad24d-136">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24d-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ad24d-137">-Tag</span></span>
<span data-ttu-id="ad24d-138">Eine Hashtable, die Ressourcenkategorien darstellt</span><span class="sxs-lookup"><span data-stu-id="ad24d-138">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24d-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="ad24d-139">-UsageThreshold</span></span>
<span data-ttu-id="ad24d-140">Das maximal zulässige Speicherkontingent für ein Dateisystem in Byte</span><span class="sxs-lookup"><span data-stu-id="ad24d-140">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad24d-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ad24d-141">-Confirm</span></span>
<span data-ttu-id="ad24d-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ad24d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad24d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad24d-143">-WhatIf</span></span>
<span data-ttu-id="ad24d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad24d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad24d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad24d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad24d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad24d-146">CommonParameters</span></span>
<span data-ttu-id="ad24d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad24d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad24d-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad24d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad24d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad24d-149">INPUTS</span></span>

### <span data-ttu-id="ad24d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="ad24d-150">System.String</span></span>

### <span data-ttu-id="ad24d-151">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="ad24d-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="ad24d-152">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ad24d-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ad24d-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad24d-153">OUTPUTS</span></span>

### <span data-ttu-id="ad24d-154">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ad24d-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ad24d-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad24d-155">NOTES</span></span>

## <span data-ttu-id="ad24d-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad24d-156">RELATED LINKS</span></span>

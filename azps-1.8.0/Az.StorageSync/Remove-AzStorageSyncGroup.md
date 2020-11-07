---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658687"
---
# <span data-ttu-id="fc72b-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc72b-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="fc72b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc72b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc72b-103">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fc72b-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="fc72b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc72b-104">SYNTAX</span></span>

### <span data-ttu-id="fc72b-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc72b-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc72b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc72b-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc72b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc72b-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc72b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc72b-108">DESCRIPTION</span></span>
<span data-ttu-id="fc72b-109">Mit diesem Befehl wird die angegebene Synchronisierungsgruppe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="fc72b-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="fc72b-110">Eine Synchronisierungsgruppe kann nur entfernt werden, wenn alle enthaltenen Endpunkte zuerst gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fc72b-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="fc72b-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc72b-111">EXAMPLES</span></span>

### <span data-ttu-id="fc72b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc72b-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="fc72b-113">Mit diesem Befehl wird die Synchronisierungsgruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="fc72b-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="fc72b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc72b-114">PARAMETERS</span></span>

### <span data-ttu-id="fc72b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc72b-115">-AsJob</span></span>
<span data-ttu-id="fc72b-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fc72b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc72b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc72b-117">-DefaultProfile</span></span>
<span data-ttu-id="fc72b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc72b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fc72b-119">-Force</span></span>
<span data-ttu-id="fc72b-120">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="fc72b-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc72b-121">-InputObject</span></span>
<span data-ttu-id="fc72b-122">SyncGroup-Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="fc72b-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fc72b-123">-Name</span></span>
<span data-ttu-id="fc72b-124">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="fc72b-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc72b-125">-PassThru</span></span>
<span data-ttu-id="fc72b-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="fc72b-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fc72b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc72b-127">-ResourceGroupName</span></span>
<span data-ttu-id="fc72b-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fc72b-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fc72b-129">-ResourceId</span></span>
<span data-ttu-id="fc72b-130">SyncGroup-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="fc72b-130">SyncGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fc72b-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="fc72b-132">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fc72b-132">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc72b-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc72b-133">-Confirm</span></span>
<span data-ttu-id="fc72b-134">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc72b-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc72b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc72b-135">-WhatIf</span></span>
<span data-ttu-id="fc72b-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc72b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc72b-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc72b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc72b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc72b-138">CommonParameters</span></span>
<span data-ttu-id="fc72b-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc72b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc72b-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc72b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc72b-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc72b-141">INPUTS</span></span>

### <span data-ttu-id="fc72b-142">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc72b-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="fc72b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fc72b-143">System.String</span></span>

### <span data-ttu-id="fc72b-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="fc72b-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fc72b-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc72b-145">OUTPUTS</span></span>

### <span data-ttu-id="fc72b-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="fc72b-146">System.Object</span></span>
## <span data-ttu-id="fc72b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc72b-147">NOTES</span></span>

## <span data-ttu-id="fc72b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc72b-148">RELATED LINKS</span></span>

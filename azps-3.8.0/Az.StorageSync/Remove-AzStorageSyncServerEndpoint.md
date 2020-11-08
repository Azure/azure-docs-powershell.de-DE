---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003380"
---
# <span data-ttu-id="e568d-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e568d-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="e568d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e568d-102">SYNOPSIS</span></span>
<span data-ttu-id="e568d-103">Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e568d-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="e568d-104">Die Synchronisierung mit diesem Speicherort wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="e568d-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="e568d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e568d-105">SYNTAX</span></span>

### <span data-ttu-id="e568d-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e568d-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e568d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e568d-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e568d-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e568d-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e568d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e568d-109">DESCRIPTION</span></span>
<span data-ttu-id="e568d-110">Das Entfernen eines Server Endpunkts ist ein zerstörerischer Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e568d-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="e568d-111">Dieser Server Standort beendet die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="e568d-111">This server location will stop syncing.</span></span> <span data-ttu-id="e568d-112">Dieser Vorgang sollte nicht zum Beheben von Synchronisierungsproblemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e568d-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="e568d-113">Wenn dieser Server Standort (einschließlich seiner Dateien) erneut zur gleichen Synchronisierungsgruppe wie ein Serverendpunkt hinzugefügt wird, kann dies zu Konfliktdateien und anderen unbeabsichtigten Folgen führen.</span><span class="sxs-lookup"><span data-stu-id="e568d-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="e568d-114">Dieser Befehl ist nur für die Außerbetriebnahme vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="e568d-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="e568d-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e568d-115">EXAMPLES</span></span>

### <span data-ttu-id="e568d-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e568d-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="e568d-117">Mit diesem Befehl wird der Serverendpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="e568d-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="e568d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e568d-118">PARAMETERS</span></span>

### <span data-ttu-id="e568d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e568d-119">-AsJob</span></span>
<span data-ttu-id="e568d-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e568d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e568d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e568d-121">-DefaultProfile</span></span>
<span data-ttu-id="e568d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e568d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e568d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e568d-123">-Force</span></span>
<span data-ttu-id="e568d-124">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="e568d-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="e568d-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e568d-125">-InputObject</span></span>
<span data-ttu-id="e568d-126">ServerEndpoint-Eingabeobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e568d-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e568d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e568d-127">-Name</span></span>
<span data-ttu-id="e568d-128">Der Name des ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e568d-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e568d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e568d-129">-PassThru</span></span>
<span data-ttu-id="e568d-130">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="e568d-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="e568d-131">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e568d-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="e568d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e568d-132">-ResourceGroupName</span></span>
<span data-ttu-id="e568d-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e568d-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="e568d-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e568d-134">-ResourceId</span></span>
<span data-ttu-id="e568d-135">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="e568d-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="e568d-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e568d-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="e568d-137">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e568d-137">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e568d-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e568d-138">-SyncGroupName</span></span>
<span data-ttu-id="e568d-139">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="e568d-139">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e568d-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e568d-140">-Confirm</span></span>
<span data-ttu-id="e568d-141">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e568d-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e568d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e568d-142">-WhatIf</span></span>
<span data-ttu-id="e568d-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e568d-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e568d-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e568d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e568d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e568d-145">CommonParameters</span></span>
<span data-ttu-id="e568d-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e568d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e568d-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e568d-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e568d-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e568d-148">INPUTS</span></span>

### <span data-ttu-id="e568d-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e568d-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="e568d-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e568d-150">System.String</span></span>

## <span data-ttu-id="e568d-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e568d-151">OUTPUTS</span></span>

### <span data-ttu-id="e568d-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="e568d-152">System.Object</span></span>
## <span data-ttu-id="e568d-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="e568d-153">NOTES</span></span>

## <span data-ttu-id="e568d-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e568d-154">RELATED LINKS</span></span>

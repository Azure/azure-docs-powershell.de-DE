---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366567"
---
# <span data-ttu-id="95433-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="95433-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="95433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95433-102">SYNOPSIS</span></span>
<span data-ttu-id="95433-103">Mit diesem Befehl wird der angegebene Serverendpunkt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="95433-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="95433-104">Die Synchronisierung mit diesem Speicherort wird sofort beendet.</span><span class="sxs-lookup"><span data-stu-id="95433-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="95433-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95433-105">SYNTAX</span></span>

### <span data-ttu-id="95433-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="95433-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95433-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95433-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95433-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95433-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95433-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95433-109">DESCRIPTION</span></span>
<span data-ttu-id="95433-110">Das Entfernen eines Serverendpunkts ist ein truktiver Vorgang.</span><span class="sxs-lookup"><span data-stu-id="95433-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="95433-111">Dieser Serverspeicherort beendet die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="95433-111">This server location will stop syncing.</span></span> <span data-ttu-id="95433-112">Dieser Vorgang sollte nicht zum Beheben von Synchronisierungsproblemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="95433-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="95433-113">Wenn dieser Serverspeicherort (inkl. seine Dateien) derselben Synchronisierungsgruppe wie ein Serverendpunkt erneut hinzugefügt wird, kann dies zu Konfliktdateien und anderen unbeabsichtigten Folgen führen.</span><span class="sxs-lookup"><span data-stu-id="95433-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="95433-114">Dieser Befehl ist nur für die Außerbetriebnahme vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="95433-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="95433-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="95433-115">EXAMPLES</span></span>

### <span data-ttu-id="95433-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="95433-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="95433-117">Mit diesem Befehl wird der Serverendpunkt entfernt.</span><span class="sxs-lookup"><span data-stu-id="95433-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="95433-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95433-118">PARAMETERS</span></span>

### <span data-ttu-id="95433-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95433-119">-AsJob</span></span>
<span data-ttu-id="95433-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="95433-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95433-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95433-121">-DefaultProfile</span></span>
<span data-ttu-id="95433-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="95433-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95433-123">-Force</span><span class="sxs-lookup"><span data-stu-id="95433-123">-Force</span></span>
<span data-ttu-id="95433-124">Liefern Sie "-Force", um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="95433-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="95433-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95433-125">-InputObject</span></span>
<span data-ttu-id="95433-126">ServerEndpoint-Eingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="95433-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="95433-127">-Name</span><span class="sxs-lookup"><span data-stu-id="95433-127">-Name</span></span>
<span data-ttu-id="95433-128">Der Name von ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="95433-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="95433-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95433-129">-PassThru</span></span>
<span data-ttu-id="95433-130">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="95433-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="95433-131">Wenn Sie den Parameter "PassThru" angeben, schreibt das Cmdlet nach erfolgreicher Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="95433-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="95433-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95433-132">-ResourceGroupName</span></span>
<span data-ttu-id="95433-133">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="95433-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="95433-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95433-134">-ResourceId</span></span>
<span data-ttu-id="95433-135">ServerEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="95433-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="95433-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="95433-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="95433-137">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="95433-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="95433-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="95433-138">-SyncGroupName</span></span>
<span data-ttu-id="95433-139">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="95433-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="95433-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95433-140">-Confirm</span></span>
<span data-ttu-id="95433-141">Fordert vor dem Ausführen des Cmdlets zur Bestätigung auf.</span><span class="sxs-lookup"><span data-stu-id="95433-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95433-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="95433-142">-WhatIf</span></span>
<span data-ttu-id="95433-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="95433-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95433-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95433-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95433-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95433-145">CommonParameters</span></span>
<span data-ttu-id="95433-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95433-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95433-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95433-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95433-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="95433-148">INPUTS</span></span>

### <span data-ttu-id="95433-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="95433-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="95433-150">System.String</span><span class="sxs-lookup"><span data-stu-id="95433-150">System.String</span></span>

## <span data-ttu-id="95433-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="95433-151">OUTPUTS</span></span>

### <span data-ttu-id="95433-152">System.Object</span><span class="sxs-lookup"><span data-stu-id="95433-152">System.Object</span></span>
## <span data-ttu-id="95433-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="95433-153">NOTES</span></span>

## <span data-ttu-id="95433-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="95433-154">RELATED LINKS</span></span>

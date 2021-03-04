---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 5ebcdee62997ed678b9696264a40076a40c36342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929603"
---
# <span data-ttu-id="fcfbd-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="fcfbd-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="fcfbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcfbd-102">SYNOPSIS</span></span>
<span data-ttu-id="fcfbd-103">Warnung: Das Aufheben der Registrierung eines Servers führt dazu, dass alle Serverendpunkte auf diesem Server kaskadiert werden.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="fcfbd-104">Mit diesem Befehl wird die Registrierung eines Servers vom Speichersynchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="fcfbd-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fcfbd-105">SYNTAX</span></span>

### <span data-ttu-id="fcfbd-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcfbd-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfbd-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcfbd-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcfbd-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcfbd-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcfbd-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fcfbd-109">DESCRIPTION</span></span>
<span data-ttu-id="fcfbd-110">Mit diesem Befehl wird die Registrierung eines Servers vom Speichersynchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="fcfbd-111">Warnung: Das Aufheben der Registrierung eines Servers führt dazu, dass alle Serverendpunkte auf diesem Server kaskadiert werden.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="fcfbd-112">Sie sollte nur aufgerufen werden, wenn Sie sicher sind, dass kein Pfad mehr auf diesem Server synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="fcfbd-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fcfbd-113">EXAMPLES</span></span>

### <span data-ttu-id="fcfbd-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcfbd-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="fcfbd-115">Mit diesem Befehl wird die Registrierung des Servers aufgehoben, wodurch alle Serverendpunkte auf diesem Server cascading gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="fcfbd-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fcfbd-116">PARAMETERS</span></span>

### <span data-ttu-id="fcfbd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcfbd-117">-AsJob</span></span>
<span data-ttu-id="fcfbd-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fcfbd-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fcfbd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcfbd-119">-DefaultProfile</span></span>
<span data-ttu-id="fcfbd-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcfbd-121">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="fcfbd-121">-Force</span></span>
<span data-ttu-id="fcfbd-122">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="fcfbd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcfbd-123">-InputObject</span></span>
<span data-ttu-id="fcfbd-124">RegisteredServer-Eingabeobjekt, das normalerweise über die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcfbd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcfbd-125">-PassThru</span></span>
<span data-ttu-id="fcfbd-126">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="fcfbd-127">Wenn Sie den Parameter PassThru angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="fcfbd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcfbd-128">-ResourceGroupName</span></span>
<span data-ttu-id="fcfbd-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcfbd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fcfbd-130">-ResourceId</span></span>
<span data-ttu-id="fcfbd-131">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="fcfbd-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="fcfbd-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="fcfbd-132">-ServerId</span></span>
<span data-ttu-id="fcfbd-133">Name des RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcfbd-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fcfbd-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="fcfbd-135">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fcfbd-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcfbd-136">-Confirm</span></span>
<span data-ttu-id="fcfbd-137">Fordert sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcfbd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcfbd-138">-WhatIf</span></span>
<span data-ttu-id="fcfbd-139">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcfbd-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcfbd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcfbd-141">CommonParameters</span></span>
<span data-ttu-id="fcfbd-142">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcfbd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcfbd-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcfbd-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcfbd-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fcfbd-144">INPUTS</span></span>

### <span data-ttu-id="fcfbd-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="fcfbd-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="fcfbd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="fcfbd-146">System.String</span></span>

### <span data-ttu-id="fcfbd-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fcfbd-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fcfbd-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fcfbd-148">OUTPUTS</span></span>

### <span data-ttu-id="fcfbd-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="fcfbd-149">System.Object</span></span>
## <span data-ttu-id="fcfbd-150">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fcfbd-150">NOTES</span></span>

## <span data-ttu-id="fcfbd-151">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fcfbd-151">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: f6de2bf731bc11a4b0ec8b6c894e6d77569ec9ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008780"
---
# <span data-ttu-id="7a682-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="7a682-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="7a682-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a682-102">SYNOPSIS</span></span>
<span data-ttu-id="7a682-103">Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7a682-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="7a682-104">Mit diesem Befehl wird die Registrierung eines Servers aus dem Speicher Synchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="7a682-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="7a682-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a682-105">SYNTAX</span></span>

### <span data-ttu-id="7a682-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a682-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a682-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a682-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a682-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a682-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a682-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a682-109">DESCRIPTION</span></span>
<span data-ttu-id="7a682-110">Mit diesem Befehl wird die Registrierung eines Servers aus dem Speicher Synchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="7a682-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="7a682-111">Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht.</span><span class="sxs-lookup"><span data-stu-id="7a682-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="7a682-112">Sie sollte nur aufgerufen werden, wenn Sie sicher sind, dass kein Pfad auf diesem Server mehr synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a682-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="7a682-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a682-113">EXAMPLES</span></span>

### <span data-ttu-id="7a682-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a682-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="7a682-115">Mit diesem Befehl wird die Registrierung des Servers aufgehoben, wodurch kaskadierende Löschungen aller Server Endpunkte auf diesem Server verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="7a682-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="7a682-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a682-116">PARAMETERS</span></span>

### <span data-ttu-id="7a682-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a682-117">-AsJob</span></span>
<span data-ttu-id="7a682-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7a682-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a682-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a682-119">-DefaultProfile</span></span>
<span data-ttu-id="7a682-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a682-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a682-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7a682-121">-Force</span></span>
<span data-ttu-id="7a682-122">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="7a682-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="7a682-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7a682-123">-InputObject</span></span>
<span data-ttu-id="7a682-124">RegisteredServer-Eingabeobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="7a682-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7a682-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a682-125">-PassThru</span></span>
<span data-ttu-id="7a682-126">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="7a682-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="7a682-127">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7a682-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="7a682-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a682-128">-ResourceGroupName</span></span>
<span data-ttu-id="7a682-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7a682-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="7a682-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7a682-130">-ResourceId</span></span>
<span data-ttu-id="7a682-131">RegisteredServer-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="7a682-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="7a682-132">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="7a682-132">-ServerId</span></span>
<span data-ttu-id="7a682-133">Der Name des registeredserver.</span><span class="sxs-lookup"><span data-stu-id="7a682-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="7a682-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7a682-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="7a682-135">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="7a682-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="7a682-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7a682-136">-Confirm</span></span>
<span data-ttu-id="7a682-137">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a682-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a682-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a682-138">-WhatIf</span></span>
<span data-ttu-id="7a682-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a682-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a682-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a682-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a682-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a682-141">CommonParameters</span></span>
<span data-ttu-id="7a682-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a682-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a682-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a682-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a682-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a682-144">INPUTS</span></span>

### <span data-ttu-id="7a682-145">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="7a682-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="7a682-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7a682-146">System.String</span></span>

### <span data-ttu-id="7a682-147">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7a682-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a682-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a682-148">OUTPUTS</span></span>

### <span data-ttu-id="7a682-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="7a682-149">System.Object</span></span>
## <span data-ttu-id="7a682-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a682-150">NOTES</span></span>

## <span data-ttu-id="7a682-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a682-151">RELATED LINKS</span></span>

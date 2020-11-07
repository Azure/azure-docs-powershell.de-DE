---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658674"
---
# <span data-ttu-id="37b87-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="37b87-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="37b87-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37b87-102">SYNOPSIS</span></span>
<span data-ttu-id="37b87-103">Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht.</span><span class="sxs-lookup"><span data-stu-id="37b87-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="37b87-104">Dieser Befehl hebt die Registrierung eines Servers auf, bei dem es sich um den Speicher Synchronisierungsdienst handelt.</span><span class="sxs-lookup"><span data-stu-id="37b87-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="37b87-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37b87-105">SYNTAX</span></span>

### <span data-ttu-id="37b87-106">InputObjectParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="37b87-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b87-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="37b87-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b87-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="37b87-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b87-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37b87-109">DESCRIPTION</span></span>
<span data-ttu-id="37b87-110">Mit diesem Befehl wird die Registrierung eines Servers aus dem Speicher Synchronisierungsdienst aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="37b87-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="37b87-111">Warnung: beim Aufheben der Registrierung eines Servers werden alle Server Endpunkte auf diesem Server kaskadiert gelöscht.</span><span class="sxs-lookup"><span data-stu-id="37b87-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="37b87-112">Sie sollte nur aufgerufen werden, wenn Sie sicher sind, dass kein Pfad auf diesem Server mehr synchronisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="37b87-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="37b87-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37b87-113">EXAMPLES</span></span>

### <span data-ttu-id="37b87-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37b87-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="37b87-115">Mit diesem Befehl wird die Registrierung des Servers aufgehoben, wodurch kaskadierende Löschungen aller Server Endpunkte auf diesem Server verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="37b87-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="37b87-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="37b87-116">PARAMETERS</span></span>

### <span data-ttu-id="37b87-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37b87-117">-AsJob</span></span>
<span data-ttu-id="37b87-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="37b87-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37b87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b87-119">-DefaultProfile</span></span>
<span data-ttu-id="37b87-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37b87-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b87-121">-Force</span><span class="sxs-lookup"><span data-stu-id="37b87-121">-Force</span></span>
<span data-ttu-id="37b87-122">Supply-Force, um die Bestätigung dieses Befehls zu überspringen.</span><span class="sxs-lookup"><span data-stu-id="37b87-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="37b87-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37b87-123">-InputObject</span></span>
<span data-ttu-id="37b87-124">RegisteredServer-Eingabeobjekt, das normalerweise durch die Pipeline übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="37b87-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="37b87-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37b87-125">-PassThru</span></span>
<span data-ttu-id="37b87-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="37b87-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="37b87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b87-127">-ResourceGroupName</span></span>
<span data-ttu-id="37b87-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37b87-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="37b87-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="37b87-129">-ResourceId</span></span>
<span data-ttu-id="37b87-130">RegisteredServer-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="37b87-130">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="37b87-131">-Server-Nr</span><span class="sxs-lookup"><span data-stu-id="37b87-131">-ServerId</span></span>
<span data-ttu-id="37b87-132">Der Name des registeredserver.</span><span class="sxs-lookup"><span data-stu-id="37b87-132">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="37b87-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="37b87-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="37b87-134">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="37b87-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="37b87-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37b87-135">-Confirm</span></span>
<span data-ttu-id="37b87-136">Fordert zur Bestätigung auf, bevor das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b87-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37b87-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37b87-137">-WhatIf</span></span>
<span data-ttu-id="37b87-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b87-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37b87-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37b87-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37b87-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b87-140">CommonParameters</span></span>
<span data-ttu-id="37b87-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b87-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b87-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b87-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b87-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37b87-143">INPUTS</span></span>

### <span data-ttu-id="37b87-144">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="37b87-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="37b87-145">System. String</span><span class="sxs-lookup"><span data-stu-id="37b87-145">System.String</span></span>

### <span data-ttu-id="37b87-146">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="37b87-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="37b87-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37b87-147">OUTPUTS</span></span>

### <span data-ttu-id="37b87-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="37b87-148">System.Object</span></span>
## <span data-ttu-id="37b87-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="37b87-149">NOTES</span></span>

## <span data-ttu-id="37b87-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37b87-150">RELATED LINKS</span></span>

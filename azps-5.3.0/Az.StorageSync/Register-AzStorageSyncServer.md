---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: bb1ce6f9ff7e846c2f485665cafad700fa4c825b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460107"
---
# <span data-ttu-id="73a21-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="73a21-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="73a21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73a21-102">SYNOPSIS</span></span>
<span data-ttu-id="73a21-103">Mit diesem Befehl wird ein Server bei einem Speichersynchronisierungsdienst registriert, der eine Vertrauensstellung erstellt.</span><span class="sxs-lookup"><span data-stu-id="73a21-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="73a21-104">PowerShell oder das Azure-Portal kann dann zum Konfigurieren der Synchronisierung auf diesem Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73a21-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="73a21-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73a21-105">SYNTAX</span></span>

### <span data-ttu-id="73a21-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="73a21-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a21-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73a21-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73a21-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="73a21-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73a21-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73a21-109">DESCRIPTION</span></span>
<span data-ttu-id="73a21-110">Mit diesem Befehl wird ein Server bei einem Speichersynchronisierungsdienst registriert, der Ressource der obersten Ebene für die Azure File Sync. Es wird eine Vertrauensbeziehung zwischen Server und Speichersynchronisierungsdienst erstellt, die sichere Datenübertragungs- und Verwaltungskanäle gewährleistet.</span><span class="sxs-lookup"><span data-stu-id="73a21-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="73a21-111">PowerShell oder das Azure-Portal können dann verwendet werden, um zu konfigurieren, welche Synchronisierungen auf diesem Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="73a21-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="73a21-112">Ein Server kann nur bei einem einzigen Speichersynchronisierungsdienst registriert werden.</span><span class="sxs-lookup"><span data-stu-id="73a21-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="73a21-113">Wenn Server jemals an der Synchronisierung derselben Gruppe von Dateien teilnehmen müssen, registrieren Sie sie beim gleichen Speichersynchronisierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="73a21-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="73a21-114">Der Befehl muss lokal auf dem Server ausgeführt werden, der registriert werden soll – entweder direkt oder über eine Remote-PowerShell-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="73a21-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="73a21-115">Ein Remotecomputerobjekt kann nicht akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="73a21-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="73a21-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73a21-116">EXAMPLES</span></span>

### <span data-ttu-id="73a21-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73a21-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="73a21-118">Dieser Befehl registriert den lokalen Server, auf dem dieser Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73a21-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="73a21-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73a21-119">PARAMETERS</span></span>

### <span data-ttu-id="73a21-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73a21-120">-AsJob</span></span>
<span data-ttu-id="73a21-121">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="73a21-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73a21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a21-122">-DefaultProfile</span></span>
<span data-ttu-id="73a21-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73a21-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73a21-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="73a21-124">-ParentObject</span></span>
<span data-ttu-id="73a21-125">StorageSyncService-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="73a21-125">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73a21-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="73a21-126">-ParentResourceId</span></span>
<span data-ttu-id="73a21-127">StorageSyncService, übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="73a21-127">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a21-128">-ResourceGroupName</span></span>
<span data-ttu-id="73a21-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="73a21-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a21-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="73a21-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="73a21-131">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="73a21-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73a21-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73a21-132">-Confirm</span></span>
<span data-ttu-id="73a21-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73a21-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73a21-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73a21-134">-WhatIf</span></span>
<span data-ttu-id="73a21-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73a21-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73a21-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73a21-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73a21-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a21-137">CommonParameters</span></span>
<span data-ttu-id="73a21-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a21-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a21-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a21-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a21-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73a21-140">INPUTS</span></span>

### <span data-ttu-id="73a21-141">System.String</span><span class="sxs-lookup"><span data-stu-id="73a21-141">System.String</span></span>

### <span data-ttu-id="73a21-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="73a21-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="73a21-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73a21-143">OUTPUTS</span></span>

### <span data-ttu-id="73a21-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="73a21-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="73a21-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73a21-145">NOTES</span></span>

## <span data-ttu-id="73a21-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73a21-146">RELATED LINKS</span></span>

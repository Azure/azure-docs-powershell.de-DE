---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375974"
---
# <span data-ttu-id="4f8a8-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4f8a8-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="4f8a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8a8-103">Ändert einen Speicher-BLOB-Container.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="4f8a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f8a8-104">SYNTAX</span></span>

### <span data-ttu-id="4f8a8-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f8a8-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8a8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4f8a8-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8a8-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="4f8a8-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4f8a8-108">DESCRIPTION</span></span>
<span data-ttu-id="4f8a8-109">Das **Cmdlet "Update-AzRmStorageContainer"** ändert einen Speicher-BLOB-Container</span><span class="sxs-lookup"><span data-stu-id="4f8a8-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="4f8a8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4f8a8-110">EXAMPLES</span></span>

### <span data-ttu-id="4f8a8-111">Beispiel 1: Ändert die Metadaten und den öffentlichen Zugriff eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="4f8a8-112">Mit diesem Befehl werden die Metadaten und der öffentliche Zugriff eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen geändert.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="4f8a8-113">Beispiel 2: Deaktivieren des öffentlichen Zugriffs auf einen Speicher-BLOB-Container mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="4f8a8-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="4f8a8-114">Dieser Befehl deaktiviert den öffentlichen Zugriff auf einen Speicher-BLOB-Container mit Speicherkontoobjekt und Containername.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="4f8a8-115">Beispiel 3: Festlegen des öffentlichen Zugriffs als BLOB für alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="4f8a8-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="4f8a8-116">Mit diesem Befehl wird der öffentliche Zugriff für alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline als BLOB festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="4f8a8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f8a8-117">PARAMETERS</span></span>

### <span data-ttu-id="4f8a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8a8-118">-DefaultProfile</span></span>
<span data-ttu-id="4f8a8-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f8a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f8a8-120">-InputObject</span></span>
<span data-ttu-id="4f8a8-121">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="4f8a8-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4f8a8-122">-Metadata</span></span>
<span data-ttu-id="4f8a8-123">Containermetadaten</span><span class="sxs-lookup"><span data-stu-id="4f8a8-123">Container Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4f8a8-124">-Name</span></span>
<span data-ttu-id="4f8a8-125">Containername</span><span class="sxs-lookup"><span data-stu-id="4f8a8-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="4f8a8-126">-PublicAccess</span></span>
<span data-ttu-id="4f8a8-127">Container PublicAccess</span><span class="sxs-lookup"><span data-stu-id="4f8a8-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f8a8-129">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f8a8-130">-StorageAccount</span></span>
<span data-ttu-id="4f8a8-131">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="4f8a8-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4f8a8-132">-StorageAccountName</span></span>
<span data-ttu-id="4f8a8-133">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8a8-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f8a8-134">-Confirm</span></span>
<span data-ttu-id="4f8a8-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8a8-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4f8a8-136">-WhatIf</span></span>
<span data-ttu-id="4f8a8-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f8a8-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8a8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8a8-139">CommonParameters</span></span>
<span data-ttu-id="4f8a8-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8a8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8a8-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f8a8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8a8-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8a8-142">INPUTS</span></span>

### <span data-ttu-id="4f8a8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4f8a8-143">System.String</span></span>

### <span data-ttu-id="4f8a8-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4f8a8-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4f8a8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="4f8a8-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4f8a8-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4f8a8-146">OUTPUTS</span></span>

### <span data-ttu-id="4f8a8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="4f8a8-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4f8a8-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4f8a8-148">NOTES</span></span>

## <span data-ttu-id="4f8a8-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4f8a8-149">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 3ece496830cf3d6b1618bd410e2352d65f6e2fad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166745"
---
# <span data-ttu-id="fcb98-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fcb98-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="fcb98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcb98-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb98-103">Ändert einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="fcb98-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="fcb98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb98-104">SYNTAX</span></span>

### <span data-ttu-id="fcb98-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcb98-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb98-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="fcb98-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb98-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="fcb98-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb98-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcb98-108">DESCRIPTION</span></span>
<span data-ttu-id="fcb98-109">Das Cmdlet **Update-AzRmStorageContainer** ändert einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="fcb98-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="fcb98-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcb98-110">EXAMPLES</span></span>

### <span data-ttu-id="fcb98-111">Beispiel 1: ändert die Metadaten und den öffentlichen Zugriff eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="fcb98-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="fcb98-112">Dieser Befehl ändert die Metadaten und den öffentlichen Zugriff eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="fcb98-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="fcb98-113">Beispiel 2: Deaktivieren des öffentlichen Zugriffs auf einen BLOB-Speichercontainer mit Speicherkonto Objekt und Containernamen</span><span class="sxs-lookup"><span data-stu-id="fcb98-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="fcb98-114">Dieser Befehl deaktiviert den öffentlichen Zugriff auf einen BLOB-Speichercontainer mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="fcb98-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fcb98-115">Beispiel 3: Einrichten des öffentlichen Zugriffs als BLOB für alle BLOB-Speichercontainer in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="fcb98-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="fcb98-116">Mit diesem Befehl wird der öffentliche Zugriff als BLOB für alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline gesetzt.</span><span class="sxs-lookup"><span data-stu-id="fcb98-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="fcb98-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb98-117">PARAMETERS</span></span>

### <span data-ttu-id="fcb98-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb98-118">-DefaultProfile</span></span>
<span data-ttu-id="fcb98-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcb98-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcb98-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fcb98-120">-InputObject</span></span>
<span data-ttu-id="fcb98-121">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="fcb98-121">Storage container object</span></span>

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

### <span data-ttu-id="fcb98-122">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="fcb98-122">-Metadata</span></span>
<span data-ttu-id="fcb98-123">Container Metadaten</span><span class="sxs-lookup"><span data-stu-id="fcb98-123">Container Metadata</span></span>

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

### <span data-ttu-id="fcb98-124">-Name</span><span class="sxs-lookup"><span data-stu-id="fcb98-124">-Name</span></span>
<span data-ttu-id="fcb98-125">Container Name</span><span class="sxs-lookup"><span data-stu-id="fcb98-125">Container Name</span></span>

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

### <span data-ttu-id="fcb98-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fcb98-126">-PublicAccess</span></span>
<span data-ttu-id="fcb98-127">Container-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="fcb98-127">Container PublicAccess</span></span>

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

### <span data-ttu-id="fcb98-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb98-128">-ResourceGroupName</span></span>
<span data-ttu-id="fcb98-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fcb98-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcb98-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcb98-130">-StorageAccount</span></span>
<span data-ttu-id="fcb98-131">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="fcb98-131">Storage account object</span></span>

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

### <span data-ttu-id="fcb98-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fcb98-132">-StorageAccountName</span></span>
<span data-ttu-id="fcb98-133">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fcb98-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="fcb98-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcb98-134">-Confirm</span></span>
<span data-ttu-id="fcb98-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcb98-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb98-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb98-136">-WhatIf</span></span>
<span data-ttu-id="fcb98-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcb98-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcb98-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcb98-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb98-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb98-139">CommonParameters</span></span>
<span data-ttu-id="fcb98-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb98-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb98-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcb98-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb98-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcb98-142">INPUTS</span></span>

### <span data-ttu-id="fcb98-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb98-143">System.String</span></span>

### <span data-ttu-id="fcb98-144">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcb98-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fcb98-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fcb98-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fcb98-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcb98-146">OUTPUTS</span></span>

### <span data-ttu-id="fcb98-147">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fcb98-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fcb98-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcb98-148">NOTES</span></span>

## <span data-ttu-id="fcb98-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcb98-149">RELATED LINKS</span></span>

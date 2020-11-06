---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498133"
---
# <span data-ttu-id="8b7cd-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b7cd-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="8b7cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b7cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8b7cd-103">Ändert einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="8b7cd-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b7cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b7cd-104">SYNTAX</span></span>

### <span data-ttu-id="8b7cd-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b7cd-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7cd-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="8b7cd-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b7cd-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="8b7cd-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b7cd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b7cd-108">DESCRIPTION</span></span>
<span data-ttu-id="8b7cd-109">Das Cmdlet **Update-AzureRmStorageContainer** ändert einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="8b7cd-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="8b7cd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b7cd-110">EXAMPLES</span></span>

### <span data-ttu-id="8b7cd-111">Beispiel 1: ändert die Metadaten und den öffentlichen Zugriff eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="8b7cd-112">Dieser Befehl ändert die Metadaten und den öffentlichen Zugriff eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="8b7cd-113">Beispiel 2: Deaktivieren des öffentlichen Zugriffs auf einen BLOB-Speichercontainer mit Speicherkonto Objekt und Containernamen</span><span class="sxs-lookup"><span data-stu-id="8b7cd-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="8b7cd-114">Dieser Befehl deaktiviert den öffentlichen Zugriff auf einen BLOB-Speichercontainer mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="8b7cd-115">Beispiel 3: Einrichten des öffentlichen Zugriffs als BLOB für alle BLOB-Speichercontainer in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="8b7cd-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="8b7cd-116">Mit diesem Befehl wird der öffentliche Zugriff als BLOB für alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline gesetzt.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="8b7cd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b7cd-117">PARAMETERS</span></span>

### <span data-ttu-id="8b7cd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b7cd-118">-DefaultProfile</span></span>
<span data-ttu-id="8b7cd-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b7cd-120">-InputObject</span></span>
<span data-ttu-id="8b7cd-121">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="8b7cd-121">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-122">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="8b7cd-122">-Metadata</span></span>
<span data-ttu-id="8b7cd-123">Container Metadaten</span><span class="sxs-lookup"><span data-stu-id="8b7cd-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8b7cd-124">-Name</span></span>
<span data-ttu-id="8b7cd-125">Container Name</span><span class="sxs-lookup"><span data-stu-id="8b7cd-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="8b7cd-126">-PublicAccess</span></span>
<span data-ttu-id="8b7cd-127">Container-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="8b7cd-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b7cd-128">-ResourceGroupName</span></span>
<span data-ttu-id="8b7cd-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b7cd-130">-StorageAccount</span></span>
<span data-ttu-id="8b7cd-131">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="8b7cd-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b7cd-132">-StorageAccountName</span></span>
<span data-ttu-id="8b7cd-133">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8b7cd-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b7cd-134">-Confirm</span></span>
<span data-ttu-id="8b7cd-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b7cd-136">-WhatIf</span></span>
<span data-ttu-id="8b7cd-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b7cd-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b7cd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b7cd-139">CommonParameters</span></span>
<span data-ttu-id="8b7cd-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b7cd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b7cd-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b7cd-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b7cd-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b7cd-142">INPUTS</span></span>

### <span data-ttu-id="8b7cd-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8b7cd-143">System.String</span></span>

## <span data-ttu-id="8b7cd-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b7cd-144">OUTPUTS</span></span>

### <span data-ttu-id="8b7cd-145">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="8b7cd-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8b7cd-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b7cd-146">NOTES</span></span>

## <span data-ttu-id="8b7cd-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b7cd-147">RELATED LINKS</span></span>


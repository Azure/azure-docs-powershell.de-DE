---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477614"
---
# <span data-ttu-id="0d0b7-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0d0b7-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="0d0b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0d0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0d0b7-103">Erstellt einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="0d0b7-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d0b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d0b7-104">SYNTAX</span></span>

### <span data-ttu-id="0d0b7-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="0d0b7-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d0b7-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="0d0b7-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d0b7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d0b7-107">DESCRIPTION</span></span>
<span data-ttu-id="0d0b7-108">Das Cmdlet " **New-AzureRmStorageContainer** " erstellt einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="0d0b7-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="0d0b7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d0b7-109">EXAMPLES</span></span>

### <span data-ttu-id="0d0b7-110">Beispiel 1: Erstellen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="0d0b7-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="0d0b7-111">Dieser Befehl erstellt einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen mit Metadaten.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="0d0b7-112">Beispiel 2: Erstellen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen mit öffentlichem Zugriff als BLOB</span><span class="sxs-lookup"><span data-stu-id="0d0b7-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="0d0b7-113">Mit diesem Befehl wird ein BLOB-Speichercontainer mit dem Speicherkonto Objekt und dem Containernamen erstellt, wobei der öffentliche Zugriff als BLOB verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="0d0b7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d0b7-114">PARAMETERS</span></span>

### <span data-ttu-id="0d0b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d0b7-115">-DefaultProfile</span></span>
<span data-ttu-id="0d0b7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d0b7-117">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="0d0b7-117">-Metadata</span></span>
<span data-ttu-id="0d0b7-118">Container Metadaten</span><span class="sxs-lookup"><span data-stu-id="0d0b7-118">Container Metadata</span></span>

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

### <span data-ttu-id="0d0b7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0d0b7-119">-Name</span></span>
<span data-ttu-id="0d0b7-120">Container Name</span><span class="sxs-lookup"><span data-stu-id="0d0b7-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d0b7-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="0d0b7-121">-PublicAccess</span></span>
<span data-ttu-id="0d0b7-122">Container-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="0d0b7-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="0d0b7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d0b7-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d0b7-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="0d0b7-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0d0b7-125">-StorageAccount</span></span>
<span data-ttu-id="0d0b7-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="0d0b7-126">Storage account object</span></span>

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

### <span data-ttu-id="0d0b7-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0d0b7-127">-StorageAccountName</span></span>
<span data-ttu-id="0d0b7-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="0d0b7-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="0d0b7-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0d0b7-129">-Confirm</span></span>
<span data-ttu-id="0d0b7-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d0b7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d0b7-131">-WhatIf</span></span>
<span data-ttu-id="0d0b7-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d0b7-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d0b7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d0b7-134">CommonParameters</span></span>
<span data-ttu-id="0d0b7-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d0b7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d0b7-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d0b7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d0b7-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0d0b7-137">INPUTS</span></span>

### <span data-ttu-id="0d0b7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0d0b7-138">System.String</span></span>

## <span data-ttu-id="0d0b7-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0d0b7-139">OUTPUTS</span></span>

### <span data-ttu-id="0d0b7-140">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="0d0b7-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0d0b7-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0d0b7-141">NOTES</span></span>

## <span data-ttu-id="0d0b7-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0d0b7-142">RELATED LINKS</span></span>


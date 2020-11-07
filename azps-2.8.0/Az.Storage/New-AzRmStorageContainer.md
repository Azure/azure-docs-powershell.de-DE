---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: efbdcc79bed4b7dd3dcca40f87db7fcef668405a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826635"
---
# <span data-ttu-id="07c06-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="07c06-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="07c06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07c06-102">SYNOPSIS</span></span>
<span data-ttu-id="07c06-103">Erstellt einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="07c06-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="07c06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07c06-104">SYNTAX</span></span>

### <span data-ttu-id="07c06-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="07c06-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07c06-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="07c06-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07c06-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07c06-107">DESCRIPTION</span></span>
<span data-ttu-id="07c06-108">Das Cmdlet " **New-AzRmStorageContainer** " erstellt einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="07c06-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="07c06-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07c06-109">EXAMPLES</span></span>

### <span data-ttu-id="07c06-110">Beispiel 1: Erstellen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen mit Metadaten</span><span class="sxs-lookup"><span data-stu-id="07c06-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="07c06-111">Dieser Befehl erstellt einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen mit Metadaten.</span><span class="sxs-lookup"><span data-stu-id="07c06-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="07c06-112">Beispiel 2: Erstellen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen mit öffentlichem Zugriff als BLOB</span><span class="sxs-lookup"><span data-stu-id="07c06-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="07c06-113">Mit diesem Befehl wird ein BLOB-Speichercontainer mit dem Speicherkonto Objekt und dem Containernamen erstellt, wobei der öffentliche Zugriff als BLOB verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07c06-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="07c06-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="07c06-114">PARAMETERS</span></span>

### <span data-ttu-id="07c06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c06-115">-DefaultProfile</span></span>
<span data-ttu-id="07c06-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07c06-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c06-117">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="07c06-117">-Metadata</span></span>
<span data-ttu-id="07c06-118">Container Metadaten</span><span class="sxs-lookup"><span data-stu-id="07c06-118">Container Metadata</span></span>

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

### <span data-ttu-id="07c06-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07c06-119">-Name</span></span>
<span data-ttu-id="07c06-120">Container Name</span><span class="sxs-lookup"><span data-stu-id="07c06-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07c06-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="07c06-121">-PublicAccess</span></span>
<span data-ttu-id="07c06-122">Container-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="07c06-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="07c06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07c06-123">-ResourceGroupName</span></span>
<span data-ttu-id="07c06-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07c06-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="07c06-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="07c06-125">-StorageAccount</span></span>
<span data-ttu-id="07c06-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="07c06-126">Storage account object</span></span>

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

### <span data-ttu-id="07c06-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="07c06-127">-StorageAccountName</span></span>
<span data-ttu-id="07c06-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="07c06-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="07c06-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="07c06-129">-Confirm</span></span>
<span data-ttu-id="07c06-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="07c06-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07c06-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07c06-131">-WhatIf</span></span>
<span data-ttu-id="07c06-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="07c06-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07c06-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="07c06-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07c06-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c06-134">CommonParameters</span></span>
<span data-ttu-id="07c06-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c06-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c06-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c06-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c06-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07c06-137">INPUTS</span></span>

### <span data-ttu-id="07c06-138">System. String</span><span class="sxs-lookup"><span data-stu-id="07c06-138">System.String</span></span>

### <span data-ttu-id="07c06-139">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="07c06-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="07c06-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07c06-140">OUTPUTS</span></span>

### <span data-ttu-id="07c06-141">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="07c06-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="07c06-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="07c06-142">NOTES</span></span>

## <span data-ttu-id="07c06-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07c06-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010391"
---
# <span data-ttu-id="b7b71-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7b71-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b7b71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7b71-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b71-103">Ruft ImmutabilityPolicy eines Speicher-BLOB-Containers ab.</span><span class="sxs-lookup"><span data-stu-id="b7b71-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b7b71-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7b71-104">SYNTAX</span></span>

### <span data-ttu-id="b7b71-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="b7b71-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7b71-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="b7b71-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7b71-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="b7b71-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7b71-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7b71-108">DESCRIPTION</span></span>
<span data-ttu-id="b7b71-109">Das Cmdlet " **Get-AzRmStorageContainerImmutabilityPolicy** " ruft ImmutabilityPolicy eines Speicher-BLOB-Containers ab.</span><span class="sxs-lookup"><span data-stu-id="b7b71-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b7b71-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7b71-110">EXAMPLES</span></span>

### <span data-ttu-id="b7b71-111">Beispiel 1: Abrufen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="b7b71-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="b7b71-112">Dieser Befehl ruft ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="b7b71-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b7b71-113">Beispiel 2: Abrufen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="b7b71-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="b7b71-114">Dieser Befehl ruft ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="b7b71-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="b7b71-115">Beispiel 3: Abrufen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="b7b71-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="b7b71-116">Dieser Befehl ruft ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="b7b71-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="b7b71-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7b71-117">PARAMETERS</span></span>

### <span data-ttu-id="b7b71-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b7b71-118">-Container</span></span>
<span data-ttu-id="b7b71-119">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="b7b71-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b71-120">-Containername</span><span class="sxs-lookup"><span data-stu-id="b7b71-120">-ContainerName</span></span>
<span data-ttu-id="b7b71-121">Container Name</span><span class="sxs-lookup"><span data-stu-id="b7b71-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7b71-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b71-122">-DefaultProfile</span></span>
<span data-ttu-id="b7b71-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7b71-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7b71-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="b7b71-124">-Etag</span></span>
<span data-ttu-id="b7b71-125">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="b7b71-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b71-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b71-126">-ResourceGroupName</span></span>
<span data-ttu-id="b7b71-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b7b71-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7b71-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7b71-128">-StorageAccount</span></span>
<span data-ttu-id="b7b71-129">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="b7b71-129">Storage account object</span></span>

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

### <span data-ttu-id="b7b71-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b7b71-130">-StorageAccountName</span></span>
<span data-ttu-id="b7b71-131">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="b7b71-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="b7b71-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b71-132">CommonParameters</span></span>
<span data-ttu-id="b7b71-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7b71-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b71-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7b71-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b71-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7b71-135">INPUTS</span></span>

### <span data-ttu-id="b7b71-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b7b71-136">System.String</span></span>

### <span data-ttu-id="b7b71-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b7b71-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b7b71-138">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b7b71-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b7b71-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7b71-139">OUTPUTS</span></span>

### <span data-ttu-id="b7b71-140">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b7b71-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b7b71-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7b71-141">NOTES</span></span>

## <span data-ttu-id="b7b71-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7b71-142">RELATED LINKS</span></span>

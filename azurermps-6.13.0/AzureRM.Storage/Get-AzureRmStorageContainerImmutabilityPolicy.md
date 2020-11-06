---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502818"
---
# <span data-ttu-id="660bc-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="660bc-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="660bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="660bc-102">SYNOPSIS</span></span>
<span data-ttu-id="660bc-103">Ruft ImmutabilityPolicy eines Speicher-BLOB-Containers ab.</span><span class="sxs-lookup"><span data-stu-id="660bc-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="660bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="660bc-104">SYNTAX</span></span>

### <span data-ttu-id="660bc-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="660bc-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="660bc-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="660bc-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="660bc-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="660bc-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="660bc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="660bc-108">DESCRIPTION</span></span>
<span data-ttu-id="660bc-109">Das Cmdlet " **Get-AzureRmStorageContainerImmutabilityPolicy** " ruft ImmutabilityPolicy eines Speicher-BLOB-Containers ab.</span><span class="sxs-lookup"><span data-stu-id="660bc-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="660bc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="660bc-110">EXAMPLES</span></span>

### <span data-ttu-id="660bc-111">Beispiel 1: Abrufen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="660bc-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="660bc-112">Dieser Befehl ruft ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="660bc-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="660bc-113">Beispiel 2: Abrufen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="660bc-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="660bc-114">Dieser Befehl ruft ImmutabilityPolicy eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="660bc-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="660bc-115">Beispiel 3: Abrufen von ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="660bc-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="660bc-116">Dieser Befehl ruft ImmutabilityPolicy eines Speicher-BLOB-Containers mit einem Speichercontainer Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="660bc-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="660bc-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="660bc-117">PARAMETERS</span></span>

### <span data-ttu-id="660bc-118">-Container</span><span class="sxs-lookup"><span data-stu-id="660bc-118">-Container</span></span>
<span data-ttu-id="660bc-119">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="660bc-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="660bc-120">-Containername</span><span class="sxs-lookup"><span data-stu-id="660bc-120">-ContainerName</span></span>
<span data-ttu-id="660bc-121">Container Name</span><span class="sxs-lookup"><span data-stu-id="660bc-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="660bc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="660bc-122">-DefaultProfile</span></span>
<span data-ttu-id="660bc-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="660bc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="660bc-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="660bc-124">-Etag</span></span>
<span data-ttu-id="660bc-125">Unveränderlichkeits Richtlinien-ETag.</span><span class="sxs-lookup"><span data-stu-id="660bc-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660bc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660bc-126">-ResourceGroupName</span></span>
<span data-ttu-id="660bc-127">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="660bc-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="660bc-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="660bc-128">-StorageAccount</span></span>
<span data-ttu-id="660bc-129">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="660bc-129">Storage account object</span></span>

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

### <span data-ttu-id="660bc-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="660bc-130">-StorageAccountName</span></span>
<span data-ttu-id="660bc-131">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="660bc-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="660bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660bc-132">CommonParameters</span></span>
<span data-ttu-id="660bc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660bc-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660bc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="660bc-135">INPUTS</span></span>

### <span data-ttu-id="660bc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="660bc-136">System.String</span></span>

## <span data-ttu-id="660bc-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="660bc-137">OUTPUTS</span></span>

### <span data-ttu-id="660bc-138">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="660bc-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="660bc-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="660bc-139">NOTES</span></span>

## <span data-ttu-id="660bc-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="660bc-140">RELATED LINKS</span></span>


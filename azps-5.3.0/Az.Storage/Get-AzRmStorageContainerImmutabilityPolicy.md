---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376282"
---
# <span data-ttu-id="b4502-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b4502-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="b4502-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4502-102">SYNOPSIS</span></span>
<span data-ttu-id="b4502-103">Ruft immutabilityPolicy eines Speicher-BLOB-Containers ab</span><span class="sxs-lookup"><span data-stu-id="b4502-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b4502-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4502-104">SYNTAX</span></span>

### <span data-ttu-id="b4502-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4502-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4502-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b4502-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b4502-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b4502-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4502-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4502-108">DESCRIPTION</span></span>
<span data-ttu-id="b4502-109">Das **Cmdlet "Get-AzRmStorageContainerImmutabilityPolicy"** ruft "ImmutabilityPolicy" eines Speicher-BLOB-Containers ab.</span><span class="sxs-lookup"><span data-stu-id="b4502-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="b4502-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4502-110">EXAMPLES</span></span>

### <span data-ttu-id="b4502-111">Beispiel 1: Get ImmutabilityPolicy of a Storage BLOB container with Storage account name and container name</span><span class="sxs-lookup"><span data-stu-id="b4502-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="b4502-112">Dieser Befehl ruft "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="b4502-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b4502-113">Beispiel 2: ImmutabilityPolicy eines Speicher-BLOB-Containers mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="b4502-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="b4502-114">Dieser Befehl ruft "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit Speicherkontoobjekt und Containername ab.</span><span class="sxs-lookup"><span data-stu-id="b4502-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="b4502-115">Beispiel 3: Get ImmutabilityPolicy of a Storage BLOB container with Storage container object</span><span class="sxs-lookup"><span data-stu-id="b4502-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="b4502-116">Dieser Befehl ruft "ImmutabilityPolicy" eines Speicher-BLOB-Containers mit Einem Speichercontainerobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="b4502-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="b4502-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4502-117">PARAMETERS</span></span>

### <span data-ttu-id="b4502-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b4502-118">-Container</span></span>
<span data-ttu-id="b4502-119">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="b4502-119">Storage container object</span></span>

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

### <span data-ttu-id="b4502-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b4502-120">-ContainerName</span></span>
<span data-ttu-id="b4502-121">Containername</span><span class="sxs-lookup"><span data-stu-id="b4502-121">Container Name</span></span>

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

### <span data-ttu-id="b4502-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4502-122">-DefaultProfile</span></span>
<span data-ttu-id="b4502-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4502-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4502-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="b4502-124">-Etag</span></span>
<span data-ttu-id="b4502-125">E-Tag der Immutbarkeitsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="b4502-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="b4502-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4502-126">-ResourceGroupName</span></span>
<span data-ttu-id="b4502-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b4502-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4502-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4502-128">-StorageAccount</span></span>
<span data-ttu-id="b4502-129">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b4502-129">Storage account object</span></span>

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

### <span data-ttu-id="b4502-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4502-130">-StorageAccountName</span></span>
<span data-ttu-id="b4502-131">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="b4502-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="b4502-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4502-132">CommonParameters</span></span>
<span data-ttu-id="b4502-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4502-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4502-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4502-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4502-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4502-135">INPUTS</span></span>

### <span data-ttu-id="b4502-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b4502-136">System.String</span></span>

### <span data-ttu-id="b4502-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4502-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b4502-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="b4502-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b4502-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4502-139">OUTPUTS</span></span>

### <span data-ttu-id="b4502-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="b4502-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="b4502-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b4502-141">NOTES</span></span>

## <span data-ttu-id="b4502-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b4502-142">RELATED LINKS</span></span>

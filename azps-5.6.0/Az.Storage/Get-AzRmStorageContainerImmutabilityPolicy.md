---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c1e68d77df44688961f867d473a9dfce1205c2dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944662"
---
# <span data-ttu-id="742c6-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="742c6-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="742c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742c6-102">SYNOPSIS</span></span>
<span data-ttu-id="742c6-103">Ruft ImmutabilityPolicy eines Speicherblobcontainers ab</span><span class="sxs-lookup"><span data-stu-id="742c6-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="742c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="742c6-104">SYNTAX</span></span>

### <span data-ttu-id="742c6-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="742c6-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742c6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="742c6-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="742c6-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="742c6-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="742c6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="742c6-108">DESCRIPTION</span></span>
<span data-ttu-id="742c6-109">Das **Get-AzRmStorageContainerImmutabilityPolicy-Cmdlet** ruft ImmutabilityPolicy eines Speicherblobscontainers ab.</span><span class="sxs-lookup"><span data-stu-id="742c6-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="742c6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="742c6-110">EXAMPLES</span></span>

### <span data-ttu-id="742c6-111">Beispiel 1: ImmutabilityPolicy eines Speicherblobcontainers mit Dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="742c6-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="742c6-112">Dieser Befehl ruft ImmutabilityPolicy eines Speicherblobcontainers mit dem Namen des Speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="742c6-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="742c6-113">Beispiel 2: ImmutabilityPolicy eines Speicherblobcontainers mit Speicherkontoobjekt und Containername</span><span class="sxs-lookup"><span data-stu-id="742c6-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="742c6-114">Dieser Befehl ruft ImmutabilityPolicy eines Speicherblobcontainers mit Speicherkontoobjekt und Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="742c6-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="742c6-115">Beispiel 3: Immutbarkeitspolicy eines Speicherblobcontainers mit Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="742c6-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="742c6-116">Dieser Befehl ruft ImmutabilityPolicy eines Speicherblobcontainers mit Speichercontainerobjekt ab.</span><span class="sxs-lookup"><span data-stu-id="742c6-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="742c6-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="742c6-117">PARAMETERS</span></span>

### <span data-ttu-id="742c6-118">-Container</span><span class="sxs-lookup"><span data-stu-id="742c6-118">-Container</span></span>
<span data-ttu-id="742c6-119">Speichercontainerobjekt</span><span class="sxs-lookup"><span data-stu-id="742c6-119">Storage container object</span></span>

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

### <span data-ttu-id="742c6-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="742c6-120">-ContainerName</span></span>
<span data-ttu-id="742c6-121">Containername</span><span class="sxs-lookup"><span data-stu-id="742c6-121">Container Name</span></span>

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

### <span data-ttu-id="742c6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742c6-122">-DefaultProfile</span></span>
<span data-ttu-id="742c6-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="742c6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="742c6-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="742c6-124">-Etag</span></span>
<span data-ttu-id="742c6-125">E-Tag für Unveränderlichkeitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="742c6-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="742c6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742c6-126">-ResourceGroupName</span></span>
<span data-ttu-id="742c6-127">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="742c6-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="742c6-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="742c6-128">-StorageAccount</span></span>
<span data-ttu-id="742c6-129">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="742c6-129">Storage account object</span></span>

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

### <span data-ttu-id="742c6-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="742c6-130">-StorageAccountName</span></span>
<span data-ttu-id="742c6-131">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="742c6-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="742c6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742c6-132">CommonParameters</span></span>
<span data-ttu-id="742c6-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="742c6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742c6-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="742c6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742c6-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="742c6-135">INPUTS</span></span>

### <span data-ttu-id="742c6-136">System.String</span><span class="sxs-lookup"><span data-stu-id="742c6-136">System.String</span></span>

### <span data-ttu-id="742c6-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="742c6-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="742c6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="742c6-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="742c6-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="742c6-139">OUTPUTS</span></span>

### <span data-ttu-id="742c6-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="742c6-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="742c6-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="742c6-141">NOTES</span></span>

## <span data-ttu-id="742c6-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="742c6-142">RELATED LINKS</span></span>

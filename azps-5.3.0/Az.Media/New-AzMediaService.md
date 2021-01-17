---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473518"
---
# <span data-ttu-id="b9b34-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9b34-101">New-AzMediaService</span></span>

## <span data-ttu-id="b9b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9b34-102">SYNOPSIS</span></span>
<span data-ttu-id="b9b34-103">Erstellt einen Mediendienst, wenn der Mediendienst bereits vorhanden ist, werden alle Eigenschaften mit der bereitgestellten Eingabe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b9b34-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="b9b34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9b34-104">SYNTAX</span></span>

### <span data-ttu-id="b9b34-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="b9b34-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9b34-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="b9b34-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9b34-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9b34-107">DESCRIPTION</span></span>
<span data-ttu-id="b9b34-108">Das **Cmdlet "New-AzMediaService"** erstellt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="b9b34-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="b9b34-109">Wenn der Mediendienst bereits vorhanden ist, aktualisiert dieses Cmdlet seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b9b34-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="b9b34-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9b34-110">EXAMPLES</span></span>

### <span data-ttu-id="b9b34-111">Beispiel1: Erstellen eines Mediendiensts nur mit dem primären Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="b9b34-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="b9b34-112">In diesem Beispiel wird gezeigt, wie Sie einen Mediendienst erstellen, bei dem nur das primäre Speicherkonto angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b9b34-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="b9b34-113">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b9b34-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="b9b34-114">Beispiel 2: Erstellen eines Mediendiensts mit mehrerem Speicher</span><span class="sxs-lookup"><span data-stu-id="b9b34-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="b9b34-115">Dieses Beispiel zeigt, wie Sie einen Mediendienst mit mehreren Speicherkonten erstellen.</span><span class="sxs-lookup"><span data-stu-id="b9b34-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="b9b34-116">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="b9b34-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="b9b34-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9b34-117">PARAMETERS</span></span>

### <span data-ttu-id="b9b34-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b9b34-118">-AccountName</span></span>
<span data-ttu-id="b9b34-119">Gibt den Namen des Mediendiensts an, den dieses Cmdlet erstellt.</span><span class="sxs-lookup"><span data-stu-id="b9b34-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9b34-120">-DefaultProfile</span></span>
<span data-ttu-id="b9b34-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b9b34-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9b34-122">-Location</span><span class="sxs-lookup"><span data-stu-id="b9b34-122">-Location</span></span>
<span data-ttu-id="b9b34-123">Gibt die Region an, in der dieses Cmdlet den Mediendienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="b9b34-123">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9b34-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9b34-125">Gibt den Namen der Ressourcengruppe an, der der Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9b34-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b9b34-126">-StorageAccountId</span></span>
<span data-ttu-id="b9b34-127">Gibt das Speicherkonto an, das dem Mediendienstkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="b9b34-127">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b9b34-128">-StorageAccounts</span></span>
<span data-ttu-id="b9b34-129">Gibt ein Array von Speicherkonten an, das dem Mediendienst zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b9b34-129">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9b34-130">-Tag</span></span>
<span data-ttu-id="b9b34-131">Die Tags, die dem Mediendienstkonto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b9b34-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="b9b34-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9b34-132">-Confirm</span></span>
<span data-ttu-id="b9b34-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b9b34-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b9b34-134">-WhatIf</span></span>
<span data-ttu-id="b9b34-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b9b34-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9b34-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b9b34-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9b34-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9b34-137">CommonParameters</span></span>
<span data-ttu-id="b9b34-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9b34-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9b34-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9b34-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9b34-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9b34-140">INPUTS</span></span>

### <span data-ttu-id="b9b34-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b9b34-141">System.String</span></span>

### <span data-ttu-id="b9b34-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span><span class="sxs-lookup"><span data-stu-id="b9b34-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="b9b34-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9b34-143">OUTPUTS</span></span>

### <span data-ttu-id="b9b34-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="b9b34-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="b9b34-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b9b34-145">NOTES</span></span>

## <span data-ttu-id="b9b34-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b9b34-146">RELATED LINKS</span></span>

[<span data-ttu-id="b9b34-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9b34-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="b9b34-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9b34-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="b9b34-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="b9b34-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)



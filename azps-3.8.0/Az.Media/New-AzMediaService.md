---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004740"
---
# <span data-ttu-id="3d442-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3d442-101">New-AzMediaService</span></span>

## <span data-ttu-id="3d442-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d442-102">SYNOPSIS</span></span>
<span data-ttu-id="3d442-103">Erstellt einen Mediendienst wenn der Mediendienst bereits vorhanden ist, werden alle Eigenschaften mit der bereitgestellten Eingabe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="3d442-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="3d442-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d442-104">SYNTAX</span></span>

### <span data-ttu-id="3d442-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="3d442-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d442-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="3d442-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d442-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d442-107">DESCRIPTION</span></span>
<span data-ttu-id="3d442-108">Das Cmdlet **New-AzMediaService** erstellt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="3d442-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="3d442-109">Wenn der Mediendienst bereits vorhanden ist, aktualisiert dieses Cmdlet seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3d442-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="3d442-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d442-110">EXAMPLES</span></span>

### <span data-ttu-id="3d442-111">Beispiel1: Erstellen eines Medien Diensts nur mit dem primären Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="3d442-111">Example1: Create a media service with the primary storage account only</span></span>
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

<span data-ttu-id="3d442-112">In diesem Beispiel wird gezeigt, wie Sie einen Mediendienst erstellen, bei dem nur primäres Speicherkonto angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3d442-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="3d442-113">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3d442-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="3d442-114">Beispiel 2: Erstellen eines Medien Diensts mit mehreren Speicher</span><span class="sxs-lookup"><span data-stu-id="3d442-114">Example 2: Create a media service with multiple storage</span></span>
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

<span data-ttu-id="3d442-115">In diesem Beispiel wird gezeigt, wie Sie einen Mediendienst mit mehreren Speicherkonten erstellen.</span><span class="sxs-lookup"><span data-stu-id="3d442-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="3d442-116">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="3d442-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="3d442-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d442-117">PARAMETERS</span></span>

### <span data-ttu-id="3d442-118">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="3d442-118">-AccountName</span></span>
<span data-ttu-id="3d442-119">Gibt den Namen des Medien Diensts an, der vom Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3d442-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3d442-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d442-120">-DefaultProfile</span></span>
<span data-ttu-id="3d442-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d442-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d442-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="3d442-122">-Location</span></span>
<span data-ttu-id="3d442-123">Gibt den Bereich an, in dem dieses Cmdlet den Mediendienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="3d442-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="3d442-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d442-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d442-125">Gibt den Namen der Ressourcengruppe an, der der Mediendienst zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3d442-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="3d442-126">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3d442-126">-StorageAccountId</span></span>
<span data-ttu-id="3d442-127">Gibt das dem Mediendienst Konto zugeordnete Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="3d442-127">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="3d442-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3d442-128">-StorageAccounts</span></span>
<span data-ttu-id="3d442-129">Gibt ein Array von Speicherkonten an, die dem Mediendienst zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d442-129">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="3d442-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d442-130">-Tag</span></span>
<span data-ttu-id="3d442-131">Die Tags, die dem Mediendienst Konto zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d442-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="3d442-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d442-132">-Confirm</span></span>
<span data-ttu-id="3d442-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d442-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d442-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d442-134">-WhatIf</span></span>
<span data-ttu-id="3d442-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d442-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d442-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d442-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d442-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d442-137">CommonParameters</span></span>
<span data-ttu-id="3d442-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d442-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d442-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d442-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d442-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d442-140">INPUTS</span></span>

### <span data-ttu-id="3d442-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3d442-141">System.String</span></span>

### <span data-ttu-id="3d442-142">Microsoft. Azure. Commands. Media. Models. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="3d442-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="3d442-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d442-143">OUTPUTS</span></span>

### <span data-ttu-id="3d442-144">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="3d442-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="3d442-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d442-145">NOTES</span></span>

## <span data-ttu-id="3d442-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d442-146">RELATED LINKS</span></span>

[<span data-ttu-id="3d442-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3d442-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="3d442-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3d442-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="3d442-149">Satz-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="3d442-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)



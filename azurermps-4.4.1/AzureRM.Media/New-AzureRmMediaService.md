---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663906"
---
# <span data-ttu-id="a1073-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1073-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="a1073-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1073-102">SYNOPSIS</span></span>
<span data-ttu-id="a1073-103">Erstellt einen Mediendienst wenn der Mediendienst bereits vorhanden ist, werden alle Eigenschaften mit der bereitgestellten Eingabe aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a1073-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1073-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1073-104">SYNTAX</span></span>

### <span data-ttu-id="a1073-105">StorageAccountIdParamSet</span><span class="sxs-lookup"><span data-stu-id="a1073-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1073-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="a1073-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1073-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1073-107">DESCRIPTION</span></span>
<span data-ttu-id="a1073-108">Das Cmdlet **New-AzureRmMediaService** erstellt einen Mediendienst.</span><span class="sxs-lookup"><span data-stu-id="a1073-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="a1073-109">Wenn der Mediendienst bereits vorhanden ist, aktualisiert dieses Cmdlet seine Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a1073-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="a1073-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1073-110">EXAMPLES</span></span>

### <span data-ttu-id="a1073-111">Beispiel1: Erstellen eines Medien Diensts nur mit dem primären Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="a1073-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="a1073-112">In diesem Beispiel wird gezeigt, wie Sie einen Mediendienst erstellen, bei dem nur primäres Speicherkonto angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1073-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="a1073-113">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a1073-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="a1073-114">Beispiel 2: Erstellen eines Medien Diensts mit mehreren Speicher</span><span class="sxs-lookup"><span data-stu-id="a1073-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="a1073-115">In diesem Beispiel wird gezeigt, wie Sie einen Mediendienst mit mehreren Speicherkonten erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1073-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="a1073-116">Dieses Skript verwendet mehrere andere Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a1073-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="a1073-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1073-117">PARAMETERS</span></span>

### <span data-ttu-id="a1073-118">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="a1073-118">-AccountName</span></span>
<span data-ttu-id="a1073-119">Gibt den Namen des Medien Diensts an, der vom Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="a1073-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a1073-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="a1073-120">-Location</span></span>
<span data-ttu-id="a1073-121">Gibt den Bereich an, in dem dieses Cmdlet den Mediendienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="a1073-121">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="a1073-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1073-122">-ResourceGroupName</span></span>
<span data-ttu-id="a1073-123">Gibt den Namen der Ressourcengruppe an, der der Mediendienst zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a1073-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="a1073-124">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a1073-124">-StorageAccountId</span></span>
<span data-ttu-id="a1073-125">Gibt das dem Mediendienst Konto zugeordnete Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="a1073-125">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="a1073-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a1073-126">-StorageAccounts</span></span>
<span data-ttu-id="a1073-127">Gibt ein Array von Speicherkonten an, die dem Mediendienst zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1073-127">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="a1073-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="a1073-128">-Tags</span></span>
<span data-ttu-id="a1073-129">Gibt Tags für den Mediendienst an.</span><span class="sxs-lookup"><span data-stu-id="a1073-129">Specifies tags for the media service.</span></span>

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

### <span data-ttu-id="a1073-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1073-130">-Confirm</span></span>
<span data-ttu-id="a1073-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1073-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1073-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1073-132">-WhatIf</span></span>
<span data-ttu-id="a1073-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1073-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1073-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1073-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1073-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1073-135">-DefaultProfile</span></span>
<span data-ttu-id="a1073-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1073-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1073-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1073-137">CommonParameters</span></span>
<span data-ttu-id="a1073-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1073-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1073-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1073-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1073-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1073-140">INPUTS</span></span>

## <span data-ttu-id="a1073-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1073-141">OUTPUTS</span></span>

### <span data-ttu-id="a1073-142">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="a1073-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="a1073-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1073-143">NOTES</span></span>

## <span data-ttu-id="a1073-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1073-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1073-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1073-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="a1073-146">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1073-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="a1073-147">Satz-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="a1073-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)



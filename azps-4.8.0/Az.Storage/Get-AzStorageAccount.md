---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: ae7a43da35ce0aa41a34639521bc610d69843062
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010390"
---
# <span data-ttu-id="dc9ad-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc9ad-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="dc9ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc9ad-102">SYNOPSIS</span></span>
<span data-ttu-id="dc9ad-103">Ruft ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-103">Gets a Storage account.</span></span>

## <span data-ttu-id="dc9ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc9ad-104">SYNTAX</span></span>

### <span data-ttu-id="dc9ad-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ad-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc9ad-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ad-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc9ad-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc9ad-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc9ad-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc9ad-108">DESCRIPTION</span></span>
<span data-ttu-id="dc9ad-109">Das Cmdlet " **Get-AzStorageAccount** " Ruft ein bestimmtes Speicherkonto oder alle Speicherkonten in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="dc9ad-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc9ad-110">EXAMPLES</span></span>

### <span data-ttu-id="dc9ad-111">Beispiel 1: Abrufen eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="dc9ad-112">Dieser Befehl ruft das angegebene Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="dc9ad-113">Beispiel 2: Abrufen aller Speicherkonten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="dc9ad-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="dc9ad-114">Dieser Befehl ruft alle Speicherkonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="dc9ad-115">Beispiel 3: Abrufen aller Speicherkonten im Abonnement</span><span class="sxs-lookup"><span data-stu-id="dc9ad-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="dc9ad-116">Dieser Befehl ruft alle Speicherkonten des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="dc9ad-117">Beispiel 4: Abrufen eines speicherkontos mit dem Status der BLOB-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="dc9ad-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="dc9ad-118">Dieser Befehl ruft eine Speicherkonten mit dem Status der BLOB-Wiederherstellung ab und zeigt den Status der BLOB-Wiederherstellung an.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="dc9ad-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc9ad-119">PARAMETERS</span></span>

### <span data-ttu-id="dc9ad-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc9ad-120">-AsJob</span></span>
<span data-ttu-id="dc9ad-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dc9ad-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ad-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc9ad-122">-DefaultProfile</span></span>
<span data-ttu-id="dc9ad-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc9ad-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="dc9ad-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="dc9ad-125">Abrufen des BlobRestoreStatus des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ad-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="dc9ad-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="dc9ad-127">Abrufen des GeoReplicationStats des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="dc9ad-127">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ad-128">-Name</span><span class="sxs-lookup"><span data-stu-id="dc9ad-128">-Name</span></span>
<span data-ttu-id="dc9ad-129">Gibt den Namen des abzurufenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc9ad-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc9ad-131">Gibt den Namen der Ressourcengruppe an, die das abzurufende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc9ad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc9ad-132">CommonParameters</span></span>
<span data-ttu-id="dc9ad-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc9ad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc9ad-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc9ad-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc9ad-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc9ad-135">INPUTS</span></span>

### <span data-ttu-id="dc9ad-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dc9ad-136">System.String</span></span>

## <span data-ttu-id="dc9ad-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc9ad-137">OUTPUTS</span></span>

### <span data-ttu-id="dc9ad-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc9ad-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="dc9ad-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc9ad-139">NOTES</span></span>

## <span data-ttu-id="dc9ad-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc9ad-140">RELATED LINKS</span></span>

[<span data-ttu-id="dc9ad-141">Neu – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc9ad-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="dc9ad-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc9ad-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="dc9ad-143">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dc9ad-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)



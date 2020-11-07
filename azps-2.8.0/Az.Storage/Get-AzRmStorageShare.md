---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826464"
---
# <span data-ttu-id="924c3-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="924c3-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="924c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="924c3-102">SYNOPSIS</span></span>
<span data-ttu-id="924c3-103">Ruft Speicherdatei Freigaben ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="924c3-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="924c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="924c3-104">SYNTAX</span></span>

### <span data-ttu-id="924c3-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="924c3-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="924c3-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="924c3-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="924c3-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="924c3-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="924c3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="924c3-108">DESCRIPTION</span></span>
<span data-ttu-id="924c3-109">Das Cmdlet " **Get-AzRmStorageShare** " ruft Speicherdatei Freigaben ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="924c3-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="924c3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="924c3-110">EXAMPLES</span></span>

### <span data-ttu-id="924c3-111">Beispiel 1: Abrufen einer Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen</span><span class="sxs-lookup"><span data-stu-id="924c3-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="924c3-112">Dieser Befehl ruft eine Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen ab.</span><span class="sxs-lookup"><span data-stu-id="924c3-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="924c3-113">Beispiel 2: Auflisten aller Speicherdatei Freigaben eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="924c3-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="924c3-114">Dieser Befehl listet alle Speicherdatei Freigaben eines speicherkontos mit dem Namen des speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="924c3-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="924c3-115">Beispiel 3: Abrufen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="924c3-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="924c3-116">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="924c3-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="924c3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="924c3-117">PARAMETERS</span></span>

### <span data-ttu-id="924c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="924c3-118">-DefaultProfile</span></span>
<span data-ttu-id="924c3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="924c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="924c3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="924c3-120">-Name</span></span>
<span data-ttu-id="924c3-121">Freigabe Name</span><span class="sxs-lookup"><span data-stu-id="924c3-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="924c3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="924c3-122">-ResourceGroupName</span></span>
<span data-ttu-id="924c3-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="924c3-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="924c3-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="924c3-124">-ResourceId</span></span>
<span data-ttu-id="924c3-125">Geben Sie eine Dateifreigabe-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="924c3-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="924c3-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="924c3-126">-StorageAccount</span></span>
<span data-ttu-id="924c3-127">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="924c3-127">Storage account object</span></span>

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

### <span data-ttu-id="924c3-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="924c3-128">-StorageAccountName</span></span>
<span data-ttu-id="924c3-129">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="924c3-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="924c3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="924c3-130">CommonParameters</span></span>
<span data-ttu-id="924c3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="924c3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="924c3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="924c3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="924c3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="924c3-133">INPUTS</span></span>

### <span data-ttu-id="924c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="924c3-134">System.String</span></span>

### <span data-ttu-id="924c3-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="924c3-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="924c3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="924c3-136">OUTPUTS</span></span>

### <span data-ttu-id="924c3-137">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="924c3-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="924c3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="924c3-138">NOTES</span></span>

## <span data-ttu-id="924c3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="924c3-139">RELATED LINKS</span></span>

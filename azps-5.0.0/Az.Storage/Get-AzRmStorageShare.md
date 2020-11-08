---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179967"
---
# <span data-ttu-id="f52c6-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f52c6-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="f52c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f52c6-102">SYNOPSIS</span></span>
<span data-ttu-id="f52c6-103">Ruft Speicherdatei Freigaben ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="f52c6-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="f52c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f52c6-104">SYNTAX</span></span>

### <span data-ttu-id="f52c6-105">AccountNameSingle (Standard)</span><span class="sxs-lookup"><span data-stu-id="f52c6-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f52c6-106">Accountname</span><span class="sxs-lookup"><span data-stu-id="f52c6-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f52c6-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="f52c6-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f52c6-108">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="f52c6-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f52c6-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="f52c6-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f52c6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f52c6-110">DESCRIPTION</span></span>
<span data-ttu-id="f52c6-111">Das Cmdlet " **Get-AzRmStorageShare** " ruft Speicherdatei Freigaben ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="f52c6-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="f52c6-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f52c6-112">EXAMPLES</span></span>

### <span data-ttu-id="f52c6-113">Beispiel 1: Abrufen einer Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen</span><span class="sxs-lookup"><span data-stu-id="f52c6-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="f52c6-114">Dieser Befehl ruft eine Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen ab.</span><span class="sxs-lookup"><span data-stu-id="f52c6-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="f52c6-115">Beispiel 2: Auflisten aller Speicherdatei Freigaben eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f52c6-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="f52c6-116">Dieser Befehl listet alle Speicherdatei Freigaben eines speicherkontos mit dem Namen des speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="f52c6-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="f52c6-117">Beispiel 3: Abrufen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="f52c6-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="f52c6-118">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="f52c6-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="f52c6-119">Beispiel 4: Abrufen einer Speicherdatei Freigabe mit der Freigabe Verwendung in Bytes</span><span class="sxs-lookup"><span data-stu-id="f52c6-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="f52c6-120">Dieser Befehl ruft eine Speicherdatei Freigabe mit dem Namen des speicherkontos und dem Freigabenamen ab und schließt die Freigabe Verwendung in Bytes ein.</span><span class="sxs-lookup"><span data-stu-id="f52c6-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="f52c6-121">Beispiel 5: Auflisten aller Speicherdatei Freigaben eines speicherkontos, einbeziehen der gelöschten Freigaben</span><span class="sxs-lookup"><span data-stu-id="f52c6-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="f52c6-122">Dieser Befehl listet alle Speicherdatei Freigaben die gelöschten Freigaben eines speicherkontos mit dem Namen des speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="f52c6-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="f52c6-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="f52c6-123">PARAMETERS</span></span>

### <span data-ttu-id="f52c6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f52c6-124">-DefaultProfile</span></span>
<span data-ttu-id="f52c6-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f52c6-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f52c6-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="f52c6-126">-GetShareUsage</span></span>
<span data-ttu-id="f52c6-127">Geben Sie diesen Parameter an, um die Freigabe Verwendung in Bytes abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f52c6-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52c6-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="f52c6-128">-IncludeDeleted</span></span>
<span data-ttu-id="f52c6-129">Gelöschte Freigaben einbeziehen, werden standardmäßig Listen Freigaben keine gelöschten Freigaben umfassen.</span><span class="sxs-lookup"><span data-stu-id="f52c6-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52c6-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f52c6-130">-Name</span></span>
<span data-ttu-id="f52c6-131">Freigabe Name</span><span class="sxs-lookup"><span data-stu-id="f52c6-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52c6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f52c6-132">-ResourceGroupName</span></span>
<span data-ttu-id="f52c6-133">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f52c6-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52c6-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f52c6-134">-ResourceId</span></span>
<span data-ttu-id="f52c6-135">Geben Sie eine Dateifreigabe-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="f52c6-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="f52c6-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f52c6-136">-StorageAccount</span></span>
<span data-ttu-id="f52c6-137">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="f52c6-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f52c6-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f52c6-138">-StorageAccountName</span></span>
<span data-ttu-id="f52c6-139">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="f52c6-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52c6-140">CommonParameters</span></span>
<span data-ttu-id="f52c6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f52c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52c6-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52c6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52c6-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f52c6-143">INPUTS</span></span>

### <span data-ttu-id="f52c6-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f52c6-144">System.String</span></span>

### <span data-ttu-id="f52c6-145">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f52c6-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f52c6-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f52c6-146">OUTPUTS</span></span>

### <span data-ttu-id="f52c6-147">Microsoft. Azure. Commands. Management. Storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="f52c6-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f52c6-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="f52c6-148">NOTES</span></span>

## <span data-ttu-id="f52c6-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f52c6-149">RELATED LINKS</span></span>

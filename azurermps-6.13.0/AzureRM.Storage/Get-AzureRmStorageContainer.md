---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477610"
---
# <span data-ttu-id="d42c5-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d42c5-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="d42c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d42c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d42c5-103">Abrufen oder Auflisten von BLOB-Speicher Containern</span><span class="sxs-lookup"><span data-stu-id="d42c5-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d42c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d42c5-104">SYNTAX</span></span>

### <span data-ttu-id="d42c5-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="d42c5-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d42c5-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="d42c5-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d42c5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d42c5-107">DESCRIPTION</span></span>
<span data-ttu-id="d42c5-108">Das Cmdlet " **Get-AzureRmStorageContainer** " ruft Speicher-BLOB-Container ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="d42c5-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="d42c5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d42c5-109">EXAMPLES</span></span>

### <span data-ttu-id="d42c5-110">Beispiel 1: Abrufen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="d42c5-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="d42c5-111">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="d42c5-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d42c5-112">Beispiel 2: Auflisten aller BLOB-Speichercontainer eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d42c5-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="d42c5-113">Dieser Befehl listet alle Speicher-BLOB-Container eines speicherkontos mit dem Namen des speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="d42c5-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="d42c5-114">Beispiel 3: Abrufen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="d42c5-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="d42c5-115">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="d42c5-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="d42c5-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="d42c5-116">PARAMETERS</span></span>

### <span data-ttu-id="d42c5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d42c5-117">-DefaultProfile</span></span>
<span data-ttu-id="d42c5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d42c5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d42c5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d42c5-119">-Name</span></span>
<span data-ttu-id="d42c5-120">Container Name</span><span class="sxs-lookup"><span data-stu-id="d42c5-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d42c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d42c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="d42c5-122">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d42c5-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d42c5-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d42c5-123">-StorageAccount</span></span>
<span data-ttu-id="d42c5-124">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="d42c5-124">Storage account object</span></span>

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

### <span data-ttu-id="d42c5-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d42c5-125">-StorageAccountName</span></span>
<span data-ttu-id="d42c5-126">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d42c5-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="d42c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d42c5-127">CommonParameters</span></span>
<span data-ttu-id="d42c5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d42c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d42c5-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d42c5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d42c5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d42c5-130">INPUTS</span></span>

### <span data-ttu-id="d42c5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d42c5-131">System.String</span></span>

## <span data-ttu-id="d42c5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d42c5-132">OUTPUTS</span></span>

### <span data-ttu-id="d42c5-133">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d42c5-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d42c5-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d42c5-134">NOTES</span></span>

## <span data-ttu-id="d42c5-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d42c5-135">RELATED LINKS</span></span>


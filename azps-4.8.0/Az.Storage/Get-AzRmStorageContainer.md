---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010392"
---
# <span data-ttu-id="9d965-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9d965-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="9d965-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d965-102">SYNOPSIS</span></span>
<span data-ttu-id="9d965-103">Abrufen oder Auflisten von BLOB-Speicher Containern</span><span class="sxs-lookup"><span data-stu-id="9d965-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="9d965-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d965-104">SYNTAX</span></span>

### <span data-ttu-id="9d965-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d965-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d965-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="9d965-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d965-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d965-107">DESCRIPTION</span></span>
<span data-ttu-id="9d965-108">Das Cmdlet " **Get-AzRmStorageContainer** " ruft Speicher-BLOB-Container ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="9d965-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="9d965-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d965-109">EXAMPLES</span></span>

### <span data-ttu-id="9d965-110">Beispiel 1: Abrufen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="9d965-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="9d965-111">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="9d965-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9d965-112">Beispiel 2: Auflisten aller BLOB-Speichercontainer eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9d965-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="9d965-113">Dieser Befehl listet alle Speicher-BLOB-Container eines speicherkontos mit dem Namen des speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="9d965-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="9d965-114">Beispiel 3: Abrufen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="9d965-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="9d965-115">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="9d965-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="9d965-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d965-116">PARAMETERS</span></span>

### <span data-ttu-id="9d965-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d965-117">-AsJob</span></span>
<span data-ttu-id="9d965-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9d965-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d965-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d965-119">-DefaultProfile</span></span>
<span data-ttu-id="9d965-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d965-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d965-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9d965-121">-Name</span></span>
<span data-ttu-id="9d965-122">Container Name</span><span class="sxs-lookup"><span data-stu-id="9d965-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d965-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d965-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d965-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d965-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d965-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d965-125">-StorageAccount</span></span>
<span data-ttu-id="9d965-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="9d965-126">Storage account object</span></span>

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

### <span data-ttu-id="9d965-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d965-127">-StorageAccountName</span></span>
<span data-ttu-id="9d965-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9d965-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="9d965-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d965-129">CommonParameters</span></span>
<span data-ttu-id="9d965-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d965-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d965-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d965-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d965-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d965-132">INPUTS</span></span>

### <span data-ttu-id="9d965-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9d965-133">System.String</span></span>

### <span data-ttu-id="9d965-134">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d965-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9d965-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d965-135">OUTPUTS</span></span>

### <span data-ttu-id="9d965-136">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="9d965-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9d965-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d965-137">NOTES</span></span>

## <span data-ttu-id="9d965-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d965-138">RELATED LINKS</span></span>

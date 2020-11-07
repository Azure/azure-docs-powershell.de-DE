---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: aa2a03355431f027a9efd374f5af45199cc77452
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826439"
---
# <span data-ttu-id="bbe90-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="bbe90-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="bbe90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bbe90-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe90-103">Abrufen oder Auflisten von BLOB-Speicher Containern</span><span class="sxs-lookup"><span data-stu-id="bbe90-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="bbe90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbe90-104">SYNTAX</span></span>

### <span data-ttu-id="bbe90-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="bbe90-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbe90-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="bbe90-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbe90-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bbe90-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe90-108">Das Cmdlet " **Get-AzRmStorageContainer** " ruft Speicher-BLOB-Container ab oder listet Sie auf.</span><span class="sxs-lookup"><span data-stu-id="bbe90-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="bbe90-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bbe90-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe90-110">Beispiel 1: Abrufen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="bbe90-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="bbe90-111">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="bbe90-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="bbe90-112">Beispiel 2: Auflisten aller BLOB-Speichercontainer eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bbe90-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="bbe90-113">Dieser Befehl listet alle Speicher-BLOB-Container eines speicherkontos mit dem Namen des speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="bbe90-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="bbe90-114">Beispiel 3: Abrufen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="bbe90-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="bbe90-115">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="bbe90-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="bbe90-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbe90-116">PARAMETERS</span></span>

### <span data-ttu-id="bbe90-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bbe90-117">-AsJob</span></span>
<span data-ttu-id="bbe90-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="bbe90-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bbe90-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe90-119">-DefaultProfile</span></span>
<span data-ttu-id="bbe90-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bbe90-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbe90-121">-Name</span><span class="sxs-lookup"><span data-stu-id="bbe90-121">-Name</span></span>
<span data-ttu-id="bbe90-122">Container Name</span><span class="sxs-lookup"><span data-stu-id="bbe90-122">Container Name</span></span>

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

### <span data-ttu-id="bbe90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe90-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbe90-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bbe90-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="bbe90-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbe90-125">-StorageAccount</span></span>
<span data-ttu-id="bbe90-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="bbe90-126">Storage account object</span></span>

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

### <span data-ttu-id="bbe90-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bbe90-127">-StorageAccountName</span></span>
<span data-ttu-id="bbe90-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bbe90-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="bbe90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe90-129">CommonParameters</span></span>
<span data-ttu-id="bbe90-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbe90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe90-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbe90-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe90-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bbe90-132">INPUTS</span></span>

### <span data-ttu-id="bbe90-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bbe90-133">System.String</span></span>

### <span data-ttu-id="bbe90-134">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bbe90-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bbe90-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bbe90-135">OUTPUTS</span></span>

### <span data-ttu-id="bbe90-136">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="bbe90-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="bbe90-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="bbe90-137">NOTES</span></span>

## <span data-ttu-id="bbe90-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bbe90-138">RELATED LINKS</span></span>

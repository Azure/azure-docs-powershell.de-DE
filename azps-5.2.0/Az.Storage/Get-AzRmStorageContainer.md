---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: da0ccdc791318f0a315bea8d2464d8d0852aec8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290621"
---
# <span data-ttu-id="9d963-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9d963-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="9d963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d963-102">SYNOPSIS</span></span>
<span data-ttu-id="9d963-103">Ruft Speicher-BLOB-Container ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="9d963-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="9d963-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d963-104">SYNTAX</span></span>

### <span data-ttu-id="9d963-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d963-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d963-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9d963-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d963-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d963-107">DESCRIPTION</span></span>
<span data-ttu-id="9d963-108">Das **Cmdlet "Get-AzRmStorageContainer"** ruft Speicher-BLOB-Container ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="9d963-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="9d963-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d963-109">EXAMPLES</span></span>

### <span data-ttu-id="9d963-110">Beispiel 1: Erhalten eines Speicher-BLOB-Containers mit dem Namen des Speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="9d963-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="9d963-111">Dieser Befehl ruft einen Speicher-BLOB-Container mit dem Namen des Speicherkontos und dem Containernamen ab.</span><span class="sxs-lookup"><span data-stu-id="9d963-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9d963-112">Beispiel 2: Auflisten aller Speicher-BLOB-Container eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="9d963-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="9d963-113">Dieser Befehl listet alle Speicher-BLOB-Container eines Speicherkontos mit dem Namen des Speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="9d963-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="9d963-114">Beispiel 3: Einen Speicher-BLOB-Container mit Speicherkontoobjekt und Containername erhalten.</span><span class="sxs-lookup"><span data-stu-id="9d963-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="9d963-115">Dieser Befehl ruft einen Speicher-BLOB-Container mit Speicherkontoobjekt und Containername ab.</span><span class="sxs-lookup"><span data-stu-id="9d963-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="9d963-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d963-116">PARAMETERS</span></span>

### <span data-ttu-id="9d963-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d963-117">-AsJob</span></span>
<span data-ttu-id="9d963-118">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9d963-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9d963-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d963-119">-DefaultProfile</span></span>
<span data-ttu-id="9d963-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d963-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d963-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9d963-121">-Name</span></span>
<span data-ttu-id="9d963-122">Containername</span><span class="sxs-lookup"><span data-stu-id="9d963-122">Container Name</span></span>

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

### <span data-ttu-id="9d963-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d963-123">-ResourceGroupName</span></span>
<span data-ttu-id="9d963-124">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="9d963-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d963-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d963-125">-StorageAccount</span></span>
<span data-ttu-id="9d963-126">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="9d963-126">Storage account object</span></span>

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

### <span data-ttu-id="9d963-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d963-127">-StorageAccountName</span></span>
<span data-ttu-id="9d963-128">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="9d963-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="9d963-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d963-129">CommonParameters</span></span>
<span data-ttu-id="9d963-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d963-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d963-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d963-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d963-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d963-132">INPUTS</span></span>

### <span data-ttu-id="9d963-133">System.String</span><span class="sxs-lookup"><span data-stu-id="9d963-133">System.String</span></span>

### <span data-ttu-id="9d963-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d963-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="9d963-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d963-135">OUTPUTS</span></span>

### <span data-ttu-id="9d963-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="9d963-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9d963-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d963-137">NOTES</span></span>

## <span data-ttu-id="9d963-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d963-138">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 351145AC-7C1E-4EB7-A17D-B8B7D8ED8DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 65afd4039fb772d1ecf522645fe41154dae42981
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173716"
---
# <span data-ttu-id="49778-101">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49778-101">New-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="49778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49778-102">SYNOPSIS</span></span>
<span data-ttu-id="49778-103">Erstellt eine Richtlinie für den gespeicherten Zugriff für eine Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="49778-103">Creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="49778-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="49778-104">SYNTAX</span></span>

```
New-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49778-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49778-105">DESCRIPTION</span></span>
<span data-ttu-id="49778-106">Das **Cmdlet "New-AzStorageQueueStoredAccessPolicy"** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speicherwarteschlange.</span><span class="sxs-lookup"><span data-stu-id="49778-106">The **New-AzStorageQueueStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage queue.</span></span>

## <span data-ttu-id="49778-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="49778-107">EXAMPLES</span></span>

### <span data-ttu-id="49778-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Speicherwarteschlange</span><span class="sxs-lookup"><span data-stu-id="49778-108">Example 1: Create a stored access policy in a storage queue</span></span>
```
PS C:\>New-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy01"
```

<span data-ttu-id="49778-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy01" in der Speicherwarteschlange namens "MyQueue" erstellt.</span><span class="sxs-lookup"><span data-stu-id="49778-109">This command creates an access policy named Policy01 in the storage queue named MyQueue.</span></span>

## <span data-ttu-id="49778-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49778-110">PARAMETERS</span></span>

### <span data-ttu-id="49778-111">-Context</span><span class="sxs-lookup"><span data-stu-id="49778-111">-Context</span></span>
<span data-ttu-id="49778-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="49778-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="49778-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49778-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49778-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49778-114">-DefaultProfile</span></span>
<span data-ttu-id="49778-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="49778-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49778-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="49778-116">-ExpiryTime</span></span>
<span data-ttu-id="49778-117">Gibt den Zeitpunkt an, zu dem die Richtlinie für den gespeicherten Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="49778-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49778-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="49778-118">-Permission</span></span>
<span data-ttu-id="49778-119">Gibt Berechtigungen in der Richtlinie für gespeicherten Zugriff für den Zugriff auf die Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="49778-119">Specifies permissions in the stored access policy to access the storage queue.</span></span>
<span data-ttu-id="49778-120">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="49778-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49778-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="49778-121">-Policy</span></span>
<span data-ttu-id="49778-122">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="49778-122">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49778-123">-Queue</span><span class="sxs-lookup"><span data-stu-id="49778-123">-Queue</span></span>
<span data-ttu-id="49778-124">Gibt den Namen der Azure-Speicherwarteschlange an.</span><span class="sxs-lookup"><span data-stu-id="49778-124">Specifies the Azure storage queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49778-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="49778-125">-StartTime</span></span>
<span data-ttu-id="49778-126">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="49778-126">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49778-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49778-127">CommonParameters</span></span>
<span data-ttu-id="49778-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49778-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49778-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49778-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49778-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="49778-130">INPUTS</span></span>

### <span data-ttu-id="49778-131">System.String</span><span class="sxs-lookup"><span data-stu-id="49778-131">System.String</span></span>

### <span data-ttu-id="49778-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="49778-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="49778-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="49778-133">OUTPUTS</span></span>

### <span data-ttu-id="49778-134">System.String</span><span class="sxs-lookup"><span data-stu-id="49778-134">System.String</span></span>

## <span data-ttu-id="49778-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="49778-135">NOTES</span></span>

## <span data-ttu-id="49778-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="49778-136">RELATED LINKS</span></span>

[<span data-ttu-id="49778-137">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49778-137">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="49778-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="49778-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="49778-139">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49778-139">Remove-AzStorageQueueStoredAccessPolicy</span></span>](./Remove-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="49778-140">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="49778-140">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)


